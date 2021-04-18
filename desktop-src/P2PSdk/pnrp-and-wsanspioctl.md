---
description: PNRP utilizza la funzione WSANSPIoctl per ricevere notifiche sulle modifiche apportate a quanto segue.
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP e WSANSPIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36dc53fb3d00eeaa2b74be643a7ea62af436e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312231"
---
# <a name="pnrp-and-wsanspioctl"></a><span data-ttu-id="112f8-103">PNRP e WSANSPIoctl</span><span class="sxs-lookup"><span data-stu-id="112f8-103">PNRP and WSANSPIoctl</span></span>

<span data-ttu-id="112f8-104">PNRP utilizza la funzione [**WSANSPIoctl**](winsock-nsp-reference-links.md) per ricevere notifiche sulle modifiche apportate ai seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="112f8-104">PNRP uses the [**WSANSPIoctl**](winsock-nsp-reference-links.md) function to receive notifications about changes to the following:</span></span>

-   <span data-ttu-id="112f8-105">Elenco di cloud di rete</span><span class="sxs-lookup"><span data-stu-id="112f8-105">A network cloud list</span></span>
-   <span data-ttu-id="112f8-106">Disponibilità dei risultati di una richiesta di risoluzione dei nomi</span><span class="sxs-lookup"><span data-stu-id="112f8-106">Availability of results of a name resolution request</span></span>

<span data-ttu-id="112f8-107">La prima chiamata a [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) definisce il tipo di informazioni a cui un client riceve una notifica.</span><span class="sxs-lookup"><span data-stu-id="112f8-107">The first call to [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) defines the type of information that a client is notified about.</span></span> <span data-ttu-id="112f8-108">Un client può ricevere una notifica con un messaggio di Windows, una routine di completamento, un handle per un oggetto WSAEVENT o una porta.</span><span class="sxs-lookup"><span data-stu-id="112f8-108">A client can be notified with a Windows message, a completion routine, a handle to a WSAEVENT object, or a port.</span></span> <span data-ttu-id="112f8-109">Per ulteriori informazioni sulle opzioni e sull'impostazione del parametro *lpCompletion* , vedere **WSANSPIoctl**.</span><span class="sxs-lookup"><span data-stu-id="112f8-109">For more information about options and setting the *lpCompletion* parameter, see **WSANSPIoctl**.</span></span>

<span data-ttu-id="112f8-110">Per continuare a ricevere notifiche dopo una chiamata a [**WSALookupServiceNext**](winsock-nsp-reference-links.md), un'applicazione deve chiamare di nuovo **WSANSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="112f8-110">To continue receiving notifications after a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md), an application must call **WSANSPIoctl** again.</span></span>

<span data-ttu-id="112f8-111">La funzione [**WSALookupServiceNext**](winsock-nsp-reference-links.md) si blocca anche se viene chiamato **WSANSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="112f8-111">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function blocks even if **WSANSPIoctl** is called.</span></span> <span data-ttu-id="112f8-112">Prima di chiamare **WSALookupServiceNext**, un'applicazione deve attendere fino a quando non riceve una notifica, se il blocco è un problema.</span><span class="sxs-lookup"><span data-stu-id="112f8-112">Before calling **WSALookupServiceNext**, an application must wait until it receives a notification—if blocking is an issue.</span></span>

<span data-ttu-id="112f8-113">Quando si chiama questa funzione, i parametri devono avere i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="112f8-113">When calling this function, the parameters must have the following values:</span></span>

<dl> <dt>

<span data-ttu-id="112f8-114"><span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*hLookup*</span><span class="sxs-lookup"><span data-stu-id="112f8-114"><span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*hLookup*</span></span>
</dt> <dd>

<span data-ttu-id="112f8-115">Specifica l'handle restituito da [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="112f8-115">Specifies the handle that [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) returns.</span></span>

</dd> <dt>

<span data-ttu-id="112f8-116"><span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*</span><span class="sxs-lookup"><span data-stu-id="112f8-116"><span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*</span></span>
</dt> <dd>

