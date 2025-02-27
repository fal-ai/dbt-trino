# dbt-trino Changelog

- This file provides a full account of all changes to `dbt-trino`
- Changes are listed under the (pre)release in which they first appear. Subsequent releases include changes from previous releases.
- "Breaking changes" listed under a version may require action from end users or external maintainers when upgrading to that version.
- Do not edit this file directly. This file is auto-generated using [changie](https://github.com/miniscruff/changie). For details on how to document a change, see [the contributing guide](https://github.com/starburstdata/dbt-trino/blob/master/CONTRIBUTING.md#adding-changelog-entry)
## dbt-trino 1.3.1 - November 04, 2022
### Fixes
- Fix table not dropped on `full-refresh` of incremental models ([#168](https://github.com/starburstdata/dbt-trino/pull/168))

### Contributors
- [@mdesmet](https://github.com/mdesmet) ([#168](https://github.com/starburstdata/dbt-trino/pull/168))
## dbt-trino 1.3.0 - October 21, 2022
### Breaking Changes
- By default incremental materializations will use views if all incremental operations can be applied atomically, please set `+views_enabled` to `false` in your incremental model if your connector doesn't support view creation to use a table instead. ([#160](https://github.com/starburstdata/dbt-trino/pull/160))
### Features
- Support for dbt 1.3 ([#160](https://github.com/starburstdata/dbt-trino/pull/160))
- added impersonate user config for ldap authentication ([#163](https://github.com/starburstdata/dbt-trino/issues/163), [#162](https://github.com/starburstdata/dbt-trino/pull/162))

### Contributors
- [@aezomz](https://github.com/aezomz) ([#162](https://github.com/starburstdata/dbt-trino/pull/162))
- [@mdesmet](https://github.com/mdesmet) ([#160](https://github.com/starburstdata/dbt-trino/pull/160), [#160](https://github.com/starburstdata/dbt-trino/pull/160))
## dbt-trino 1.2.3 - October 13, 2022
### Features
- Support `on_schema_change` on incremental models ([#48](https://github.com/starburstdata/dbt-trino/issues/48), [#134](https://github.com/starburstdata/dbt-trino/pull/134))
- Support security grants ([#130](https://github.com/starburstdata/dbt-trino/pull/130))
### Fixes
- Support mixed-case schemata through `TrinoQuotePolicy` ([#131](https://github.com/starburstdata/dbt-trino/issues/131), [#132](https://github.com/starburstdata/dbt-trino/pull/132))
- Adding Kerberos auth configs from the trino-python-client ([#137](https://github.com/starburstdata/dbt-trino/pull/137))
- Ignore case when matching relations ([#140](https://github.com/starburstdata/dbt-trino/issues/140), [#141](https://github.com/starburstdata/dbt-trino/pull/141))
- Fixes instantiation of CertificateAuthentication object from trino-python-client ([#149](https://github.com/starburstdata/dbt-trino/issues/149), [#150](https://github.com/starburstdata/dbt-trino/pull/150))
### Under the Hood
- Add testing for Starburst Galaxy ([#128](https://github.com/starburstdata/dbt-trino/issues/128), [#123](https://github.com/starburstdata/dbt-trino/pull/123))
- Add QuotePolicy for relations to not use quoted identifiers by default ([#131](https://github.com/starburstdata/dbt-trino/issues/131), [#132](https://github.com/starburstdata/dbt-trino/pull/132))
- Enable MERGE tests for Galaxy ([#133](https://github.com/starburstdata/dbt-trino/issues/133), [#139](https://github.com/starburstdata/dbt-trino/pull/139))
- Change `get_columns_in_relation` implementation to use `describe` to also support string relations ([#145](https://github.com/starburstdata/dbt-trino/pull/145))
### Dependencies
- Bump tox from 3.25.1 to 3.26.0 ([#27](https://github.com/starburstdata/dbt-trino/issues/27), [#124](https://github.com/starburstdata/dbt-trino/pull/124))
- Bump mypy from 0.971 to 0.981 ([#138](https://github.com/starburstdata/dbt-trino/pull/138))
- Bump mypy from 0.981 to 0.982 ([#143](https://github.com/starburstdata/dbt-trino/pull/143))

### Contributors
- [@BendettaSD](https://github.com/BendettaSD) ([#137](https://github.com/starburstdata/dbt-trino/pull/137))
- [@KateShopify](https://github.com/KateShopify) ([#150](https://github.com/starburstdata/dbt-trino/pull/150))
- [@bachng2017](https://github.com/bachng2017) ([#141](https://github.com/starburstdata/dbt-trino/pull/141))
- [@dependabot[bot]](https://github.com/dependabot[bot]) ([#124](https://github.com/starburstdata/dbt-trino/pull/124), [#138](https://github.com/starburstdata/dbt-trino/pull/138), [#143](https://github.com/starburstdata/dbt-trino/pull/143))
- [@hovaesco](https://github.com/hovaesco) ([#123](https://github.com/starburstdata/dbt-trino/pull/123), [#139](https://github.com/starburstdata/dbt-trino/pull/139))
- [@mdesmet](https://github.com/mdesmet) ([#134](https://github.com/starburstdata/dbt-trino/pull/134), [#130](https://github.com/starburstdata/dbt-trino/pull/130), [#132](https://github.com/starburstdata/dbt-trino/pull/132), [#132](https://github.com/starburstdata/dbt-trino/pull/132), [#145](https://github.com/starburstdata/dbt-trino/pull/145))
## dbt-trino 1.2.2 - September 15, 2022
### Features
- Support snapshot materialization ([#6](https://github.com/starburstdata/dbt-trino/issues/6), [#120](https://github.com/starburstdata/dbt-trino/pull/120))
### Under the Hood
- Add comments to catalog macro ([#115](https://github.com/starburstdata/dbt-trino/issues/115), [#116](https://github.com/starburstdata/dbt-trino/pull/116))
### Dependencies
- Bump black from 22.6.0 to 22.8.0 ([#27](https://github.com/starburstdata/dbt-trino/issues/27), [#119](https://github.com/starburstdata/dbt-trino/pull/119))

### Contributors
- [@dependabot[bot]](https://github.com/dependabot[bot]) ([#119](https://github.com/starburstdata/dbt-trino/pull/119))
- [@hovaesco](https://github.com/hovaesco) ([#116](https://github.com/starburstdata/dbt-trino/pull/116))
- [@mdesmet](https://github.com/mdesmet) ([#120](https://github.com/starburstdata/dbt-trino/pull/120))
## dbt-trino 1.2.1 - August 25, 2022
### Features
- Support `delete+insert` materialization ([#103](https://github.com/starburstdata/dbt-trino/issues/103), [#62](https://github.com/starburstdata/dbt-trino/pull/62))
- Add support for persist_docs ([#76](https://github.com/starburstdata/dbt-trino/issues/76), [#77](https://github.com/starburstdata/dbt-trino/pull/77))
- Add `merge` materialization ([#105](https://github.com/starburstdata/dbt-trino/issues/105), [#104](https://github.com/starburstdata/dbt-trino/pull/104))
### Under the Hood
- Improve developer experience (changie, pre-commit, black, isort) ([#97](https://github.com/starburstdata/dbt-trino/issues/97), [#98](https://github.com/starburstdata/dbt-trino/pull/98))
- Implement Veracode SCA security scan ([#100](https://github.com/starburstdata/dbt-trino/issues/100), [#90](https://github.com/starburstdata/dbt-trino/pull/90))
- Implement Dependabot for automated dependency updates ([#99](https://github.com/starburstdata/dbt-trino/issues/99), [#89](https://github.com/starburstdata/dbt-trino/pull/89))
### Security
- Require pyyaml 6.0 ([#96](https://github.com/starburstdata/dbt-trino/issues/96), [#106](https://github.com/starburstdata/dbt-trino/pull/106))

### Contributors
- [@hovaesco](https://github.com/hovaesco) ([#77](https://github.com/starburstdata/dbt-trino/pull/77), [#104](https://github.com/starburstdata/dbt-trino/pull/104))
- [@mdesmet](https://github.com/mdesmet) ([#62](https://github.com/starburstdata/dbt-trino/pull/62), [#98](https://github.com/starburstdata/dbt-trino/pull/98), [#90](https://github.com/starburstdata/dbt-trino/pull/90), [#89](https://github.com/starburstdata/dbt-trino/pull/89), [#106](https://github.com/starburstdata/dbt-trino/pull/106))
## dbt-trino 1.2.0 (August 3, 2022)

### Features
- Configurable retries of database operations ([#83](https://github.com/starburstdata/dbt-trino/pull/83))

### Fixes
- Fix `TrinoKerberosCredentials.trino_auth()` for kerberos authentication ([#78](https://github.com/starburstdata/dbt-trino/pull/78))

### Under the hood
- Move crossdb macros from trino-dbt-utils to adapter ([#83](https://github.com/starburstdata/dbt-trino/pull/83))
- Added dbt 1.2.0 standard adapter tests ([#83](https://github.com/starburstdata/dbt-trino/pull/83))
- Run CI on python 3.9 and 3.10 ([#83](https://github.com/starburstdata/dbt-trino/pull/83))

Contributors:
* [@vivianhsu0214](https://github.com/vivianhsu0214) ([#78](https://github.com/starburstdata/dbt-trino/pull/78))
* [@mdesmet](https://github.com/mdesmet) ([#83](https://github.com/starburstdata/dbt-trino/pull/83))
## dbt-trino 1.1.1 (June 20, 2022)

### Fixes
- Enable setting session properties per dbt model when `session_properties` is not defined in the dbt profile ([#71](https://github.com/starburstdata/dbt-trino/pull/71))
- Support impersonation with JWT, certificate and OAuth authentication ([#73](https://github.com/starburstdata/dbt-trino/issues/73), [#74](https://github.com/starburstdata/dbt-trino/pull/74))

Contributors:
* [@findinpath](https://github.com/findinpath) ([#71](https://github.com/starburstdata/dbt-trino/pull/71))
* [@mdesmet](https://github.com/mdesmet) ([#74](https://github.com/starburstdata/dbt-trino/pull/74))
## dbt-trino 1.1.0 (May 9, 2022)

### Features
- Add support for `on_table_exists` in table materialization ([#26](https://github.com/starburstdata/dbt-trino/issues/26), [#54](https://github.com/starburstdata/dbt-trino/pull/54))
- Adds support for OAuth2 authentication using web browser ([#40](https://github.com/starburstdata/dbt-trino/issues/40), [#41](https://github.com/starburstdata/dbt-trino/pull/41))
- Add `view_security` to define security mode for views ([#65](https://github.com/starburstdata/dbt-trino/pull/65))
- Support for dbt source freshness ([#28](https://github.com/starburstdata/dbt-trino/issues/28), [#61](https://github.com/starburstdata/dbt-trino/pull/61))

### Fixes
- Add support for future versions of dbt-core ([#55](https://github.com/starburstdata/dbt-trino/issues/55), [#65](https://github.com/starburstdata/dbt-trino/pull/65))

### Under the hood
- Add PostgreSQL docker container for testing ([#66](https://github.com/starburstdata/dbt-trino/issues/66), [#67](https://github.com/starburstdata/dbt-trino/pull/67))
- Migrate to new adapter testing framework ([#57](https://github.com/starburstdata/dbt-trino/issues/57), [#65](https://github.com/starburstdata/dbt-trino/pull/65))
- Implement trino-python-client's prepared statements using `experimental_python_types` ([#61](https://github.com/starburstdata/dbt-trino/pull/61))

Contributors:
* [@hovaesco](https://github.com/hovaesco) ([#54](https://github.com/starburstdata/dbt-trino/pull/54), [#65](https://github.com/starburstdata/dbt-trino/pull/65), [#67](https://github.com/starburstdata/dbt-trino/pull/67))
* [@smith-m](https://github.com/smith-m) ([#65](https://github.com/starburstdata/dbt-trino/pull/65))
* [@mdesmet](https://github.com/mdesmet) ([#41](https://github.com/starburstdata/dbt-trino/pull/41), [#61](https://github.com/starburstdata/dbt-trino/pull/61))
## dbt-trino 1.0.3 (March 2, 2022)

### Features
- Adds support for Trino certificate authentication ([#45](https://github.com/starburstdata/dbt-trino/pull/45))

### Fixes
- Supporting custom schemas in incremental models ([#17](https://github.com/starburstdata/dbt-trino/issues/17), [#39](https://github.com/starburstdata/dbt-trino/pull/39))
- Supporting column type overrides in seeds ([#42](https://github.com/starburstdata/dbt-trino/issues/42)), ([#44](https://github.com/starburstdata/dbt-trino/pull/44))

### Under the hood
- Add missing tests to Makefile ([#43](https://github.com/starburstdata/dbt-trino/pull/43))
- Introduce PR template and `CHANGELOG.md` ([#47](https://github.com/starburstdata/dbt-trino/pull/47))

Contributors:
* [@hovaesco](https://github.com/hovaesco) ([#43](https://github.com/starburstdata/dbt-trino/pull/43), [#47](https://github.com/starburstdata/dbt-trino/pull/47))
* [@austenLacy](https://github.com/austenLacy) ([#45](https://github.com/starburstdata/dbt-trino/pull/45))
* [@rahulj51](https://github.com/rahulj51) ([#39](https://github.com/starburstdata/dbt-trino/pull/39))
* [@mdesmet](https://github.com/mdesmet) ([#44](https://github.com/starburstdata/dbt-trino/pull/44))
## dbt-trino 1.0.1 (January 24, 2022)

### Features
- Add support for JWT authentication ([#31](https://github.com/starburstdata/dbt-trino/issues/31), [#32](https://github.com/starburstdata/dbt-trino/pull/32))
- Adds certificate authentication as an optional credential parameter ([#23](https://github.com/starburstdata/dbt-trino/issues/23), [#24](https://github.com/starburstdata/dbt-trino/pull/24))

### Fixes
- Drop redundant transaction queries ([#20](https://github.com/starburstdata/dbt-trino/issues/20), [#30](https://github.com/starburstdata/dbt-trino/pull/30))

### Under the hood
- Upgrade to dbt-core 1.0.1 ([#34](https://github.com/starburstdata/dbt-trino/pull/34))

Contributors:
* [@Haunfelder](https://github.com/Haunfelder) ([#24](https://github.com/starburstdata/dbt-trino/pull/24))
* [@hovaesco](https://github.com/hovaesco) ([#30](https://github.com/starburstdata/dbt-trino/pull/30), [#32](https://github.com/starburstdata/dbt-trino/pull/32),  [#34](https://github.com/starburstdata/dbt-trino/pull/34))
## dbt-trino 1.0.0  (December 20, 2021)

### Features
- Add support for dbt `current_timestamp()` macro ([#15](https://github.com/starburstdata/dbt-trino/pull/15))

### Fixes
- Change default batch size to 1000 ([#16](https://github.com/starburstdata/dbt-trino/issues/16), [#18](https://github.com/starburstdata/dbt-trino/pull/18))

### Under the hood
- Add CI for Trino and Starburst ([#14](https://github.com/starburstdata/dbt-trino/pull/14))
- Add release pipeline ([#21](https://github.com/starburstdata/dbt-trino/pull/21))
- Upgrade to dbt-core 1.0.0 and variety of adjustments ([#25](https://github.com/starburstdata/dbt-trino/pull/25))

Contributors:
* [@findinpath](https://github.com/findinpath) ([#15](https://github.com/starburstdata/dbt-trino/pull/15))
* [@hovaesco](https://github.com/hovaesco) ([#14](https://github.com/starburstdata/dbt-trino/pull/14), [#18](https://github.com/starburstdata/dbt-trino/pull/18), [#21](https://github.com/starburstdata/dbt-trino/pull/21), [#25](https://github.com/starburstdata/dbt-trino/pull/25))
## dbt-trino 0.21.0  (October 8, 2021)

### Features
- Adding support for incremental models append strategy ([#1](https://github.com/starburstdata/dbt-trino/issues/1), [#10](https://github.com/starburstdata/dbt-trino/pull/10))

### Under the hood
- Upgrade to dbt-core 0.21.0 ([#11](https://github.com/starburstdata/dbt-trino/pull/11))

Contributors:
* [@findinpath](https://github.com/findinpath) ([#10](https://github.com/starburstdata/dbt-trino/pull/10))
* [@hovaesco](https://github.com/hovaesco) ([#11](https://github.com/starburstdata/dbt-trino/pull/11))
