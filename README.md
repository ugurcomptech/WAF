# aaWAF

Bu döküman üzerinde aaPanel'in geliştirmiş olduğu aaWAF hakkında bilgiler içermektedir. 


## WAF Nedir?


![image](https://github.com/user-attachments/assets/fc21ce82-8b50-4648-ab68-c8676a4ab8ce)


Web Application Firewall (WAF), web uygulamalarını hedef alan zararlı trafik ve siber saldırılara karşı koruma sağlayan bir güvenlik sistemidir. WAF, gelen ve giden HTTP/HTTPS isteklerini filtreleyerek SQL enjeksiyonu, XSS (Cross-Site Scripting), ve diğer yaygın web saldırılarını engeller. Bu sayede, web uygulamalarının güvenliğini artırarak veri ihlallerine ve sistem açıklarına karşı bir koruma katmanı sağlar.


## WAF Kurulumu

Aşağıda bulunan kodu sunucunuza yapıştırınız.

```
URL=https://node.aapanel.com/cloudwaf_en/scripts/install_cloudwaf_en.sh && if [ -f /usr/bin/curl ];then curl -sSO "$URL" ;else wget -O install_cloudwaf_en.sh "$URL";fi;bash install_cloudwaf_en.sh
```

![image](https://github.com/user-attachments/assets/a758a9b6-9485-4a2c-b1c4-5555310c9949)

Kurulum tamamlandıktan sonra aşağıdaki görüntülenir:

![image](https://github.com/user-attachments/assets/481da505-8127-4129-882f-f801a63f1892)


## WAF Konsol

Konsolun varsayılan bağlantı noktası 8379'dur. Sunucunun güvenlik grubu veya donanım güvenlik duvarı varsa  8379 numaralı bağlantı noktasını açmanız gerekmektedir.

Kurulum tamamlandıktan sonra, Tarayıcı erişiminde görüntülenen adresi kullanın, kullanıcı adını ve şifreyi girin, aaWAF Konsoluna Giriş Yapın

Not: Tarayıcı güvenlik soruları sorar, lütfen ona güvenin. Bunun nedeni tarayıcının kendinden imzalı sertifikaya güvenmemesidir.


![image](https://github.com/user-attachments/assets/9bdc4d08-a58d-4824-a4d9-a989ea524cd0)


Giriş sağladıktan gerekli ayarlamalar için lütfen okumaya devam ediniz.

## Web Site Ekleme


Web site >> Add Web Site sayfasına erişip domaini ve var ise SSL'inizi belirtebilirsiniz. Ekleyeceğiniz web sitenizin A kaydınız WAF'a ait olan IP adresinizi girmeniz gerekmektedir.

**Örnek:** example.com domaininizin asıl IP adresi 192.168.10.20 olarak olduğunu varsayalım. WAF sunucunuzun IP adresini de 192.168.10.25 olarak varsayalım. DNS bölgenize giriş yapıp WAF sunucunuza ait olan 192.168.10.25 adresinzi yazmanız gerekmetkedir

```
@ IN A 192.168.10.25
```

![image](https://github.com/user-attachments/assets/3e56ef3f-7bc5-46c6-9b5c-1ef9c53ac1c4)



