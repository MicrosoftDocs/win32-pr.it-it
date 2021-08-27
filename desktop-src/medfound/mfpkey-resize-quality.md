---
description: Specifica se usare un algoritmo che produce video di qualità superiore o un algoritmo più veloce.
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: MFPKEY_RESIZE_QUALITY proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8aeb59935c8fc3462b713967ed2b14a0adfcf731fa1a71fec434b0e07d4309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973410"
---
# <a name="mfpkey_resize_quality-property"></a>Proprietà MFPKEY \_ RESIZE \_ QUALITY

Specifica se usare un algoritmo che produce video di qualità superiore o un algoritmo più veloce.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

VT \_ BOOL

## <a name="applies-to"></a>Si applica a

-   [DSP di Ridimensionamento video](videoresizer.md)

## <a name="remarks"></a>Commenti

Usare uno dei valori seguenti:



| Valore     | Descrizione          |
|-----------|----------------------|
| VT \_ FALSE | Algoritmo più veloce     |
| VT \_ TRUE  | Video di qualità superiore |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
