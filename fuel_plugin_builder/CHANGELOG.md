# Changelog

## 2.0.5 (UNRELEASED)

## 2.0.4 (2014-06-23)

- Fix, remove plugin package from previous build
  https://bugs.launchpad.net/fuel/+bug/1464143

## 2.0.3 (2014-06-08)

- New "monitoring" group
  https://bugs.launchpad.net/fuel/+bug/1458592
- Fix, fail build, if there are invalid deb packages for ubuntu repository
  https://bugs.launchpad.net/fuel/+bug/1447981
- Fix dependency package name for newer CentOS
  https://bugs.launchpad.net/fuel/+bug/1455882

## 2.0.2 (2014-05-15)

- Reverted fix for https://bugs.launchpad.net/fuel/+bug/1447981
  because it caused creation of broken ubuntu repository
  https://bugs.launchpad.net/fuel-plugins/+bug/1455130

## 2.0.1 (2014-05-08)

- Fix, fail build, if there are invalid deb packages for ubuntu repository
  https://bugs.launchpad.net/fuel/+bug/1447981
- Fix validation for UI restrictions
  https://bugs.launchpad.net/fuel/+bug/1448147
- Fix packages duplication after plugin build
  https://bugs.launchpad.net/fuel/+bug/1451751
- Fix plugin name validation
  https://bugs.launchpad.net/fuel/+bug/1439760

## 2.0.0 (2014-04-30)

- New package version "2.0.0", which is generated by default
- For plugins with 2.0.0 package version, fpb builds rpm packages
  instead of *.fp archives. It was required for plugins updates
  https://github.com/stackforge/fuel-specs/blob/master/specs/6.1/plugins-security-fixes.rst
- New "reboot" task for 2.0.0 plugins, which can reboot the node
  and wait until reboot process is finished, see more details in the specification
  https://github.com/stackforge/fuel-specs/blob/master/specs/6.1/reboot-task-type-for-plugin-developers.rst
- New required field groups, now you can specify a list of groups
  which your plugin implements, see more details in the specification
  https://github.com/stackforge/fuel-specs/blob/master/specs/6.1/plugin-groups.rst
- New required field authors (for plugins with 2.0.0 package version)
- New required field licenses (for plugins with 2.0.0 package version)
- New required field homepage (for plugins with 2.0.0 package version)
- New parameter "--package-version", to generate the plugins in old
  format (e.g. package version 1.0.0)
- Fixed, plugins with package version 2.0.0, generate Release file
  for Ubuntu repositories
  https://bugs.launchpad.net/fuel/+bug/1435892
- New format of stages for plugins with package version 2.0.0,
  added numerical postfixes
  https://github.com/stackforge/fuel-specs/blob/master/specs/6.1/plugins-deployment-order.rst

## 1.0.2 (2014-12-19)

- Show correct message, if 'timeout' field is not specified for
  task in tasks.yaml
  https://bugs.launchpad.net/fuel/+bug/1396234
- Print error messages to stderr instead of stdout
- Fixed validation for environment_config.yaml file, "attributes"
  field is optional
  https://bugs.launchpad.net/fuel/+bug/1396491
- Improved validation for environment_config.yaml file, added
  required fields for attributes
- Generate file with SHA1 checksums for each file in the plugin
  https://bugs.launchpad.net/fuel/+bug/1403960

## 1.0.1 (2014-11-20)

- Show instruction for CentOS if not all requirements are installed
- Fixed bug, deploy.sh doesn't have execution permission
  https://bugs.launchpad.net/fuel/+bug/1392736
- Fixed bug, don't fail validation if environment_config.yaml file has checkbox
  https://bugs.launchpad.net/fuel/+bug/1392807

## 1.0.0 (2014-11-13)

Initial public release

- Plugin create
- Plugin build
- Plugin check
