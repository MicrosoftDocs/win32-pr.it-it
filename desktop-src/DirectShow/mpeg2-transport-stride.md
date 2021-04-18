---
description: La \_ struttura dello stride del trasporto MPEG2 \_ descrive il formato dei pacchetti di flusso di trasporto MPEG-2.
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: Struttura MPEG2_TRANSPORT_STRIDE (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MPEG2_TRANSPORT_STRIDE
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 4a0cdc21bdd8c320728da0c0af8c0af023de68eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325167"
---
# <a name="mpeg2_transport_stride-structure"></a>\_ \_ Struttura stride trasporto MPEG2

La `MPEG2_TRANSPORT_STRIDE` struttura descrive il formato dei pacchetti MPEG-2 Transport Stream (TS). Questa struttura consente flussi di trasporto in cui i pacchetti di trasporto da 188 byte non sono contigui. Ai fini di questa documentazione, questi pacchetti sono detti *pacchetti stride*.

I pacchetti stride sono identificati dal seguente tipo di supporto:



|             |                                        |
|-------------|----------------------------------------|
| Tipo principale  | \_Flusso MEDIATYPE                      |
| Subtype     | \_ \_ Stride trasporto MPEG2 \_ MEDIASUBTYPE |
| Tipo di formato | FORMATO \_ None                           |



 

Il formato del blocco (**pbFormat**) è facoltativo. Se il blocco di formato è incluso, deve iniziare con una struttura dello **\_ \_ stride del trasporto MPEG2** . Questa struttura definisce il layout del pacchetto di trasporto all'interno del pacchetto stride. Se il blocco di formato è **null**, si presuppone che i pacchetti usino un set di valori predefiniti. per informazioni dettagliate, vedere la sezione Osservazioni.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a>Members

<dl> <dt>

**dwOffset**
</dt> <dd>

Specifica l'offset, in byte, dall'inizio del pacchetto al primo byte del pacchetto di trasporto incorporato. Il valore deve essere compreso tra zero e `(dwStride - dwPacketLength)` , inclusi.

</dd> <dt>

**dwPacketLength**
</dt> <dd>

Specifica la lunghezza, in byte, del pacchetto di trasporto incorporato. Per i pacchetti di trasporto MPEG-2 standard, il valore deve essere pari a 188 byte.

</dd> <dt>

**dwStride**
</dt> <dd>

Specifica la lunghezza in byte dell'intero pacchetto stride. Il valore deve essere almeno `(dwOffset + dwPacketLength)` .

</dd> </dl>

## <a name="remarks"></a>Commenti

Il diagramma seguente illustra le relazioni tra i membri della struttura.

![pacchetto MPEG-2 stride](images/mpeg2-stride-packet.png)

I buffer di input che contengono pacchetti stride in multiplex presentano alcune restrizioni:

-   I pacchetti stride devono essere compressi in modo contiguo all'interno del buffer.
-   Nessun byte può precedere il primo pacchetto stride o seguire l'ultimo pacchetto stride.
-   Un numero integrale di pacchetti stride deve rientrare nel buffer; ovvero la lunghezza del buffer% dwStride è uguale a zero.

Non esiste alcuna restrizione per il numero di pacchetti stride per buffer.

Se il tipo di supporto non contiene un blocco di formato (**pbFormat** è **null**), vengono usati i valori predefiniti seguenti:

-   **dwOffset**: 0
-   **dwPacketLength**: 188
-   **dwStride**: 188

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Bdatypes. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture DirectShow](directshow-structures.md)
</dt> <dt>

[Tipi di supporti MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 




