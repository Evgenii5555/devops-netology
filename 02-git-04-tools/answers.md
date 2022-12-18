1) 
git show aefea
aefead2207ef7e2aa5dc81a34aedf0cad4c32545
Update CHANGELOG.md

2)
git tag --points-at 85024d3
v0.12.23

3)
git show b8d720^
commit 56cd7859e05c36c06b56d013b55a252d0bb7e158

git show b8d720^2
commit 9ea88f22fc6269854151c571162c5bcf958bee2b

4)
git log --oneline v0.12.23...v0.12.24^
b14b74c493 [Website] vmc provider links
3f235065b9 Update CHANGELOG.md
6ae64e247b registry: Fix panic when server is unreachable
5c619ca1ba website: Remove links to the getting started guide's old location
06275647e2 Update CHANGELOG.md
d5f9411f51 command: Fix bug when using terraform login on Windows
4b6d06cc5d Update CHANGELOG.md
dd01a35078 Update CHANGELOG.md
225466bc3e Cleanup after v0.12.23 release

5)
Выводим коммиты где создавалась и удалялась функция.
git log -S"func providerSource" --oneline
5af1e6234a main: Honor explicit provider_installation CLI config when present
8c928e8358 main: Consult local directories as potential mirrors of providers
Нас интересует нижний коммит.
проверяем:
git show 8c928e8358



6)
ищем файл с функцией
git grep --name-only "func globalPluginDirs"
plugins.go

Выводим коммиты где изменялась функция
git log --pretty=format:"%h" -q -L :globalPluginDirs:plugins.go
78b1220558
52dbf94834
41ab0aef7a
66ebff90cd
8364383c35

7)
git log --pretty=format:"%an %ai" -S"func synchronizedWriters"
James Bardin 2020-11-30 18:02:04 -0500
Martin Atkins 2017-05-03 16:25:41 -0700

автор: Martin Atkins