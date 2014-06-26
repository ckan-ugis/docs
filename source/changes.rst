Описание изменений:
***********************
 Обновление CKAN
 --------------------------------
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
