AC_INIT(pwauth, 2.3.12~mwp)
AM_INIT_AUTOMAKE(foreign)
AC_PREREQ(2.69)

AC_CONFIG_SRCDIR(Makefile.in)
AC_CONFIG_FILES(Makefile)

AC_ARG_ENABLE(shadow-none,
    [AS_HELP_STRING(--enable-shadow-none,
        authenticate using legacy password file)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(SHADOW_NONE)])])

AC_ARG_ENABLE(shadow-bsd,
    [AS_HELP_STRING(--enable-shadow-bsd,
        authenticate using BSD style shadow password file)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(SHADOW_BSD)])])

AC_ARG_ENABLE(shadow-sun,
    [AS_HELP_STRING(--enable-shadow-sun,
        authenticate using Sun style shadow password file)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(SHADOW_SUN)])])

AC_ARG_ENABLE(shadow-jfh,
    [AS_HELP_STRING(--enable-shadow-jfh,
        authenticate using JFH shadow API)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(SHADOW_JFH)])])

AC_ARG_ENABLE(shadow-mdw,
    [AS_HELP_STRING(--enable-shadow-mdw,
        authenticate using MDW shadow API)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(SHADOW_MDW)])])

AC_ARG_ENABLE(shadow-aix,
    [AS_HELP_STRING(--enable-shadow-aix,
        authenticate using AIX style shadow password file)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(SHADOW_AIX)])])

AC_ARG_ENABLE(shadow-hpux,
    [AS_HELP_STRING(--enable-shadow-hpux,
        authenticate using HPUX style shadow password file)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(SHADOW_HPUX)])])

AC_ARG_ENABLE(pam,
    [AS_HELP_STRING(--enable-pam,
        authenticate using PAM)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(PAM)])])

AC_ARG_ENABLE(pam-solaris,
    [AS_HELP_STRING(--enable-pam-solaris,
        authenticate using PAM on Solaris)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(PAM_SOLARIS)])])

AC_ARG_ENABLE(pam-solaris-26,
    [AS_HELP_STRING(--enable-pam-solaris-26,
        authenticate using PAM on Solaris 2.6)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(PAM_SOLARIS_26)])])

AC_ARG_ENABLE(pam-old-os-x,
    [AS_HELP_STRING(--enable-pam-old-os-x,
        authenticate using PAM on older versions of OS X)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(PAM_OLD_OS_X)])])

AC_ARG_ENABLE(login-conf-openbsd,
    [AS_HELP_STRING(--enable-login-conf-openbsd,
        authenticate using OpenBSD login.conf)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(PAM_OLD_OS_X)])])

AC_ARG_ENABLE(authenticate-aix,
    [AS_HELP_STRING(--enable-authenticate-aix,
        authenticate using AIX system call)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(AUTHENTICATE_AIX)])])

AC_ARG_ENABLE(faillog-jfh,
    [AS_HELP_STRING(--enable-faillog-jfh,
        enable JFH failure logging)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(FAILLOG_JFH)])])

AC_ARG_ENABLE(faillog-openbsd,
    [AS_HELP_STRING(--enable-faillog-openbsd,
        enable OpenBSD failure logging)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(FAILLOG_OPENBSD)])])

AC_ARG_ENABLE(faillog-pwauth,
    [AS_HELP_STRING(--enable-faillog-pwauth,
        enable pwauth failure logging)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(FAILLOG_PWAUTH)])])

AC_ARG_ENABLE(path-faillog,
    [AS_HELP_STRING(--enable-path-faillog=<path>,
        specify path of failure log)],
    [AS_IF([test "x$enableval" != xno],
        [AC_DEFINE_UNQUOTED(PATH_FAILLOG, "$enableval")])])

AC_ARG_ENABLE(max-fail-count,
    [AS_HELP_STRING(--enable-max-fail-count=<number>,
        specify maximum failure count)],
    [AS_IF([test "x$enableval" != xno],
        [AC_DEFINE_UNQUOTED(MAX_FAIL_COUNT, $enableval)])])

