---
title: ACK per il frammento
description: Utilizzare il ACK per il pacchetto del frammento per confermare la richiesta del frammento del client.
ms.assetid: f5466489-2d5e-4850-a39c-37bc4923a7ac
keywords:
- ACK per BITS frammenti
topic_type:
- apiref
api_name:
- Ack for Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef28381313ce00fd6089ebf845ed342ccae455c7
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "103963549"
---
# <a name="ack-for-fragment"></a><span data-ttu-id="40b65-104">ACK per il frammento</span><span class="sxs-lookup"><span data-stu-id="40b65-104">Ack for Fragment</span></span>

<span data-ttu-id="40b65-105">Utilizzare il **ACK per** il pacchetto del frammento per confermare la richiesta del [**frammento**](fragment.md) del client.</span><span class="sxs-lookup"><span data-stu-id="40b65-105">Use the **Ack for Fragment** packet to acknowledge the client's [**Fragment**](fragment.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
BITS-Received-Content-Range: range
BITS-Reply-URL: url
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="40b65-106">Intestazioni</span><span class="sxs-lookup"><span data-stu-id="40b65-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="40b65-107"><span id="reason-code"></span><span id="REASON-CODE"></span>codice motivo</span><span class="sxs-lookup"><span data-stu-id="40b65-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="40b65-108">Sostituire Reason-Code con un codice motivo HTTP.</span><span class="sxs-lookup"><span data-stu-id="40b65-108">Replace reason-code with an HTTP reason code.</span></span> <span data-ttu-id="40b65-109">La tabella seguente illustra i codici motivo tipici per una risposta a una richiesta di [**frammento**](fragment.md) .</span><span class="sxs-lookup"><span data-stu-id="40b65-109">The following table shows the typical reason codes for a response to a [**Fragment**](fragment.md) request.</span></span> <span data-ttu-id="40b65-110">Per un elenco di codici motivo HTTP, vedere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="40b65-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>



| <span data-ttu-id="40b65-111">Codice motivo</span><span class="sxs-lookup"><span data-stu-id="40b65-111">Reason code</span></span>    | <span data-ttu-id="40b65-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40b65-112">Description</span></span>                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40b65-113">200</span><span class="sxs-lookup"><span data-stu-id="40b65-113">200</span></span><br/> | <span data-ttu-id="40b65-114">OK.</span><span class="sxs-lookup"><span data-stu-id="40b65-114">OK.</span></span> <span data-ttu-id="40b65-115">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="40b65-115">The request was successful.</span></span><br/>                                                                             |
| <span data-ttu-id="40b65-116">416</span><span class="sxs-lookup"><span data-stu-id="40b65-116">416</span></span><br/> | <span data-ttu-id="40b65-117">Range: not-Impossibile attenersi all'.</span><span class="sxs-lookup"><span data-stu-id="40b65-117">Range-Not-Satisfiable.</span></span> <span data-ttu-id="40b65-118">Il client ha inviato un frammento il cui intervallo non è contiguo al frammento precedente.</span><span class="sxs-lookup"><span data-stu-id="40b65-118">The client sent a fragment whose range is not contiguous with the previous fragment.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="40b65-119"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>motivo-Descrizione</span><span class="sxs-lookup"><span data-stu-id="40b65-119"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="40b65-120">Sostituire Reason-Description con la descrizione HTTP associata al codice motivo.</span><span class="sxs-lookup"><span data-stu-id="40b65-120">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="40b65-121">Ad esempio, impostare Reason-Description su OK se Reason-Code è 200.</span><span class="sxs-lookup"><span data-stu-id="40b65-121">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="40b65-122"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo-pacchetto</span><span class="sxs-lookup"><span data-stu-id="40b65-122"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="40b65-123">Identifica il pacchetto di risposta come pacchetto ACK.</span><span class="sxs-lookup"><span data-stu-id="40b65-123">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="40b65-124"><span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-Received-Content-Range</span><span class="sxs-lookup"><span data-stu-id="40b65-124"><span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-Received-Content-Range</span></span>
</dt> <dd>

<span data-ttu-id="40b65-125">Offset in base zero al byte successivo che il server prevede che il client invii.</span><span class="sxs-lookup"><span data-stu-id="40b65-125">Zero-based offset to the next byte the server expects the client to send.</span></span> <span data-ttu-id="40b65-126">Se, ad esempio, il frammento contiene l'intervallo 128 212, impostare intervallo su 213.</span><span class="sxs-lookup"><span data-stu-id="40b65-126">For example, if the fragment contained the range 128 212, you would set range to 213.</span></span>

</dd> <dt>

<span data-ttu-id="40b65-127"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BIT-session-ID</span><span class="sxs-lookup"><span data-stu-id="40b65-127"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="40b65-128">GUID di stringa che identifica la sessione per il client.</span><span class="sxs-lookup"><span data-stu-id="40b65-128">String GUID that identifies the session to the client.</span></span> <span data-ttu-id="40b65-129">Sostituire {GUID} con l'identificatore di sessione inviato dal client nel pacchetto di richiesta del [**frammento**](fragment.md) .</span><span class="sxs-lookup"><span data-stu-id="40b65-129">Replace {guid} with the session identifier that the client sent in the [**Fragment**](fragment.md) request packet.</span></span> <span data-ttu-id="40b65-130">Se non si riconosce l'identificatore di sessione, impostare l'intestazione BITS-Error-Code su BG \_ E la \_ sessione \_ non \_ trovata.</span><span class="sxs-lookup"><span data-stu-id="40b65-130">If you do not recognize the session identifier, set the BITS-Error-Code header to BG\_E\_SESSION\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="40b65-131"><span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-Reply-URL</span><span class="sxs-lookup"><span data-stu-id="40b65-131"><span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-Reply-URL</span></span>
</dt> <dd>

