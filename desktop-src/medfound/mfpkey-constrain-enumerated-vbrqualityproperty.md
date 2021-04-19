---
description: Specifica se le modalità enumerate dal codificatore sono limeted a quelle che soddisfano un requisito di qualità fornito da MFPKEY \_ desired \_ VBRQUALITY.
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: Proprietà MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9e63ab955bbe7726ab67bdab057fe2d397942
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333538"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a>MFPKEY \_ vincolata \_ \_ Proprietà VBRQUALITY enumerata

Specifica se le modalità enumerate dal codificatore sono limeted a quelle che soddisfano un requisito di qualità fornito da [**MFPKEY \_ desired \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md).

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**\_bool VT**

## <a name="default-value"></a>Valore predefinito

**VARIANTE \_ false**

## <a name="remarks"></a>Commenti

Per enumerare le modalità VBR che soddisfano un determinato requisito di qualità, impostare le proprietà del codificatore seguenti.

-   Impostare [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) su **Variant \_ true**.
-   Impostare **MFPKEY \_ vincolate \_ Enumerated \_ VBRQUALITY** su **Variant \_ true**.
-   Impostare [**MFPKEY \_ desired \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) sulla qualità desiderata. Per le modalità Lossless, impostare la qualità desiderata su 100.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista o Windows 7<br/>                                                   |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
