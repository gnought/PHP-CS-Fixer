==============================================
Rule ``no_unreachable_default_argument_value``
==============================================

In function arguments there must not be arguments with default values before
non-default ones.

Warning
-------

Using this rule is risky
~~~~~~~~~~~~~~~~~~~~~~~~

Modifies the signature of functions; therefore risky when using systems (such as
some Symfony components) that rely on those (for example through reflection).

Examples
--------

Example #1
~~~~~~~~~~

.. code-block:: diff

   --- Original
   +++ New
    <?php
   -function example($foo = "two words", $bar) {}
   +function example($foo, $bar) {}

Rule sets
---------

The rule is part of the following rule sets:

- `@PER-CS1.0:risky <./../../ruleSets/PER-CS1.0Risky.rst>`_
- `@PER-CS2.0:risky <./../../ruleSets/PER-CS2.0Risky.rst>`_
- `@PER-CS:risky <./../../ruleSets/PER-CSRisky.rst>`_
- `@PER:risky <./../../ruleSets/PERRisky.rst>`_
- `@PHP80Migration:risky <./../../ruleSets/PHP80MigrationRisky.rst>`_
- `@PHP82Migration:risky <./../../ruleSets/PHP82MigrationRisky.rst>`_
- `@PSR12:risky <./../../ruleSets/PSR12Risky.rst>`_
- `@PhpCsFixer:risky <./../../ruleSets/PhpCsFixerRisky.rst>`_
- `@Symfony:risky <./../../ruleSets/SymfonyRisky.rst>`_

References
----------

- Fixer class: `PhpCsFixer\\Fixer\\FunctionNotation\\NoUnreachableDefaultArgumentValueFixer <./../../../src/Fixer/FunctionNotation/NoUnreachableDefaultArgumentValueFixer.php>`_
- Test class: `PhpCsFixer\\Tests\\Fixer\\FunctionNotation\\NoUnreachableDefaultArgumentValueFixerTest <./../../../tests/Fixer/FunctionNotation/NoUnreachableDefaultArgumentValueFixerTest.php>`_

The test class defines officially supported behaviour. Each test case is a part of our backward compatibility promise.
