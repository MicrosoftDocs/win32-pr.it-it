---
description: Specifica se il codificatore è vincolato da un requisito di latenza massima.
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: Proprietà MFPKEY_CONSTRAINENCLATENCY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f880006bf2aba04196547a79e74f94a7210edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310645"
---
# <a name="mfpkey_constrainenclatency-property"></a>\_Proprietà CONSTRAINENCLATENCY di MFPKEY

Specifica se il codificatore è vincolato da un requisito di latenza massima.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**\_bool VT**

## <a name="default-value"></a>Valore predefinito

**VARIANTE \_ false**

## <a name="remarks"></a>Commenti

Se si lascia questa proprietà sul valore predefinito **Variant \_ false**, il codificatore enumera un set predefinito di modalità con circa 2000 millisecondi di latenza del codificatore. Se si imposta questa proprietà su **Variant \_ true**, è necessario specificare anche una latenza massima del codificatore impostando la proprietà [**MFPKEY \_ MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) . In tal caso, il codificatore crea le modalità che soddisfano il requisito di latenza ed enumera solo le modalità. Il codificatore garantisce un campione di output non appena il codificatore ha ricevuto l'input per un periodo di tempo uguale a **MFPKEY \_ MAXENCLATENCYMS**.

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

 

 
