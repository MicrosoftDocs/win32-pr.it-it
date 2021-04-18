---
description: Specifica il flag di informazioni di produzione audio in un flusso audio Dolby Digital. Questa proprietà si applica ai codificatori audio Dolby Digital.
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: Proprietà AVEncDDProductionInfoExists (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5069c8d30f0266b0727f735ede822be491c4a4a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304227"
---
# <a name="avencddproductioninfoexists-property"></a>Proprietà AVEncDDProductionInfoExists

Specifica il flag di informazioni di produzione audio in un flusso audio Dolby Digital. Questa proprietà si applica ai codificatori audio Dolby Digital.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncDDProductionInfoExists**

## <a name="remarks"></a>Commenti

Se il valore è **Variant \_ true**, le impostazioni del livello di combinazione e del tipo di chat sono valide. Specificare queste impostazioni con le proprietà [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) e [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) .

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

 

 




