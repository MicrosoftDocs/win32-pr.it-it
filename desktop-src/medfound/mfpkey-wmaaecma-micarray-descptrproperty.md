---
description: Specifica la geometria della matrice di microfoni per il DSP di acquisizione voce.
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: Proprietà MFPKEY_WMAAECMA_MICARRAY_DESCPTR (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e433f50d9d7640575f1314c5acc13d7751fde0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309117"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a>MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR proprietà

Specifica la geometria della matrice di microfoni per il DSP di acquisizione voce.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

\_BLOB VT

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

Il valore di questa proprietà è una [**struttura \_ \_ \_ Geometry della matrice KSAUDIO MIC**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) . Questa struttura viene definita nel file di intestazione KsMedia. h. Per ottenere la geometria della matrice di microfoni, eseguire una query sul dispositivo audio per la \_ \_ Proprietà Geometry della matrice KSPROPERTY audio mic chiamando \_ \_ il metodo **IKsControl:: KSPROPERTY** sul dispositivo. Per ulteriori informazioni sugli array di microfoni, scaricare il white paper [come compilare e utilizzare gli array di microfoni per Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

Impostare questa proprietà se si utilizza il DSP in modalità filtro ed è abilitata l'elaborazione di matrici di microfoni. Se si usa il DSP in modalità origine, il DSP esegue automaticamente una query sul dispositivo per le informazioni di geometria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP di acquisizione vocale](voicecapturedmo.md)
</dt> </dl>

 

 
