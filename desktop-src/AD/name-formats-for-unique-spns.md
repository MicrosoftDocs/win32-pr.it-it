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
# <a name="name-formats-for-unique-spns"></a><span data-ttu-id="43d19-105">Formati dei nomi per nomi SPN univoci</span><span class="sxs-lookup"><span data-stu-id="43d19-105">Name Formats for Unique SPNs</span></span>

<span data-ttu-id="43d19-106">Un nome SPN deve essere univoco nella foresta in cui è registrato.</span><span class="sxs-lookup"><span data-stu-id="43d19-106">An SPN must be unique in the forest in which it is registered.</span></span> <span data-ttu-id="43d19-107">Se non è univoco, l'autenticazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="43d19-107">If it is not unique, authentication will fail.</span></span> <span data-ttu-id="43d19-108">La sintassi del nome SPN ha quattro elementi: due elementi obbligatori e due elementi aggiuntivi che è possibile usare, se necessario, per produrre un nome univoco come elencato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="43d19-108">The SPN syntax has four elements: two required elements and two additional elements that you can use, if necessary, to produce a unique name as listed in the following table.</span></span>


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
<th><span data-ttu-id="43d19-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="43d19-109">Element</span></span></th>
<th><span data-ttu-id="43d19-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43d19-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43d19-111">&quot;&lt;classe Service&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="43d19-111">&quot;&lt;service class&gt;&quot;</span></span></td>
<td><span data-ttu-id="43d19-112">Stringa che identifica la classe generale del servizio. ad esempio, &quot; SqlServer &quot; .</span><span class="sxs-lookup"><span data-stu-id="43d19-112">A string that identifies the general class of service; for example, &quot;SqlServer&quot;.</span></span> <span data-ttu-id="43d19-113">Sono presenti nomi di classi di servizi noti, ad esempio &quot; www &quot; per un servizio Web o &quot; LDAP &quot; per un servizio directory.</span><span class="sxs-lookup"><span data-stu-id="43d19-113">There are well-known service class names, such as &quot;www&quot; for a web service or &quot;ldap&quot; for a directory service.</span></span> <span data-ttu-id="43d19-114">In generale, può trattarsi di qualsiasi stringa univoca per la classe del servizio.</span><span class="sxs-lookup"><span data-stu-id="43d19-114">In general, this can be any string that is unique to the service class.</span></span> <span data-ttu-id="43d19-115">Tenere presente che la sintassi SPN utilizza una barra (/) per separare gli elementi, pertanto questo carattere non può essere visualizzato in un nome di classe del servizio.</span><span class="sxs-lookup"><span data-stu-id="43d19-115">Be aware that the SPN syntax uses a forward slash (/) to separate elements, so this character cannot appear in a service class name.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43d19-116">&quot;&lt;host&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="43d19-116">&quot;&lt;host&gt;&quot;</span></span></td>
<td><span data-ttu-id="43d19-117">Nome del computer in cui è in esecuzione il servizio.</span><span class="sxs-lookup"><span data-stu-id="43d19-117">The name of the computer on which the service is running.</span></span> <span data-ttu-id="43d19-118">Può trattarsi di un nome DNS completo o di un nome NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="43d19-118">This can be a fully qualified DNS name or a NetBIOS name.</span></span> <span data-ttu-id="43d19-119">Tenere presente che per i nomi NetBIOS non è garantita l'univocità nella foresta e pertanto un nome SPN che contiene il nome NetBIOS potrebbe non essere univoco.</span><span class="sxs-lookup"><span data-stu-id="43d19-119">Be aware that NetBIOS names are not guaranteed to be unique in a forest, so an SPN that contains a NetBIOS name may not be unique.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43d19-120">&quot;&lt;porta&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="43d19-120">&quot;&lt;port&gt;&quot;</span></span></td>
<td><span data-ttu-id="43d19-121">Numero di porta facoltativo per distinguere tra più istanze della stessa classe di servizio in un singolo computer host.</span><span class="sxs-lookup"><span data-stu-id="43d19-121">An optional port number to differentiate between multiple instances of the same service class on a single host computer.</span></span> <span data-ttu-id="43d19-122">Omettere questo componente se il servizio utilizza la porta predefinita per la relativa classe del servizio.</span><span class="sxs-lookup"><span data-stu-id="43d19-122">Omit this component if the service uses the default port for its service class.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43d19-123">&quot;&lt;nome del servizio&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="43d19-123">&quot;&lt;service name&gt;&quot;</span></span></td>
<td><span data-ttu-id="43d19-124">Nome facoltativo utilizzato negli SPN di un servizio replicabile per identificare i dati o i servizi forniti dal servizio o dal dominio servito dal servizio.</span><span class="sxs-lookup"><span data-stu-id="43d19-124">An optional name used in the SPNs of a replicable service to identify the data or services provided by the service or the domain served by the service.</span></span> <span data-ttu-id="43d19-125">Questo componente può avere uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="43d19-125">This component can have one of the following formats:</span></span>
<ul>
<li><span data-ttu-id="43d19-126">Nome distinto o objectGUID di un oggetto in Active Directory Domain Services, ad esempio un punto di connessione del servizio (SCP).</span><span class="sxs-lookup"><span data-stu-id="43d19-126">The distinguished name or objectGUID of an object in Active Directory Domain Services, such as a service connection point (SCP).</span></span></li>
<li><span data-ttu-id="43d19-127">Nome DNS del dominio per un servizio che fornisce un servizio specificato per un dominio nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="43d19-127">The DNS name of the domain for a service that provides a specified service for a domain as a whole.</span></span></li>
<li><span data-ttu-id="43d19-128">Nome DNS di un record SRV o MX.</span><span class="sxs-lookup"><span data-stu-id="43d19-128">The DNS name of an SRV or MX record.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="43d19-129">I componenti presenti nei nomi SPN di un servizio dipendono dal modo in cui il servizio viene identificato e replicato.</span><span class="sxs-lookup"><span data-stu-id="43d19-129">The components present in a service's SPNs depend on how the service is identified and replicated.</span></span> <span data-ttu-id="43d19-130">Esistono due scenari di base: servizi basati su host e servizi replicabili.</span><span class="sxs-lookup"><span data-stu-id="43d19-130">There are two basic scenarios: host-based services and replicable services.</span></span>

