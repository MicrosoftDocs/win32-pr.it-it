---
title: ACK per Cancel-Session
description: Usare ACK per Cancel-Session pacchetto per confermare la richiesta di Cancel-Session del client. Il server invia il riconoscimento dopo il rilascio di tutte le risorse associate alla sessione di caricamento.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- ACK per Cancel-Session BITS
topic_type:
- apiref
api_name:
- Ack for Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b85ff937b720a69ee2722cef2f02b25273ea58d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104047568"
---
# <a name="ack-for-cancel-session"></a><span data-ttu-id="c6636-105">ACK per Cancel-Session</span><span class="sxs-lookup"><span data-stu-id="c6636-105">Ack for Cancel-Session</span></span>

<span data-ttu-id="c6636-106">Usare **ACK per il pacchetto Annulla sessione** per confermare la richiesta di [**annullamento della sessione**](cancel-session.md) del client.</span><span class="sxs-lookup"><span data-stu-id="c6636-106">Use the **Ack for Cancel-Session** packet to acknowledge the client's [**Cancel-Session**](cancel-session.md) request.</span></span> <span data-ttu-id="c6636-107">Il server invia il riconoscimento dopo il rilascio di tutte le risorse associate alla sessione di caricamento.</span><span class="sxs-lookup"><span data-stu-id="c6636-107">The server sends the acknowledgment after releasing all resources associated with the upload session.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="c6636-108">Intestazioni</span><span class="sxs-lookup"><span data-stu-id="c6636-108">Headers</span></span>

<dl> <dt>

<span data-ttu-id="c6636-109"><span id="reason-code"></span><span id="REASON-CODE"></span>codice motivo</span><span class="sxs-lookup"><span data-stu-id="c6636-109"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="c6636-110">Sostituire Reason-Code con il codice motivo HTTP.</span><span class="sxs-lookup"><span data-stu-id="c6636-110">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="c6636-111">Ad esempio, impostare Reason-Code su 200 in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c6636-111">For example, set reason-code to 200 if success.</span></span> <span data-ttu-id="c6636-112">Per un elenco di codici motivo HTTP, vedere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="c6636-112">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="c6636-113"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>motivo-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6636-113"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="c6636-114">Sostituire Reason-Description con la descrizione HTTP associata al codice motivo.</span><span class="sxs-lookup"><span data-stu-id="c6636-114">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="c6636-115">Ad esempio, impostare Reason-Description su OK se Reason-Code è 200.</span><span class="sxs-lookup"><span data-stu-id="c6636-115">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="c6636-116"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo-pacchetto</span><span class="sxs-lookup"><span data-stu-id="c6636-116"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="c6636-117">Identifica il pacchetto di risposta come pacchetto ACK.</span><span class="sxs-lookup"><span data-stu-id="c6636-117">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="c6636-118"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BIT-session-ID</span><span class="sxs-lookup"><span data-stu-id="c6636-118"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="c6636-119">GUID di stringa che identifica la sessione per il client.</span><span class="sxs-lookup"><span data-stu-id="c6636-119">String GUID that identifies the session to the client.</span></span> <span data-ttu-id="c6636-120">Sostituire {GUID} con l'identificatore di sessione inviato dal client nel pacchetto di richiesta di [**annullamento della sessione**](cancel-session.md) .</span><span class="sxs-lookup"><span data-stu-id="c6636-120">Replace {guid} with the session identifier that the client sent in the [**Cancel-Session**](cancel-session.md) request packet.</span></span> <span data-ttu-id="c6636-121">Se non si riconosce l'identificatore di sessione, impostare l'intestazione BITS-Error-Code su BG \_ E la \_ sessione \_ non \_ trovata.</span><span class="sxs-lookup"><span data-stu-id="c6636-121">If you do not recognize the session identifier, set the BITS-Error-Code header to BG\_E\_SESSION\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="c6636-122"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Lunghezza del contenuto</span><span class="sxs-lookup"><span data-stu-id="c6636-122"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="c6636-123">Sostituire length con il numero di byte inclusi nel corpo della risposta.</span><span class="sxs-lookup"><span data-stu-id="c6636-123">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="c6636-124">Obbligatorio anche se il corpo della risposta non include il contenuto.</span><span class="sxs-lookup"><span data-stu-id="c6636-124">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="c6636-125"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-errore-codice</span><span class="sxs-lookup"><span data-stu-id="c6636-125"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="c6636-126">Sostituire error-code con un numero esadecimale che rappresenta un valore HRESULT associato a un errore sul lato server.</span><span class="sxs-lookup"><span data-stu-id="c6636-126">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="c6636-127">Includere questa intestazione solo se il codice motivo non è 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="c6636-127">Only include this header if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="c6636-128"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-errore-contesto</span><span class="sxs-lookup"><span data-stu-id="c6636-128"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="c6636-129">Sostituire Error-context con un numero esadecimale che rappresenta il contesto in cui si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="c6636-129">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="c6636-130">Specificare il numero esadecimale per [**BG_ERROR_CONTEXT_REMOTE_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) se il server ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="c6636-130">Specify the hexadecimal number for [**BG_ERROR_CONTEXT_REMOTE_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="c6636-131">In caso contrario, specificare il numero esadecimale per l' **\_ \_ \_ \_ applicazione remota del contesto di errore BG** (0x7) se l'errore è stato generato dall'applicazione a cui viene passato il file di caricamento.</span><span class="sxs-lookup"><span data-stu-id="c6636-131">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="c6636-132">Includere questa intestazione solo se il codice motivo non è 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="c6636-132">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6636-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6636-133">Remarks</span></span>

<span data-ttu-id="c6636-134">Il client BITS invia nuovamente il pacchetto [**Annulla sessione**](cancel-session.md) se il codice motivo è compreso nell'intervallo da 500 a 599, a meno che non sia presente l'intestazione bits-error-code con un valore di BG \_ E \_ Session \_ non \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="c6636-134">The BITS client resends the [**Cancel-Session**](cancel-session.md) packet if the reason-code is in the range from 500 through 599, unless the BITS-Error-Code header is present with a value of BG\_E\_SESSION\_NOT\_FOUND.</span></span> <span data-ttu-id="c6636-135">Il client non tenterà di eseguire un nuovo tentativo per i codici motivo da 100 a 499.</span><span class="sxs-lookup"><span data-stu-id="c6636-135">The client will not retry for reason codes 100 through 499.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6636-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6636-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6636-137">**ACK per chiusura sessione**</span><span class="sxs-lookup"><span data-stu-id="c6636-137">**Ack for Close-Session**</span></span>](ack-for-close-session.md)
</dt> <dt>

[<span data-ttu-id="c6636-138">**Annulla-sessione**</span><span class="sxs-lookup"><span data-stu-id="c6636-138">**Cancel-Session**</span></span>](cancel-session.md)
</dt> </dl>

 

 




