---
description: Specifica il numero di fotogrammi video codificati dal codec.
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: MFPKEY_CODEDFRAMES proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e836f2177311a2ffc13065187a1affce93c6dbe74ff9ff4c99ef78a6f492b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954731"
---
# <a name="mfpkey_codedframes-property"></a>Proprietà CODEDFRAMES MFPKEY \_

Specifica il numero di fotogrammi video codificati dal codec.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCCodedFrames

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

Questo valore è uguale a [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) meno eventuali fotogrammi eliminati a causa di vincoli di velocità in bit. È possibile ottenere questo valore dopo aver completato il passaggio degli esempi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




