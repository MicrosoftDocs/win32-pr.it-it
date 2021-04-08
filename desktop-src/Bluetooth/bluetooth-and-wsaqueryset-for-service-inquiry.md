---
title: Bluetooth e WSAQUERYSET per la richiesta di assistenza
description: Uso della struttura WSAQUERYSET con le funzioni WSALookupServiceBegin e WSALookupServiceNext per ottenere informazioni sul processo di richiesta del servizio.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth e WSAQUERYSET per richieste di assistenza Bluetooth
- WSAQUERYSET Bluetooth, per la richiesta di assistenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656fa407829112005c9c54c5ab84c9c1bf2f4e33
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732202"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a><span data-ttu-id="38f6b-105">Bluetooth e WSAQUERYSET per la richiesta di assistenza</span><span class="sxs-lookup"><span data-stu-id="38f6b-105">Bluetooth and WSAQUERYSET for Service Inquiry</span></span>

<span data-ttu-id="38f6b-106">Bluetooth usa la struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , con varie funzioni, per facilitare l'individuazione di dispositivi e servizi nello spazio dei nomi Bluetooth, NS \_ BTH.</span><span class="sxs-lookup"><span data-stu-id="38f6b-106">Bluetooth uses the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure, with various functions, to facilitate the discovery of devices and services in the Bluetooth namespace, NS\_BTH.</span></span>

