---
description: Specifica il livello di qualità desiderato per la codifica vbr (variable-bit rate) basata sulla qualità (1 passaggio) dei flussi audio.
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: MFPKEY_DESIRED_VBRQUALITY proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f52ab8cc791a5309b5df6537d133bce68e49d66a15ab79c12beeb7411cece8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939945"
---
# <a name="mfpkey_desired_vbrquality-property"></a>Proprietà MFPKEY \_ DESIRED \_ VBRQUALITY

Specifica il livello di qualità desiderato per la codifica vbr (variable-bit rate) basata sulla qualità (1 passaggio) dei flussi audio.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

**VT \_ UI4**

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Questo valore può essere compreso tra 0 e 100, dove 100 è la qualità massima. Il valore 0 indica che il metodo di codifica VBR basato sulla qualità non deve essere usato.

Per enumerare le modalità VBR che soddisfano un determinato requisito di qualità, impostare le proprietà del codificatore seguenti.

-   Impostare [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) su **VARIANT \_ TRUE.**
-   Impostare [**MFPKEY \_ CONSTRAIN \_ ENUMERATED \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) su **VARIANT \_ TRUE.**
-   Impostare **MFPKEY \_ DESIRED \_ VBRQUALITY** sulla qualità desiderata. Per le modalità senza perdita di dati, impostare la qualità desiderata su 100.

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

 

 
