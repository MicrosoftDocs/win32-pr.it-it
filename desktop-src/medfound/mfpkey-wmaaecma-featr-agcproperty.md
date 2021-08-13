---
description: Specifica se il DSP di acquisizione vocale esegue il controllo automatico del guadagno.
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: MFPKEY_WMAAECMA_FEATR_AGC proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f038b18657363677e0953f8fe973c2e3029130ffc2183a08344e1b0cd6905747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343811"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a>Proprietà MFPKEY \_ WMAAECMA \_ FEATR \_ AGC

Specifica se il DSP di acquisizione vocale esegue il controllo automatico del guadagno.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

VT \_ BOOL

## <a name="default-value"></a>Valore predefinito

VARIANT \_ FALSE

## <a name="applies-to"></a>Si applica a

-   [Voice Capture DSP](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Il controllo automatico del guadagno è un componente DSP (Digital Signal Processing) che regola il guadagno in modo che il livello di output del segnale rimanga entro lo stesso intervallo approssimativo.

Questa proprietà può avere i valori seguenti.



| Valore          | Descrizione                     |
|----------------|---------------------------------|
| VARIANT \_ FALSE | Disabilitare il controllo automatico del guadagno. |
| VARIANT \_ TRUE  | Abilitare il controllo automatico del guadagno.  |



 

Il valore predefinito di questa proprietà è VARIANT \_ FALSE (disabilitato). Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) su VARIANT \_ TRUE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Voice Capture DSP](voicecapturedmo.md)
</dt> </dl>

 

 
