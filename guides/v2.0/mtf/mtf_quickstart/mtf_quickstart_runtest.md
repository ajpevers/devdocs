---
layout: default
group: mtf-guide
subgroup: 30_Quickstart
title: Quick start with the Functional Testing Framework
menu_title: Test run
menu_order: 3
github_link: mtf/mtf_quickstart/mtf_quickstart_runtest.md
redirect_from: /guides/v1.0/mtf/mtf_quickstart/mtf_quickstart_runtest.html
---
<h2 id="mtf_quickstart_testrun">Test run</h2>

All tests classified by categories in corresponding directories in `<magento2>/dev/tests/functional/tests/app/Magento`.

FTF uses PHPUnit, which is located in `<magento2>/dev/tests/functional/vendor/bin` directory.

Be sure that your system is ready for test run.

- <a href="{{site.gdeurl}}mtf/mtf_installation.html#mtf_install_pre">Magento is ready for tests</a>
- <a href="{{site.gdeurl}}mtf/mtf_installation.html#mtf_install_check">The Functional Testing Framework is installed</a>
- <a href="{{site.gdeurl}}mtf/mtf_quickstart/mtf_quickstart_config.html">The Functional Testing Framework is configured</a>
- <a href="{{site.gdeurl}}mtf/mtf_quickstart/mtf_quickstart_environmemt.html">Environment is ready to test run</a>

### Run all tests {#mtf_quickstart_testrun_all}

Enter in terminal:
    
    cd <magento2>/dev/tests/functional
    vendor/bin/phpunit

This command will run all tests from `<magento2>/dev/tests/functional/tests/app/Magento/`.

### Run particular test {#mtf_quickstart_testrun_one}

Enter in terminal:

    cd <magento2>/dev/tests/functional
    vendor/bin/phpunit --filter <name of test>

Name of test is the name of PHP file with test.

Example:

Let's check creating of new category. For this we should run `<magento2>/dev/tests/functional/tests/app/Magento/Catalog/Test/TestCase/Category/CreateCategoryEntityTest.php`. To run this test enter the following script in your terminal:

    cd <magento2>/dev/tests/functional
    vendor/bin/phpunit --filter CreateCategoryEntityTest

<h2 id="mtf_install_pre">Next Steps</h2>

[&lt;&lt; Prepare environment for test]({{ site.gdeurl }}mtf/mtf_quickstart/mtf_quickstart_environmemt.html) | [See logs for failed tests &gt;&gt;]({{ site.gdeurl }}mtf/mtf_quickstart/mtf_quickstart_logs.html)