<span data-ttu-id="38f6b-107">Le funzioni [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) e [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usano la struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) per ottenere i dati sul processo di richiesta del servizio.</span><span class="sxs-lookup"><span data-stu-id="38f6b-107">The [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) and [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) functions use the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure to obtain data about the service inquiry process.</span></span> <span data-ttu-id="38f6b-108">La tabella seguente descrive come impostare i valori dei membri nella struttura **WSAQUERYSET** a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="38f6b-108">The following table describes how to set the member values in the **WSAQUERYSET** structure for this purpose.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="38f6b-109">Membro</span><span class="sxs-lookup"><span data-stu-id="38f6b-109">Member</span></span></th>
<th><span data-ttu-id="38f6b-110">Input per WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="38f6b-110">Input to WSALookupServiceBegin</span></span></th>
<th><span data-ttu-id="38f6b-111">Valore restituito da WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="38f6b-111">Returned value from WSALookupServiceNext</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="38f6b-112"><strong>dwSize</strong></span><span class="sxs-lookup"><span data-stu-id="38f6b-112"><strong>dwSize</strong></span></span></td>
<td><span data-ttu-id="38f6b-113">Deve essere impostato su <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="38f6b-113">Must be set to <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span></span></td>
<td><span data-ttu-id="38f6b-114"><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) restituito dal sistema.</span><span class="sxs-lookup"><span data-stu-id="38f6b-114"><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) returned by system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38f6b-115"><strong>dwOutputFlags</strong></span><span class="sxs-lookup"><span data-stu-id="38f6b-115"><strong>dwOutputFlags</strong></span></span></td>
<td><span data-ttu-id="38f6b-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-116">Not used.</span></span></td>
<td><span data-ttu-id="38f6b-117">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-117">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38f6b-118"><strong>lpszServiceInstanceName</strong></span><span class="sxs-lookup"><span data-stu-id="38f6b-118"><strong>lpszServiceInstanceName</strong></span></span></td>
<td><span data-ttu-id="38f6b-119">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-119">Not used.</span></span></td>
<td><span data-ttu-id="38f6b-120">Nome visualizzato del servizio, convertito come stringa con codifica UTF-8 dalla codifica della lingua predefinita dell'attributo Bluetooth ServiceName SDP.</span><span class="sxs-lookup"><span data-stu-id="38f6b-120">Display name of the service, converted as a UTF-8 encoded string from the default language encoding of the Bluetooth ServiceName SDP attribute.</span></span> <span data-ttu-id="38f6b-121">Restituito se viene specificato LUP_RETURN_NAME.</span><span class="sxs-lookup"><span data-stu-id="38f6b-121">Returned if LUP_RETURN_NAME is specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38f6b-122"><strong>lpServiceClassId</strong></span><span class="sxs-lookup"><span data-stu-id="38f6b-122"><strong>lpServiceClassId</strong></span></span></td>
<td><span data-ttu-id="38f6b-123">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="38f6b-123">Required.</span></span> <span data-ttu-id="38f6b-124">UUID del singolo Bluetooth più specifico per i servizi per i quali viene eseguita la ricerca.</span><span class="sxs-lookup"><span data-stu-id="38f6b-124">The most specific single Bluetooth UUID for the services for which the search is being conducted.</span></span> <span data-ttu-id="38f6b-125">Se, ad esempio, questo valore è impostato sull'UUID del protocollo L2CAP, restituisce tutti i servizi usando il protocollo L2CAP sul dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="38f6b-125">For example, if this value is set to the UUID of the L2CAP protocol, it returns all services using the L2CAP protocol on the target device.</span></span> <span data-ttu-id="38f6b-126">Se impostato sull'UUID di un servizio specifico, restituirà solo le istanze di tale servizio.</span><span class="sxs-lookup"><span data-stu-id="38f6b-126">If set to the UUID of a specific service, it would return only the instances of that service.</span></span></td>
<td><span data-ttu-id="38f6b-127">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-127">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38f6b-128"><strong>lpVersion</strong></span><span class="sxs-lookup"><span data-stu-id="38f6b-128"><strong>lpVersion</strong></span></span></td>
<td><span data-ttu-id="38f6b-129">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-129">Not used.</span></span></td>
<td><span data-ttu-id="38f6b-130">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-130">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38f6b-131"><strong>lpszComment</strong></span><span class="sxs-lookup"><span data-stu-id="38f6b-131"><strong>lpszComment</strong></span></span></td>
<td><span data-ttu-id="38f6b-132">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-132">Not used.</span></span></td>
<td><span data-ttu-id="38f6b-133">Descrizione del servizio, convertita come stringa con codifica UTF-8 dalla codifica della lingua predefinita dell'attributo Bluetooth ServiceDescription SDP.</span><span class="sxs-lookup"><span data-stu-id="38f6b-133">Description of the service, converted as a UTF-8 encoded string from the default language encoding of the Bluetooth ServiceDescription SDP attribute.</span></span> <span data-ttu-id="38f6b-134">Restituito se viene specificato <strong>LUP_RETURN_COMMENT</strong> .</span><span class="sxs-lookup"><span data-stu-id="38f6b-134">Returned if <strong>LUP_RETURN_COMMENT</strong> is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38f6b-135"><strong>dwNameSpace</strong></span><span class="sxs-lookup"><span data-stu-id="38f6b-135"><strong>dwNameSpace</strong></span></span></td>
<td><span data-ttu-id="38f6b-136">Deve essere NS_BTH.</span><span class="sxs-lookup"><span data-stu-id="38f6b-136">Must be NS_BTH.</span></span></td>
<td><span data-ttu-id="38f6b-137">Restituisce NS_BTH.</span><span class="sxs-lookup"><span data-stu-id="38f6b-137">Returns NS_BTH.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38f6b-138"><strong>lpNSProviderId</strong></span><span class="sxs-lookup"><span data-stu-id="38f6b-138"><strong>lpNSProviderId</strong></span></span></td>
<td><span data-ttu-id="38f6b-139">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-139">Not used.</span></span></td>
<td><span data-ttu-id="38f6b-140">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-140">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38f6b-141"><strong>lpszContext</strong></span><span class="sxs-lookup"><span data-stu-id="38f6b-141"><strong>lpszContext</strong></span></span></td>
<td><span data-ttu-id="38f6b-142">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="38f6b-142">Required.</span></span> <span data-ttu-id="38f6b-143">Indirizzo del dispositivo Bluetooth con cui stabilire una connessione SDP ed eseguire query per i servizi.</span><span class="sxs-lookup"><span data-stu-id="38f6b-143">The Bluetooth Device Address with which to establish an SDP connection and query for services.</span></span> <span data-ttu-id="38f6b-144">Questo valore deve essere una stringa convertita tramite la chiamata di funzione <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="38f6b-144">This value must be a string that was converted by using the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> function call.</span></span> <span data-ttu-id="38f6b-145">Se viene fornito l'indirizzo del dispositivo Bluetooth locale, viene eseguita la ricerca nel database SDP locale.</span><span class="sxs-lookup"><span data-stu-id="38f6b-145">If the local Bluetooth device address is provided, the local SDP database is searched.</span></span></td>
<td><span data-ttu-id="38f6b-146">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-146">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38f6b-147"><strong>dwNumberOfProtocols</strong></span><span class="sxs-lookup"><span data-stu-id="38f6b-147"><strong>dwNumberOfProtocols</strong></span></span></td>
<td><span data-ttu-id="38f6b-148">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-148">Not used.</span></span></td>
<td><span data-ttu-id="38f6b-149">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-149">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38f6b-150"><strong>lpafpProtocols</strong></span><span class="sxs-lookup"><span data-stu-id="38f6b-150"><strong>lpafpProtocols</strong></span></span></td>
<td><span data-ttu-id="38f6b-151">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-151">Not used.</span></span></td>
<td><span data-ttu-id="38f6b-152">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-152">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38f6b-153"><strong>lpszQueryString</strong></span><span class="sxs-lookup"><span data-stu-id="38f6b-153"><strong>lpszQueryString</strong></span></span></td>
<td><span data-ttu-id="38f6b-154">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-154">Not used.</span></span></td>
<td><span data-ttu-id="38f6b-155">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-155">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38f6b-156"><strong>dwNumberOfCsAddrs</strong></span><span class="sxs-lookup"><span data-stu-id="38f6b-156"><strong>dwNumberOfCsAddrs</strong></span></span></td>
<td><span data-ttu-id="38f6b-157">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-157">Not used.</span></span></td>
<td><span data-ttu-id="38f6b-158">Indica il numero di elementi nella matrice di strutture di <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="38f6b-158">Indicates the number of elements in the array of <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> structures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38f6b-159"><strong>lpcsaBuffer</strong></span><span class="sxs-lookup"><span data-stu-id="38f6b-159"><strong>lpcsaBuffer</strong></span></span></td>
<td><span data-ttu-id="38f6b-160">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38f6b-160">Not used.</span></span></td>
<td><span data-ttu-id="38f6b-161">Puntatore a una struttura <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> il cui membro <strong>LocalAddr. lpSockaddr</strong> fa riferimento a un <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> che contiene l'indirizzo di connessione completo del servizio remoto, convertito dalla prima voce dell'attributo Bluetooth ProtocolDescriptorList SDP.</span><span class="sxs-lookup"><span data-stu-id="38f6b-161">Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> structure whose <strong>LocalAddr.lpSockaddr</strong> member points to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> that contains the complete connectable address of the remote service, converted from the first entry of the Bluetooth ProtocolDescriptorList SDP attribute.</span></span> <span data-ttu-id="38f6b-162">Restituito se viene specificato <strong>LUP_RETURN_ADDR</strong> .</span><span class="sxs-lookup"><span data-stu-id="38f6b-162">Returned if <strong>LUP_RETURN_ADDR</strong> is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="38f6b-163"><strong>lpBlob</strong></span><span class="sxs-lookup"><span data-stu-id="38f6b-163"><strong>lpBlob</strong></span></span></td>
<td><span data-ttu-id="38f6b-164">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="38f6b-164">Optional.</span></span> <span data-ttu-id="38f6b-165">Puntatore a una struttura <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> che contiene parametri avanzati per limitare i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="38f6b-165">Pointer to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> structure that contains advanced parameters to limit the results of the search.</span></span> <span data-ttu-id="38f6b-166">Se specificato, <strong>lpServiceClassId</strong> viene ignorato e le query memorizzate nella cache non vengono eseguite correttamente.</span><span class="sxs-lookup"><span data-stu-id="38f6b-166">If provided, <strong>lpServiceClassId</strong> is ignored and cached queries do not succeed.</span></span></td>
<td><ul>
<li><span data-ttu-id="38f6b-167">Se viene eseguita la ricerca di un servizio: puntatore a una struttura <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> che restituisce gli handle del servizio.</span><span class="sxs-lookup"><span data-stu-id="38f6b-167">If a service search is performed: Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure that returns the service handles.</span></span> <span data-ttu-id="38f6b-168">(<strong>BLOB. cbSize</strong>)/<strong>sizeof</strong>(ulong) calcola il numero di handle.</span><span class="sxs-lookup"><span data-stu-id="38f6b-168">(<strong>BLOB.cbSize</strong>)/<strong>sizeof</strong>(ULONG) calculates the number of handles.</span></span> <span data-ttu-id="38f6b-169"><strong>BLOB. pBlobData</strong> è una matrice di valori ULONG che rappresenta gli handle del servizio.</span><span class="sxs-lookup"><span data-stu-id="38f6b-169"><strong>BLOB.pBlobData</strong> is an array of ULONG values representing the service handles.</span></span></li>
<li><span data-ttu-id="38f6b-170">Se viene eseguito un attributo o una ricerca serviceAttribute: puntatore a una struttura <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> che restituisce il record SDP binario.</span><span class="sxs-lookup"><span data-stu-id="38f6b-170">If an attribute or serviceAttribute search is performed: Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure that returns the binary SDP record.</span></span> <span data-ttu-id="38f6b-171"><strong>BLOB. cbSize</strong> è la dimensione del record SDP binario.</span><span class="sxs-lookup"><span data-stu-id="38f6b-171"><strong>BLOB.cbSize</strong> is the size of the binary SDP record.</span></span> <span data-ttu-id="38f6b-172"><strong>BLOB. pBlobData</strong> punta al record stesso.</span><span class="sxs-lookup"><span data-stu-id="38f6b-172"><strong>BLOB.pBlobData</strong> points to the record itself.</span></span> <span data-ttu-id="38f6b-173">Il record SDP binario è necessario in molti casi perché solo un numero limitato di attributi SDP può essere convertito nella struttura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> e vengono convertite solo le stringhe UTF-8 codificate predefinite.</span><span class="sxs-lookup"><span data-stu-id="38f6b-173">The binary SDP record is necessary in many cases because only a limited number of SDP attributes are able to be converted to the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> structure, and only default encoded UTF-8 strings are converted.</span></span> <span data-ttu-id="38f6b-174">Le funzioni per semplificare l'analisi del record SDP binario sono disponibili nella sezione di <a href="bluetooth-reference.md">riferimento Bluetooth</a> .</span><span class="sxs-lookup"><span data-stu-id="38f6b-174">Functions to assist in parsing the binary SDP record are provided in the <a href="bluetooth-reference.md">Bluetooth Reference</a> section.</span></span></li>
<li><span data-ttu-id="38f6b-175">Restituito se viene specificato LUP_RETURN_BLOB.</span><span class="sxs-lookup"><span data-stu-id="38f6b-175">Returned if LUP_RETURN_BLOB is specified.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="38f6b-176">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="38f6b-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38f6b-177">Bluetooth e WSAQUERYSET per il servizio set</span><span class="sxs-lookup"><span data-stu-id="38f6b-177">Bluetooth and WSAQUERYSET for Set Service</span></span>](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[<span data-ttu-id="38f6b-178">Bluetooth e WSAQUERYSET per la richiesta del dispositivo</span><span class="sxs-lookup"><span data-stu-id="38f6b-178">Bluetooth and WSAQUERYSET for Device Inquiry</span></span>](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="38f6b-179">Bluetooth e BLOB</span><span class="sxs-lookup"><span data-stu-id="38f6b-179">Bluetooth and BLOB</span></span>](bluetooth-and-blob.md)
</dt> <dt>

[<span data-ttu-id="38f6b-180">Bluetooth e WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="38f6b-180">Bluetooth and WSALookupServiceBegin</span></span>](bluetooth-and-wsasetservice.md)
</dt> <dt>

<span data-ttu-id="38f6b-181">Bluetooth e WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="38f6b-181">Bluetooth and WSALookupServiceNext</span></span>
</dt> <dt>

[<span data-ttu-id="38f6b-182">Informazioni di riferimento su Bluetooth</span><span class="sxs-lookup"><span data-stu-id="38f6b-182">Bluetooth Reference</span></span>](bluetooth-reference.md)
</dt> <dt>

[<span data-ttu-id="38f6b-183">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="38f6b-183">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="38f6b-184">**\_servizio query \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="38f6b-184">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="38f6b-185">**\_informazioni CSADDR**</span><span class="sxs-lookup"><span data-stu-id="38f6b-185">**CSADDR\_INFO**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[<span data-ttu-id="38f6b-186">**\_BTH sockaddr**</span><span class="sxs-lookup"><span data-stu-id="38f6b-186">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="38f6b-187">**WSAAddressToString**</span><span class="sxs-lookup"><span data-stu-id="38f6b-187">**WSAAddressToString**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[<span data-ttu-id="38f6b-188">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="38f6b-188">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="38f6b-189">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="38f6b-189">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 