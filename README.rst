===============
django-cracklib
===============

This django module runs password validation through cracklib_.

It requires module python-cracklib.

It is recommended that you also install your locales' dictionaries, like packages wbritish, wfrench or simmilar.

Configuration
=============

Add to your AUTH_PASSWORD_VALIDATORS_::

   {
      'NAME': 'django_cracklib.password_validation.CrackPasswordValidator',
   },

Cracklib checks for password lengths, numeric characters and dictionaries, so you may remove MinimumLengthValidator, CommonPasswordValidator and NumericPasswordValidator. If you do, however, make sure you keep UserAttributeSimilarityValidator.

For translations to work, you'll need to install the module as an application::

    INSTALLED_APPS = [
        ...
        'django_cracklib',
    ]

.. _cracklib: https://github.com/cracklib/cracklib
.. _AUTH_PASSWORD_VALIDATORS: https://docs.djangoproject.com/en/dev/topics/auth/passwords/#module-django.contrib.auth.password_validation
