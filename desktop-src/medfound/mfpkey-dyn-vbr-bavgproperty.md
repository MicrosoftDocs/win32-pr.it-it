---
description: Specifica la finestra del buffer, in millisecondi, per un codificatore configurato per l'utilizzo della codifica VBR media controllabile.
ms.assetid: ce330ce0-4bda-4340-b21c-63a8b9168cf4
title: Proprietà MFPKEY_DYN_VBR_BAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e117c2852f660b015bcdd95224178730d2e2a1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310632"
---
# <a name="mfpkey_dyn_vbr_bavg-property"></a>MFPKEY \_ dyn \_ - \_ Proprietà BAVG VBR

Specifica la finestra del buffer, in millisecondi, per un codificatore configurato per l'utilizzo della codifica VBR media controllabile.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**VT \_ I4**

## <a name="remarks"></a>Commenti

Se le proprietà [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) e [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) sono entrambe impostate su **Variant \_ true**, il codificatore usa la codifica VBR media controllabile. In tal caso, il codificatore viene configurato in base al valore di questa proprietà e alla proprietà [**MFPKEY \_ dyn \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md) .

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

 

 
