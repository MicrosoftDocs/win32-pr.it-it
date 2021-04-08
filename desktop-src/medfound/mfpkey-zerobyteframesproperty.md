---
description: Specifica il numero di fotogrammi video ignorati perché sono duplicati dei frame precedenti.
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: Proprietà MFPKEY_ZEROBYTEFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffcf29d099b3a3fb27a307e970af7af1a5c3d58b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880077"
---
# <a name="mfpkey_zerobyteframes-property"></a>\_Proprietà ZEROBYTEFRAMES di MFPKEY

Specifica il numero di fotogrammi video ignorati perché sono duplicati dei frame precedenti.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCZeroByteFrames

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

Questo valore non viene sottratto dal numero totale di frame passati ([MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md)) durante il calcolo del numero di frame codificati ([MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md)).

È possibile arrestare il codec ignorando i frame duplicati impostando [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) su Variant \_ true.

È possibile ottenere questo valore al termine del passaggio degli esempi.

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

 

 




