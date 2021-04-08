---
description: Specifica il numero di campi da ignorare durante la codifica.
ms.assetid: 82f2a2c1-52ff-410d-b5da-b2419c0adfe3
title: Proprietà AVEncVideoNoOfFieldsToSkip (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708ef409fb907520d6a582599da2050a1353636c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876358"
---
# <a name="avencvideonooffieldstoskip-property"></a>Proprietà AVEncVideoNoOfFieldsToSkip

Specifica il numero di campi da ignorare durante la codifica.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt64** (**VT \_ UI8**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoNoOfFieldsToSkip**

## <a name="remarks"></a>Commenti

Per video progressivo, impostare questa proprietà su due volte il numero di frame da ignorare.

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

 

 




