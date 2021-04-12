---
title: Formato dei log degli errori dell'API del server HTTP
description: In generale, i file di log degli errori dell'API del server HTTP hanno lo stesso formato dei log degli errori W3C, ad eccezione del fatto che i file di log degli errori dell'API server HTTP non contengono intestazioni di colonna.
ms.assetid: 436f898c-9063-4aee-b276-e6ab935e3606
keywords:
- API server HTTP, formato log degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2eb914251a809178adef28c8a61b1a174c6e86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221127"
---
# <a name="format-of-the-http-server-api-error-logs"></a><span data-ttu-id="af78d-104">Formato dei log degli errori dell'API del server HTTP</span><span class="sxs-lookup"><span data-stu-id="af78d-104">Format of the HTTP Server API Error Logs</span></span>

<span data-ttu-id="af78d-105">In generale, i file di log degli errori dell'API del server HTTP hanno lo stesso formato dei log degli errori W3C, ad eccezione del fatto che i file di log degli errori dell'API server HTTP non contengono intestazioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="af78d-105">In general, HTTP Server API error log files have the same format as W3C error logs except that HTTP Server API error log files do not contain column headings.</span></span> <span data-ttu-id="af78d-106">Ogni riga di un log degli errori dell'API del server HTTP registra un errore con i campi in un ordine specifico.</span><span class="sxs-lookup"><span data-stu-id="af78d-106">Each line of an HTTP Server API error log records one error with fields in a specific order.</span></span> <span data-ttu-id="af78d-107">Ogni campo è separato dal campo precedente per un singolo carattere di spazio (0x0020).</span><span class="sxs-lookup"><span data-stu-id="af78d-107">Each field is separated from the preceding field by a single space character (0x0020).</span></span> <span data-ttu-id="af78d-108">All'interno di ogni campo, i caratteri di spazio, le tabulazioni e i caratteri di controllo non stampabili vengono sostituiti da segni più (0x002B).</span><span class="sxs-lookup"><span data-stu-id="af78d-108">Within each field, space characters, tabs, and unprintable control characters are replaced by plus signs (0x002B).</span></span>

