---
description: Specifica la dimensione del frame audio utilizzata dal DSP di acquisizione voce.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: Proprietà MFPKEY_WMAAECMA_FEATR_FRAME_SIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5623cf3d26b968c7e7745fa0c01c69c034505cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309132"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a>\_ \_ \_ Proprietà dimensioni frame feat MFPKEY \_ WMAAECMA

Specifica la dimensione del frame audio utilizzata dal DSP di acquisizione voce.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="applies-to"></a>Si applica a

-   [DSP di acquisizione vocale](voicecapturedmo.md)

## <a name="remarks"></a>Commenti

L'algoritmo Acoustic Echo Cancel (AEC) elabora i campioni audio PCM un frame alla volta. Il valore di questa proprietà corrisponde alla dimensione del frame audio, in esempi. Prima di impostare questa proprietà, è necessario impostare la proprietà [MFPKEY \_ WMAAECMA \_ feature \_ mode](mfpkey-wmaaecma-feature-modeproperty.md) su Variant \_ true.

Il DSP di acquisizione vocale supporta le seguenti dimensioni dei frame:

-   80
-   128
-   160
-   240
-   256
-   320

Se il valore di questa proprietà è zero, il DSP seleziona le dimensioni del frame in base alla modalità di sistema e al formato di output.

Per prestazioni ottimali, tuttavia, è consigliabile usare il valore predefinito per le applicazioni. Se la modalità di elaborazione è solo una matrice di microfoni, il valore predefinito è 320 esempi. Per tutte le altre modalità di elaborazione, il valore predefinito è 160 esempi. Per altre informazioni sulle modalità di elaborazione del DSP di acquisizione vocale, vedere [ \_ modalità di \_ sistema \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-system-modeproperty.md).

Dopo la prima chiamata a [**IMediaObject:: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) o [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), è possibile leggere questa proprietà per ottenere le dimensioni effettive del frame in uso, anche quando la [**\_ modalità della \_ funzionalità \_ MFPKEY WMAAECMA**](mfpkey-wmaaecma-feature-modeproperty.md) è false.

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

 

 
