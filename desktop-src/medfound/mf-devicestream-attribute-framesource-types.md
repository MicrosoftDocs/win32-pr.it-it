---
description: Rappresenta il tipo di origine del frame.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: Attributo MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8823a828a81290fe3b039c8959d694c62331622f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309574"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a>\_Attributo di \_ \_ tipi origine frame dell'attributo MF DEVICESTREAM \_

Rappresenta il tipo di origine del frame.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo valore di questo attributo deve essere una maschera di maschera di uno o più valori dell'enumerazione [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) . Per supportare la compatibilità con le versioni precedenti, quando questo attributo non è definito per un tipo di supporto, si presuppone che il valore di **MFFrameSourceTypes:: color**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1607 \[\]<br/>                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