<span data-ttu-id="af78d-109">Nella tabella seguente vengono identificati i campi e l'ordine dei campi in un record del log degli errori.</span><span class="sxs-lookup"><span data-stu-id="af78d-109">The following table identifies the fields and the order of the fields in an error log record.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af78d-110">Campo</span><span class="sxs-lookup"><span data-stu-id="af78d-110">Field</span></span></th>
<th><span data-ttu-id="af78d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af78d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="af78d-112"><span id="Date"></span><span id="date"></span><span id="DATE"></span>Data</span><span class="sxs-lookup"><span data-stu-id="af78d-112"><span id="Date"></span><span id="date"></span><span id="DATE"></span>Date</span></span><br/></td>
<td><span data-ttu-id="af78d-113">Il campo della data segue il formato W3C ed è basato sull'ora UTC (Coordinated Universal Time). Il campo della data è sempre di 10 caratteri nel formato &quot; aaaa-mm-gg &quot; .</span><span class="sxs-lookup"><span data-stu-id="af78d-113">The Date field follows the W3C format and is based on Coordinated Universal Time (UTC).The Date field is always 10 characters in the form of &quot;YYYY-MM-DD&quot;.</span></span> <span data-ttu-id="af78d-114">Ad esempio, il 1 ° maggio 2003 è espresso come &quot; 2003-05-01 &quot; .</span><span class="sxs-lookup"><span data-stu-id="af78d-114">For example, May 1, 2003 is expressed as &quot;2003-05-01&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af78d-115"><span id="Time"></span><span id="time"></span><span id="TIME"></span>Tempo</span><span class="sxs-lookup"><span data-stu-id="af78d-115"><span id="Time"></span><span id="time"></span><span id="TIME"></span>Time</span></span><br/></td>
<td><span data-ttu-id="af78d-116">Il campo time segue il formato W3C ed è basato su UTC.</span><span class="sxs-lookup"><span data-stu-id="af78d-116">The Time field follows the W3C format and is based on UTC.</span></span> <span data-ttu-id="af78d-117">Il campo dell'ora è sempre di 8 caratteri nel formato &quot; mm: HH: SS &quot; .</span><span class="sxs-lookup"><span data-stu-id="af78d-117">The time field is always 8 characters in the form of &quot;MM:HH:SS&quot;.</span></span> <span data-ttu-id="af78d-118">Ad esempio, 5:30 PM (UTC) viene espresso come &quot; 17:30:00 &quot; .</span><span class="sxs-lookup"><span data-stu-id="af78d-118">For example, 5:30 PM (UTC) is expressed as &quot;17:30:00&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af78d-119"><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Indirizzo IP client</span><span class="sxs-lookup"><span data-stu-id="af78d-119"><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Client IP Address</span></span><br/></td>
<td><span data-ttu-id="af78d-120">Indirizzo IP del client interessato che può essere un indirizzo IPv4 o un indirizzo IPv6.</span><span class="sxs-lookup"><span data-stu-id="af78d-120">The IP address of the affected client that can be either an IPv4 address or an IPv6 address.</span></span> <span data-ttu-id="af78d-121">Se l'indirizzo IP del client è un indirizzo IPv6, anche il campo elemento ScopeId viene incluso nell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="af78d-121">If the client IP address is an IPv6 address, the ScopeId field is also included in the address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af78d-122"><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Porta client</span><span class="sxs-lookup"><span data-stu-id="af78d-122"><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Client Port</span></span><br/></td>
<td><span data-ttu-id="af78d-123">Numero di porta per il client interessato.</span><span class="sxs-lookup"><span data-stu-id="af78d-123">The port number for the affected client.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af78d-124"><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Indirizzo IP del server</span><span class="sxs-lookup"><span data-stu-id="af78d-124"><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Server IP Address</span></span><br/></td>
<td><span data-ttu-id="af78d-125">Indirizzo IP del server interessato che può essere un indirizzo IPv4 o un indirizzo IPv6.</span><span class="sxs-lookup"><span data-stu-id="af78d-125">The IP address of the affected server that can be either an IPv4 address or an IPv6 address.</span></span> <span data-ttu-id="af78d-126">Se l'indirizzo IP del server è un indirizzo IPv6, anche il campo elemento ScopeId viene incluso nell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="af78d-126">If the server IP address is an IPv6 address, the ScopeId field is also included in the address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af78d-127"><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Porta server</span><span class="sxs-lookup"><span data-stu-id="af78d-127"><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Server Port</span></span><br/></td>
<td><span data-ttu-id="af78d-128">Numero di porta del server interessato.</span><span class="sxs-lookup"><span data-stu-id="af78d-128">The port number of the affected server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af78d-129"><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Versione protocollo</span><span class="sxs-lookup"><span data-stu-id="af78d-129"><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Protocol Version</span></span><br/></td>
<td><span data-ttu-id="af78d-130">Versione del protocollo in uso.</span><span class="sxs-lookup"><span data-stu-id="af78d-130">The version of the protocol that is being used.</span></span> <br/>
<ul>
<li><span data-ttu-id="af78d-131">Se la connessione non è stata analizzata abbastanza per determinare la versione del protocollo, viene usato un trattino (0x002D) come segnaposto per il campo vuoto.</span><span class="sxs-lookup"><span data-stu-id="af78d-131">If the connection has not been parsed enough to determine the protocol version, then a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
<li><span data-ttu-id="af78d-132">Se il numero di versione principale o secondario analizzato è maggiore o uguale a 10, la versione viene registrata come &quot; http/?.? &quot; .</span><span class="sxs-lookup"><span data-stu-id="af78d-132">If either the major or minor version number parsed is greater than or equal to 10, the version is logged as &quot;HTTP/?.?&quot;.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af78d-133"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verbo</span><span class="sxs-lookup"><span data-stu-id="af78d-133"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verb</span></span><br/></td>
<td><span data-ttu-id="af78d-134">Stato del verbo passato dall'ultima richiesta analizzata.</span><span class="sxs-lookup"><span data-stu-id="af78d-134">The verb state passed by the last request parsed.</span></span> <span data-ttu-id="af78d-135">Sono inclusi verbi sconosciuti, ma qualsiasi verbo che supera i 255 byte viene troncato a questa lunghezza.</span><span class="sxs-lookup"><span data-stu-id="af78d-135">Unknown verbs are included, but any verb that is more than 255 bytes is truncated to this length.</span></span> <span data-ttu-id="af78d-136">Se un verbo non è disponibile, viene usato un trattino (0x002D) come segnaposto per il campo vuoto.</span><span class="sxs-lookup"><span data-stu-id="af78d-136">If a verb is not available, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af78d-137"><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + query</span><span class="sxs-lookup"><span data-stu-id="af78d-137"><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + Query</span></span><br/></td>
<td><span data-ttu-id="af78d-138">L'URL e qualsiasi query associata vengono registrati come un solo campo, separati da un punto interrogativo (0x3F).</span><span class="sxs-lookup"><span data-stu-id="af78d-138">The URL and any query associated with it are logged as one field, separated by a question mark (0x3F).</span></span> <span data-ttu-id="af78d-139">Questo campo è troncato al limite di lunghezza di 4096 byte.</span><span class="sxs-lookup"><span data-stu-id="af78d-139">This field is truncated at its length limit of 4096 bytes.</span></span>
<ul>
<li><span data-ttu-id="af78d-140">Se l'URL è stato analizzato ( &quot; cotto &quot; ), viene registrato con la conversione della tabella codici locale e viene considerato come un campo Unicode.</span><span class="sxs-lookup"><span data-stu-id="af78d-140">If this URL has been parsed (&quot;cooked&quot;), it is logged with local code page conversion, and is treated as a Unicode field.</span></span></li>
<li><span data-ttu-id="af78d-141">Se questo URL non è stato analizzato ( &quot; cotto &quot; ) al momento della registrazione, viene copiato esattamente, senza alcuna conversione Unicode.</span><span class="sxs-lookup"><span data-stu-id="af78d-141">If this URL has not been parsed (&quot;cooked&quot;) at the time of logging, it is copied exactly, without any Unicode conversion.</span></span></li>
<li><span data-ttu-id="af78d-142">Se l'API del server HTTP non è in grado di analizzare questo URL, viene usato un trattino (0x002D) come segnaposto per il campo vuoto.</span><span class="sxs-lookup"><span data-stu-id="af78d-142">If the HTTP Server API cannot parse this URL, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af78d-143"><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Stato protocollo</span><span class="sxs-lookup"><span data-stu-id="af78d-143"><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Protocol Status</span></span><br/></td>
<td><span data-ttu-id="af78d-144">Lo stato del protocollo non può essere maggiore di 999.</span><span class="sxs-lookup"><span data-stu-id="af78d-144">The protocol status cannot exceed 999.</span></span> <br/>
<ul>
<li><span data-ttu-id="af78d-145">Se lo stato del protocollo della risposta a una richiesta è disponibile, viene registrato in questo campo.</span><span class="sxs-lookup"><span data-stu-id="af78d-145">If the protocol status of the response to a request is available, it is logged in this field.</span></span></li>
<li><span data-ttu-id="af78d-146">Se lo stato del protocollo non è disponibile, viene usato un trattino (0x002D) come segnaposto per il campo vuoto.</span><span class="sxs-lookup"><span data-stu-id="af78d-146">If the protocol status is not available, a hyphen (0x002D) is used as a placeholder for the empty field.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af78d-147"><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId</span><span class="sxs-lookup"><span data-stu-id="af78d-147"><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId</span></span><br/></td>
<td><span data-ttu-id="af78d-148">Non usato in questa versione dell'API del server HTTP.</span><span class="sxs-lookup"><span data-stu-id="af78d-148">Not used in this version of the HTTP Server API.</span></span> <span data-ttu-id="af78d-149">In questo campo viene sempre visualizzato un trattino del segnaposto (0x002D).</span><span class="sxs-lookup"><span data-stu-id="af78d-149">A placeholder hyphen (0x002D) always appears in this field.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af78d-150"><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Frase motivo</span><span class="sxs-lookup"><span data-stu-id="af78d-150"><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Reason Phrase</span></span><br/></td>
<td><span data-ttu-id="af78d-151">Questo campo contiene una stringa che identifica il tipo di errore registrato.</span><span class="sxs-lookup"><span data-stu-id="af78d-151">This field contains a string that identifies the kind of error that is being logged.</span></span> <span data-ttu-id="af78d-152">Non viene mai lasciata vuota.</span><span class="sxs-lookup"><span data-stu-id="af78d-152">It is never left empty.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="af78d-153">Le righe di esempio seguenti proseguono da un log degli errori dell'API del server HTTP:</span><span class="sxs-lookup"><span data-stu-id="af78d-153">The following sample lines are from an HTTP Server API error log:</span></span>

``` syntax
2002-07-05 18:45:09 172.31.77.6 2094 172.31.77.6 80 
                    HTTP/1.1 GET /qos/1kbfile.txt 503 - ConnLimit
2002-07-05 19:51:59 127.0.0.1 2780 127.0.0.1 80 
                    HTTP/1.1 GET /ThisIsMyUrl.htm 400 - Hostname
2002-07-05 19:53:00 127.0.0.1 2894 127.0.0.1 80 
                    HTTP/2.0 GET / 505 - Version_N/S
2002-07-05 20:06:01 172.31.77.6 64388 127.0.0.1 80 
                    - - - - - Timer_MinBytesPerSecond
```

 

 





