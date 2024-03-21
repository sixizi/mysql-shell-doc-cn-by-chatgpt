## A.1 mysqlsh — MySQL Shell

MySQL Shell 是一个高级命令行客户端和 MySQL 的代码编辑器。除了 SQL 之外，MySQL Shell 还为 JavaScript 和 Python 提供了脚本功能。有关使用 MySQL Shell 的信息，请参见 MySQL Shell 8.0。当 MySQL Shell 通过 X 协议连接到 MySQL Server 时，可以使用 X DevAPI 来处理关系型和文档数据，参见使用 MySQL 作为文档存储。MySQL Shell 包含了 AdminAPI，使您能够处理 InnoDB Cluster、InnoDB ClusterSet 和 InnoDB ReplicaSet 部署；参见第 6 章，MySQL AdminAPI。

这里描述的许多选项与 MySQL Shell 和 MySQL Server 实例之间的连接有关。更多信息请参见第 4.3 节，“MySQL Shell 连接”。

`mysqlsh` 支持以下命令行选项。

表 A.1 `mysqlsh` 选项

| 选项名称                  | 描述                                                         | 引入版本 | 弃用版本 |
| ------------------------- | :----------------------------------------------------------- | -------: | -------- |
| --                        | API 命令行集成的开始                                         |          |          |
| --auth-method             | 使用的认证方法                                               |          |          |
| --cluster                 | 连接到 InnoDB 集群                                           |    8.0.4 |          |
| --column-type-info        | 在结果集中打印列的元数据                                     |   8.0.14 |          |
| --compress                | 压缩客户端和服务器之间发送的所有信息                         |   8.0.14 |          |
| --connect-timeout         | 全局会话的连接超时时间                                       |   8.0.13 |          |
| --credential-store-helper | 密码的秘密存储助手                                           |   8.0.12 |          |
| --database                | 使用的模式（--schema 的别名）                                |          |          |
| --dba                     | 在与 MySQL 5.7 服务器的连接中启用 X 协议                     |          |          |
| --dba-log-sql             | 记录 AdminAPI 操作执行的 SQL 语句                            |   8.0.18 | 8.0.30   |
| --dbpassword              | 连接服务器时使用的密码                                       |          | 8.0.13   |
| --dbuser                  | 连接服务器时使用的 MySQL 用户名                              |          | 8.0.13   |
| --execute                 | 执行命令并退出                                               |          |          |
| --fido-register-factor    | 为服务器认证注册 FIDO 设备                                   |   8.0.29 |          |
| --file                    | 在批处理模式下处理的文件                                     |          |          |
| --force                   | 即使发生错误，也继续在 SQL 和批处理模式下执行                |          |          |
| --get-server-public-key   | 从服务器请求 RSA 公钥                                        |          |          |
| --help                    | 显示帮助信息并退出                                           |          |          |
| --histignore              | 不添加到历史记录的字符串                                     |    8.0.3 |          |
| --host                    | MySQL 服务器实例所在的主机                                   |          |          |
| --import                  | 从文件或标准输入导入 JSON 文档                               |   8.0.13 |          |
| --interactive             | 在批处理模式下模拟交互模式                                   |          |          |
| --js, --javascript        | 以 JavaScript 模式启动                                       |          |          |
| --json                    | 以 JSON 格式打印输出                                         |          |          |
| --log-file                | 此实例的日志文件位置                                         |   8.0.27 |          |
| --log-level               | 指定日志级别                                                 |          |          |
| --log-sql                 | 将所有 MySQL Shell 生成的 SQL 语句记录到 MySQL Shell 日志文件。 |   8.0.30 |          |
| -ma                       | 自动检测会话的传输协议                                       |    8.0.3 | 8.0.13   |
| --mysql, -mc              | 使用经典 MySQL 协议创建会话                                  |    8.0.3 |          |
| --mysql-plugin-dir        | 客户端插件安装的目录                                         |   8.0.27 |          |
| --mysqlx, -mx             | 使用 X 协议创建会话                                          |    8.0.3 |          |
| --name-cache              | 根据活动的默认模式自动加载表名                               |    8.0.4 |          |
| --no-name-cache           | 禁用自动完成                                                 |    8.0.4 |          |
| --no-password             | 此连接未提供密码                                             |          |          |
| --no-wizard, --nw         | 禁用交互式向导                                               |          |          |
| --pager                   | 用于显示输出的外部分页工具                                   |   8.0.13 |          |
| --password                | 连接服务器时使用的密码（--dbpassword 的别名）                |          |          |
| --password1               | 多因素认证的密码 1（等同于 --password）                      |   8.0.28 |          |
| --password2               | 多因素认证的密码 2                                           |   8.0.28 |          |
| --password3               | 多因素认证的密码 3                                           |   8.0.28 |          |
| --passwords-from-stdin    | 从标准输入读取密码                                           |          |          |
| --port                    | 连接的 TCP/IP 端口号                                         |          |          |
| --py, --python            | 以 Python 模式启动                                           |          |          |
| --pyc                     | 执行 Python 命令并退出。在此之后指定的任何选项都被视为处理命令的参数。 |   8.0.31 |          |
| --quiet-start             | 启动时不打印介绍性信息                                       |          |          |
| --recreate-schema         | 删除并重新创建模式                                           |          |          |
| --redirect-primary        | 确保连接到 InnoDB 集群的主节点                               |    8.0.4 |          |
| --redirect-secondary      | 确保连接到 InnoDB 集群的辅助节点                             |          |          |
| --result-format           | 设置此会话的输出格式                                         |   8.0.14 |          |
| --save-passwords          | 密码在秘密存储中的存储方式                                   |   8.0.12 |          |
| --schema                  | 使用的模式                                                   |          |          |
| --server-public-key-path  | 包含 RSA 公钥的文件的路径名                                  |          |          |
| --show-warnings           | 如果有任何警告，在每个语句之后显示警告（在 SQL 模式下）      |          |          |
| --socket                  | 使用的 Unix 套接字文件或 Windows 命名管道（仅限经典 MySQL 协议） |          |          |
| --sql                     | 以 SQL 模式启动，自动检测用于连接的协议                      |          |          |
| --sqlc                    | 使用经典 MySQL 协议连接的 SQL 模式启动                       |          |          |
| --sqlx                    | 使用 X 协议连接的 SQL 模式启动                               |    8.0.3 |          |
| --ssh                     | 连接到 SSH 服务器的 URI                                      |   8.0.28 |          |
| --ssh-config-file         | 连接到 SSH 服务器的配置文件                                  |   8.0.28 |          |
| --ssh-identity-file       | 连接到 SSH 服务器的身份文件                                  |   8.0.28 |          |
| --ssl-ca                  | 包含受信任 SSL 证书颁发机构列表的文件                        |          |          |
| --ssl-capath              | 包含受信任 SSL 证书颁发机构证书文件的目录                    |          |          |
| --ssl-cert                | 包含 X.509 证书的文件                                        |          |          |
| --ssl-cipher              | 要使用的 SSL 密码名                                          |          |          |
| --ssl-crl                 |                                                              |          |          |
| --ssl-crlpath             | 包含证书吊销列表文件的目录                                   |          |          |
| --ssl-key                 | 包含 X.509 密钥的文件                                        |          |          |
| --ssl-mode                | 连接到服务器的期望安全状态                                   |          |          |
| --syslog                  | 将交互式 SQL 语句记录到系统日志设施                          |   8.0.24 |          |
| --tabbed                  | 以制表符分隔的格式显示输出                                   |          |          |
| --table                   | 以表格格式显示输出                                           |          |          |
| --tls-version             | 加密连接允许的 TLS 协议                                      |          |          |
| --uri                     | 会话信息的 URI 格式                                          |          |          |
| --user                    | 连接服务器时使用的 MySQL 用户名（--dbuser 的别名）           |          |          |
| --verbose                 | 激活控制台的详细输出                                         |   8.0.17 |          |
| --version                 | 显示版本信息并退出                                           |          |          |
| --vertical                | 纵向显示所有 SQL 结果                                        |          |          |

