===============
django-cracklib
===============

This django module runs password validation through cracklib_.

.. _cracklib: https://github.com/cracklib/cracklib

Dependencies
============

It requires module python-cracklib.

It is recommended that you also install your locales' dictionaries, like packages wbritish, wfrench or simmilar.

Set up
======

Add to your AUTH_PASSWORD_VALIDATORS::

   {
      'NAME': 'django_cracklib.password_validator.CrackPasswordValidator',
   },

Cracklib checks for password lengths, numeric characters and dictionaries, so you may remove MinimumLengthValidator, CommonPasswordValidator and NumericPasswordValidator. However, make sure you keep UserAttributeSimilarityValidator.

For translations to work, you'll need to install the module as an application::

    INSTALLED_APPS = [
        ...
        'django_cracklib',
    ]