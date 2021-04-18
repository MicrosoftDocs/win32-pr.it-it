---
description: Specifica il livello di qualità desiderato per la codifica con velocità in bit (VBR) basata sulla qualità (1-pass) dei flussi audio.
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: Proprietà MFPKEY_DESIRED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa0f2cf86db076fa211f9c850db15de730a3a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310635"
---
# <a name="mfpkey_desired_vbrquality-property"></a>MFPKEY \_ \_ Proprietà VBRQUALITY desiderata

Specifica il livello di qualità desiderato per la codifica con velocità in bit (VBR) basata sulla qualità (1-pass) dei flussi audio.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**\_UI4 VT**

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Questo valore può essere compreso tra 0 e 100, dove 100 è la qualità massima. Il valore 0 indica che non è necessario utilizzare il metodo di codifica VBR basato sulla qualità.

Per enumerare le modalità VBR che soddisfano un determinato requisito di qualità, impostare le proprietà del codificatore seguenti.

-   Impostare [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) su **Variant \_ true**.
-   Impostare [**MFPKEY \_ vincolate \_ Enumerated \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) su **Variant \_ true**.
-   Impostare **MFPKEY \_ desired \_ VBRQUALITY** sulla qualità desiderata. Per le modalità Lossless, impostare la qualità desiderata su 100.

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

 

 
