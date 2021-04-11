---
title: Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo
description: Questo argomento descrive come usare la funzione WSALookupServiceBegin per eseguire una richiesta di dispositivi visibili e fantasma. Per ulteriori informazioni, vedere Individuazione di dispositivi e servizi Bluetooth.
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth e WSALookupServiceBegin per la richiesta di dispositivo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfbcab2a3134289630b4b301390f85e83d1d3d0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104118583"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a><span data-ttu-id="7cbff-105">Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo</span><span class="sxs-lookup"><span data-stu-id="7cbff-105">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>

<span data-ttu-id="7cbff-106">Questo argomento descrive come usare la funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) per eseguire una richiesta di dispositivi visibili e fantasma.</span><span class="sxs-lookup"><span data-stu-id="7cbff-106">This topic describes how to use the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function to perform an inquiry of both visible and ghosted devices.</span></span> <span data-ttu-id="7cbff-107">Per ulteriori informazioni, vedere [individuazione di dispositivi e servizi Bluetooth](discovering-bluetooth-devices-and-services.md).</span><span class="sxs-lookup"><span data-stu-id="7cbff-107">For more information, see [Discovering Bluetooth Devices and Services](discovering-bluetooth-devices-and-services.md).</span></span>

<span data-ttu-id="7cbff-108">La funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) usa una struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) nel primo parametro, *lpqsRestrictions*, per definire i criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="7cbff-108">The [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function uses a [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure in its first parameter, *lpqsRestrictions*, to define search criteria.</span></span> <span data-ttu-id="7cbff-109">Bluetooth fornisce linee guida specifiche per l'uso della funzione **WSALookupServiceBegin** e di **WSAQUERYSET**.</span><span class="sxs-lookup"><span data-stu-id="7cbff-109">Bluetooth provides specific guidelines for use of the **WSALookupServiceBegin** function and **WSAQUERYSET**.</span></span>

<span data-ttu-id="7cbff-110">La tabella seguente elenca le restrizioni che si applicano alla struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) passata al parametro *lpqsRestrictions* durante l'esecuzione di query per i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="7cbff-110">The following table lists restrictions that apply to the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure passed to the *lpqsRestrictions* parameter when querying for devices.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cbff-111">Membro WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="7cbff-111">WSAQUERYSET member</span></span></th>
<th><span data-ttu-id="7cbff-112">Restrizione</span><span class="sxs-lookup"><span data-stu-id="7cbff-112">Restriction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cbff-113"><strong>dwSize</strong></span><span class="sxs-lookup"><span data-stu-id="7cbff-113"><strong>dwSize</strong></span></span></td>
<td><span data-ttu-id="7cbff-114">Impostare su <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="7cbff-114">Set to <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cbff-115"><strong>lpBlob</strong></span><span class="sxs-lookup"><span data-stu-id="7cbff-115"><strong>lpBlob</strong></span></span></td>
<td><span data-ttu-id="7cbff-116">Questo membro contiene un puntatore facoltativo a una struttura <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="7cbff-116">This member contains an optional pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure.</span></span> <span data-ttu-id="7cbff-117">Se questo membro viene specificato, i parametri validi per la richiesta di informazioni sul dispositivo per <strong>LUP_FLUSHCACHE</strong> sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7cbff-117">If this member is specified, the valid device inquire parameters for <strong>LUP_FLUSHCACHE</strong> are as follows:</span></span>
<ul>
<li><span data-ttu-id="7cbff-118">Il membro <strong>cbSize</strong> della struttura <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> deve essere <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</span><span class="sxs-lookup"><span data-stu-id="7cbff-118">The <strong>cbSize</strong> member of the <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure must be <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</span></span></li>
<li><span data-ttu-id="7cbff-119">Il membro <strong>pBlobData</strong> è un puntatore a una struttura di <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> , per cui il membro <strong>lap</strong> è il codice di accesso di richiesta Bluetooth e il membro <strong>length</strong> è la lunghezza, in secondi, dell'indagine.</span><span class="sxs-lookup"><span data-stu-id="7cbff-119">The <strong>pBlobData</strong> member is a pointer to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> structure, for which the <strong>LAP</strong> member is the Bluetooth inquiry access code, and the <strong>length</strong> member is the length, in seconds, of the inquiry.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cbff-120"><strong>dwNameSpace</strong></span><span class="sxs-lookup"><span data-stu-id="7cbff-120"><strong>dwNameSpace</strong></span></span></td>
<td><span data-ttu-id="7cbff-121">Impostare su <strong>NS_BTH</strong>.</span><span class="sxs-lookup"><span data-stu-id="7cbff-121">Set to <strong>NS_BTH</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cbff-122">Altri membri</span><span class="sxs-lookup"><span data-stu-id="7cbff-122">Other members</span></span></td>
<td><span data-ttu-id="7cbff-123">Gli altri membri della struttura <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="7cbff-123">Other members of the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> structure are ignored.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7cbff-124">I flag elencati nella tabella seguente vengono usati nel parametro *dwControlFlags* per controllare i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="7cbff-124">The flags listed in the following table are used in the *dwControlFlags* parameter to control the query results.</span></span> <span data-ttu-id="7cbff-125">I **flag \_ LUP** e **LUP \_ FlushCache** vengono usati dalla funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) ; i restanti flag vengono usati nelle chiamate alla funzione [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .</span><span class="sxs-lookup"><span data-stu-id="7cbff-125">The **LUP\_CONTAINERS** and **LUP\_FLUSHCACHE** flags are used by the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function; the rest of the flags are used in calls to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span>

| <span data-ttu-id="7cbff-126">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="7cbff-126">Flag</span></span>               | <span data-ttu-id="7cbff-127">Risultato</span><span class="sxs-lookup"><span data-stu-id="7cbff-127">Result</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cbff-128">\_contenitori LUP</span><span class="sxs-lookup"><span data-stu-id="7cbff-128">LUP\_CONTAINERS</span></span>    | <span data-ttu-id="7cbff-129">Specifica che lo scopo della query è ottenere un elenco di dispositivi Bluetooth e non un elenco di servizi.</span><span class="sxs-lookup"><span data-stu-id="7cbff-129">Specifies that the query purpose is to obtain a list of Bluetooth devices and not a list of services.</span></span> <span data-ttu-id="7cbff-130">Questo flag deve essere impostato.</span><span class="sxs-lookup"><span data-stu-id="7cbff-130">This flag must be set.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="7cbff-131">\_FlushCache LUP</span><span class="sxs-lookup"><span data-stu-id="7cbff-131">LUP\_FLUSHCACHE</span></span>    | <span data-ttu-id="7cbff-132">Attiva un'indagine sui dispositivi locali o causa la restituzione dei risultati memorizzati nella cache delle query precedenti.</span><span class="sxs-lookup"><span data-stu-id="7cbff-132">Triggers an inquiry of local devices or causes cached results from previous queries to be returned.</span></span>                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="7cbff-133">\_tipo restituito \_ LUP</span><span class="sxs-lookup"><span data-stu-id="7cbff-133">LUP\_RETURN\_TYPE</span></span>  | <span data-ttu-id="7cbff-134">Restituisce il MERLUZZo Bluetooth (classe dei bit del dispositivo) direttamente nel membro **lpServiceClassId** della struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .</span><span class="sxs-lookup"><span data-stu-id="7cbff-134">Return the Bluetooth COD (class of device bits) directly in the **lpServiceClassId** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span> <span data-ttu-id="7cbff-135">Il MERLUZZo viene mappato al membro **Data1** del GUID.</span><span class="sxs-lookup"><span data-stu-id="7cbff-135">The COD is mapped to the **Data1** member of the GUID.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="7cbff-136">\_servizio LUP res \_</span><span class="sxs-lookup"><span data-stu-id="7cbff-136">LUP\_RES\_SERVICE</span></span>  | <span data-ttu-id="7cbff-137">Restituisce informazioni per l'indirizzo Bluetooth locale.</span><span class="sxs-lookup"><span data-stu-id="7cbff-137">Return information for the local Bluetooth address.</span></span> <span data-ttu-id="7cbff-138">Questo flag ha effetto solo se viene specificato anche **LUP \_ return \_ addr** .</span><span class="sxs-lookup"><span data-stu-id="7cbff-138">This flag has an effect only if **LUP\_RETURN\_ADDR** is also specified.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="7cbff-139">\_nome restituito \_ LUP</span><span class="sxs-lookup"><span data-stu-id="7cbff-139">LUP\_RETURN\_NAME</span></span>  | <span data-ttu-id="7cbff-140">Restituisce il nome visualizzato del dispositivo nel membro **lpszServiceInstanceName** della struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) per ogni chiamata alla funzione [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .</span><span class="sxs-lookup"><span data-stu-id="7cbff-140">Return the display name of the device in the **lpszServiceInstanceName** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure for each call to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span> <span data-ttu-id="7cbff-141">Questo flag deve essere specificato anche per recuperare il membro del **nome** della struttura di [**\_ \_ informazioni sul dispositivo BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) quando si specifica il flag del **\_ \_ BLOB restituito LUP** .</span><span class="sxs-lookup"><span data-stu-id="7cbff-141">This flag must also be specified to retrieve the **name** member of the [**BTH\_DEVICE\_INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) structure when specifying the **LUP\_RETURN\_BLOB** flag.</span></span> |
| <span data-ttu-id="7cbff-142">LUP \_ restituire \_ addr</span><span class="sxs-lookup"><span data-stu-id="7cbff-142">LUP\_RETURN\_ADDR</span></span>  | <span data-ttu-id="7cbff-143">Restituisce una [**struttura SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) che contiene l'indirizzo a 48 bit del peer nel membro **lpcsaBuffer** della struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) per ogni chiamata alla funzione [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) .</span><span class="sxs-lookup"><span data-stu-id="7cbff-143">Return a [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure that contains the 48-bit address of the peer in the **lpcsaBuffer** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure for each call to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span> <span data-ttu-id="7cbff-144">Gli altri membri della struttura **sockaddr \_ BTH** saranno vuoti.</span><span class="sxs-lookup"><span data-stu-id="7cbff-144">Other members in the **SOCKADDR\_BTH** structure will be empty.</span></span>                                                            |
| <span data-ttu-id="7cbff-145">\_BLOB restituito \_ LUP</span><span class="sxs-lookup"><span data-stu-id="7cbff-145">LUP\_RETURN\_BLOB</span></span>  | <span data-ttu-id="7cbff-146">Restituisce la struttura delle [**\_ \_ informazioni sul dispositivo BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) per ogni chiamata successiva a [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span><span class="sxs-lookup"><span data-stu-id="7cbff-146">Return the [**BTH\_DEVICE\_INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) structure on each subsequent call to [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="7cbff-147">\_FLUSHPREVIOUS LUP</span><span class="sxs-lookup"><span data-stu-id="7cbff-147">LUP\_FLUSHPREVIOUS</span></span> | <span data-ttu-id="7cbff-148">Ignorare il successivo dispositivo disponibile e restituire il dispositivo che lo segue.</span><span class="sxs-lookup"><span data-stu-id="7cbff-148">Skip the next available device, and return the device that follows it.</span></span>                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="7cbff-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7cbff-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cbff-150">Bluetooth e WSALookupServiceBegin per l'individuazione del servizio</span><span class="sxs-lookup"><span data-stu-id="7cbff-150">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="7cbff-151">Bluetooth e WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="7cbff-151">Bluetooth and WSALookupServiceNext</span></span>](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="7cbff-152">Bluetooth e WSAQUERYSET per la richiesta del dispositivo</span><span class="sxs-lookup"><span data-stu-id="7cbff-152">Bluetooth and WSAQUERYSET for Device Inquiry</span></span>](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="7cbff-153">Individuazione di dispositivi e servizi Bluetooth</span><span class="sxs-lookup"><span data-stu-id="7cbff-153">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="7cbff-154">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="7cbff-154">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="7cbff-155">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="7cbff-155">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="7cbff-156">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="7cbff-156">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="7cbff-157">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="7cbff-157">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="7cbff-158">**\_dispositivo di query BTH \_**</span><span class="sxs-lookup"><span data-stu-id="7cbff-158">**BTH\_QUERY\_DEVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[<span data-ttu-id="7cbff-159">**\_BTH sockaddr**</span><span class="sxs-lookup"><span data-stu-id="7cbff-159">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="7cbff-160">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="7cbff-160">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="7cbff-161">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="7cbff-161">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 