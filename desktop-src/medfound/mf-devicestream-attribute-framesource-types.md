---
description: Rappresenta il tipo di origine del frame.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce2e7f90f4e5f23e99bac8e532455fac1309cc0e20177c5800d85f4580e20a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013191"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a>Attributo \_ DEVICESTREAM \_ MF \_ - ATTRIBUTO FRAMESOURCE \_ TYPES

Rappresenta il tipo di origine del frame.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo valore di questo attributo deve essere una maschera di bit di uno o più valori [**dell'enumerazione MFFrameSourceTypes.**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) Per supportare la compatibilità con le versioni precedenti, quando questo attributo non è definito per un tipo di supporto, si presuppone che abbia il valore **MFFrameSourceTypes::Color**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1607 \[\]<br/>                          |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