--help, -?

显示帮助信息并退出。

--

标志 `mysqlsh` 选项列表的结束，以及 MySQL Shell API 命令行集成的命令及其参数的开始。您可以使用此语法从命令行执行 MySQL Shell 全局对象的方法：

```mysqlsh
[options] -- object method [arguments]
```

更多信息请参见第 5.8 节，“API 命令行集成”。

--auth-method=method

用于账户的认证方法。取决于账户密码使用的认证插件。对于使用经典 MySQL 协议的 MySQL Shell 连接，请指定认证插件的名称，例如 `caching_sha2_password`。对于使用 X 协议的 MySQL Shell 连接，请指定以下选项之一：

- AUTO: 让库选择认证方法。
- FALLBACK: 让库选择认证方法，但不使用任何与 MySQL 5.7 不兼容的认证方法。
- FROM_CAPABILITIES: 让库根据服务器实例宣布的能力选择认证方法。
- MYSQL41: 使用 MySQL 4.1 及更高版本支持的挑战-响应认证协议，不发送明文密码。此选项与使用 `mysql_native_password` 认证插件的账户兼容。
- PLAIN: 发送明文密码进行认证。仅在加密连接下使用此选项。此选项可以用于使用 `caching_sha2_password` 认证插件的账户的缓存凭据进行认证，前提是有 SSL 连接。参见使用 X 插件与 Caching SHA-2 认证插件。
- SHA256_MEMORY: 使用存储在内存中的哈希密码进行认证。此选项可以用于使用 `caching_sha2_password` 认证插件的账户的缓存凭据进行认证，其中有一个非 SSL 连接。参见使用 X 插件与 Caching SHA-2 认证插件。

