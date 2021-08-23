---
description: Specifica la modalità di utilizzo delle informazioni sui colori nelle operazioni di ricerca del movimento.
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: MFPKEY_MOTIONSEARCHLEVEL proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b53c6bf8f94b2b9817249d96cffbfa0da251dbbcb0545c141230de90f80485af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555411"
---
# <a name="mfpkey_motionsearchlevel-property"></a>Proprietà MFPKEY \_ MOTIONSEARCHLEVEL

Specifica la modalità di utilizzo delle informazioni sui colori nelle operazioni di ricerca del movimento.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCMotionSearchLevel

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Questa proprietà può essere impostata su uno dei valori seguenti.



| Valore | Informazioni video usate                           |
|-------|--------------------------------------------------|
| 0     | Solo luminanza.                                       |
| 1     | Luma con chroma integer più vicino.                |
| 2     | Luminanza con crominanza vera.                           |
| -1    | Macroblock-adaptive con croma vera.            |
| -2    | Macroblock-adaptive con la croma dell'intero più vicino. |



 

Per impostazione predefinita, il codec esegue la ricerca del movimento solo nel canale luma. L'inclusione di informazioni sulla croma nella stima del movimento può migliorare significativamente la qualità del video codificato. La ricerca del movimento con luma e la vera chroma offre la migliore qualità video, ma al costo delle prestazioni più elevato. Le due modalità dinamiche (-1 e -2) e la modalità luma con la modalità chroma integer più vicina offriranno compromessi ragionevoli tra qualità e prestazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




