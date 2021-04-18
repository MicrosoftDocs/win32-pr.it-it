---
description: Specifica se il codificatore usa la codifica VBR media controllabile.
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: Proprietà MFPKEY_AVGCONSTRAINED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0623fb4a73e3721f9079f2a1e5e330ecb466a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306753"
---
# <a name="mfpkey_avgconstrained-property"></a>\_Proprietà AVGCONSTRAINED di MFPKEY

Specifica se il codificatore usa la codifica VBR media controllabile.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**\_bool VT**

## <a name="default-value"></a>Valore predefinito

**VARIANTE \_ false**

## <a name="remarks"></a>Commenti

Se questa proprietà e la proprietà [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) sono entrambe impostate su **Variant \_ true**, il codificatore usa la codifica VBR media controllabile. In tal caso, il codificatore viene configurato in base ai valori di [**MFPKEY \_ dyn \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) e [**MFPKEY \_ dyn \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
