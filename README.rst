==========
 shssword
==========

very simple password management system

insert/udpate
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
  
  # copy to clipboard
  $ pwdfor :key
  
  # list all passwords
  $ pwdls

deleting
========

::

  # pwddel :key

bash completion
===============

::

  . pwdcnf
  complete -o filenames -F _pwdcomp pwdshow
  complete -o filenames -F _pwdcomp pwdfor
  complete -o filenames -F _pwdcomp pwddel
