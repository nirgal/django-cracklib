This django module delegates password validation to cracklib.

It requires module python-cracklib

Usage: Add to your AUTH_PASSWORD_VALIDATORS::

   {
      'NAME': 'django_cracklib.password_validator.CrackPasswordValidator',
   },

