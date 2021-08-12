---
description: Specifica la durata dell'eco che l'algoritmo di annullamento dell'eco acustica (AEC) può gestire, in millisecondi.
ms.assetid: d451b90f-7ef7-4f66-be83-aca93e3ad894
title: MFPKEY_WMAAECMA_FEATR_ECHO_LENGTH proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4b8f22b87622c00c296f194cb7ba618c55b04901ac30ce216d7387e2e04033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242028"
---
# <a name="mfpkey_wmaaecma_featr_echo_length-property"></a>Proprietà MFPKEY \_ WMAAECMA \_ FEATR \_ ECHO \_ LENGTH

Specifica la durata dell'eco che l'algoritmo di annullamento dell'eco acustica (AEC) può gestire, in millisecondi.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

256

## <a name="applies-to"></a>Si applica a

-   [Voice Capture DSP](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

L'algoritmo AEC usa un filtro adattivo la cui lunghezza è determinata dalla durata dell'eco. È consigliabile che le applicazioni usino uno dei valori seguenti:

-   128
-   256
-   512
-   1024

Il valore predefinito è 256 millisecondi, sufficiente per la maggior parte degli ambienti di ufficio e casa. Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) su VARIANT \_ TRUE.

Il DSP usa questa proprietà solo quando è abilitata l'elaborazione AEC.

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

 

 