对于使用经典 MySQL 协议的 MySQL Shell 连接，请指定用户账户使用的认证插件的名称，例如 `caching_sha2_password`（这是 MySQL 8.0 中创建用户账户的默认设置）。MySQL Shell 使用 MySQL 客户端库进行客户端端认证。以下认证方法需要额外配置：

- clear_text_password: 简单的 LDAP 认证需要 `mysql_clear_password` 客户端插件。它内置于 MySQL 客户端库中，但出于安全考虑，默认情况下不启用。从 MySQL Shell 8.0.27 开始，当您使用 `--auth-method=clear_text_password` 连接选项指定它时，MySQL Shell 会启用并使用该插件。此认证类型只适用于使用 SSL 或套接字的安全连接，因此您必须在使用它之前配置安全连接。请注意，使用 `ssl-mode=preferred` 选项时，SSL 连接不是必须的，因此设置此选项的连接不被视为 SSL 连接。更多信息，请参见第 4.3.4 节，“使用加密连接”。

- authentication_ldap_sasl_client: `authentication_ldap_sasl_client` 客户端插件用于基于 SASL 的 LDAP 认证，包括 GSSAPI/Kerberos 认证。它不内置于 MySQL 客户端库中，但随 MySQL 服务器包一起提供。要加载它，您必须使用 `--mysql-plugin-dir` 选项（从 MySQL Shell 8.0.27 开始可用）来指定 MySQL 服务器包中插件的路径。

- authentication_kerberos_client: `authentication_kerberos_client` 客户端插件用于 Kerberos 认证。它不内置于 MySQL 客户端库中，但随 MySQL 服务器包一起提供。要加载它，您必须使用 `--mysql-plugin-dir` 选项（从 MySQL Shell 8.0.27 开始可用）来指定 MySQL 服务器包中插件的路径。

当使用 `--auth-method` 选项指定 `authentication_ldap_sasl_client` 或 `authentication_kerberos_client` 插件，并使用 `--mysql-plugin-dir` 选项提供插件路径时，从 MySQL 8.0.27 开始支持 Kerberos 认证的缓存票据授予票据（TGTs）。使用缓存 TGTs 时，不要在连接选项中指定用户和密码。当您指定这些插件之一并且没有指定用户和密码时，MySQL Shell 不会提供系统用户名，不会提示输入密码，也不会尝试使用秘密存储助手检索或存储凭据。

更多信息，请参见第 4.3.5 节，“使用 LDAP 和 Kerberos 认证”。

--cluster

确保目标服务器是 InnoDB 集群的一部分，如果是，将集群全局变量设置为集群对象。

--column-type-info

在 SQL 模式下，在打印查询返回的结果集之前，打印结果集中每列的元数据，如列类型和排序规则。

列类型以 MySQL Shell 使用的类型（Type）和原始数据库使用的类型（DBType）返回。对于使用经典 MySQL 协议的 MySQL Shell 连接，DBType 是由协议返回的；对于使用 X 协议的连接，DBType 是根据可用信息推断的。列长度（Length）以字节返回。

--compress[={required|preferred|disabled}], -C [{required|preferred|disabled}]

