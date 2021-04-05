---
title: Frammento
description: Usare il pacchetto di frammenti per inviare un frammento del file di caricamento al server.
ms.assetid: d6df7e47-a240-4be2-a9c4-24a13e622861
keywords:
- BIT frammenti
topic_type:
- apiref
api_name:
- Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5103e90ec84a20ff4c04d9036a744919d9b1fd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104117391"
---
# <a name="fragment"></a><span data-ttu-id="d4dc2-104">Frammento</span><span class="sxs-lookup"><span data-stu-id="d4dc2-104">Fragment</span></span>

<span data-ttu-id="d4dc2-105">Usare il pacchetto di **frammenti** per inviare un frammento del file di caricamento al server.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-105">Use the **Fragment** packet to send a fragment of the upload file to the server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Fragment
BITS-Session-Id: {guid}
Content-Name: filename
Content-Length: length
Content-Range: Bytes range/total-length
Content-Encoding: encoding
```

## <a name="headers"></a><span data-ttu-id="d4dc2-106">Intestazioni</span><span class="sxs-lookup"><span data-stu-id="d4dc2-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="d4dc2-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_post BITS</span><span class="sxs-lookup"><span data-stu-id="d4dc2-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="d4dc2-108">Verbo specifico di BITS che identifica il pacchetto nel server BITS.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="d4dc2-109">Sostituire Remote-URL con l'URI assoluto o relativo.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="d4dc2-110">In genere, sostituire Remote-URL con il nome file remoto del processo.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="d4dc2-111">Per considerazioni sul bilanciamento del carico di rete, vedere l'intestazione BITS-host-ID nel pacchetto di [**creazione della sessione**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="d4dc2-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="d4dc2-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo-pacchetto</span><span class="sxs-lookup"><span data-stu-id="d4dc2-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="d4dc2-113">Identifica il pacchetto della richiesta come pacchetto di frammenti.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-113">Identifies this request packet as a Fragment packet.</span></span>

</dd> <dt>

<span data-ttu-id="d4dc2-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BIT-session-ID</span><span class="sxs-lookup"><span data-stu-id="d4dc2-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="d4dc2-115">GUID di stringa che identifica la sessione al server.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="d4dc2-116">Sostituire {GUID} con l'identificatore di sessione restituito dal server nell' [**ACK per**](ack-for-create-session.md) il pacchetto di risposta per la creazione della sessione.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> <dt>

<span data-ttu-id="d4dc2-117"><span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Content-Name</span><span class="sxs-lookup"><span data-stu-id="d4dc2-117"><span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Content-Name</span></span>
</dt> <dd>

<span data-ttu-id="d4dc2-118">Specificare questa intestazione solo con il frammento iniziale.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-118">Specify this header only with the initial fragment.</span></span> <span data-ttu-id="d4dc2-119">Sostituire filename con il nome del file locale dal processo.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-119">Replace filename with the name of the local file name from the job.</span></span> <span data-ttu-id="d4dc2-120">Il nome non include il percorso.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-120">The name does not include the path.</span></span>

</dd> <dt>

<span data-ttu-id="d4dc2-121"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Lunghezza del contenuto</span><span class="sxs-lookup"><span data-stu-id="d4dc2-121"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="d4dc2-122">Sostituire length con il numero di byte inviati nel corpo del frammento.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-122">Replace length with the number of bytes sent in the fragment body.</span></span>

</dd> <dt>

<span data-ttu-id="d4dc2-123"><span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Intervallo di contenuto</span><span class="sxs-lookup"><span data-stu-id="d4dc2-123"><span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Content-Range</span></span>
</dt> <dd>

<span data-ttu-id="d4dc2-124">Indica al server dove applicare l'intervallo nel file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-124">Tells the server where to apply the range in the destination file.</span></span> <span data-ttu-id="d4dc2-125">Sostituire Range con gli offset di inizio e di fine dell'intervallo nel file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-125">Replace range with the start and end offsets of the range in the destination file.</span></span> <span data-ttu-id="d4dc2-126">Gli offset sono in base zero.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-126">The offsets are zero-based.</span></span> <span data-ttu-id="d4dc2-127">Se l'intervallo specificato si sovrappone a un intervallo esistente, BITS scrive solo la parte non sovrapposta dell'intervallo; BITS non sovrascrive il contenuto esistente.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-127">If the given range overlaps an existing range, BITS writes only the non-overlapping portion of the range; BITS does not overwrite existing content.</span></span> <span data-ttu-id="d4dc2-128">Se, ad esempio, il primo pacchetto contiene l'intervallo compreso tra 0 e 100 e il secondo pacchetto contiene l'intervallo da 50 a 150, BITS scrive solo i byte da 101 a 150 dal secondo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-128">For example, if the first packet contained the range 0 through 100 and the second packet contained the range 50 through 150, BITS writes only bytes 101 through 150 from the second packet.</span></span> <span data-ttu-id="d4dc2-129">Sostituire Total-length con il numero totale di byte nel file.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-129">Replace total-length with the total number of bytes in the file.</span></span>

</dd> <dt>

<span data-ttu-id="d4dc2-130"><span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Codifica del contenuto</span><span class="sxs-lookup"><span data-stu-id="d4dc2-130"><span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Content-Encoding</span></span>
</dt> <dd>

<span data-ttu-id="d4dc2-131">Sostituire la codifica con il tipo di codifica usato dal client per il frammento.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-131">Replace encoding with the type of encoding the client uses on the fragment.</span></span> <span data-ttu-id="d4dc2-132">Il client deve usare la codifica identificata dal server nell'intestazione Accept-Encoding dell'ACK per il pacchetto di risposta di [**creazione-sessione**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="d4dc2-132">The client must use the encoding that the server identifies in the Accept-Encoding header of the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span> <span data-ttu-id="d4dc2-133">Il server usa il tipo di codifica per decodificare il frammento.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-133">The server uses the encoding type to decode the fragment.</span></span> <span data-ttu-id="d4dc2-134">Tutti i frammenti devono specificare la stessa codifica.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-134">All fragments must specify the same encoding.</span></span>

<span data-ttu-id="d4dc2-135">Non inviare questa intestazione se il tipo di codifica è Identity.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-135">Do not send this header if the encoding type is Identity.</span></span> <span data-ttu-id="d4dc2-136">Il server BITS supporta solo la codifica Identity.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-136">The BITS server supports only Identity encoding.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4dc2-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4dc2-137">Remarks</span></span>

<span data-ttu-id="d4dc2-138">Il frammento è un intervallo di byte inviati nel corpo del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-138">The fragment is a range of bytes sent in the body of the packet.</span></span> <span data-ttu-id="d4dc2-139">Il client invia i frammenti in ordine sequenziale a partire dall'offset zero. il server non tiene traccia degli intervalli non contigui.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-139">The client sends the fragments in sequential order starting with offset zero; the server does not keep track of non-contiguous ranges.</span></span> <span data-ttu-id="d4dc2-140">Se il client invia intervalli non contigui, il server restituisce un codice restituito HTTP 416 (Range-not-Impossibile attenersi all') nell'ACK per la risposta del [**frammento**](ack-for-fragment.md) .</span><span class="sxs-lookup"><span data-stu-id="d4dc2-140">If the client sends non-contiguous ranges, the server returns an HTTP 416 (range-not-satisfiable) return code in the [**Ack for Fragment**](ack-for-fragment.md) response.</span></span>

<span data-ttu-id="d4dc2-141">Le intestazioni Content-*xxxx* sono intestazioni HTTP 1,1 standard.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-141">The Content-*xxxx* headers are standard HTTP 1.1 headers.</span></span> <span data-ttu-id="d4dc2-142">Per ulteriori informazioni sulle intestazioni Content-*xxxx* , vedere la specifica [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) .</span><span class="sxs-lookup"><span data-stu-id="d4dc2-142">For more details on the Content-*xxxx* headers, see the [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) specification.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4dc2-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4dc2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4dc2-144">**ACK per il frammento**</span><span class="sxs-lookup"><span data-stu-id="d4dc2-144">**Ack for Fragment**</span></span>](ack-for-fragment.md)
</dt> <dt>

[<span data-ttu-id="d4dc2-145">**Chiudi sessione**</span><span class="sxs-lookup"><span data-stu-id="d4dc2-145">**Close-Session**</span></span>](close-session.md)
</dt> <dt>

[<span data-ttu-id="d4dc2-146">**Creazione sessione**</span><span class="sxs-lookup"><span data-stu-id="d4dc2-146">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




