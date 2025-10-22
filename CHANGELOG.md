# Changelog

## [2.0.0](https://github.com/Goorsky1/klio/compare/v1.3.0...v2.0.0) (2025-10-22)


### ⚠ BREAKING CHANGES

* commands with no apiVersion specified are not supported anymore.
* manifest.yaml file was renamed back to command.yaml
* up to now klio before running any command was setting two env variables - G2A_CLI_LOG_LEVEL and G2A_CLI_GLOBAL_COMMAND. Former was renamed to KLIO_LOG_LEVEL and latter was removed.
* this commit removes support for previous central registry and changes format of g2a.yaml file.

### Features

* add --upgrade flag ([2d9c323](https://github.com/Goorsky1/klio/commit/2d9c323888fa4eac44a6b79b71ef1e21c829f502))
* add --upgrade flag ([#88](https://github.com/Goorsky1/klio/issues/88)) ([deffa47](https://github.com/Goorsky1/klio/commit/deffa4742c8279a8c0efb23ad9bb1d565aa82fd0))
* add "get" command ([f2cebba](https://github.com/Goorsky1/klio/commit/f2cebba797f575ddad99016bf55afe428ebeb650))
* add "raw mode" to logs processor ([1769510](https://github.com/Goorsky1/klio/commit/176951050501bed49f45da3233b90770427c4d2e))
* add possibility to define alternative command repositories ([a1dded8](https://github.com/Goorsky1/klio/commit/a1dded847bb93050b7bf5453b6f340f69f933ead))
* add progress bar when downloading commands ([a745eb5](https://github.com/Goorsky1/klio/commit/a745eb55c8d9dd55f514181f73d312338d68611d)), closes [#20](https://github.com/Goorsky1/klio/issues/20)
* add root (g2a) command and implement commands discovery ([26b1f11](https://github.com/Goorsky1/klio/commit/26b1f119a17abbd07991a61e1a079168a3bdeb62))
* auto download divergent project commands ([#86](https://github.com/Goorsky1/klio/issues/86)) ([bf2893a](https://github.com/Goorsky1/klio/commit/bf2893adb1b03eeb8b3efba192cc2fdbb477a78f))
* cache result of new version check for 24h ([f3d2453](https://github.com/Goorsky1/klio/commit/f3d2453e646e75acfeef1e2e59db89d839e50142))
* capture output of command run by runner ([f17c39b](https://github.com/Goorsky1/klio/commit/f17c39b977af36b19956237e91139b65831e9834))
* change registries map ([854c9fb](https://github.com/Goorsky1/klio/commit/854c9fb9952da2ea92a4a89fb5e319de770c3549))
* check for new root version ([9ec421c](https://github.com/Goorsky1/klio/commit/9ec421c36ade7d92418cb2c455cbd4214fc1f98a))
* check for new version during command run ([dfa39b0](https://github.com/Goorsky1/klio/commit/dfa39b07425b54a2380540161eea172befb67b99))
* control logs level and tags using escape sequences ([7e2864e](https://github.com/Goorsky1/klio/commit/7e2864e1b9536a33da06c7687dc6e25fa2f1669c))
* docker only on release ([22748b6](https://github.com/Goorsky1/klio/commit/22748b6c088bffc7c0b47202bd1d2810130a0ecf))
* **g2a-com#48:** expose internal logger in pkg ([#69](https://github.com/Goorsky1/klio/issues/69)) ([362e2df](https://github.com/Goorsky1/klio/commit/362e2df6e68838419a366acb9014076a8aac44e0))
* **g2a-com#52:** add 'remove' command ([#59](https://github.com/Goorsky1/klio/issues/59)) ([d05de37](https://github.com/Goorsky1/klio/commit/d05de37757853add6796a84fdfcd18f2e7519aa5))
* **get:** download all commands defined in g2a.yaml when called without args ([8668aa5](https://github.com/Goorsky1/klio/commit/8668aa572c32b447db3c3ec2a5c021e886a7fb5e))
* **get:** initialise klio.yaml when it doesn't exist ([9088a70](https://github.com/Goorsky1/klio/commit/9088a7027d5783b14553f150661c347bce21dbd5)), closes [#8](https://github.com/Goorsky1/klio/issues/8) [#22](https://github.com/Goorsky1/klio/issues/22)
* implement configurable default registry ([7dc9746](https://github.com/Goorsky1/klio/commit/7dc9746ef7c340b7eb6815c5a391960b1f0f2154))
* **log:** export default log levels from log package ([c4ed69a](https://github.com/Goorsky1/klio/commit/c4ed69adc1beda7cdb4b95c7c8d014fadaab2eb6))
* provide docker image with cli automatically ([bb840ac](https://github.com/Goorsky1/klio/commit/bb840acc98b5a2ff9721f677f99be214b25be105))
* require apiVersion in command.yaml ([c33f93c](https://github.com/Goorsky1/klio/commit/c33f93c1e067d2ca5f262263ec957d3f1c2d479c))
* restore compatibility with commands created for klio v2 ([5eadf52](https://github.com/Goorsky1/klio/commit/5eadf5273304dee659ebd7f4659c8977a723fb73)), closes [#28](https://github.com/Goorsky1/klio/issues/28)
* **root:** use executables in place of go plugins as an external commands ([f8fc2cd](https://github.com/Goorsky1/klio/commit/f8fc2cd2016e8d0b307c9def2e7133457b2aba53))
* set env which definies command run globally ([6b1e715](https://github.com/Goorsky1/klio/commit/6b1e715c10c3428041f66c0247969d0a981f8efc))
* set log level from ENV ([45932ee](https://github.com/Goorsky1/klio/commit/45932eec5bcd45528798f3b095d728c6c3ab28dc))
* **subcommand:** add subcommand package containing helpers for writing subcommands ([9995b59](https://github.com/Goorsky1/klio/commit/9995b5968059d9d8ebe14735db58a95f1200e0d8))
* support multiple registries ([25140aa](https://github.com/Goorsky1/klio/commit/25140aacefeded3177927d961e80db338f118088))


### Bug Fixes

* calculate checksum correctly when downloading command in one chunk ([0f5ffb5](https://github.com/Goorsky1/klio/commit/0f5ffb582f2929a7535d0ebdbe0066727ea9f947)), closes [#14](https://github.com/Goorsky1/klio/issues/14)
* change Manager interface, remove fatal with defer in place ([24a0f6f](https://github.com/Goorsky1/klio/commit/24a0f6fd65048e5165b5fe0dec455ecab1b42c40))
* change mod of created files when extracting tar ([7f22f2b](https://github.com/Goorsky1/klio/commit/7f22f2b9a038112332232ed3891a73ee89c52ef7))
* change module name ([4a476fb](https://github.com/Goorsky1/klio/commit/4a476fbfe3efae4ecc80dafa8286dc87d5f67fe9))
* chmod not supported on windows ([2b1c60f](https://github.com/Goorsky1/klio/commit/2b1c60f692f2d886a410fb62262d352127f9f729))
* copy directory when rename fails ([d966658](https://github.com/Goorsky1/klio/commit/d966658a829e4a723c1807fdb2a0321cb10f6819))
* corrupting g2a.yaml after install fixed ([366b312](https://github.com/Goorsky1/klio/commit/366b31212ed1da10c0ea49f141b40bac52019efb))
* fail when registries not passed ([d9a0bb1](https://github.com/Goorsky1/klio/commit/d9a0bb17194e42bf7747140e5f230bcd0175b085))
* fix "file exists" error when extracting tarballs ([f9c7d42](https://github.com/Goorsky1/klio/commit/f9c7d422db79da9f6a2f16ed4266ad5bbb3569a7))
* fix "to many open files" error during downloading command ([ebf26c4](https://github.com/Goorsky1/klio/commit/ebf26c449f9d5ff05fe54f0defd8218864e7a5c0))
* fix checking for new version ([1bd1524](https://github.com/Goorsky1/klio/commit/1bd1524b2ab130f98d041e243e14e847a43172db))
* fix discovering local commands ([def3f8e](https://github.com/Goorsky1/klio/commit/def3f8e996b1de70f2d14e85c7ee7d147a007855))
* fix loading g2a.yaml and command.yaml ([1d6141d](https://github.com/Goorsky1/klio/commit/1d6141d69da9e8c398620149d2e1dce7e5897789))
* fix SIGSEGV when passed more than 3 -v params ([1cf5fd0](https://github.com/Goorsky1/klio/commit/1cf5fd0155a76be5ab3fd7f7bd50af14dc71ebb1))
* **get:** ensure cli-commands directory exists ([6b6f971](https://github.com/Goorsky1/klio/commit/6b6f9715d5b172d13b3fdc1d3ffee53fc4284917))
* Global scope in local scope (should be project) ([fab3765](https://github.com/Goorsky1/klio/commit/fab3765551b54a3ad0a67962cdead9ef88f03dff))
* install commands when klio.yaml is empty ([6bfa84f](https://github.com/Goorsky1/klio/commit/6bfa84f2c769acba11f18aac6ec1116de2ab2373))
* **log:** change color of fatal log entries ([f66dd9b](https://github.com/Goorsky1/klio/commit/f66dd9b3885da8be6afb8a8516bc262df35ea7ca))
* missing blank lines in sub commands output ([8c9fdd6](https://github.com/Goorsky1/klio/commit/8c9fdd6f6c6fc8451c323aba2df53ed39b7f0cac))
* print warn about new version to stderr ([c44cd6b](https://github.com/Goorsky1/klio/commit/c44cd6b6319b66a566ca692a270eb0db5126b375))
* properly format warn log ([#80](https://github.com/Goorsky1/klio/issues/80)) ([db1e9de](https://github.com/Goorsky1/klio/commit/db1e9de67ae92d35fb80250c46040a4a7a916fc3))
* remove bugged SetOuput and allow to create new logger instance ([#71](https://github.com/Goorsky1/klio/issues/71)) ([f8ec6fb](https://github.com/Goorsky1/klio/commit/f8ec6fbc62d432cb38966295c9605cbdb426c0d8))
* remove checksums from klio.yaml ([1616a58](https://github.com/Goorsky1/klio/commit/1616a584e312c39f2214e899c73db12a0b718b22)), closes [#32](https://github.com/Goorsky1/klio/issues/32)
* remove unused release-please param ([#78](https://github.com/Goorsky1/klio/issues/78)) ([383091d](https://github.com/Goorsky1/klio/commit/383091dfcca16801e4ed421d0cb640c527fb0566))
* return proper exit code from subcommands ([7b2bd3f](https://github.com/Goorsky1/klio/commit/7b2bd3f0fb488488a0c7cac00e0a30543cd60185))
* success message and implicit dependencies ([2ad5504](https://github.com/Goorsky1/klio/commit/2ad55047c021d3f278591243a996a350a1fdd1aa))
* traverse the whole path to find project config ([0234848](https://github.com/Goorsky1/klio/commit/02348485061170f568eb87928a1d6e10037f24ad))
* update CLI version in install script ([6fd6dbf](https://github.com/Goorsky1/klio/commit/6fd6dbfb7b35678e3968772062418b5150b3a7ed))
* update flush func to respect log level and add new line ([#73](https://github.com/Goorsky1/klio/issues/73)) ([e503488](https://github.com/Goorsky1/klio/commit/e5034886ec5411ebe2d3a59a61d87bccb465495c))
* various fixes after refactor ([bc081ef](https://github.com/Goorsky1/klio/commit/bc081efcdf2bbb28cc39a4bbf917810f8d712943))
* wrong logging on exit ([ca1137e](https://github.com/Goorsky1/klio/commit/ca1137e8c3ecb635709543abbf6283d3836c5a3c))
* wrong set of legacy APIVersions ([c7c6423](https://github.com/Goorsky1/klio/commit/c7c642369d87ca81f6af5b920c71161cbcc54ab8))


### Code Refactoring

* rename CLI to klio ([ec90198](https://github.com/Goorsky1/klio/commit/ec90198f6b8fca4a9eab78a43098384c485cb5cc)), closes [#3](https://github.com/Goorsky1/klio/issues/3) [#10](https://github.com/Goorsky1/klio/issues/10)

## [1.3.0](https://github.com/g2a-com/klio/compare/v1.2.0...v1.3.0) (2025-07-29)


### Features

* add --upgrade flag ([#88](https://github.com/g2a-com/klio/issues/88)) ([deffa47](https://github.com/g2a-com/klio/commit/deffa4742c8279a8c0efb23ad9bb1d565aa82fd0))

## [1.2.0](https://github.com/g2a-com/klio/compare/v1.1.4...v1.2.0) (2025-02-10)


### Features

* auto download divergent project commands ([#86](https://github.com/g2a-com/klio/issues/86)) ([bf2893a](https://github.com/g2a-com/klio/commit/bf2893adb1b03eeb8b3efba192cc2fdbb477a78f))

## [1.1.4](https://github.com/g2a-com/klio/compare/v1.1.3...v1.1.4) (2024-10-10)


### Bug Fixes

* properly format warn log ([#80](https://github.com/g2a-com/klio/issues/80)) ([db1e9de](https://github.com/g2a-com/klio/commit/db1e9de67ae92d35fb80250c46040a4a7a916fc3))

## [1.1.3](https://github.com/g2a-com/klio/compare/v1.1.2...v1.1.3) (2024-07-30)


### Bug Fixes

* remove unused release-please param ([#78](https://github.com/g2a-com/klio/issues/78)) ([383091d](https://github.com/g2a-com/klio/commit/383091dfcca16801e4ed421d0cb640c527fb0566))

### [1.1.2](https://www.github.com/g2a-com/klio/compare/v1.1.1...v1.1.2) (2024-06-03)


### Bug Fixes

* update flush func to respect log level and add new line ([#73](https://www.github.com/g2a-com/klio/issues/73)) ([e503488](https://www.github.com/g2a-com/klio/commit/e5034886ec5411ebe2d3a59a61d87bccb465495c))

### [1.1.1](https://www.github.com/g2a-com/klio/compare/v1.1.0...v1.1.1) (2024-05-24)


### Bug Fixes

* remove bugged SetOuput and allow to create new logger instance ([#71](https://www.github.com/g2a-com/klio/issues/71)) ([f8ec6fb](https://www.github.com/g2a-com/klio/commit/f8ec6fbc62d432cb38966295c9605cbdb426c0d8))

## [1.1.0](https://www.github.com/g2a-com/klio/compare/v1.0.1...v1.1.0) (2024-05-21)


### Features

* **g2a-com#48:** expose internal logger in pkg ([#69](https://www.github.com/g2a-com/klio/issues/69)) ([362e2df](https://www.github.com/g2a-com/klio/commit/362e2df6e68838419a366acb9014076a8aac44e0))
* **g2a-com#52:** add 'remove' command ([#59](https://www.github.com/g2a-com/klio/issues/59)) ([d05de37](https://www.github.com/g2a-com/klio/commit/d05de37757853add6796a84fdfcd18f2e7519aa5))


### Bug Fixes

* change Manager interface, remove fatal with defer in place ([24a0f6f](https://www.github.com/g2a-com/klio/commit/24a0f6fd65048e5165b5fe0dec455ecab1b42c40))
* Global scope in local scope (should be project) ([fab3765](https://www.github.com/g2a-com/klio/commit/fab3765551b54a3ad0a67962cdead9ef88f03dff))
* success message and implicit dependencies ([2ad5504](https://www.github.com/g2a-com/klio/commit/2ad55047c021d3f278591243a996a350a1fdd1aa))
* traverse the whole path to find project config ([0234848](https://www.github.com/g2a-com/klio/commit/02348485061170f568eb87928a1d6e10037f24ad))
* various fixes after refactor ([bc081ef](https://www.github.com/g2a-com/klio/commit/bc081efcdf2bbb28cc39a4bbf917810f8d712943))
* wrong logging on exit ([ca1137e](https://www.github.com/g2a-com/klio/commit/ca1137e8c3ecb635709543abbf6283d3836c5a3c))