## <a name="host-based-services"></a><span data-ttu-id="43d19-131">Servizi basati su host</span><span class="sxs-lookup"><span data-stu-id="43d19-131">Host-based services</span></span>

<span data-ttu-id="43d19-132">Per un servizio basato su host, il &lt; componente "nome servizio &gt; " viene omesso perché il servizio viene identificato in modo univoco dalla classe del servizio e dal nome del computer host in cui è installato il servizio.</span><span class="sxs-lookup"><span data-stu-id="43d19-132">For a host-based service, the "&lt;service name&gt;" component is omitted because the service is uniquely identified by the service class and the name of the host computer on which the service is installed.</span></span>


```C++
<service class>/<host>
```



<span data-ttu-id="43d19-133">Solo la classe del servizio è sufficiente per identificare i client le funzionalità fornite dal servizio.</span><span class="sxs-lookup"><span data-stu-id="43d19-133">The service class alone is sufficient to identify for clients the features that the service provides.</span></span> <span data-ttu-id="43d19-134">È possibile installare istanze della classe del servizio in molti computer e ogni istanza fornisce servizi identificati con il relativo computer host.</span><span class="sxs-lookup"><span data-stu-id="43d19-134">You can install instances of the service class on many computers and each instance provides services that are identified with its host computer.</span></span> <span data-ttu-id="43d19-135">FTP e Telnet sono esempi di servizi basati su host.</span><span class="sxs-lookup"><span data-stu-id="43d19-135">FTP and Telnet are examples of host-based services.</span></span> <span data-ttu-id="43d19-136">Gli SPN di un'istanza del servizio basata su host possono includere il numero di porta se il servizio utilizza una porta non predefinita o se sono presenti più istanze del servizio nell'host.</span><span class="sxs-lookup"><span data-stu-id="43d19-136">The SPNs of a host-based service instance can include the port number if the service uses a non-default port or there are multiple instances of the service on the host.</span></span>


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a><span data-ttu-id="43d19-137">Servizi replicabili</span><span class="sxs-lookup"><span data-stu-id="43d19-137">Replicable services</span></span>

