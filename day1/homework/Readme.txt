#################################################
# Created on: 2015年12月31日
# @author: 张晓宇
# Email: 61411916@qq.com
# Blog: http://www.cnblogs.com/zhangxiaxuan/
#################################################

特殊强调：
    1、博客园博客主页地址为http://www.cnblogs.com/zhangxiaxuan/
    2、博客园博客主页地址为http://www.cnblogs.com/zhangxiaxuan/
    3、博客园博客主页地址为http://www.cnblogs.com/zhangxiaxuan/
    4、重要的是事情说三遍！！！


作业一：登陆验证
    1、输入用户名密码
    2、认证成功系那是欢迎信息
    3、输错三次后锁定

程序结构：
程序包含两个文件login.py和account.db。其中login.py文件为主程序，account.db为账户文件，保存用户的用户名密码等信息

程序配置：
    用户文件：
        1、用户文件每个用户的信息占用一行
        2、每个字段用空格分隔
        3、由于使用空格进行分隔，所以用户信息不能包括空格
        4、用户第一个字段必须是用户名，其他用户信息顺序没有要求，但要和主程序中对应配置的列号一致即可，且所有用户的信息排列顺序必须一致
        5、用户文件中用户状态有两种锁定和正常，用lock和unlock表示
        6、用户文件严格区分大小写
        7、用户名不能是quit

    主程序：主程序有如下需要配置的参数
        account_file_path：用户文件的文件名（绝对目录或相对位置均可，但必须存在）
        password_col_num：用户信息中密码所在的列数（从0开始）
        status_col_num：用户信息中用户状态所在的列数（从0开始）
        error_count_num：用户信息中错误次数所在的列数（从0开始）
        error_count_max：密码最多可以输错的次数，达到次数目即被锁定，可根据业务需要设定
        app_info：系统信息，可根据实际需要进行配置

运行环境：Python3.0或以上版本并配置好环境变量（linux主机为了和自带的python2.x版本不冲突，需将python3.X的可执行文件重名为python3或创建名为python3的软链接链接到python的可知文件）

执行方法：
    1、Linux：直接执行# python3 login.py或#./login.py（需要给主程序文件添加可执行权限）
    2、Window：执行python login.py

使用方法：
    1、按照控制台提示输入用户名和密码
    2、如果要退出程序在输入用户名的地方输入quit退出程序


###############################我是分割线，华丽丽的分割线###########################################

作业二：三级菜单（此三级非彼三级）
    1、三级菜单
    2、可依次进入子菜单

程序结构：
程序包含两个文件login.py和account.db。其中login.py文件为主程序，account.db为账户文件，保存用户的用户名密码等信息

程序配置：
    主程序：主程序有如下需要配置的参数
        provinces：定义省一级菜单，格式为字典，{"菜单序号":"省名称", ...}
        citys：定义省一级菜单，格式为二级嵌套字典{"省名称":{"菜单序号":"市名称"}, ...}，注意：省名称要与省一级菜单的省名称一一对应
        area：定义区县一级菜单，格式为二级嵌套字典{"市名称":{"菜单序号":"区县名称"}, ...}，注意：市名称要与市一级的市名称一一对应
        app_info：系统信息，主要用于显示
        注意：所有菜单的菜单编号不能是b和q

运行环境：Python3.0或以上版本并配置好环境变量（linux主机为了和自带的python2.x版本不冲突，需将python3.X的可执行文件重名为python3或创建名为python3的软链接链接到python的可知文件）

执行方法：
    1、Linux：直接执行# python3 munu_list.py或#./menu_list.py（需要给主程序文件添加可执行权限）
    2、Window：执行python menu_list.py

使用方法：
    1、输入菜单编号即可进入相应菜单的下一级子菜单，如果是最后一级菜单则直接打印最后的结果退出程序
    2、除了第一级菜单，键入b返回上一级菜单
    3、在任何一级菜单，键入q则退出程序
