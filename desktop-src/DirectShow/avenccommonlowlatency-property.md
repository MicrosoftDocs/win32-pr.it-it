---
description: Specifica se il flusso di output deve essere strutturato in modo che il flusso codificato abbia una latenza di decodifica bassa.
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: Proprietà AVEncCommonLowLatency (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a13dd59b7aa09f6b0f2aa6a4c31031d090d41c85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225481"
---
# <a name="avenccommonlowlatency-property"></a>Proprietà AVEncCommonLowLatency

Specifica se il flusso di output deve essere strutturato in modo che il flusso codificato abbia una latenza di decodifica bassa.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncCommonLowLatency**

## <a name="remarks"></a>Commenti

La latenza di decodifica viene definita come la quantità di dati che il decodificatore deve memorizzare nel buffer. Se ad esempio si imposta questa proprietà su **Variant \_ true** in un codificatore video MPEG, vengono limitati i tipi di strutture GOP che il codificatore può utilizzare.

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

 

 




