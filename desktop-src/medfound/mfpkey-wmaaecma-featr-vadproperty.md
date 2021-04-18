---
description: Specifica il tipo di rilevamento dell'attività vocale eseguita dal DSP di acquisizione voce.
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: Proprietà MFPKEY_WMAAECMA_FEATR_VAD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e41b8ad80d909a0285b266587d02c09c08d794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309120"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a>MFPKEY \_ WMAAECMA \_ featr \_ Proprietà VAD

Specifica il tipo di rilevamento dell'attività vocale eseguita dal DSP di acquisizione voce.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Il valore di questa proprietà è un membro dell'enumerazione [della \_ \_ modalità VAD AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) . L'output del rilevamento dell'attività vocale è un numero compreso tra 0 e 3, calcolato per ogni fotogramma audio. Il DSP codifica il risultato nel bit più basso dei primi due esempi audio in ogni frame audio. Il significato del valore dipende dalla modalità specificata.

Il codice seguente mostra come estrarre i risultati dai dati audio. In questo esempio, *pOutput* è un puntatore all'inizio di un frame audio nei dati di output.


```
int AecDecodeVAD(short *pOutput)
{
    int iVAD = (*pOutput) & 0x01;
    pOutput++;
    iVAD |= (*pOutput << 1) & 0x02;
    return iVAD;
}
```



Il valore predefinito di questa proprietà è 0 (disabilitato). Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
