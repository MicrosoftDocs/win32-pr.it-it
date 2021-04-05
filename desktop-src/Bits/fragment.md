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
# <a name="fragment"></a>Frammento

Usare il pacchetto di **frammenti** per inviare un frammento del file di caricamento al server.

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

<span id="BITS_POST"></span><span id="bits_post"></span>\_post BITS
</dt> <dd>

Verbo specifico di BITS che identifica il pacchetto nel server BITS.

Sostituire Remote-URL con l'URI assoluto o relativo. In genere, sostituire Remote-URL con il nome file remoto del processo. Per considerazioni sul bilanciamento del carico di rete, vedere l'intestazione BITS-host-ID nel pacchetto di [**creazione della sessione**](create-session.md) .

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo-pacchetto
</dt> <dd>

Identifica il pacchetto della richiesta come pacchetto di frammenti.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BIT-session-ID
</dt> <dd>

GUID di stringa che identifica la sessione al server. Sostituire {GUID} con l'identificatore di sessione restituito dal server nell' [**ACK per**](ack-for-create-session.md) il pacchetto di risposta per la creazione della sessione.

</dd> <dt>

<span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Content-Name
</dt> <dd>

Specificare questa intestazione solo con il frammento iniziale. Sostituire filename con il nome del file locale dal processo. Il nome non include il percorso.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Lunghezza del contenuto
</dt> <dd>

Sostituire length con il numero di byte inviati nel corpo del frammento.

</dd> <dt>

<span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Intervallo di contenuto
</dt> <dd>

Indica al server dove applicare l'intervallo nel file di destinazione. Sostituire Range con gli offset di inizio e di fine dell'intervallo nel file di destinazione. Gli offset sono in base zero. Se l'intervallo specificato si sovrappone a un intervallo esistente, BITS scrive solo la parte non sovrapposta dell'intervallo; BITS non sovrascrive il contenuto esistente. Se, ad esempio, il primo pacchetto contiene l'intervallo compreso tra 0 e 100 e il secondo pacchetto contiene l'intervallo da 50 a 150, BITS scrive solo i byte da 101 a 150 dal secondo pacchetto. Sostituire Total-length con il numero totale di byte nel file.

</dd> <dt>

<span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Codifica del contenuto
</dt> <dd>

Sostituire la codifica con il tipo di codifica usato dal client per il frammento. Il client deve usare la codifica identificata dal server nell'intestazione Accept-Encoding dell'ACK per il pacchetto di risposta di [**creazione-sessione**](ack-for-create-session.md) . Il server usa il tipo di codifica per decodificare il frammento. Tutti i frammenti devono specificare la stessa codifica.

Non inviare questa intestazione se il tipo di codifica è Identity. Il server BITS supporta solo la codifica Identity.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il frammento è un intervallo di byte inviati nel corpo del pacchetto. Il client invia i frammenti in ordine sequenziale a partire dall'offset zero. il server non tiene traccia degli intervalli non contigui. Se il client invia intervalli non contigui, il server restituisce un codice restituito HTTP 416 (Range-not-Impossibile attenersi all') nell'ACK per la risposta del [**frammento**](ack-for-fragment.md) .

Le intestazioni Content-*xxxx* sono intestazioni HTTP 1,1 standard. Per ulteriori informazioni sulle intestazioni Content-*xxxx* , vedere la specifica [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ACK per il frammento**](ack-for-fragment.md)
</dt> <dt>

[**Chiudi sessione**](close-session.md)
</dt> <dt>

[**Creazione sessione**](create-session.md)
</dt> </dl>

 

 




