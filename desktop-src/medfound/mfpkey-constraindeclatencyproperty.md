---
description: Specifica se il codificatore è vincolato da un requisito di latenza del decodificatore massimo.
ms.assetid: 054e445e-fc71-4d4f-9e9f-f5ff71f0b4ee
title: Proprietà MFPKEY_CONSTRAINDECLATENCY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343bcc9bd365b9f1321b200baa203fc27784594c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310646"
---
# <a name="mfpkey_constraindeclatency-property"></a>\_Proprietà CONSTRAINDECLATENCY di MFPKEY

Specifica se il codificatore è vincolato da un requisito di latenza del decodificatore massimo.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**\_bool VT**

## <a name="default-value"></a>Valore predefinito

**VARIANTE \_ false**

## <a name="remarks"></a>Commenti

Se si lascia questa proprietà sul valore predefinito **Variant \_ false**, il codificatore enumera un set predefinito di modalità con circa 1500 millisecondi di latenza del decodificatore. Se si imposta questa proprietà su **Variant \_ true**, è necessario specificare anche una latenza di decodificazione massima impostando la proprietà [**MFPKEY \_ MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) . In tal caso, il codificatore crea le modalità che soddisfano il requisito di latenza ed enumera solo le modalità. Il codificatore garantisce che i requisiti di preroll (dimensione del buffer del decodificatore) siano minori o uguali a **MFPKEY \_ MAXDECLATENCYMS**.

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

 

 
