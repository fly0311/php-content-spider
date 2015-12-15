# PHP-content-spider
这是一套基于PHP端网站内容抓取后台管理程序，兼容BOOSTRAP<br/> 
<br/>
后台是使用ACI(autocodeigniter,基于Codeigniter和bootstrap的后台管理程序)

<hr/>
# 安装步骤
1. 找到 application/config.php 中<br/>
 	将 <br/>
   	$config['base_url'] = '';<br/>
   	换成你的域名或者IP如 $config['base_url'] = 'http://www.xxx.com'; $config['base_url'] = 'http://localhost';<br/>
   	$config['base_url'] = 'http://localhost/aci';<br/>

 2. 找到 application/database.php中<br/>
 	将
 	'hostname' => 'localhost',<br/>
	'username' => '',<br/>
	'password' => '',<br/>
	'database' => '',<br/>
	换成你真实数据库信息，分别为主机名称，数据库用户名，数据库密码，数据库名称<br/>

 3. 找到 application/constant.php中<br/>
 	将<br/>
 	define('SITE_URL', '/');<br/>
 	*换成和你相对于站点的根目录，如果是当前是根目录不需要修改，如果是子类目，就换成你的子目录如 define('SITE_URL', '/aci/');<br/>

  4. 将“安装SQL.sql” 安装SQL 导入到你的数据库中<br/>

  5. 找到 application/aci.php中<br/>
 	将<br/>
 	$config['aci_status'] = array (<br/>
	  'systemVersion' => '1.0.0',<br/>
	  'installED' => false,<br/>
	);<br/>

	改成 'installED'=>true;<br/>

6. 安装完成，请删除“安装SQL.sql” 文件，<br/>

7. 进入后台，运行 http://你的安装网址/adminpanel/manage/cache ，会自动更新一下栏目缓存<br/>
