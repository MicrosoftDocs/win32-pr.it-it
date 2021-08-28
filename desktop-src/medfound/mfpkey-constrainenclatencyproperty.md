---
description: Specifica se il codificatore è vincolato da un requisito di latenza massima.
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: MFPKEY_CONSTRAINENCLATENCY proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172b92b0b4d39602f0535b8bf1ef4456a896972e56c6da10f6585e5221fa7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113421"
---
# <a name="mfpkey_constrainenclatency-property"></a>Proprietà MFPKEY \_ CONSTRAINENCLATENCY

Specifica se il codificatore è vincolato da un requisito di latenza massima.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

**VT \_ BOOL**

## <a name="default-value"></a>Valore predefinito

**VARIANT \_ FALSE**

## <a name="remarks"></a>Commenti

Se si lascia questa proprietà sul valore predefinito **VARIANT \_ FALSE,** il codificatore enumera un set predefinito di modalità con circa 2000 millisecondi di latenza del codificatore. Se si imposta questa proprietà su **VARIANT \_ TRUE,** è necessario specificare anche una latenza massima del codificatore impostando la proprietà [**MFPKEY \_ MAXENCLATENCYMS.**](mfpkey-maxenclatencymsproperty.md) In tal caso, il codificatore crea modalità che soddisfano il requisito di latenza ed enumera solo tali modalità. Il codificatore garantisce un esempio di output non appena il codificatore ha ricevuto l'input per un periodo di tempo uguale a **MFPKEY \_ MAXENCLATENCYMS.**

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

 

 