控制使用此连接在客户端和服务器之间发送的信息的压缩。在 MySQL Shell 8.0.14 至 8.0.19 中，此选项仅适用于经典 MySQL 协议连接，并且不使用 required、preferred 和 disabled 选项。在这些版本中，当您指定 `--compress` 时，如果可能，会激活压缩。从 MySQL Shell 8.0.20 开始，它也适用于 X 协议连接，您可以选择指定 required、preferred 或 disabled。从 MySQL Shell 8.0.20 开始，仅指定 `--compress` 时，其含义为 `--compress=required`。有关在所有版本中使用 MySQL Shell 的压缩控制的信息，请参见第 4.3.7 节，“使用压缩连接”。

--connect-timeout=ms

配置 MySQL Shell 等待通过命令行参数指定的全局会话建立的时间（以毫秒为单位）。

--credential-store-helper=helper

用于存储和检索密码的秘密存储助手。参见第 4.4 节，“可插拔密码存储”。

--database=name, -D name

要使用的默认模式。这是 `--schema` 的别名。

--dba=enableXProtocol

在与 MySQL 5.7 服务器的连接中启用 X 插件，以便您可以使用 X 协议连接进行后续连接。需要使用经典 MySQL 协议进行连接。对于默认启用 X 插件的 MySQL 8.0 服务器，此项不相关。

--dba-log-sql[=0|1|2]

记录由 AdminAPI 操作执行的 SQL 语句（排除沙盒操作）。默认情况下，即使设置了 `--log-level` 和 `--verbose` 选项，这类语句也不会写入 MySQL Shell 应用日志文件或作为详细输出发送到控制台。选项的值是 0 到 2 范围内的整数。0 不记录或显示此类语句，这是如果您不指定选项时的默认行为。1 记录由 AdminAPI 操作执行的 SQL 语句，但不包括 SELECT 语句和 SHOW 语句（如果您在命令行上指定选项而不带值，则为默认设置）。2 记录常规 AdminAPI 操作执行的 SQL 语句，包括 SELECT 和 SHOW 语句。更多信息，请参见第 12 章，MySQL Shell 日志和调试。

--log-sql[=off|error|on|all|unfiltered]

将 MySQL Shell 执行的所有 SQL 语句记录到 MySQL Shell 日志文件 `mysqlsh.log`。

以下选项可用：

- off: 不记录任何 MySQL Shell SQL 语句。
- error: （默认值）仅记录失败的 MySQL Shell SQL 语句。
- on: 记录所有 MySQL Shell SQL 语句，除了那些符合 logSql.ignorePattern 和 logSql.ignorePatternUnsafe 定义的忽略模式的语句。更多信息，请参见过滤 SQL 日志记录。
- all: 记录所有 MySQL Shell SQL 语句，除了那些符合 logSql.ignorePatternUnsafe 定义的忽略模式的语句。更多信息，请参见过滤 SQL 日志记录。
- unfiltered: 记录所有 MySQL Shell SQL 语句，不进行过滤。

--dbpassword[=password]

在 MySQL Shell 8.0.13 版本中弃用。请改用 `--password[=password]`。

--dbuser=user_name

在 MySQL Shell 8.0.13 版本中弃用。请改用 `--user=user_name`。

--execute=command, -e command

使用当前活动语言执行命令并退出。此选项与 `--file=file_name` 选项互斥。

--fido-register-factor

必须执行 FIDO 设备注册的因素或因素。此选项值必须是单个值，或用逗号分隔的两个值。每个值必须是 2 或 3，因此允许的选项值是 '2'、'3'、'2,3' 和 '3,2'。例如：

```mysqlsh
--user=user_name --password1 --fido-register-factor=2
Enter password: (输入因素 1 密码)
```

为了注册一个仅使用 FIDO 设备进行无密码认证的账户，您使用 `--fido-register-factor=2` 提供临时密码。服务器在注册成功后将 FIDO 认证移到第一个因素。

注意：如果在连接到服务器时您没有指定密码，MySQL Shell 会提示输入密码。在使用 FIDO 设备设置无密码认证后，使用以下方法之一绕过密码提示，进行连接：

- 指定连接选项 `--no-password`，或者 `--password=` 并留空值。
- 在连接字符串中，用户名后面跟一个冒号（:），例如：`mysqlsh user_name:@localhost`
- 密码提示出现时按 Enter 键。

MySQL Shell 的 `--fido-register-factor` 选项与 mysql 客户端选项的工作方式相同。更多详情和说明，请参见 FIDO 可插拔认证。

