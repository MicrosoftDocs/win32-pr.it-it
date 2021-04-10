---
title: ACK per ping
description: Usare ACK per il pacchetto ping per confermare la richiesta ping del client.
ms.assetid: 2e288564-d06f-4b45-b0c0-7aab1897da40
keywords:
- ACK per BITS ping
topic_type:
- apiref
api_name:
- Ack for Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a3ca765c8bd7758f19abe396ad0449a5895d8e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "103963548"
---
# <a name="ack-for-ping"></a><span data-ttu-id="09ca9-104">ACK per ping</span><span class="sxs-lookup"><span data-stu-id="09ca9-104">Ack for Ping</span></span>

<span data-ttu-id="09ca9-105">Usare **ACK per** il pacchetto ping per confermare la richiesta [**ping**](ping.md) del client.</span><span class="sxs-lookup"><span data-stu-id="09ca9-105">Use the **Ack for Ping** packet to acknowledge the client's [**Ping**](ping.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="09ca9-106">Intestazioni</span><span class="sxs-lookup"><span data-stu-id="09ca9-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="09ca9-107"><span id="reason-code"></span><span id="REASON-CODE"></span>codice motivo</span><span class="sxs-lookup"><span data-stu-id="09ca9-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="09ca9-108">Sostituire Reason-Code con il codice motivo HTTP.</span><span class="sxs-lookup"><span data-stu-id="09ca9-108">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="09ca9-109">Ad esempio, impostare Reason-Code su 200 in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="09ca9-109">For example, set reason-code to 200 if success.</span></span> <span data-ttu-id="09ca9-110">Per un elenco di codici motivo HTTP, vedere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="09ca9-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="09ca9-111"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>motivo-Descrizione</span><span class="sxs-lookup"><span data-stu-id="09ca9-111"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="09ca9-112">Sostituire Reason-Description con la descrizione HTTP associata al codice motivo.</span><span class="sxs-lookup"><span data-stu-id="09ca9-112">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="09ca9-113">Ad esempio, impostare Reason-Description su OK se Reason-Code è 200.</span><span class="sxs-lookup"><span data-stu-id="09ca9-113">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="09ca9-114"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo-pacchetto</span><span class="sxs-lookup"><span data-stu-id="09ca9-114"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="09ca9-115">Identifica il pacchetto di risposta come pacchetto ACK.</span><span class="sxs-lookup"><span data-stu-id="09ca9-115">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="09ca9-116"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Lunghezza del contenuto</span><span class="sxs-lookup"><span data-stu-id="09ca9-116"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="09ca9-117">Sostituire length con il numero di byte inclusi nel corpo della risposta.</span><span class="sxs-lookup"><span data-stu-id="09ca9-117">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="09ca9-118">Obbligatorio anche se il corpo della risposta non include il contenuto.</span><span class="sxs-lookup"><span data-stu-id="09ca9-118">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="09ca9-119"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-errore-codice</span><span class="sxs-lookup"><span data-stu-id="09ca9-119"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="09ca9-120">Sostituire error-code con un numero esadecimale che rappresenta un valore HRESULT associato a un errore sul lato server.</span><span class="sxs-lookup"><span data-stu-id="09ca9-120">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="09ca9-121">Includere questa intestazione solo se il codice motivo non è 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="09ca9-121">Include this header only if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="09ca9-122"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-errore-contesto</span><span class="sxs-lookup"><span data-stu-id="09ca9-122"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="09ca9-123">Sostituire Error-context con un numero esadecimale che rappresenta il contesto in cui si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="09ca9-123">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="09ca9-124">Specificare il numero esadecimale per il [**\_ \_ \_ \_ file remoto del contesto di errore BG**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) se il server ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="09ca9-124">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="09ca9-125">In caso contrario, specificare il numero esadecimale per l' **\_ \_ \_ \_ applicazione remota del contesto di errore BG** (0x7) se l'errore è stato generato dall'applicazione a cui viene passato il file di caricamento.</span><span class="sxs-lookup"><span data-stu-id="09ca9-125">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="09ca9-126">Includere questa intestazione solo se il codice motivo non è 200 o 201.</span><span class="sxs-lookup"><span data-stu-id="09ca9-126">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="09ca9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09ca9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09ca9-128">**Ping**</span><span class="sxs-lookup"><span data-stu-id="09ca9-128">**Ping**</span></span>](ping.md)
</dt> </dl>

 

 




