---
description: Specifica se il codificatore usa la codifica VBR con controllo medio.
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: MFPKEY_AVGCONSTRAINED proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e7231cb3807be8f4467592ac0138a75ea277bdf8a13dfb3564d3572036e7ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874093"
---
# <a name="mfpkey_avgconstrained-property"></a>Proprietà MFPKEY \_ AVGCONSTRAINED

Specifica se il codificatore usa la codifica VBR con controllo medio.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**VT \_ BOOL**

## <a name="default-value"></a>Valore predefinito

**VARIANT \_ FALSE**

## <a name="remarks"></a>Commenti

Se questa proprietà e la [**proprietà MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) sono entrambe impostate su **VARIANT \_ TRUE,** il codificatore usa la codifica VBR con controllo medio. In tal caso, il codificatore si configura in base ai valori di [**MFPKEY \_ DYN \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) e [**MFPKEY \_ DYN \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md).

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

 

 