--file=file_name, -f file_name

指定要在批处理模式下处理的文件。在此之后指定的任何选项都作为处理文件的参数使用。

--force

即使发生错误，也继续在 SQL 和批处理模式下处理。

--histignore=strings

指定不添加到 MySQL Shell 历史记录中的字符串。字符串由冒号分隔。匹配不区分大小写，可以使用通配符 * 和 ?。默认忽略的字符串指定为 “*IDENTIFIED*:*PASSWORD*”。参见第 5.5 节，“代码历史”。

--host=host_name, -h host_name

连接到给定主机上的 MySQL 服务器。在 Windows 上，如果您指定 `--host=.` 或 `-h .`（将主机名指定为句点），MySQL Shell 将使用默认命名管道（名称为 MySQL）连接，或者使用 `--socket` 选项指定的其他命名管道连接。

--get-server-public-key

MySQL Shell 的 `--get-server-public-key` 等效项。

如果给出 `--server-public-key-path=file_name` 并指定了有效的公钥文件，则优先于 `--get-server-public-key`。

重要提示：仅支持使用经典 MySQL 协议连接。

参见 Caching SHA-2 可插拔认证。

--import

使用 JSON 导入工具从文件或标准输入导入 JSON 文档到 MySQL Server 集合或关系表中。有关指令，请参见第 11.2 节，“JSON 导入工具”。

--interactive[=full], -i

在批处理模式中模拟交互模式。

--js, --javascript

以 JavaScript 模式启动。

--json[={off|pretty|raw}]

控制此会话的 MySQL Shell 输出的 JSON 包装。此选项旨在用于 MySQL Shell 与其他程序的接口，例如作为测试的一部分。当 `--json` 选项没有值或值为 pretty 时，输出以美化打印的 JSON 生成。值为 raw 时，输出以原始 JSON 格式生成。在这些情况下，`--result-format` 选项及其别名和 resultFormat MySQL Shell 配置选项的值被忽略。值为 off 时，不进行 JSON 包装，结果集以 `--result-format` 选项或 resultFormat 配置选项指定的格式正常输出。

--log-file=path