<span data-ttu-id="43d19-138">Per un servizio replicabile possono essere presenti una o più istanze del servizio (repliche) e i client non differenziano la replica a cui si connettono perché ognuno fornisce lo stesso servizio.</span><span class="sxs-lookup"><span data-stu-id="43d19-138">For a replicable service there can be one or many instances of the service (replicas), and clients do not differentiate which replica they connect to because each provides the same service.</span></span> <span data-ttu-id="43d19-139">Gli SPN per ogni replica hanno gli stessi &lt; componenti "classe di servizio &gt; " e " &lt; nome servizio &gt; ", dove " &lt; nome servizio &gt; " identifica più specificamente le funzionalità fornite dal servizio.</span><span class="sxs-lookup"><span data-stu-id="43d19-139">The SPNs for each replica have the same "&lt;service class&gt;" and "&lt;service name&gt;" components, where "&lt;service name&gt;" identifies more specifically the features provided by the service.</span></span> <span data-ttu-id="43d19-140">Solo i &lt; componenti "host &gt; " e "porta" facoltativi &lt; &gt; variano da SPN a SPN.</span><span class="sxs-lookup"><span data-stu-id="43d19-140">Only the "&lt;host&gt;" and optional "&lt;port&gt;" components would vary from SPN to SPN.</span></span>


```C++
<service class>/<host>:<port>/<service name>
```



<span data-ttu-id="43d19-141">Un esempio di servizio replicabile è costituito da un'istanza di un servizio di database che fornisce l'accesso a un database specificato.</span><span class="sxs-lookup"><span data-stu-id="43d19-141">An example of a replicable service would be an instance of a database service that provides access to a specified database.</span></span> <span data-ttu-id="43d19-142">In questo caso, " &lt; classe di servizio &gt; " identifica l'applicazione di database e " &lt; nome servizio &gt; " identifica il database specifico.</span><span class="sxs-lookup"><span data-stu-id="43d19-142">In this case, "&lt;service class&gt;" identifies the database application and "&lt;service name&gt;" identifies the specific database.</span></span> <span data-ttu-id="43d19-143">" &lt; nome servizio &gt; " può essere il nome distinto di un punto di connessione del servizio (SCP) contenente i dati di connessione per il database.</span><span class="sxs-lookup"><span data-stu-id="43d19-143">"&lt;service name&gt;" could be the distinguished name of a service connection point (SCP) containing connection data for the database.</span></span>


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



<span data-ttu-id="43d19-144">Se i client utilizzeranno il nome NetBIOS per comporre il nome SPN di un servizio, ogni replica deve registrare anche un nome SPN contenente il nome NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="43d19-144">If clients will use the NetBIOS name to compose a service's SPN, each replica must also register an SPN containing the NetBIOS name.</span></span>


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



<span data-ttu-id="43d19-145">Un altro esempio di servizio replicabile è quello che fornisce servizi a un intero dominio.</span><span class="sxs-lookup"><span data-stu-id="43d19-145">Another example of a replicable service is one that provides services to an entire domain.</span></span> <span data-ttu-id="43d19-146">In questo caso, il &lt; componente "nome servizio &gt; " è il nome DNS del dominio servito.</span><span class="sxs-lookup"><span data-stu-id="43d19-146">In this case, the "&lt;service name&gt;" component is the DNS name of the domain being served.</span></span> <span data-ttu-id="43d19-147">Un KDC Kerberos è un esempio di questo tipo di servizio replicabile.</span><span class="sxs-lookup"><span data-stu-id="43d19-147">A Kerberos KDC is an example of this type of replicable service.</span></span>

<span data-ttu-id="43d19-148">Tenere presente che, se il nome DNS di un computer cambia, il sistema aggiorna l' &lt; elemento "host &gt; " per tutti i nomi SPN registrati per l'host nella foresta.</span><span class="sxs-lookup"><span data-stu-id="43d19-148">Be aware that if the DNS name of a computer changes, the system updates the "&lt;host&gt;" element for all registered SPNs for that host in the forest.</span></span>

 

 




