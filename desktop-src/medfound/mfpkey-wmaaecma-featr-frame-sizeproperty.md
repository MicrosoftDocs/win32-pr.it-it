---
description: Specifica le dimensioni del fotogramma audio usate dal DSP di acquisizione vocale.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: MFPKEY_WMAAECMA_FEATR_FRAME_SIZE proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812a9c7b85a36b730caffe7679cc742a3bc029546a12839afd95a8c8ab58bfeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973290"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a>Proprietà MFPKEY \_ WMAAECMA \_ FEATR \_ FRAME \_ SIZE

Specifica le dimensioni del fotogramma audio usate dal DSP di acquisizione vocale.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="applies-to"></a>Si applica a

-   [Voice Capture DSP](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

L'algoritmo di annullamento dell'eco acustica (AEC) elabora i campioni audio PCM un fotogramma alla volta. Il valore di questa proprietà è la dimensione del fotogramma audio, in campioni. Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) su VARIANT \_ TRUE.

Il DSP di acquisizione vocale supporta le dimensioni dei fotogrammi seguenti:

-   80
-   128
-   160
-   240
-   256
-   320

Se il valore di questa proprietà è zero, il DSP seleziona le dimensioni del frame in base alla modalità di sistema e al formato di output.

Per ottenere prestazioni ottimali, tuttavia, è consigliabile che le applicazioni usino il valore predefinito. Se la modalità di elaborazione è solo una matrice di microfoni, il valore predefinito è 320 campioni. Per tutte le altre modalità di elaborazione, il valore predefinito è 160 campioni. Per altre informazioni sulle modalità di elaborazione di Voice Capture DSP, vedere [MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE](mfpkey-wmaaecma-system-modeproperty.md).

Dopo la prima chiamata a [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) o [**IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), è possibile leggere questa proprietà per ottenere le dimensioni effettive del frame in uso, anche quando [**MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE**](mfpkey-wmaaecma-feature-modeproperty.md) è false.

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

 

 