AC_ARG_ENABLE(reset-fail-count,
    [AS_HELP_STRING(--enable-reset-fail-count,
        enable reset of failure count)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(RESET_FAIL_COUNT)])])

AC_ARG_ENABLE(unix-lastlog,
    [AS_HELP_STRING(--enable-unix-lastlog,
        enable updating of lastlog entry)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(UNIX_LASTLOG)])])

AC_ARG_ENABLE(nologin-file,
    [AS_HELP_STRING(--enable-nologin-file=<path>,
        enable checking of nologin file)],
    [AS_IF([test "x$enableval" != xno],
        [AC_DEFINE_UNQUOTED(NOLOGIN_FILE, "$enableval")])])

AC_ARG_ENABLE(min-nologin-uid,
    [AS_HELP_STRING(--enable-min-nologin-uid=<uid>,
        specify minimum uid permitted to login)],
    [AS_IF([test "x$enableval" != xno],
        [AC_DEFINE_UNQUOTED(MIN_NOLOGIN_UID, $enableval)])])

AC_ARG_ENABLE(check-login-expiration,
    [AS_HELP_STRING(--enable-check-login-expiration,
        enable checking login expiration)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(CHECK_LOGIN_EXPIRATION)])])

AC_ARG_ENABLE(check-password-expiration,
    [AS_HELP_STRING(--enable-check-password-expiration,
        enable checking password expiration)],
    [AS_IF([test "x$enableval" != xno],
        [AC_DEFINE(CHECK_PASSWORD_EXPIRATION)])])

AC_ARG_ENABLE(server-uids,
    [AS_HELP_STRING(--enable-server-uids=<comma_seperated_uid_list>,
        enable checking of uids)],
    [AS_IF([test "x$enableval" != xno],
        [AC_DEFINE_UNQUOTED(SERVER_UIDS, $enableval)])])

AC_ARG_ENABLE(min-unix-id,
    [AS_HELP_STRING(--enable-min-unix-id=<uid>,
        enable minimum authenticatable uid)],
    [AS_IF([test "x$enableval" != xno],
        [AC_DEFINE_UNQUOTED(MIN_UNIX_UID, $enableval)])])

AC_ARG_ENABLE(ignore-case,
    [AS_HELP_STRING(--enable-ignore-case,
        enable case insensitive authentication)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(IGNORE_CASE)])])

AC_ARG_ENABLE(domain-name,
    [AS_HELP_STRING(--enable-domain-name,
        enable windows domain name stripping)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(DOMAIN_NAME)])])

AC_ARG_ENABLE(sleep-lock,
    [AS_HELP_STRING(--enable-sleep-lock=<path>,
        enable sleep lock)],
    [AS_IF([test "x$enableval" != xno],
        [AC_DEFINE_UNQUOTED(SLEEP_LOCK, "$enableval")])])

AC_ARG_ENABLE(sleep-time,
    [AS_HELP_STRING(--enable-sleep-time=<seconds>,
        specify sleep time)],
    [AS_IF([test "x$enableval" != xno],
        [AC_DEFINE_UNQUOTED(SLEEP_TIME, $enableval)])])

AC_ARG_ENABLE(env-method,
    [AS_HELP_STRING(--enable-env-method,
        enable passing of parameters in environment)],
    [AS_IF([test "x$enableval" != xno], [AC_DEFINE(ENV_METHOD)])])

AC_CHECK_HEADER(lastlog.h, [AC_DEFINE(HAVE_LASTLOG_H)])
AC_CHECK_HEADER(paths.h, [AC_DEFINE(PATHS_H)])

AS_IF([test "x${enable_shadow_none-no}" != xno],
    [AC_SEARCH_LIBS(crypt, crypt)])

AS_IF([test "x${enable_pam-no}" != xno],
    [AC_SEARCH_LIBS(pam_start, pam)])

AC_PROG_CC
AC_OUTPUT