<span data-ttu-id="112f8-117">Deve essere **una \_ \_ \_ modifica di notifica NSP di sio**.</span><span class="sxs-lookup"><span data-stu-id="112f8-117">Must be **SIO\_NSP\_NOTIFY\_CHANGE**.</span></span>

</dd> <dt>

<span data-ttu-id="112f8-118"><span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*</span><span class="sxs-lookup"><span data-stu-id="112f8-118"><span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="112f8-119">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="112f8-119">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="112f8-120"><span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*</span><span class="sxs-lookup"><span data-stu-id="112f8-120"><span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="112f8-121">Deve essere zero (0).</span><span class="sxs-lookup"><span data-stu-id="112f8-121">Must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="112f8-122"><span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="112f8-122"><span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="112f8-123">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="112f8-123">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="112f8-124"><span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="112f8-124"><span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="112f8-125">Deve essere zero (0).</span><span class="sxs-lookup"><span data-stu-id="112f8-125">Must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="112f8-126"><span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="112f8-126"><span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*</span></span>
</dt> <dd>

<span data-ttu-id="112f8-127">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="112f8-127">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="112f8-128"><span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*</span><span class="sxs-lookup"><span data-stu-id="112f8-128"><span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*</span></span>
</dt> <dd>

<span data-ttu-id="112f8-129">Specifica **null** o un puntatore a una struttura [**WSACOMPLETION**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="112f8-129">Specifies either **NULL** or a pointer to a [**WSACOMPLETION**](winsock-nsp-reference-links.md) structure.</span></span>

</dd> </dl>

<span data-ttu-id="112f8-130">Dopo la ricezione di una notifica, chiamare [**WSALookupServiceNext**](winsock-nsp-reference-links.md) una volta per ottenere i risultati.</span><span class="sxs-lookup"><span data-stu-id="112f8-130">After a notification is received, call [**WSALookupServiceNext**](winsock-nsp-reference-links.md) one time to obtain the results.</span></span>

<span data-ttu-id="112f8-131">Per terminare una ricerca, chiamare [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).</span><span class="sxs-lookup"><span data-stu-id="112f8-131">To end a search, call [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).</span></span>

## <a name="resolution-notifications"></a><span data-ttu-id="112f8-132">Notifiche di risoluzione</span><span class="sxs-lookup"><span data-stu-id="112f8-132">Resolution Notifications</span></span>

<span data-ttu-id="112f8-133">Un client può ricevere una notifica ogni volta che viene aggiunta una voce di risoluzione dei nomi.</span><span class="sxs-lookup"><span data-stu-id="112f8-133">A client can be notified any time that a name resolution entry is added.</span></span> <span data-ttu-id="112f8-134">Il client chiama quindi [**WSALookupServiceNext**](winsock-nsp-reference-links.md) per ottenere i dati di risoluzione.</span><span class="sxs-lookup"><span data-stu-id="112f8-134">The client then calls [**WSALookupServiceNext**](winsock-nsp-reference-links.md) to obtain the resolution data.</span></span>

<span data-ttu-id="112f8-135">Se il client non utilizza questa tecnica, è possibile bloccare una chiamata a [**WSALookupServiceNext**](winsock-nsp-reference-links.md) fino a quando non si verifica il timeout specificato.</span><span class="sxs-lookup"><span data-stu-id="112f8-135">If the client does not use this technique, a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md) can be blocked until the specified timeout occurs.</span></span>

## <a name="cloud-list-notifications"></a><span data-ttu-id="112f8-136">Notifiche degli elenchi cloud</span><span class="sxs-lookup"><span data-stu-id="112f8-136">Cloud List Notifications</span></span>

<span data-ttu-id="112f8-137">Un client può ricevere una notifica ogni volta che viene apportata una modifica a un set di cloud.</span><span class="sxs-lookup"><span data-stu-id="112f8-137">A client can be notified any time there is a change to a set of clouds.</span></span>

