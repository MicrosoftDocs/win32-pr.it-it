---
description: Specifica se il DSP di acquisizione vocale archivia le statistiche del timestamp nel Registro di sistema.
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: MFPKEY_WMAAECMA_RETRIEVE_TS_STATS proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c28f9812bb5f1324fcb1153b84f5a6704c7481c8356073fd02b8d95b57a8e497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953501"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a>Proprietà MFPKEY \_ WMAAECMA \_ RETRIEVE \_ TS \_ STATS

Specifica se il DSP di acquisizione vocale archivia le statistiche del timestamp nel Registro di sistema.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

VT \_ BOOL

## <a name="default-value"></a>Valore predefinito

VARIANT \_ FALSE

## <a name="applies-to"></a>Si applica a

-   [Voice Capture DSP](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Gli algoritmi di annullamento dell'eco acustica dipendono da timestamp accurati nei flussi audio. In realtà, i timestamp sono spesso imperfetti e dispositivi audio diversi possono presentare diverse frequenze di varianza e deriva. Quando AEC è abilitato, il DSP raccoglie statistiche sui timestamp e usa queste informazioni per compensare le imprecisioni.

Se il valore di questa proprietà è VARIANT TRUE, il DSP salva le statistiche raccolte \_ nel Registro di sistema. La volta successiva che il DSP esegue AEC usando la stessa coppia di dispositivi audio, legge le informazioni statistiche dal Registro di sistema, che consente al DSP di ottenere prestazioni più efficienti.

Se si imposta il valore di questa proprietà su VARIANT TRUE e si usa DSP in modalità filtro, è necessario impostare anche la proprietà \_ [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID.](mfpkey-wmaaecma-devicepair-guidproperty.md) In modalità di origine, questa operazione non è necessaria.

Il valore predefinito di questa proprietà è VARIANT \_ FALSE. Il DSP usa questa proprietà solo quando è abilitata l'elaborazione AEC.

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

 

 
