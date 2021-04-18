---
description: Specifica il numero di fotogrammi video codificati dal codec.
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: Proprietà MFPKEY_CODEDFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708bb6c200701cdf48fa8407108be2161fdb4f61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314022"
---
# <a name="mfpkey_codedframes-property"></a>\_Proprietà CODEDFRAMES di MFPKEY

Specifica il numero di fotogrammi video codificati dal codec.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCCodedFrames

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

Questo valore è uguale a [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) meno tutti i frame eliminati a causa di vincoli di velocità in bit. È possibile ottenere questo valore al termine del passaggio degli esempi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




