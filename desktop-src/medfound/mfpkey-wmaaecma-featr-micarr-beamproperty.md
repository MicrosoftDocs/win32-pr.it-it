---
description: Specifica quale dispositivo DSP di acquisizione vocale usa per l'elaborazione della matrice del microfono.
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: MFPKEY_WMAAECMA_FEATR_MICARR_BEAM proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9a91cef7d270af37adc8fda9805d7bf275ef9877883ed8ff8cfdbf9e7a55e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953531"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a>Proprietà MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ BEAM

Specifica quale dispositivo DSP di acquisizione vocale usa per l'elaborazione della matrice del microfono.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="applies-to"></a>Si applica a

-   [Voice Capture DSP](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Impostare questa proprietà se il valore della proprietà [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ MODE](mfpkey-wmaaecma-featr-micarr-modeproperty.md) è MICARRAY \_ EXTERN \_ BEAM.

Se il valore di [**MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ MODE**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) è MICARRAY \_ SINGLE PLUG-IN, è possibile leggere questa proprietà per eseguire una query sulla trave selezionata dal \_ DSP.

Questa proprietà può avere i valori seguenti. I valori sono in gradi orizzontali.



| Valore | Descrizione              |
|-------|--------------------------|
| 0     | -50 gradi.             |
| 1     | -40 gradi.             |
| 2     | -30 gradi.             |
| 3     | -20 gradi.             |
| 4     | -10 gradi.             |
| 5     | 0 gradi (raggio centrale). |
| 6     | 10 gradi.              |
| 7     | 20 gradi.              |
| 8     | 30 gradi.              |
| 9     | 40 gradi.              |
| 10    | 50 gradi.              |



 

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

 

 
