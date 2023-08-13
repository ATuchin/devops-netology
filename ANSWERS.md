1 Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.
ОТВЕТ

git show aefea
Полный хэш
commit aefead2207ef7e2aa5dc81a34aedf0cad4c32545

Автор и детали
Author: Alisdair McDiarmid <alisdair@users.noreply.github.com>
Date:   Thu Jun 18 10:29:58 2020 -0400
BUG FIXES:
 * backend/s3: Prefer AWS shared configuration over EC2 metadata credentials by default ([#25134](https://github.com/hashicorp/terraform/issues/25134))
 * backend/s3: Prefer ECS credentials over EC2 metadata credentials by default ([#25134](https://github.com/hashicorp/terraform/issues/25134))
 * backend/s3: Remove hardcoded AWS Provider messaging ([#25134](https://github.com/hashicorp/terraform/issues/25134))
+* command: Fix bug with global `-v`/`-version`/`--version` flags introduced in 0.13.0beta2 [GH-25277]
 * command/0.13upgrade: Fix `0.13upgrade` usage help text to include options ([#25127](https://github.com/hashicorp/terraform/issues/25127))
 * command/0.13upgrade: Do not add source for builtin provider ([#25215](https://github.com/hashicorp/terraform/issues/25215))
 * command/apply: Fix bug which caused Terraform to silently exit on Windows when using absolute plan path ([#25233](https://github.com/hashicorp/terraform/issues/25233))

2 Какому тегу соответствует коммит 85024d3? Ответ Тэг v0.12.23
commit 85024d3100126de36331c6982bfaac02cdab9e76 (tag: v0.12.23)

3 Сколько родителей у коммита b8d720? Напишите их хеши.
commit b8d720f8340221f2146e4e4870bf2ee0bc48f2d5
Ответ  коммит образовался путем слиянияMerge: 56cd7859e0 9ea88f22fc 
Первый родитель 56cd7859e05c36c06b56d013b55a252d0bb7e158

4 Перечислите хеши и комментарии всех коммитов, которые были сделаны между тегами v0.12.23 и v0.12.24.

Ответ
КОМАНДА git log --pretty=format:"%H %s" v0.12.23..v0.12.24
Хэши
33ff1c03bb960b332be3af2e333462dde88b279e v0.12.24
b14b74c4939dcab573326f4e3ee2a62e23e12f89 [Website] vmc provider links
3f235065b9347a758efadc92295b540ee0a5e26e Update CHANGELOG.md
6ae64e247b332925b872447e9ce869657281c2bf registry: Fix panic when server is unreachable
5c619ca1baf2e21a155fcdb4c264cc9e24a2a353 website: Remove links to the getting started guide's old location
06275647e2b53d97d4f0a19a0fec11f6d69820b5 Update CHANGELOG.md
d5f9411f5108260320064349b757f55c09bc4b80 command: Fix bug when using terraform login on Windows
4b6d06cc5dcb78af637bbb19c198faff37a066ed Update CHANGELOG.md
dd01a35078f040ca984cdd349f18d0b67e486c35 Update CHANGELOG.md
225466bc3e5f35baa5d07197bbc079345b77525e Cleanup after v0.12.23 release

5 Найдите коммит, в котором была создана функция func providerSource, её определение в коде выглядит так: func providerSource(...) (вместо троеточия перечислены аргументы).

Ответ git log -S 'func providerSource(' --reverse --date=short ищем появление далее смотрим коммит 
git show 8c928e83589d90a031f811fae52a81be7153e82f
в нем есть +func providerSource(services *disco.Disco) getproviders.Source {

 
Хэш 8c928e83589d90a031f811fae52a81be7153e82f 
/ providerSource constructs a provider source based on a combination of the
// CLI configuration and some default search locations. This will be the
// provider source used for provider installation in the "terraform init"
// command, unless overridden by the special -plugin-dir option.
func providerSource(configs []*cliconfig.ProviderInstallation, services *disco.Disco) (getproviders.Source, tfdiags.Diagnostics)


6 Найдите все коммиты, в которых была изменена функция globalPluginDirs.
Ответ Шаг 1 поиск функции  где она создана git grep -p "globalPluginDirs("
Шаг 2 ищем изменения функции по коммитам git log -L :globalPluginDirs:plugins.go

commit 78b12205587fe839f10d946ea3fdc06719decb05
Author: Pam Selle <204372+pselle@users.noreply.github.com>
commit 52dbf94834cb970b510f2fba853a5b49ad9b1a46
Author: James Bardin <j.bardin@gmail.com>
commit 41ab0aef7a0fe030e84018973a64135b11abcd70
Author: James Bardin <j.bardin@gmail.com>
commit 66ebff90cdfaa6938f26f908c7ebad8d547fea17
Author: James Bardin <j.bardin@gmail.com>



7 Кто автор функции synchronizedWriters?
Ответ git log -S 'synchronizedWriters' --pretty=format:"%an %ad" --reverse --date=short

commit 5ac311e2a91e381e2f52234668b49ba670aa0fe5
Author: Martin Atkins <mart@degeneration.co.uk>
Date:   Wed May 3 16:25:41 2017 -0700

