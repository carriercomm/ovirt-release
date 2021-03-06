dnl
dnl ovirt-release -- repo files for oVirt projects
dnl Copyright (C) 2014-2015 Red Hat, Inc.
dnl
dnl This library is free software; you can redistribute it and/or
dnl modify it under the terms of the GNU Lesser General Public
dnl License as published by the Free Software Foundation; either
dnl version 2.1 of the License, or (at your option) any later version.
dnl
dnl This library is distributed in the hope that it will be useful,
dnl but WITHOUT ANY WARRANTY; without even the implied warranty of
dnl MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
dnl Lesser General Public License for more details.
dnl
dnl You should have received a copy of the GNU Lesser General Public
dnl License along with this library; if not, write to the Free Software
dnl Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA
dnl


define([VERSION_NUMBER], [001])
define([VERSION_SUFFIX], [_alpha])
define([OVIRT_VERSION_MAJOR], [3])
define([OVIRT_VERSION_MINOR], [6])
AC_INIT([ovirt-release][]OVIRT_VERSION_MAJOR[]OVIRT_VERSION_MINOR, VERSION_NUMBER[]VERSION_SUFFIX, [infra@ovirt.org])
AM_INIT_AUTOMAKE

PACKAGE_RPM_VERSION="VERSION_NUMBER"
AC_SUBST([PACKAGE_RPM_VERSION])

PACKAGE_RPM_RELEASE="0.2.$(echo VERSION_SUFFIX | sed 's/^_//')"
AC_SUBST([PACKAGE_RPM_RELEASE])

OVIRT_SLOT="OVIRT_VERSION_MAJOR.OVIRT_VERSION_MINOR"
AC_SUBST([OVIRT_SLOT])

AC_ARG_WITH([ovirt-yum-repo],[AC_HELP_STRING([--with-ovirt-yum-repo],
            [Specify yum repo. default: "http://resources.ovirt.org"])],
            [OVIRT_YUM_REPO="$withval"],
            [OVIRT_YUM_REPO="http://resources.ovirt.org"])
AC_SUBST([OVIRT_YUM_REPO])

AC_ARG_WITH([repo-url-key],[AC_HELP_STRING([--with-repo-url-key],
            [Specify yum repo. default: "mirrorlist"])],
            [REPO_URL_KEY="$withval"],
            [REPO_URL_KEY="mirrorlist"])
AC_SUBST([REPO_URL_KEY])

AC_ARG_WITH([repo-path-normal],[AC_HELP_STRING([--with-repo-path-normal],
            [Specify path on yum-repo. default: "/pub/yum-repo/mirrorlist-ovirt-${OVIRT_SLOT}-snapshot-"])],
            [REPO_PATH_NORMAL="$withval"],
            [REPO_PATH_NORMAL="/pub/yum-repo/mirrorlist-ovirt-${OVIRT_SLOT}-snapshot-"])
AC_SUBST([REPO_PATH_NORMAL])

AC_ARG_WITH([repo-path-static],[AC_HELP_STRING([--with-repo-path-static],
            [Specify static path on yum-repo. default: "/pub/yum-repo/mirrorlist-ovirt-${OVIRT_SLOT}-snapshot-static-"])],
            [REPO_PATH_STATIC="$withval"],
            [REPO_PATH_STATIC="/pub/yum-repo/mirrorlist-ovirt-${OVIRT_SLOT}-snapshot-static-"])
AC_SUBST([REPO_PATH_STATIC])

AC_ARG_WITH([ovirt-yum-repo],[AC_HELP_STRING([--with-ovirt-yum-repo],
            [Specify yum repo. default: "http://resources.ovirt.org"])],
            [OVIRT_YUM_REPO="$withval"],
            [OVIRT_YUM_REPO="http://resources.ovirt.org"])
AC_SUBST([OVIRT_YUM_REPO])

PRODUCT_NAME=oVirt\ Packages\ Repository

AC_CONFIG_FILES([
            Makefile
            ovirt-el6-deps.repo
            ovirt-el7-deps.repo
            ovirt-f20-deps.repo
            ovirt-f21-deps.repo
            ovirt-f22-deps.repo
            ovirt-release36.spec
            ovirt.repo
])
AC_OUTPUT
