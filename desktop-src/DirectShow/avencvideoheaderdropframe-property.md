---
description: Specifica il valore del flag drop-frame nell'intestazione Group of Pictures (GOP).
ms.assetid: 37f8f5f6-ddcb-44ab-a727-632b78e6f599
title: Proprietà AVEncVideoHeaderDropFrame (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 741911c400256f02f917e143dbc83bfa0eca04bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876966"
---
# <a name="avencvideoheaderdropframe-property"></a>Proprietà AVEncVideoHeaderDropFrame

Specifica il valore del flag drop-frame nell'intestazione Group of Pictures (GOP).

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoHeaderDropFrame**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà può essere 0 o 1.

## <a name="remarks"></a>Commenti

La modalità drop frame viene usata nel video NTSC per correggere la discrepanza tra il video, ovvero 29,97 fotogrammi al secondo e la visualizzazione del codice temporale, ovvero 30 fotogrammi al secondo. In modalità di rilascio frame, i numeri di frame 00 e 01 vengono ignorati all'inizio di ogni minuto, ad eccezione dei minuti che sono persino multipli di dieci (00, 10, 20 e così via). Vengono eliminati solo i numeri di frame nel codice temporale; non vengono eliminati frame effettivi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP di Windows 2000 Professional \[ desktop apps \|\]<br/>                     |
| Server minimo supportato<br/> | App desktop di Windows 2000 Server \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




