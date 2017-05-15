========================================
Файл конфигурации
========================================

Общие настройки задаются в разделе ``General configuration`` файла ``conf.py``.

Изменение названия и копирайта
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
::

    # General information about the project.
    project = 'My Project'
    copyright = '2017, Ivan Ivanov'


.. _unicode_label:

Cтроки Unicode
~~~~~~~~~~~~~~

Использование кириллических символов в названиях проекта и других строках, может приводить к ошибкам генерации. В версии Sphinx для Python 3  таких проблем не наблюдается. В версии для Python 2.7 перед каждой кириллической строкой необходимо ставить  ``u``.

.. code-block:: python

    project = u'Мой проект'
    copyright = u'2017, Иван Иванов'


.. _versions-conf:

Версии публикации
~~~~~~~~~~~~~~~~~
Изменить параметры ``version`` и ``release``:
::

    # The short X.Y version.
    version = '1'
    # The full version, including alpha/beta/rc tags.
    release = '1'


.. _lang-conf:

Смена HTML-темы
~~~~~~~~~~~~~~~

В строке ``html_theme`` указать название используемой темы:
::

    html_theme = 'sphinx_rtd_theme'

Раскомментировать строку `html_theme_path` и прописать в ней путь к HTML-теме: 
::
    
    html_theme_path = ['.']

В Sphinx есть ряд встроенных тем. Для их подключения достаточно написать название темы в строке ``html_theme``, путь указывать не надо. Названия стандартных тем:

* default
* sphinxdoc
* scrolls
* agogo
* traditional
* nature
* haiku
* pyramid

Некоторые из перечисленных тем поддерживают дополнительные настройки. Подробнее смотрите раздел `HTML theming support <http://sphinx-doc.org/theming.html>`_ официальной документации Sphinx.

.. note:: В Read The Docs при значении  ``html_theme = 'default'`` используется тема Read The Docs.

