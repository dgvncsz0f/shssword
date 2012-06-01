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

::

  . pwdcnf
  complete -o filenames -F _pwdcomp pwdshow
  complete -o filenames -F _pwdcomp pwdfor
  complete -o filenames -F _pwdcomp pwddel

