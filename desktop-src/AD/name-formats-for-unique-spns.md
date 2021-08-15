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
ms.openlocfilehash: ce939d642180192500790253158eaa03dc41c8d173aed2d96d5175f07e39c101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025719"
---
# <a name="name-formats-for-unique-spns"></a>Formati dei nomi per nomi SPN univoci

Un nome SPN deve essere univoco nella foresta in cui è registrato. Se non è univoco, l'autenticazione avrà esito negativo. La sintassi SPN include quattro elementi: due elementi obbligatori e due elementi aggiuntivi che è possibile usare, se necessario, per produrre un nome univoco, come elencato nella tabella seguente.


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
<td>&quot;&lt;classe di servizio&gt;&quot;</td>
<td>Stringa che identifica la classe di servizio generale. ad esempio, &quot; SqlServer &quot; . Esistono nomi noti delle classi di servizio, ad esempio &quot; www per un servizio Web o ldap per un servizio &quot; &quot; &quot; directory. In generale, può trattarsi di qualsiasi stringa univoca per la classe di servizio. Tenere presente che la sintassi SPN usa una barra (/) per separare gli elementi, pertanto questo carattere non può essere visualizzato in un nome di classe di servizio.</td>
</tr>
<tr class="even">
<td>&quot;&lt;Host&gt;&quot;</td>
<td>Nome del computer in cui è in esecuzione il servizio. Può trattarsi di un nome DNS completo o di un nome NetBIOS. Tenere presente che per i nomi NetBIOS non è garantita l'univocità nella foresta e pertanto un nome SPN che contiene il nome NetBIOS potrebbe non essere univoco.</td>
</tr>
<tr class="odd">
<td>&quot;&lt;porta&gt;&quot;</td>
<td>Numero di porta facoltativo per distinguere tra più istanze della stessa classe di servizio in un singolo computer host. Omettere questo componente se il servizio usa la porta predefinita per la relativa classe di servizio.</td>
</tr>
<tr class="even">
<td>&quot;&lt;nome del servizio&gt;&quot;</td>
<td>Nome facoltativo usato nei nomi SPN di un servizio replicabile per identificare i dati o i servizi forniti dal servizio o dal dominio servito dal servizio. Questo componente può avere uno dei formati seguenti:
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

Per un servizio basato su host, il componente " service name " viene omesso perché il servizio è identificato in modo univoco dalla classe del servizio e dal nome del computer host in cui è installato il &lt; &gt; servizio.


```C++
<service class>/<host>
```



La sola classe di servizio è sufficiente per identificare per i client le funzionalità fornite dal servizio. È possibile installare istanze della classe di servizio in molti computer e ogni istanza fornisce servizi identificati con il computer host. FTP e Telnet sono esempi di servizi basati su host. I nomi SPN di un'istanza del servizio basata su host possono includere il numero di porta se il servizio usa una porta non predefinita o se nell'host sono presenti più istanze del servizio.


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a>Servizi replicabili

Per un servizio replicabile possono essere presenti una o più istanze del servizio (repliche) e i client non differenziano la replica a cui si connettono perché ognuna fornisce lo stesso servizio. I nomi SPN per ogni replica hanno gli stessi componenti " classe di servizio " e " nome servizio ", dove " nome del servizio " identifica in modo più specifico le funzionalità &lt; &gt; fornite dal &lt; &gt; &lt; &gt; servizio. Solo i componenti " &lt; host &gt; " e "porta" facoltativi variano da &lt; &gt; SPN a SPN.


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

 

 




