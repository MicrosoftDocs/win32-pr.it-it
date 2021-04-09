---
description: Specifica il compromesso tra movimento e immagini fisse. Questa proprietà si applica solo alla modalità di controllo della velocità in bit costante (CBR).
ms.assetid: e657e971-4624-4c87-ad51-6bf0cd1f9246
title: Proprietà AVEncVideoCBRMotionTradeoff (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b746559f48858f995cbd87184a2f13ada33db7c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965785"
---
# <a name="avencvideocbrmotiontradeoff-property"></a>Proprietà AVEncVideoCBRMotionTradeoff

Specifica il compromesso tra movimento e immagini fisse. Questa proprietà si applica solo alla modalità di controllo della velocità in bit costante (CBR).

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoCBRMotionTradeoff**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà presenta l'intervallo seguente.



| Valore | Descrizione               |
|-------|---------------------------|
| 0     | Ottimizza per immagini ancora |
| 100   | Ottimizza per il movimento.      |



 

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

 

 




