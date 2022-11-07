# Wordpress in locale
Il primo passo  svolto in questo progetto è stato portarmi in locale il sito web creato con wordpress.

É stato necessario il server web , in questo caso ho usato Apache,il database e PHP, perchè Wordpress è scritto in PHP.

Da Xamp, lancio Apache che è il web server locale,
e MySQL che ci gestisce il database.

Necessario : creare il database per wordpress.

Andare su Xamp -- -> launch Mysql -> Explorer --> httdocs ---> progetto  ----> nome_database   ----> cartella wordpress  ----> tutte le cartelle di wordpress contenute qui.


Il sito web è un blog , dove sono contenute all'interno articoli per il cloud.
É un sito per poter far capire alle aziende i notevoli vantaggi nell'usare il cloud.





-------------------------------------------------------------------------------------------------------------------------------------------------------------------------




# Template di cloud formation come modello di esempio

Ho creato un account di aws gratuito, dove da qui vado a creare un template di CloudFOrmation , utilizzando un modello di esempio  (wordpress blog).
Qui imposto il nome del database, la password del database e la password della root del database, scelgo il tipo di istanza ec2
(t2.micro), istanza idonea a livello gratuito, imposto il nome della coppia di chiavi, e l'intervallo di indirizzi IP.

Fatto ciò , saranno create le risorse (web server e il security group). Hl security group ha delle regole in entrata (concede l'accesso dalla porta 80 e dalla porta 22) da qualsiasi indirizzo ipv4.
In output dello stack, ritrovo l'url del sito web. 
Tale url mi direziona verso la pagina di login di wordpress. Da qui ho impostato e creato il sito web ospitato sull'istanza ec2.

Su questo link è presente il sito web creato.
http://ec2-35-158-160-6.eu-central-1.compute.amazonaws.com/wordpress/


------------------------------------------------------------------------------------------------------------------------------------------------------------


# Template di cloudformation impostato da VScode

Ho creato un template di cloudformation che mi crea le risorse necessarie per ospitare un sito web,
un security group con regole in entrata impostate. Queste regole concedono l'ingresso dalla porta 80 e dalla porta 22. 
Ho creato una subnet con un blocco CIDR impostato,
,un'istanza ec2 con impostato, il tipo dell'istanza, il nome della coppia di chiavi, l'id dell'AMI,
Ho creato un VPC con un blocco CIDR impostato,
un Internet Gateway, la route e la route table con impostato il VPC di riferimento.

il template si chiama Risorse necessarie.


------------------------------------------------------------------------------------------------------------------------------------------------------------

# Sito web ospitato su altervista.org

Sul template di CLoudFormation, non è impostato il certificato SSL. Per rendere il sito sicuro , ho creato un account di altervista , per far ospiare il sito web con certificato SSL.

Questo è il sito web :

https://percheilcloud.altervista.org/


