---
title: Formati dei nomi per nomi SPN univoci
description: Un nome SPN deve essere univoco nella foresta in cui è registrato.
ms.assetid: dd3f9f7c-b64c-4bd8-924f-a8880ee3b71e
ms.tgt_platform: multiple
keywords:
- Formati dei nomi per AD SPN univoci
- Nome dell'entità servizio AD, formati dei nomi per
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bda13cf5a095f8f2fd7ef1a209c6f3aeebd6654
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220927"
---
# <a name="name-formats-for-unique-spns"></a>Formati dei nomi per nomi SPN univoci

Un nome SPN deve essere univoco nella foresta in cui è registrato. Se non è univoco, l'autenticazione avrà esito negativo. La sintassi del nome SPN ha quattro elementi: due elementi obbligatori e due elementi aggiuntivi che è possibile usare, se necessario, per produrre un nome univoco come elencato nella tabella seguente.


```C++
<service class>/<host>:<port>/<service name>
```





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;&lt;classe Service&gt;&quot;</td>
<td>Stringa che identifica la classe generale del servizio. ad esempio, &quot; SqlServer &quot; . Sono presenti nomi di classi di servizi noti, ad esempio &quot; www &quot; per un servizio Web o &quot; LDAP &quot; per un servizio directory. In generale, può trattarsi di qualsiasi stringa univoca per la classe del servizio. Tenere presente che la sintassi SPN utilizza una barra (/) per separare gli elementi, pertanto questo carattere non può essere visualizzato in un nome di classe del servizio.</td>
</tr>
<tr class="even">
<td>&quot;&lt;host&gt;&quot;</td>
<td>Nome del computer in cui è in esecuzione il servizio. Può trattarsi di un nome DNS completo o di un nome NetBIOS. Tenere presente che per i nomi NetBIOS non è garantita l'univocità nella foresta e pertanto un nome SPN che contiene il nome NetBIOS potrebbe non essere univoco.</td>
</tr>
<tr class="odd">
<td>&quot;&lt;porta&gt;&quot;</td>
<td>Numero di porta facoltativo per distinguere tra più istanze della stessa classe di servizio in un singolo computer host. Omettere questo componente se il servizio utilizza la porta predefinita per la relativa classe del servizio.</td>
</tr>
<tr class="even">
<td>&quot;&lt;nome del servizio&gt;&quot;</td>
<td>Nome facoltativo utilizzato negli SPN di un servizio replicabile per identificare i dati o i servizi forniti dal servizio o dal dominio servito dal servizio. Questo componente può avere uno dei seguenti formati:
<ul>
<li>Nome distinto o objectGUID di un oggetto in Active Directory Domain Services, ad esempio un punto di connessione del servizio (SCP).</li>
<li>Nome DNS del dominio per un servizio che fornisce un servizio specificato per un dominio nel suo complesso.</li>
<li>Nome DNS di un record SRV o MX.</li>
</ul></td>
</tr>
</tbody>
</table>



 

I componenti presenti nei nomi SPN di un servizio dipendono dal modo in cui il servizio viene identificato e replicato. Esistono due scenari di base: servizi basati su host e servizi replicabili.

## <a name="host-based-services"></a>Servizi basati su host

Per un servizio basato su host, il &lt; componente "nome servizio &gt; " viene omesso perché il servizio viene identificato in modo univoco dalla classe del servizio e dal nome del computer host in cui è installato il servizio.


```C++
<service class>/<host>
```



Solo la classe del servizio è sufficiente per identificare i client le funzionalità fornite dal servizio. È possibile installare istanze della classe del servizio in molti computer e ogni istanza fornisce servizi identificati con il relativo computer host. FTP e Telnet sono esempi di servizi basati su host. Gli SPN di un'istanza del servizio basata su host possono includere il numero di porta se il servizio utilizza una porta non predefinita o se sono presenti più istanze del servizio nell'host.


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a>Servizi replicabili

Per un servizio replicabile possono essere presenti una o più istanze del servizio (repliche) e i client non differenziano la replica a cui si connettono perché ognuno fornisce lo stesso servizio. Gli SPN per ogni replica hanno gli stessi &lt; componenti "classe di servizio &gt; " e " &lt; nome servizio &gt; ", dove " &lt; nome servizio &gt; " identifica più specificamente le funzionalità fornite dal servizio. Solo i &lt; componenti "host &gt; " e "porta" facoltativi &lt; &gt; variano da SPN a SPN.


```C++
<service class>/<host>:<port>/<service name>
```



Un esempio di servizio replicabile è costituito da un'istanza di un servizio di database che fornisce l'accesso a un database specificato. In questo caso, " &lt; classe di servizio &gt; " identifica l'applicazione di database e " &lt; nome servizio &gt; " identifica il database specifico. " &lt; nome servizio &gt; " può essere il nome distinto di un punto di connessione del servizio (SCP) contenente i dati di connessione per il database.


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



Se i client utilizzeranno il nome NetBIOS per comporre il nome SPN di un servizio, ogni replica deve registrare anche un nome SPN contenente il nome NetBIOS.


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



Un altro esempio di servizio replicabile è quello che fornisce servizi a un intero dominio. In questo caso, il &lt; componente "nome servizio &gt; " è il nome DNS del dominio servito. Un KDC Kerberos è un esempio di questo tipo di servizio replicabile.

Tenere presente che, se il nome DNS di un computer cambia, il sistema aggiorna l' &lt; elemento "host &gt; " per tutti i nomi SPN registrati per l'host nella foresta.

 

 




