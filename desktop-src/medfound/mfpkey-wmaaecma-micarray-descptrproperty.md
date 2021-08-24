---
description: Specifica la geometria della matrice del microfono per il provider di servizi di acquisizione vocale.
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: MFPKEY_WMAAECMA_MICARRAY_DESCPTR proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b2bf0b495e7b57ba60cf5cc993b85a143836c8666e06d6b849ece3693b2a334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722945"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a>Proprietà MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR

Specifica la geometria della matrice del microfono per il provider di servizi di acquisizione vocale.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ BLOB

## <a name="applies-to"></a>Si applica a

-   [Provider di servizi di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Il valore di questa proprietà è una [**struttura GEOMETRY KSAUDIO \_ MIC \_ ARRAY. \_**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) Questa struttura è definita nel file di intestazione KsMedia.h. Per ottenere la geometria della matrice di microfoni, eseguire una query sul dispositivo audio per la proprietà KSPROPERTY AUDIO MIC ARRAY GEOMETRY chiamando il metodo \_ \_ \_ \_ **IKsControl::KSProperty** nel dispositivo. Per altre informazioni sulle matrici di microfoni, scaricare il white paper [how to Build and Use Microphone Arrays for Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

Impostare questa proprietà se si usa DSP in modalità filtro e l'elaborazione della matrice microfono è abilitata. Se si usa DSP in modalità di origine, il provider di servizi di configurazione esegue automaticamente una query sul dispositivo per ottenere le informazioni sulla geometria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Provider di servizi di acquisizione vocale](voicecapturedmo.md)
</dt> </dl>

 

 
