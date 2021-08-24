---
description: Specifica il tipo di rilevamento dell'attività vocale eseguito dal provider di servizi di acquisizione vocale.
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: MFPKEY_WMAAECMA_FEATR_VAD proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17e23662a8c6966a64140311f24c9af00dc53454cea19c025451698ddbbbd0dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953511"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a>Proprietà MFPKEY \_ WMAAECMA \_ FEATR \_ VAD

Specifica il tipo di rilevamento dell'attività vocale eseguito dal provider di servizi di acquisizione vocale.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="applies-to"></a>Si applica a

-   [Provider di servizi di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Il valore di questa proprietà è un membro [dell'enumerazione AEC \_ VAD \_ ](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) MODE. L'output del rilevamento dell'attività vocale è un numero da 0 a 3, calcolato per ogni fotogramma audio. Il DSP codifica il risultato nel bit più basso dei primi due campioni audio in ogni fotogramma audio. Il significato del valore dipende dalla modalità specificata.

Il codice seguente illustra come estrarre i risultati dai dati audio. In questo esempio *pOutput* è un puntatore all'inizio di un frame audio nei dati di output.


```
int AecDecodeVAD(short *pOutput)
{
    int iVAD = (*pOutput) & 0x01;
    pOutput++;
    iVAD |= (*pOutput << 1) & 0x02;
    return iVAD;
}
```



Il valore predefinito di questa proprietà è 0 (disabilitato). Prima di impostare questa proprietà, è necessario impostare la [proprietà MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) su VARIANT \_ TRUE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
