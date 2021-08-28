---
title: Formati dei nomi per nomi SPN univoci
description: Un nome SPN deve essere univoco nella foresta in cui è registrato.
ms.assetid: dd3f9f7c-b64c-4bd8-924f-a8880ee3b71e
ms.tgt_platform: multiple
keywords:
- Formati dei nomi per nomi SPN univoci AD
- Nome entità servizio AD, Formati dei nomi per
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b041f88bc025c604ec5f0ad9a6bf5ba7f4cdabc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472337"
---
# <a name="name-formats-for-unique-spns"></a>Formati dei nomi per nomi SPN univoci

Un nome SPN deve essere univoco nella foresta in cui è registrato. Se non è univoco, l'autenticazione avrà esito negativo. La sintassi SPN include quattro elementi: due elementi obbligatori e due elementi aggiuntivi che è possibile usare, se necessario, per produrre un nome univoco come elencato nella tabella seguente.


```C++
<service class>/<host>:<port>/<service name>
```






| Elemento | Descrizione | 
|---------|-------------|
| "<service class>" | Stringa che identifica la classe di servizio generale. ad esempio "SqlServer". Esistono nomi noti delle classi di servizio, ad esempio "www" per un servizio Web o "ldap" per un servizio directory. In generale, può essere qualsiasi stringa univoca per la classe di servizio. Tenere presente che la sintassi SPN usa una barra (/) per separare gli elementi, pertanto questo carattere non può essere visualizzato nel nome di una classe di servizio. | 
| "<host>" | Nome del computer in cui è in esecuzione il servizio. Può trattarsi di un nome DNS completo o di un nome NetBIOS. Tenere presente che per i nomi NetBIOS non è garantita l'univocità nella foresta e pertanto un nome SPN che contiene il nome NetBIOS potrebbe non essere univoco. | 
| "<port>" | Numero di porta facoltativo per distinguere tra più istanze della stessa classe di servizio in un singolo computer host. Omettere questo componente se il servizio usa la porta predefinita per la relativa classe di servizio. | 
| "<service name>" | Nome facoltativo usato nei nomi SPN di un servizio replicabile per identificare i dati o i servizi forniti dal servizio o dal dominio servito dal servizio. Questo componente può avere uno dei formati seguenti:<ul><li>Nome distinto o objectGUID di un oggetto in Active Directory Domain Services, ad esempio un punto di connessione del servizio (SCP).</li><li>Nome DNS del dominio per un servizio che fornisce un servizio specificato per un dominio nel suo complesso.</li><li>Nome DNS di un record SRV o MX.</li></ul> | 




 

I componenti presenti nei nomi SPN di un servizio dipendono dal modo in cui il servizio viene identificato e replicato. Esistono due scenari di base: servizi basati su host e servizi replicabili.

## <a name="host-based-services"></a>Servizi basati su host

Per un servizio basato su host, il componente " service name " viene omesso perché il servizio è identificato in modo univoco dalla classe del servizio e dal nome del computer host in cui è installato il &lt; &gt; servizio.


```C++
<service class>/<host>
```



La sola classe di servizio è sufficiente per identificare per i client le funzionalità fornite dal servizio. È possibile installare istanze della classe di servizio in molti computer e ogni istanza fornisce servizi identificati con il computer host. FTP e Telnet sono esempi di servizi basati su host. I nomi SPN di un'istanza del servizio basata su host possono includere il numero di porta se il servizio usa una porta non predefinita o se nell'host sono presenti più istanze del servizio.


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a>Servizi replicabili

Per un servizio replicabile possono essere presenti una o più istanze del servizio (repliche) e i client non differenziano la replica a cui si connettono perché ognuna fornisce lo stesso servizio. I nomi SPN per ogni replica hanno gli stessi componenti " classe di servizio " e " nome del servizio ", dove " nome del servizio " identifica in modo più specifico le funzionalità &lt; &gt; fornite dal &lt; &gt; &lt; &gt; servizio. Solo i componenti " &lt; host &gt; " e &lt; "porta" &gt; facoltativi variano da SPN a SPN.


```C++
<service class>/<host>:<port>/<service name>
```



Un esempio di servizio replicabile è un'istanza di un servizio di database che fornisce l'accesso a un database specificato. In questo caso, " &lt; classe di servizio " identifica &gt; l'applicazione di database e " &lt; nome del servizio " identifica il database &gt; specifico. " service name " può essere il nome distinto di un punto di connessione del servizio (SCP) contenente i dati &lt; di connessione per il &gt; database.


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



Se i client useranno il nome NetBIOS per comporre il nome SPN di un servizio, ogni replica deve registrare anche un nome SPN contenente il nome NetBIOS.


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



Un altro esempio di servizio replicabile è quello che fornisce servizi a un intero dominio. In questo caso, il componente " &lt; service name " è il nome DNS del dominio &gt; servito. Un KDC Kerberos è un esempio di questo tipo di servizio replicabile.

Tenere presente che se il nome DNS di un computer cambia, il sistema aggiorna l'elemento " host " per tutti i nomi SPN registrati per tale &lt; &gt; host nella foresta.

 

 