更改此 MySQL Shell 实例的 MySQL Shell 应用日志文件 `mysqlsh.log` 的位置。应用日志文件的默认位置是用户配置路径，默认为 Windows 上的 `%APPDATA%\MySQL\mysqlsh\` 或 Unix 上的 `~/.mysqlsh/`。您可以通过定义环境变量 MYSQLSH_USER_CONFIG_HOME 来覆盖所有 MySQL Shell 实例的用户配置路径。`--log-file` 选项适用于个别 MySQL Shell 实例，意味着不同的实例可以写入不同的位置。

--log-level=N

更改 MySQL Shell 应用日志文件 `mysqlsh.log` 的日志级别，或禁用日志记录到文件。该选项需要一个值，可以是从 1 到 8 范围内的整数，或者是 none、internal、error、warning、info、debug、debug2 或 debug3 之一。指定 1 或 none 禁用应用日志文件的日志记录。如果您未指定此选项，默认级别为 5（info）。参见第 12 章，MySQL Shell 日志和调试。

-ma

在 MySQL Shell 8.0.13 版本中弃用。自动尝试使用 X 协议创建会话的连接，并在 X 协议不可用时回退到经典 MySQL 协议。

--mysql, --mc

设置在启动时创建的全局会话以使用经典 MySQL 协议连接。从 MySQL Shell 8.0.13 开始，`--mc` 选项使用两个连字符替换之前的单连字符 `-mc` 选项。

--mysql-plugin-dir=path

通过覆盖 shell.options.mysqlPluginDir 设置的值，设置客户端认证插件的非持久路径。客户端插件随 MySQL 服务器包提供，并且可以相对于 MySQL 基目录（basedir 系统变量的值）定位。例如：

- Windows 主机类型上的 `C:\program files\mysql\mysql Server 8.0\lib\plugin`
- Linux 主机类型上的 `/usr/local/mysql/lib/plugin`

有关随服务器一起提供的客户端认证插件的列表，请参见可用的认证插件。

--mysqlx, --mx

设置在启动时创建的全局会话以使用 X 协议连接。从 MySQL Shell 8.0.13 开始，`--mx` 选项使用两个连字符替换之前的单连字符 `-mx` 选项。

--name-cache

基于活动的默认模式自动加载表名。

--no-name-cache, -A

基于活动的默认模式和 DevAPI db 对象，禁用表名的自动完成加载。使用 `\rehash` 手动重新加载名称信息。

--no-password

当连接到服务器时，如果用户有无密码账户（这是不安全的，不推荐），或者使用 Unix 套接字连接的套接字对等证书认证，则必须使用 `--no-password` 明确指定不提供密码，且不需要密码提示。

--no-wizard, -nw

禁用诸如创建连接、dba.configureInstance()、Cluster.rebootClusterFromCompleteOutage() 等操作提供的交互式向导。当您希望脚本化 MySQL Shell 并不希望显示交互式提示时，使用此选项。有关更多信息，请参见第 5.6 节，“批处理代码执行”和第 5.8 节，“API 命令行集成”。

--pager=name

MySQL Shell 用于在 SQL 模式下执行语句和其他选定命令（如在线帮助）显示文本输出的外部分页工具。如果您未设置分页工具，则使用 PAGER 环境变量指定的分页工具。参见第 4.6 节，“使用分页工具”。

--passwords-from-stdin

从标准输入而不是终端读取密码。此选项不影响任何其他密码行为，如密码提示。

--password[=password], -ppassword

连接到服务器时使用的密码。MySQL Shell 接受的最大密码长度为 128 个字符。

--password=password (-ppassword) 带有值提供用于连接的密码。使用长格式 `--password=` 时，您必须使用等号而不是空格来分隔选项及其值。使用短格式 `-p` 时，选项及其值之间不能有空格。如果在任一情况下使用了空格，该值不会被解释为密码，可能会被解释为另一个连接参数。

在命令行上指定密码应该被视为不安全的。请参见结束用户密码安全指南。您可以使用选项文件来避免在命令行上给出密码。

没有值且没有等号的 `--password`，或没有值的 `-p`，请求密码提示。

`--password=` 带有空值与 `--no-password` 有相同效果，指定用户连接时没有密码

提供。当连接到服务器时，如果用户有无密码账户（这是不安全的，不推荐），或者使用 Unix 套接字连接的套接字对等证书认证，则必须使用这些方法之一明确指定不提供密码，且不需要密码提示。

--password1[=password]

--password1、--password2 和 --password3 是用于需要多因素认证的账户的密码。您可以提供多达三个密码。这些选项的工作方式与 `--password` 选项相同，且 `--password1` 被视为等同于该选项。您可以在命令行后跟随选项指定密码值（这是不安全的），或者如果选项没有给出密码值，MySQL Shell 会依次提示用户输入每个密码。这些选项从 MySQL Shell 8.0.28 开始可用，仅支持使用命令行参数进行的经典 MySQL 协议连接。

--password2[=password]

用于账户的第二个认证方法所需的密码。参见 `--password1` 选项的描述。

--password3[=password]

用于账户的第三个认证方法所需的密码。参见 `--password1` 选项的描述。

--port=port_num, -P port_num

用于连接的 TCP/IP 端口号。默认为端口 33060。

--py, --python

以 Python 模式启动。

--pyc=pythonCommand, -c

执行一个 Python 命令并退出。在此之后指定的任何选项都被视为处理命令的参数。

--pym

在 MySQL Shell 的 Python 模式中执行指定的 Python 模块作为脚本。`--pym` 的工作方式与 Python 的 `-m` 命令行选项相同。此选项从 MySQL Shell 8.0.22 开始可用。

--quiet-start[=1|2]

启动时不打印介绍性信息。MySQL Shell 通常在启动和连接时打印有关产品的信息、会话信息（如默认模式和连接 ID）、警告消息以及返回的任何错误。当您指定 `--quiet-start` 时没有值或值为 1，不打印 MySQL Shell 产品的信息，但会打印会话信息、警告和错误。值为 2 时，只打印错误。

--recreate-schema

删除并重新创建在连接选项中指定的模式，无论是作为 URI 类型连接字符串的一部分还是使用 `--schema`、`--database` 或 `-D` 选项指定的。如果模式存在，则会被删除。

--redirect-primary

确保目标服务器是 InnoDB 集群或 InnoDB ReplicaSet 的一部分，如果它不是主节点，找到主节点并连接到它。如果在使用此选项时以下任何一种情况为真，MySQL Shell 将以错误退出：

- 没有指定实例
- 在 InnoDB 集群中，群组复制未激活
- InnoDB 集群元数据不存在
- 没有法定人数

--replicaset

确保目标服务器属于 InnoDB ReplicaSet，如果是，用 InnoDB ReplicaSet 填充 rs 全局变量。然后，您可以使用 rs 全局变量来管理 InnoDB ReplicaSet，例如通过发出 `rs.status()`。

--redirect-secondary

确保目标服务器是单主 InnoDB 集群或 InnoDB ReplicaSet 的一部分，如果它不是辅助节点，找到一个辅助节点并连接到它。如果在使用此选项时以下任何一种情况为真，MySQL Shell 将以错误退出：

- 在 InnoDB 集群中，群组复制未激活
- InnoDB 集群元数据不存在
- 没有法定人数
- 集群不是单主模式且正在多主模式运行
- 没有可用的辅助节点，例如因为只有一个服务器实例

--result-format={table|tabbed|vertical|json|json/pretty|ndjson|json/raw|json/array}

为此会话设置 resultFormat MySQL Shell 配置选项的值。格式如下：

- table: 交互模式的默认值，除非在配置文件中为 resultFormat 配置选项持久设置了另一个值，在这种情况下，应用那个默认值。也可以使用 `--table` 别名。
- tabbed: 批处理模式的默认值，除非在配置文件中为 resultFormat 配置选项持久设置了另一个值，在这种情况下，应用那个默认值。也可以使用 `--tabbed` 别名。
- vertical: 产生等同于 SQL 查询的 \G 终止符的输出。也可以使用 `--vertical` 或 `-E` 别名。
- json 或 json/pretty: 产生美化打印的 JSON。
- ndjson 或 json/raw: 产生以新行分隔的原始 JSON。
- json/array: 产生包装在 JSON 数组中的原始 JSON。

如果使用 `--json` 命令行选项激活会话的输出的 JSON 包装，则 `--result-format` 选项及其别名和 resultFormat 配置选项的值将被忽略。

--save-passwords={always|prompt|never}

控制是否自动将密码存储在秘密存储中。`always` 意味着密码总是被存储，除非它们已经在存储中或服务器 URL 被过滤器排除。`never` 意味着密码永远不会被存储。`prompt`，这是默认设置，意味着会询问用户是否存储密码。参见第 4.4 节，“可插拔密码存储”。

--schema=name, -D name

要使用的默认模式。

--server-public-key-path=file_name

MySQL Shell 的 `--server-public-key-path`等效项。

如果给出 `--server-public-key-path=file_name` 并指定了有效的公钥文件，则优先于 `--get-server-public-key`。

重要提示：仅支持使用经典 MySQL 协议连接。

参见 caching_sha2_password 插件 Caching SHA-2 可插拔认证。

--show-warnings={true|false}

当指定 true 时，默认情况下，在 SQL 模式中，如果有任何警告，MySQL Shell 会在每条 SQL 语句后显示警告。如果指定 false，则不显示警告。

--socket[=path], -S [path]

在 Unix 上，当指定路径时，该路径是用于连接的 Unix 套接字文件的名称。如果您指定 `--socket` 无值且无等号，或 `-S` 无值，则使用相应协议的默认 Unix 套接字文件。

在 Windows 上，路径是用于连接的命名管道的名称。管道名称不区分大小写。在 Windows 上，您必须指定路径，且 `--socket` 选项仅适用于经典 MySQL 协议会话。

如果您指定了套接字，那么就不能指定端口或主机名（除了 localhost 在 Unix 上或点（.）在 Windows 上）。

--sql

以 SQL 模式启动，自动检测连接信息中未指定的协议。当未指定使用哪种协议时，默认使用 X 协议连接，如果 X 协议不可用，则回退到经典 MySQL 协议连接。要强制连接使用特定协议，请参见 `--sqlx` 或 `--sqlc` 选项。或者，作为 URI 类型连接字符串的一部分指定协议，或使用 `--port` 选项。更多信息，请参见第 4.3 节，“MySQL Shell 连接”和 MySQL Shell 端口。

--sqlc

以 SQL 模式启动，强制连接使用经典 MySQL 协议，例如，用于与不支持 X 协议的服务器使用 MySQL Shell。如果您在连接中未指定端口，并且提供了此选项，MySQL Shell 将使用通常是 3306 的默认经典 MySQL 协议端口。您连接的端口必须支持经典 MySQL 协议，因此例如，如果您指定的连接使用 X 协议默认端口 33060，则连接会因错误而失败。更多信息，请参见第 4.3 节，“MySQL Shell 连接”和 MySQL Shell 端口。

--sqlx

以 SQL 模式启动，强制连接使用 X 协议。如果您在连接中未指定端口，并且提供了此选项，MySQL Shell 将使用通常是 33060 的默认 X 协议端口。您连接的端口必须支持 X 协议，因此例如，如果您指定的连接使用经典 MySQL 协议默认端口 3306，则连接会因错误而失败。更多信息，请参见第 4.3 节，“MySQL Shell 连接”和 MySQL Shell 端口。

--ssh=str

创建一个 SSH 隧道，提供加密连接到 MySQL 服务器实例。提供连接到 SSH 服务器的 URI 格式为 [user@]host[:port]，例如：

```
--ssh root@198.51.100.4:2222
```

使用此选项时，您还必须指定 `--user`、`--host` 和 `--port` 选项，或者 URI，用于连接到 MySQL 服务器实例。有关从 MySQL Shell 使用 SSH 隧道连接的信息，请参见第 4.3.6 节，“使用 SSH 隧道”。

--ssh-config-file=path

指定连接到 SSH 服务器的 SSH 配置文件的路径。您可以使用 MySQL Shell 配置选项 ssh.configFile 设置自定义文件作为默认值，如果未指定此选项。如果 ssh.configFile 未设置，默认为标准的 SSH 配置文件 `~/.ssh/config`。如果您指定 `--ssh-config-file` 为空值，则忽略 ssh.configFile 指定的默认文件，改用 `~/.ssh/config` 文件。

--ssh-identity-file=path

指定连接到 SSH 服务器的身份文件的路径。如果未指定此选项，默认为 SSH 配置文件夹中的标准私钥文件 (`~/.ssh/id_rsa`)。

--ssl*

以 `--ssl` 开头的选项指定是否使用 SSL 连接到服务器，并指明在哪里找到 SSL 密钥和证书。mysqlsh 的 SSL 选项的功能方式与 MySQL 服务器的 SSL 选项相同，更多信息，请参见加密连接的命令选项。

mysqlsh 接受这些 SSL 选项：`--ssl-mode`、`--ssl-ca`、`--ssl-capath`、`--ssl-cert`、`--ssl-cipher`、`--ssl-crl`、`--ssl-crlpath`、`--ssl-key`、`--tls-version`。

--syslog

将您在 MySQL Shell 的 SQL 模式中发出的 SQL 语句发送到操作系统的系统日志设施（Unix 上的 syslog 或 Windows 的事件日志）。当 MySQL Shell 以交互模式启动时，即正常启动或使用 `--interactive` 选项启动时，才会进行 SQL 语句的系统日志记录，如果在启动时使用 `--execute` 或 `--file` 选项运行 mysqlsh 进入批处理模式，则不进行系统日志记录。更多信息，请参见第 12.3 节，“用户 SQL 语句的系统日志记录”。

--tabbed

在交互模式下以制表符分隔的格式显示结果。该模式的默认格式是表格格式。此选项是 `--result-format=tabbed` 选项的别名。

--table

在批处理模式下以表格格式显示结果。该模式的默认格式是制表符分隔格式。此选项是 `--result-format=table` 选项的别名。

--uri=str

在启动时创建连接，指定连接选项在 URI 类型字符串中，如在连接到服务器使用 URI 类型字符串或键值对描述的部分详细介绍。

--user=user_name, -u user_name

连接到服务器时使用的 MySQL 用户名。

--verbose[=0|1|2|3|4]

激活详细输出到控制台并指定详细级别。值是从 0 到 4 的范围内的整数。0 不显示任何消息，这是您未指定选项时的默认详细级别。1 显示错误、警告和信息性消息（如果您在命令行上指定选项而不带值，则为默认设置）。2、3 和 4 添加更高级别的调试消息。参见第 12 章，MySQL Shell 日志和调试获取更多信息。

--version, -V

显示 MySQL Shell 的版本信息并退出。

--vertical, -E

垂直显示结果，如同为 SQL 查询使用 \G 终止符时。此选项是 `--result-format=vertical` 选项的别名。