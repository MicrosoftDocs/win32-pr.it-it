---
description: Specifica la finestra del buffer, in millisecondi, per un codificatore configurato per l'uso della codifica VBR controllabile mediamente.
ms.assetid: ce330ce0-4bda-4340-b21c-63a8b9168cf4
title: MFPKEY_DYN_VBR_BAVG proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77ba4d3f3d7a5587a7c8aa90771f58accd8a80864dd5a875c6c580eb9e29e01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738161"
---
# <a name="mfpkey_dyn_vbr_bavg-property"></a>Proprietà MFPKEY \_ DYN \_ VBR \_ BAVG

Specifica la finestra del buffer, in millisecondi, per un codificatore configurato per l'uso della codifica VBR controllabile mediamente.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

**VT \_ I4**

## <a name="remarks"></a>Commenti

Se le [**proprietà MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) e [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) sono entrambe impostate su **VARIANT \_ TRUE,** il codificatore usa la codifica VBR controllabile mediamente. In tal caso, il codificatore si configura in base al valore di questa proprietà e alla proprietà [**MFPKEY \_ DYN \_ VBR \_ RAVG.**](mfpkey-dyn-vbr-ravgproperty.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
