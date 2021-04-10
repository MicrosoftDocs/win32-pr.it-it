---
description: Specifica i dati del controllo sezionamento.
ms.assetid: ae3399e9-b78c-473d-8ed5-e570dfb676aa
title: Struttura DXVA_Slice_HEVC_Short (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Slice_HEVC_Short
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 0d0f88e1534ef3d901023ebdee8ce9c36a8c2cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049307"
---
# <a name="dxva_slice_hevc_short-structure"></a>DXVA \_ Slice \_ HEVC \_ breve struttura

Specifica i dati del controllo sezionamento.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DXVA_Slice_HEVC_Short {
  UINT   BSNALunitDataLocation;
  UINT   SliceBytesInBuffer;
  USHORT wBadSliceChopping;
} DXVA_Slice_HEVC_Short, *LPDXVA_Slice_HEVC_Short;
```



## <a name="members"></a>Members

<dl> <dt>

**BSNALunitDataLocation**
</dt> <dd>

Specifica la posizione dell'unità NAL.

</dd> <dt>

**SliceBytesInBuffer**
</dt> <dd>

Il numero di byte nel buffer di dati Bitstream associato a questa struttura di dati del controllo Slice.

</dd> <dt>

**wBadSliceChopping**
</dt> <dd>

Se si usa l'analisi Bitstream fuori host, questo valore indica il sezionamento della sezione non valida e contiene uno dei valori seguenti:



| Requisito | Valore |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valore | Descrizione                                                                                                                                                                                                                                             |
| 0     | Tutti i bit per la sezione si trovano all'interno del buffer dei dati Bitstream corrispondente.                                                                                                                                                                      |
| 1     | Il buffer di dati Bitstream contiene l'inizio della sezione, ma non l'intera sezione, perché il buffer è pieno.                                                                                                                                        |
| 2     | Il buffer di dati Bitstream contiene la fine della sezione. Non contiene l'inizio della sezione, perché l'inizio della sezione si trova nel buffer dei dati Bitstream precedente.                                                                  |
| 3     | Il buffer di dati Bitstream non contiene l'inizio della sezione perché l'inizio della sezione si trova nel buffer dei dati Bitstream precedente e non contiene la fine della sezione perché anche il buffer dei dati Bitstream corrente è pieno. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

**DXVA \_ Slice \_ HEVC \_ short** contiene i dati di controllo delle sezioni che vengono passati all'acceleratore hardware dal decodificatore software host.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                      |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture di Media Foundation](media-foundation-structures.md)
</dt> </dl>

 

 