<span data-ttu-id="112f8-138">La funzione [**WSALookupServiceNext**](winsock-nsp-reference-links.md) restituisce **WSA \_ E \_ non \_ più** come delimitatore di set.</span><span class="sxs-lookup"><span data-stu-id="112f8-138">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function returns **WSA\_E\_NO\_MORE** as a set delimiter.</span></span> <span data-ttu-id="112f8-139">L'applicazione client deve enumerare i cloud esistenti fino a quando non viene restituito questo messaggio e quindi utilizzare uno schema di notifica per recuperare le modifiche successive non appena si verificano.</span><span class="sxs-lookup"><span data-stu-id="112f8-139">The client application must enumerate existing clouds until this message is returned, and then use a notification scheme to retrieve subsequent changes as they occur.</span></span> <span data-ttu-id="112f8-140">Un'applicazione client può anche chiamare **WSALookupServiceNext**, ma la chiamata viene bloccata fino a quando non si verifica una modifica.</span><span class="sxs-lookup"><span data-stu-id="112f8-140">A client application can also call **WSALookupServiceNext**, but the call is blocked until a change occurs.</span></span>

<span data-ttu-id="112f8-141">La funzione [**WSALookupServiceNext**](winsock-nsp-reference-links.md) restituisce un cloud in una struttura **WSAQUERYSET** .</span><span class="sxs-lookup"><span data-stu-id="112f8-141">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function returns a cloud in a **WSAQUERYSET** structure.</span></span> <span data-ttu-id="112f8-142">Nel membro **dwOutputFlags** viene restituito uno dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="112f8-142">One of the following flags is returned in the **dwOutputFlags** member.</span></span>



| <span data-ttu-id="112f8-143">Valore</span><span class="sxs-lookup"><span data-stu-id="112f8-143">Value</span></span>               | <span data-ttu-id="112f8-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="112f8-144">Description</span></span>                                             |
|---------------------|---------------------------------------------------------|
| <span data-ttu-id="112f8-145">RISULTATO \_ \_ aggiunto</span><span class="sxs-lookup"><span data-stu-id="112f8-145">RESULT\_IS\_ADDED</span></span>   | <span data-ttu-id="112f8-146">Viene aggiunto il cloud restituito.</span><span class="sxs-lookup"><span data-stu-id="112f8-146">The cloud that is returned is added.</span></span>                    |
| <span data-ttu-id="112f8-147">RISULTATO \_ \_ modificato</span><span class="sxs-lookup"><span data-stu-id="112f8-147">RESULT\_IS\_CHANGED</span></span> | <span data-ttu-id="112f8-148">Il cloud restituito viene modificato.</span><span class="sxs-lookup"><span data-stu-id="112f8-148">The cloud that is returned is changed.</span></span>                  |
| <span data-ttu-id="112f8-149">RISULTATO \_ \_ eliminato</span><span class="sxs-lookup"><span data-stu-id="112f8-149">RESULT\_IS\_DELETED</span></span> | <span data-ttu-id="112f8-150">Il cloud restituito viene eliminato e non è valido.</span><span class="sxs-lookup"><span data-stu-id="112f8-150">The cloud that is returned is deleted and is not valid.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="112f8-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="112f8-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="112f8-152">PNRP e WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="112f8-152">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="112f8-153">PNRP e WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="112f8-153">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="112f8-154">PNRP e WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="112f8-154">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="112f8-155">Codici di errore PNRP NSP</span><span class="sxs-lookup"><span data-stu-id="112f8-155">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="112f8-156">**WSANSPIoctl**</span><span class="sxs-lookup"><span data-stu-id="112f8-156">**WSANSPIoctl**</span></span>](winsock-nsp-reference-links.md)
</dt> <dt>

<span data-ttu-id="112f8-157">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="112f8-157">**WSALookupServiceBegin**</span></span>
</dt> <dt>

<span data-ttu-id="112f8-158">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="112f8-158">**WSALookupServiceEnd**</span></span>
</dt> <dt>

<span data-ttu-id="112f8-159">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="112f8-159">**WSAQUERYSET**</span></span>
</dt> </dl>

 

 



