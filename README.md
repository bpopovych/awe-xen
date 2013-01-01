awe-xen
=======

Ebuilds for Xen hypervisor


NOTE
------

For successful xen-tools installation following tricks should be applied

- use LANG="en_US.utf8"
- in pyconfig.h unset HAVE_ATTRIBUTE_FORMAT_PARSETUPLE in order to avoid
warning like "‘PyArg_ParseTuple’ is an unrecognized format function type"

> --- /usr/include/python2.7/pyconfig.h  
> +++ /usr/include/python2.7/pyconfig.h  
> @@ -69,7 +69,7 @@  
>  #define HAVE_ATANH 1  
>    
>  /* Define if GCC supports __attribute__((format(PyArg_ParseTuple, 2, 3))) */  
> -#define HAVE_ATTRIBUTE_FORMAT_PARSETUPLE 1  
> +//#define HAVE_ATTRIBUTE_FORMAT_PARSETUPLE 1  
>    
>  /* Define to 1 if you have the `bind_textdomain_codeset' function. */  
>  #define HAVE_BIND_TEXTDOMAIN_CODESET 1  

