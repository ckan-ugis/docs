***********************
﻿Описание изменений
***********************

 Обновление CKAN
========================================

С версии 2.0.3 до версии 2.2

http://docs.ckan.org/en/latest/maintaining/upgrading/index.html

Запуск virtualenv:

.. code-block:: none 
	
	sudo -s
	source /usr/lib/ckan/default/bin/activate
	
Бэкап базы данных:

.. code-block:: none 

	/usr/lib/ckan/default/bin/paster db dump --config=/etc/ckan/default/production.ini ugis_ckan_database.pg_dump 
	
\- заменил development.ini на production.ini т.к. изначально установлена production версия CKAN (из бинарников).


.. note::

Most errors with paster commands can be solved by remembering to activate your virtual environment and change to the ckan directory before running the command:

.. code-block:: none 

	. /usr/lib/ckan/default/bin/activate
	cd /usr/lib/ckan/default/src/ckan

Безопасность
============================

reCAPTCHA 

В production.ini:

ckan.recaptcha.publickey
---------------------------

The public key for your Recaptcha account, for example:

.. code-block:: none 

	ckan.recaptcha.publickey = 6Lc...-KLc

To get a Recaptcha account, sign up at: http://www.google.com/recaptcha

ckan.recaptcha.privatekey
--------------------------

The private key for your Recaptcha account, for example:

.. code-block:: none 

	ckan.recaptcha.privatekey = 6Lc...-jP

Setting both ckan.recaptcha.publickey and ckan.recaptcha.privatekey adds captcha to the user registration form. This has been effective at preventing bots registering users and creating spam packages.