<span data-ttu-id="40b65-132">Contiene l'URL dei dati di risposta di un processo di caricamento-risposta.</span><span class="sxs-lookup"><span data-stu-id="40b65-132">Contains the URL to the reply data of an upload-reply job.</span></span> <span data-ttu-id="40b65-133">Includere questa intestazione nella risposta del frammento finale dopo che il caricamento è stato completato e si riceve una risposta dall'applicazione server, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="40b65-133">Include this header in the final fragment response after the upload is complete and you receive a response from the server application, if applicable.</span></span>

<span data-ttu-id="40b65-134">Usare l'intestazione Content-Range della richiesta Fragment per determinare se il caricamento è stato completato.</span><span class="sxs-lookup"><span data-stu-id="40b65-134">Use the Content-Range header from the Fragment request to determine whether the upload is complete.</span></span> <span data-ttu-id="40b65-135">Il caricamento è completo se l'offset finale del valore dell'intervallo è uguale al valore di lunghezza totale meno uno.</span><span class="sxs-lookup"><span data-stu-id="40b65-135">The upload is complete if the end offset of the range value equals the total-length value minus one.</span></span>

<span data-ttu-id="40b65-136">Il server BITS inserisce il file di caricamento nell'applicazione server dopo aver determinato che il caricamento è stato completato.</span><span class="sxs-lookup"><span data-stu-id="40b65-136">The BITS server posts the upload file to the server application after it determines the upload is complete.</span></span> <span data-ttu-id="40b65-137">L'applicazione server elabora il file e genera la risposta.</span><span class="sxs-lookup"><span data-stu-id="40b65-137">The server application processes the file and generates the reply.</span></span> <span data-ttu-id="40b65-138">Il server BITS imposta il valore di BITS-Reply-URL sull'URL del file di risposta dall'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="40b65-138">The BITS server sets the value of BITS-Reply-URL to the URL of the reply file from the server application.</span></span>

</dd> <dt>

<span data-ttu-id="40b65-139"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Lunghezza del contenuto</span><span class="sxs-lookup"><span data-stu-id="40b65-139"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="40b65-140">Sostituire length con il numero di byte inclusi nel corpo della risposta.</span><span class="sxs-lookup"><span data-stu-id="40b65-140">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="40b65-141">Content-Length è obbligatorio, anche se il corpo della risposta non include il contenuto.</span><span class="sxs-lookup"><span data-stu-id="40b65-141">Content-Length is required, even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="40b65-142"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-errore-codice</span><span class="sxs-lookup"><span data-stu-id="40b65-142"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="40b65-143">Sostituire error-code con un numero esadecimale che rappresenta un valore HRESULT associato a un errore sul lato server.</span><span class="sxs-lookup"><span data-stu-id="40b65-143">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="40b65-144">Includere questa intestazione solo se il codice motivo non è 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="40b65-144">Only include this header if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="40b65-145"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-errore-contesto</span><span class="sxs-lookup"><span data-stu-id="40b65-145"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="40b65-146">Sostituire Error-context con un numero esadecimale che rappresenta il contesto in cui si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="40b65-146">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="40b65-147">Specificare il numero esadecimale per il [**\_ \_ \_ \_ file remoto del contesto di errore BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) se il server ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="40b65-147">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="40b65-148">In caso contrario, specificare il numero esadecimale per l' **\_ \_ \_ \_ applicazione remota del contesto di errore BG** (0x7) se l'errore è stato generato dall'applicazione a cui viene passato il file di caricamento.</span><span class="sxs-lookup"><span data-stu-id="40b65-148">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="40b65-149">Includere questa intestazione solo se il codice motivo non è 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="40b65-149">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40b65-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="40b65-150">Remarks</span></span>

<span data-ttu-id="40b65-151">Se la sessione è per un processo di caricamento-risposta, potrebbe verificarsi un ritardo prima che il client riceva l'ACK finale per la risposta del **frammento** .</span><span class="sxs-lookup"><span data-stu-id="40b65-151">If the session is for an upload-reply job, there may be a delay before the client receives the final **Ack for Fragment** response.</span></span> <span data-ttu-id="40b65-152">La lunghezza del ritardo dipende dalla quantità di tempo richiesta dall'applicazione server (applicazione a cui il server invia il file di caricamento) per generare la risposta.</span><span class="sxs-lookup"><span data-stu-id="40b65-152">The length of the delay depends on the amount of time the server application (application to which the server posts the upload file) takes to generate the reply.</span></span>

## <a name="see-also"></a><span data-ttu-id="40b65-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40b65-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40b65-154">**Creazione sessione**</span><span class="sxs-lookup"><span data-stu-id="40b65-154">**Create-Session**</span></span>](create-session.md)
</dt> <dt>

[<span data-ttu-id="40b65-155">**Frammento**</span><span class="sxs-lookup"><span data-stu-id="40b65-155">**Fragment**</span></span>](fragment.md)
</dt> </dl>

 

 





