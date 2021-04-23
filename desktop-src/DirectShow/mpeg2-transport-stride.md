---
description: La struttura MPEG2 \_ TRANSPORT STRIDE descrive il formato dei pacchetti \_ TS (Transport Stream) MPEG-2.
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: MPEG2_TRANSPORT_STRIDE struttura (Bdatypes.h)
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
ms.openlocfilehash: 5153f6f79c2807634149222a126a7256a65ffe8a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908489"
---
# <a name="mpeg2_transport_stride-structure"></a>Struttura STRIDE DEL TRASPORTO MPEG2 \_ \_

La `MPEG2_TRANSPORT_STRIDE` struttura descrive il formato dei pacchetti TS (Transport Stream) MPEG-2. Questa struttura consente flussi di trasporto in cui i pacchetti di trasporto a 188 byte non sono contigui. Ai fini di questa documentazione, tali pacchetti vengono definiti pacchetti *stride*.

I pacchetti Stride sono identificati dal tipo di supporto seguente:



| Label | Valore |
|-------------|----------------------------------------|
| Tipo principale  | Flusso \_ MEDIATYPE                      |
| Subtype     | MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE |
| Tipo di formato | FORMAT \_ None                           |



 

Il blocco di formato (**pbFormat**) è facoltativo. Se il blocco di formato è incluso, deve iniziare con una **struttura \_ MPEG2 TRANSPORT \_ STRIDE.** Questa struttura definisce il layout del pacchetto di trasporto all'interno del pacchetto stride. Se il blocco di formato **è NULL,** si presuppone che i pacchetti usino un set di valori predefiniti. Per informazioni dettagliate, vedere la sezione Osservazioni.

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

Specifica la lunghezza in byte del pacchetto di trasporto incorporato. Per i pacchetti di trasporto MPEG-2 standard, il valore deve essere 188 byte.

</dd> <dt>

**dwStride**
</dt> <dd>

Specifica la lunghezza in byte dell'intero pacchetto stride. Il valore deve essere almeno `(dwOffset + dwPacketLength)` .

</dd> </dl>

## <a name="remarks"></a>Commenti

Il diagramma seguente illustra le relazioni tra i membri della struttura.

![Pacchetto mpeg-2 stride](images/mpeg2-stride-packet.png)

I buffer di input che contengono pacchetti stride multiplexed hanno alcune restrizioni:

-   I pacchetti Stride devono essere imballati in modo contiguo all'interno del buffer.
-   Nessun byte può precedere il primo pacchetto stride o seguire l'ultimo pacchetto stride.
-   Un numero integrale di pacchetti stride deve essere contenuto nel buffer. in altri, la lunghezza del buffer % dwStride è uguale a zero.

Non esiste alcuna restrizione sul numero di pacchetti stride per buffer.

Se il tipo di supporto non contiene un blocco di formato (**pbFormat** è **NULL),** vengono usati i valori predefiniti seguenti:

-   **dwOffset**: 0
-   **dwPacketLength**: 188
-   **dwStride**: 188

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Bdatypes.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture DirectShow](directshow-structures.md)
</dt> <dt>

[Tipi di supporti MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 




