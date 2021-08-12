---
description: Specifica la velocità in bit media, in bit al secondo, per un codificatore configurato per l'uso della codifica VBR mediamente controllabile.
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: MFPKEY_DYN_VBR_RAVG proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48ee3d3a9b9a60b664041b9c6f84c38b8da9ceef87f73177f2ace792cf043992
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242613"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a>Proprietà MFPKEY \_ DYN \_ VBR \_ RAVG

Specifica la velocità in bit media, in bit al secondo, per un codificatore configurato per l'uso della codifica VBR mediamente controllabile.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**VT \_ I4**

## <a name="remarks"></a>Commenti

Se le [**proprietà MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) e [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) sono entrambe impostate su **VARIANT \_ TRUE,** il codificatore usa la codifica VBR con controllo medio. In tal caso, il codificatore si configura in base al valore di questa proprietà e alla proprietà [**MFPKEY \_ DYN \_ VBR \_ BAVG.**](mfpkey-dyn-vbr-bavgproperty.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
