# Apache AXIS <=1.4 Զ������ִ�и���

## ǰ��

��֪����ʦ��������صķ������£�https://xz.aliyun.com/t/5513

������axis1��AdminService��ͨ��soap���������Ӧ���Service,Ȼ���ִ�����еķ�������������������һ������������freemarker����е�ĳ����������������ҿɴ�������������ִ��

��ϸ��������֪ԭ��

���ǹؼ�poc���ִ����ˣ����ǳ��Ա��ظ���

## ©������

1�������

jdk1.8+tomcat8.5+axis1.4+freemarker-2.3.28

���ص�ַ��

http://apache.fayea.com/axis/axis/java/1.4/

https://freemarker.apache.org/freemarkerdownload.html

�����ص�axis-bin-1_4ѹ�����е�webappsĿ¼�µ�axisĿ¼������tomcat��webappsĿ¼��

Ȼ�����ص�����freemarker-2.3.28.jar����axis\WEB-INF\libĿ¼��

![](pic/freemarker.png)

����tomcat�����http://localhost:8080/axis���ұ�����8081�˿�

![](pic/axis.png)

![](pic/services.png)

���ز���©�������Ѵ�ã�����Զ���ǲ������õģ���ΪĬ�������ǹر�Զ�̹���ģ�����������Զ������

��ʱ���axis\WEB-INF��û��server-config.wsdd�ļ��ģ�Ӧ����ʹ�õ�Դ���Ĭ������

2��©������

������֪�ϵ����£������һ������ܼ򵥣���������һ���Զ����Service������Ӧ�����õ���template.utility.Execute������Service���������⣬ע������ͷ����SOAPAction

![](pic/add-service.png)

�����ɹ��������server-config.wsdd�ļ����������������

![](pic/config.png)

�鿴������Service

![](pic/TestService.png)

Ȼ����Ҫ����������Service�������ִ������ĺ���exec������������List��List��xml�ṹ�п��Կ���Array�ṹ

���������￨ס�ˣ������˺ܾö�û�ɹ�

��������burp��wsdler���������Ȼ���ٳ��Թ���

![](pic/burp-wsdler.png)

ֱ�ӷ��ͱ���

![](pic/error-1.png)

��һЩ����������ȥ������

![](pic/error-2.png)

������ʾ��Ҫ������˵�������ǶԵģ����������ǻص������Ĺ����ˣ�Ӧ������Ҫ�����ַ������ͣ�������ô��ʾ�ַ����أ��˽���soap��xml֮�����ճɹ�ִ������

![](pic/rce.png)

���Լ��һ��

![](pic/rce2.png)

## �ܽ�

��Ҫ����ΪAxis��δ��Ȩ���ʣ���Ĭ���������ǲ�����Զ�̷���AdminService�ģ���ͨ�����Service���������������µ������⺯��������Ҫ�������һ��������������������

## ֪ʶ��

soapЭ���飺

https://www.w3cschool.cn/soap/

xml schema:

https://www.w3cschool.cn/xmlschema

xml�������ͣ�

https://www.w3.org/TR/xmlschema11-2/#built-in-primitive-datatypes

## TODO

1����������ľ���̶Ȳ�����֪ԭ�ģ�Ӧ�û���ʲôtips

2��Axis2��¼��������̨���ϴ��Զ���Service���Ƿ���ִ��������룿

