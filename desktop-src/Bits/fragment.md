---
title: Frammento
description: Usare il pacchetto Fragment per inviare un frammento del file di caricamento al server.
ms.assetid: d6df7e47-a240-4be2-a9c4-24a13e622861
keywords:
- FRAMMENTO BITS
topic_type:
- apiref
api_name:
- Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613acaabc017b9e673d2cba6a64f84db054a4cdc0d73a0639fcf8455edff8298
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528831"
---
# <a name="fragment"></a>Frammento

Usare il **pacchetto Fragment** per inviare un frammento del file di caricamento al server.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Fragment
BITS-Session-Id: {guid}
Content-Name: filename
Content-Length: length
Content-Range: Bytes range/total-length
Content-Encoding: encoding
```

## <a name="headers"></a>Intestazioni

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

Verbo specifico di BITS che identifica questo pacchetto per il server BITS.

Sostituire remote-URL con l'URI assoluto o relativo. In genere, sostituire remote-URL con il nome file remoto del processo. Per considerazioni sul bilanciamento del carico di rete, vedere l'intestazione BITS-Host-Id nel [**pacchetto Create-Session.**](create-session.md)

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>TIPO DI PACCHETTO BITS
</dt> <dd>

Identifica questo pacchetto di richiesta come pacchetto frammento.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id
</dt> <dd>

GUID stringa che identifica la sessione nel server. Sostituire {guid} con l'identificatore di sessione restituito dal server nel pacchetto di risposta [**Ack for Create-Session.**](ack-for-create-session.md)

</dd> <dt>

<span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Nome contenuto
</dt> <dd>

Specificare questa intestazione solo con il frammento iniziale. Sostituire filename con il nome del file locale del processo. Il nome non include il percorso.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Lunghezza contenuto
</dt> <dd>

Sostituire length con il numero di byte inviati nel corpo del frammento.

</dd> <dt>

<span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Intervallo di contenuto
</dt> <dd>

Indica al server dove applicare l'intervallo nel file di destinazione. Sostituire range con gli offset iniziale e finale dell'intervallo nel file di destinazione. Gli offset sono in base zero. Se l'intervallo specificato si sovrappone a un intervallo esistente, BITS scrive solo la parte non sovrapposta dell'intervallo; BITS non sovrascrive il contenuto esistente. Ad esempio, se il primo pacchetto contiene l'intervallo da 0 a 100 e il secondo pacchetto contiene l'intervallo da 50 a 150, BITS scrive solo i byte da 101 a 150 dal secondo pacchetto. Sostituire total-length con il numero totale di byte nel file.

</dd> <dt>

<span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Codifica del contenuto
</dt> <dd>

Sostituire encoding con il tipo di codifica utilizzato dal client nel frammento. Il client deve usare la codifica identificata dal server nell'intestazione Accept-Encoding del pacchetto di risposta [**Ack for Create-Session.**](ack-for-create-session.md) Il server usa il tipo di codifica per decodificare il frammento. Tutti i frammenti devono specificare la stessa codifica.

Non inviare questa intestazione se il tipo di codifica è Identity. Il server BITS supporta solo la codifica Identity.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il frammento è un intervallo di byte inviati nel corpo del pacchetto. Il client invia i frammenti in ordine sequenziale a partire dall'offset zero. il server non tiene traccia degli intervalli non contigui. Se il client invia intervalli non contigui, il server restituisce un codice restituito HTTP 416 (range-not-satisfiable) nella risposta [**Ack for Fragment.**](ack-for-fragment.md)

Le intestazioni Content-*xxxx* sono intestazioni HTTP 1.1 standard. Per altri dettagli sulle intestazioni Content-*xxxx,* vedere la [specifica RFC 2616.](https://www.ietf.org/rfc/rfc2616.txt)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Ack for Fragment**](ack-for-fragment.md)
</dt> <dt>

[**Chiudi sessione**](close-session.md)
</dt> <dt>

[**Create-Session**](create-session.md)
</dt> </dl>

 

 




