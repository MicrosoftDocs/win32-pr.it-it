---
title: ACK per Create-Session
description: Usare ACK per Create-Session pacchetto per confermare la richiesta di Create-Session del client.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- ACK per Create-Session BITS
topic_type:
- apiref
api_name:
- Ack for Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d978ec4c5693a5087734975c412b999ed7d5890
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "106300669"
---
# <a name="ack-for-create-session"></a><span data-ttu-id="a6755-104">ACK per Create-Session</span><span class="sxs-lookup"><span data-stu-id="a6755-104">Ack for Create-Session</span></span>

<span data-ttu-id="a6755-105">Usare ACK per il pacchetto di **creazione sessione** per confermare la richiesta di [**creazione sessione**](create-session.md) del client.</span><span class="sxs-lookup"><span data-stu-id="a6755-105">Use the **Ack for Create-Session** packet to acknowledge the client's [**Create-Session**](create-session.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Protocol: {guid}
BITS-Session-Id: {guid}
BITS-Host-Id: PublicHostName
BITS-Host-Id-Fallback-Timeout: Timeout
Accept-Encoding: Identity
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="a6755-106">Intestazioni</span><span class="sxs-lookup"><span data-stu-id="a6755-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="a6755-107"><span id="reason-code"></span><span id="REASON-CODE"></span>codice motivo</span><span class="sxs-lookup"><span data-stu-id="a6755-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="a6755-108">Sostituire Reason-Code con il codice motivo HTTP.</span><span class="sxs-lookup"><span data-stu-id="a6755-108">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="a6755-109">La tabella seguente illustra i codici motivo tipici per una risposta a una richiesta di [**creazione sessione**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="a6755-109">The following table shows the typical reason codes for a response to a [**Create-Session**](create-session.md) request.</span></span> <span data-ttu-id="a6755-110">Per un elenco di codici motivo HTTP, vedere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="a6755-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>



| <span data-ttu-id="a6755-111">Codice motivo</span><span class="sxs-lookup"><span data-stu-id="a6755-111">Reason code</span></span>    | <span data-ttu-id="a6755-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6755-112">Description</span></span>                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a6755-113">200</span><span class="sxs-lookup"><span data-stu-id="a6755-113">200</span></span><br/> | <span data-ttu-id="a6755-114">OK.</span><span class="sxs-lookup"><span data-stu-id="a6755-114">OK.</span></span> <span data-ttu-id="a6755-115">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a6755-115">The request was successful.</span></span><br/>                                          |
| <span data-ttu-id="a6755-116">201</span><span class="sxs-lookup"><span data-stu-id="a6755-116">201</span></span><br/> | <span data-ttu-id="a6755-117">Creazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="a6755-117">Created.</span></span> <span data-ttu-id="a6755-118">La sessione è stata creata.</span><span class="sxs-lookup"><span data-stu-id="a6755-118">The session was created.</span></span><br/>                                        |
| <span data-ttu-id="a6755-119">403</span><span class="sxs-lookup"><span data-stu-id="a6755-119">403</span></span><br/> | <span data-ttu-id="a6755-120">Non consentito.</span><span class="sxs-lookup"><span data-stu-id="a6755-120">Forbidden.</span></span> <span data-ttu-id="a6755-121">L'utente non è autorizzato a caricare i file nell'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="a6755-121">The user is not allowed to upload files to the specified URL.</span></span><br/> |
| <span data-ttu-id="a6755-122">404</span><span class="sxs-lookup"><span data-stu-id="a6755-122">404</span></span><br/> | <span data-ttu-id="a6755-123">Non trovato.</span><span class="sxs-lookup"><span data-stu-id="a6755-123">Not Found.</span></span> <span data-ttu-id="a6755-124">L'URL specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="a6755-124">The specified URL does not exist.</span></span><br/>                             |
| <span data-ttu-id="a6755-125">409</span><span class="sxs-lookup"><span data-stu-id="a6755-125">409</span></span><br/> | <span data-ttu-id="a6755-126">Conflitto.</span><span class="sxs-lookup"><span data-stu-id="a6755-126">Conflict.</span></span> <span data-ttu-id="a6755-127">Il file esiste nel server e non può essere sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="a6755-127">The file exists on the server and cannot be overwritten.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="a6755-128"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>motivo-Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6755-128"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="a6755-129">Sostituire Reason-Description con la descrizione HTTP associata al codice motivo.</span><span class="sxs-lookup"><span data-stu-id="a6755-129">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="a6755-130">Ad esempio, impostare Reason-Description su OK se Reason-Code è 200.</span><span class="sxs-lookup"><span data-stu-id="a6755-130">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="a6755-131"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo-pacchetto</span><span class="sxs-lookup"><span data-stu-id="a6755-131"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="a6755-132">Identifica il pacchetto di risposta come pacchetto ACK.</span><span class="sxs-lookup"><span data-stu-id="a6755-132">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="a6755-133"><span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-protocollo</span><span class="sxs-lookup"><span data-stu-id="a6755-133"><span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-Protocol</span></span>
</dt> <dd>

<span data-ttu-id="a6755-134">GUID di stringa che identifica il protocollo che il server vuole usare per questa sessione.</span><span class="sxs-lookup"><span data-stu-id="a6755-134">String GUID that identifies the protocol that the server wants to use for this session.</span></span> <span data-ttu-id="a6755-135">Sostituire {GUID} con l'identificatore di protocollo dall'elenco dei protocolli inclusi dal client nella richiesta di [**creazione sessione**](create-session.md) . l'intestazione BITS-supported-Protocol contiene l'elenco.</span><span class="sxs-lookup"><span data-stu-id="a6755-135">Replace {guid} with the protocol identifier from the list of protocols the client includes in the [**Create-Session**](create-session.md) request; the BITS-Supported-Protocol header contains the list.</span></span> <span data-ttu-id="a6755-136">Includere questa intestazione solo se il codice motivo è 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="a6755-136">Include this header only if the reason-code is 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="a6755-137"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BIT-session-ID</span><span class="sxs-lookup"><span data-stu-id="a6755-137"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="a6755-138">GUID di stringa che identifica questa sessione con il client.</span><span class="sxs-lookup"><span data-stu-id="a6755-138">String GUID that identifies this session to the client.</span></span> <span data-ttu-id="a6755-139">Sostituire {GUID} con l'identificatore di sessione inviato dal client in tutti i pacchetti di richiesta successivi.</span><span class="sxs-lookup"><span data-stu-id="a6755-139">Replace {guid} with the session identifier that the client sends in all subsequent request packets.</span></span>

<span data-ttu-id="a6755-140">BITS usa un GUID per identificare la sessione, ma è possibile usare qualsiasi stringa HTTP-Legal fino a 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="a6755-140">BITS uses a GUID to identify the session, but you can use any HTTP-legal string up to 100 characters.</span></span>

</dd> <dt>

<span data-ttu-id="a6755-141"><span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BIT-host-ID</span><span class="sxs-lookup"><span data-stu-id="a6755-141"><span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-Host-Id</span></span>
</dt> <dd>

<span data-ttu-id="a6755-142">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a6755-142">Optional.</span></span> <span data-ttu-id="a6755-143">Includere questa intestazione solo se è impostata la [Proprietà estensione IIS BITS](bits-iis-extension-properties.md), BITSHostId.</span><span class="sxs-lookup"><span data-stu-id="a6755-143">Include this header only if the [BITS IIS extension property](bits-iis-extension-properties.md), BITSHostId, is set.</span></span> <span data-ttu-id="a6755-144">Sostituire PublicHostName con il nome o l'indirizzo IP del server della proprietà BITSHostId.</span><span class="sxs-lookup"><span data-stu-id="a6755-144">Replace PublicHostName with the server name or IP address from the BITSHostId property.</span></span>

<span data-ttu-id="a6755-145">Il client deve sostituire la parte server dell'URL remoto in tutti i pacchetti successivi.</span><span class="sxs-lookup"><span data-stu-id="a6755-145">The client must replace the server portion of the remote-URL on all subsequent packets.</span></span> <span data-ttu-id="a6755-146">Se il client non specifica questo nome host nei pacchetti successivi, è possibile che il processo venga riavviato in un altro server della farm, lasciando un file di caricamento parziale nel server precedente.</span><span class="sxs-lookup"><span data-stu-id="a6755-146">If the client does not specify this host name on subsequent packets, it is possible that the job will begin again on another server in the farm, leaving a partial upload file on the previous server.</span></span>

</dd> <dt>

<span data-ttu-id="a6755-147"><span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-host-ID-fallback-timeout</span><span class="sxs-lookup"><span data-stu-id="a6755-147"><span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-Host-Id-Fallback-Timeout</span></span>
</dt> <dd>

<span data-ttu-id="a6755-148">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a6755-148">Optional.</span></span> <span data-ttu-id="a6755-149">Includere questa intestazione solo se è specificata l'intestazione BITS-host-ID.</span><span class="sxs-lookup"><span data-stu-id="a6755-149">Include this header only if the BITS-Host-Id header is specified.</span></span> <span data-ttu-id="a6755-150">Sostituire timeout con il valore di timeout della proprietà BITSHostIdFallbackTimeout.</span><span class="sxs-lookup"><span data-stu-id="a6755-150">Replace Timeout with the time-out value from the BITSHostIdFallbackTimeout property.</span></span> <span data-ttu-id="a6755-151">La proprietà BITSHostIdFallbackTimeout è una delle [proprietà dell'estensione IIS BITS](bits-iis-extension-properties.md).</span><span class="sxs-lookup"><span data-stu-id="a6755-151">The BITSHostIdFallbackTimeout property is one of the [BITS IIS extension properties](bits-iis-extension-properties.md).</span></span>

<span data-ttu-id="a6755-152">Il client usa il periodo di timeout per determinare il tempo che tenta di riconnettersi al nome del server specificato nell'intestazione BITS-host-ID prima di ripristinare il nome host specificato nel nome file remoto del processo.</span><span class="sxs-lookup"><span data-stu-id="a6755-152">The client uses the time-out period to determine how long it tries to reconnect to the server name specified in the BITS-Host-Id header before reverting to the host name specified in the remote file name of the job.</span></span> <span data-ttu-id="a6755-153">Il timer inizia quando BITS non è in grado di connettersi al server BITS-host-ID.</span><span class="sxs-lookup"><span data-stu-id="a6755-153">The timer begins when BITS is unable to connect to the BITS-Host-Id server.</span></span> <span data-ttu-id="a6755-154">Il timer viene reimpostato quando viene ripristinata una connessione al server.</span><span class="sxs-lookup"><span data-stu-id="a6755-154">The timer is reset when a connection to the server is restored.</span></span> <span data-ttu-id="a6755-155">Se non viene specificato un periodo di timeout, il client non viene mai ripristinato al nome host specificato nel nome file remoto.</span><span class="sxs-lookup"><span data-stu-id="a6755-155">If a time-out period is not specified, the client never reverts to the host name specified in the remote file name.</span></span>

</dd> <dt>

<span data-ttu-id="a6755-156"><span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accept-Encoding</span><span class="sxs-lookup"><span data-stu-id="a6755-156"><span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accept-Encoding</span></span>
</dt> <dd>

<span data-ttu-id="a6755-157">Identifica lo schema di codifica da utilizzare per i frammenti inviati al server.</span><span class="sxs-lookup"><span data-stu-id="a6755-157">Identifies the encoding scheme to use on the fragments sent to the server.</span></span> <span data-ttu-id="a6755-158">Il pacchetto del frammento contiene il frammento codificato nel corpo del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a6755-158">The Fragment packet contains the encoded fragment in the body of the packet.</span></span> <span data-ttu-id="a6755-159">Il server BITS richiede la codifica dell'identità (testo normale).</span><span class="sxs-lookup"><span data-stu-id="a6755-159">The BITS server requires Identity encoding (plaintext).</span></span> <span data-ttu-id="a6755-160">Includere questa intestazione solo se il codice motivo è 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="a6755-160">Include this header only if the Reason-code is 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="a6755-161"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Lunghezza del contenuto</span><span class="sxs-lookup"><span data-stu-id="a6755-161"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="a6755-162">Sostituire length con il numero di byte inclusi nel corpo della risposta.</span><span class="sxs-lookup"><span data-stu-id="a6755-162">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="a6755-163">Obbligatorio anche se il corpo della risposta non include il contenuto.</span><span class="sxs-lookup"><span data-stu-id="a6755-163">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="a6755-164"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-errore-codice</span><span class="sxs-lookup"><span data-stu-id="a6755-164"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="a6755-165">Sostituire error-code con un numero esadecimale che rappresenta un valore HRESULT associato a un errore sul lato server.</span><span class="sxs-lookup"><span data-stu-id="a6755-165">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="a6755-166">Includere questa intestazione solo se il codice motivo non è 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="a6755-166">Include this header only if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="a6755-167"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-errore-contesto</span><span class="sxs-lookup"><span data-stu-id="a6755-167"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="a6755-168">Sostituire Error-context con un numero esadecimale che rappresenta il contesto in cui si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="a6755-168">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="a6755-169">Specificare il numero esadecimale per il [**\_ \_ \_ \_ file remoto del contesto di errore BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) se il server ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="a6755-169">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="a6755-170">In caso contrario, specificare il numero esadecimale per l' **\_ \_ \_ \_ applicazione remota del contesto di errore BG** (0x7) se l'errore è stato generato dall'applicazione a cui viene passato il file di caricamento.</span><span class="sxs-lookup"><span data-stu-id="a6755-170">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="a6755-171">Includere questa intestazione solo se il codice motivo non è 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="a6755-171">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="a6755-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6755-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6755-173">**Creazione sessione**</span><span class="sxs-lookup"><span data-stu-id="a6755-173">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 





