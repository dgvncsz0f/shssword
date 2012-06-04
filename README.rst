==========
 shssword
==========

very simple password management system

insert/update
=============

::
  
  # user-suplied password
  $ pwdset :key
  
  # system-generated password
  $ pwdgen :key :size

  # arbitrary string
  $ cat /some/file | pwdread :key

querying
========

::

  # show the password
  $ pwdshow :key
  
  # copy to primary selection
  $ pwdcopy :key
  
  # list all passwords
  $ pwdlist

deleting
========

::

  # remove a given key
  $ pwdrm :key

bash completion
===============

`pwdlist` must be found on $PATH for this to work:

::

  . pwdcnf
  complete -o filenames -F _pwdcomp pwdshow
  complete -o filenames -F _pwdcomp pwdfor
  complete -o filenames -F _pwdcomp pwddel

dependencies
============

* gnupg

* xsel

* xargs

* find

* coreutils: mv, tr, dirname, basename, readlink

* at least one of the following must be present (here listed as debian
  packages) for `pwdgen` to work:

  - libcrypt-generatepassword-perl

  - pwgen

  - makepasswd

tips
====

* modify your $PATH variable to use these scripts;

* use *gpg-agent*, makes life a lot easier;
