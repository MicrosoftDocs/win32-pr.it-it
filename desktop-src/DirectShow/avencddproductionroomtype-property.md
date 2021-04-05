---
description: Specifica il tipo di stanza per un flusso audio Dolby Digital. Questa proprietà si applica ai codificatori audio Dolby Digital.
ms.assetid: d19b6b9d-9606-48a8-ac8e-cdbf15588a8f
title: Proprietà AVEncDDProductionRoomType (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc2eed0bb491fc982a5102507e5b55bf610880a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125199"
---
# <a name="avencddproductionroomtype-property"></a>Proprietà AVEncDDProductionRoomType

Specifica il tipo di stanza per un flusso audio Dolby Digital. Questa proprietà si applica ai codificatori audio Dolby Digital.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncDDProductionRoomType**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro dell'enumerazione [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) .

## <a name="remarks"></a>Commenti

Il *tipo di chat room* si riferisce alle dimensioni della stanza utilizzata durante la produzione. Se si imposta questa proprietà, impostare la proprietà [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) su **true**.

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

 

