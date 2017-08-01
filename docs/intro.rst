Welcome
-------

F5's Automation, Orchestration and Programmability Trainingへようこそ！
このラボは、F5が提供する様々なプログラマビリティツールを活用するSuper NetOps及びDevOpsエンジニアを対象としています。F5のハンズオントレーニング環境を利用したい方は、F5までお問い合わせください。

このラボで使うプログラマビリティツールは、完全なDevOps CI(Continuous Integration)/CD(Continuous Delivery) パイプラインを活用しており、
以下のGitHubリポジトリから取得可能です。

https://github.com/f5devcentral/f5-automation-labs/

バグ修正や新機能追加のリクエストは、このリポジトリの `Issue <https://github.com/f5devcentral/f5-automation-labs/issues>`_ を開くことによって行うことができます。


はじめに
---------------
インストラクターの指示に従い、ジャンプホストにアクセスしてください。

.. NOTE::
	このラボでは、すべての作業はWindows Jumphostから行います。
	また、ローカルのPCに特別なアプリケーションをインストールする必要はございません。

ネットワーク構成
------------
	
このラボのネットワークトポロジは、データプレーンのトラフックフローではなくコントロールプレーンのプログラマビリティに焦点を当てるので、データプレーンは非常にシンプルです。ラボ環境には以下のコンポーネントが含まれています。

-  2 x F5 BIG-IP VE (v12.1)

-  1 x F5 iWorkflow VE (v2.1)

-  1 x Linux LAMP Webserver (xubuntu 14.04)

-  1 x Linux Docker Server (CentOS 7)

-  1 x Windows Jumphost

各コンポーネントのVLAN、IPアドレス、およびID/PASSWORDは以下をお使い下さい。

.. list-table::
    :widths: 20 40 40
    :header-rows: 1
    :stub-columns: 1

    * - **Component**
      - **VLAN/IP Address(es)**
      - **Credentials**
    * - Windows Jumphost
      - - **Management:** 10.1.1.250
        - **Internal:** 10.1.10.250
        - **External:** 10.1.20.250
      - Administrator/*available in instance details*
    * - BIG-IP A
      - - **Management:** 10.1.1.4
        - **Internal:** 10.1.10.1
        - **Internal (Float):** 10.1.10.3
        - **External:** 10.1.20.1
      - admin/admin
    * - BIG-IP B
      - - **Management:** 10.1.1.5
        - **Internal:** 10.1.10.2
        - **Internal (Float):** 10.1.10.3
        - **External:** 10.1.20.2
      - admin/admin
    * - iWorkflow
      - - **Management:** 10.1.1.6
      - admin/admin
    * - Linux Server
      - - **Management:** 10.1.1.7
        - **Internal:** 10.1.10.10-13
      - root/default
    * - Docker Server
      - - **Management:** 10.1.1.8
      - root/default
