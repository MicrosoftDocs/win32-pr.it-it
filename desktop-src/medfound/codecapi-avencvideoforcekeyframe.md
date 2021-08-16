---
description: Forza il codificatore a codificare il fotogramma successivo come fotogramma chiave.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: CODECAPI_AVEncVideoForceKeyFrame proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2e28738dcd7398ce04abe7f71778e94d7d5d4f49393365e92c43bbb347d98c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880707"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a>CODECAPI \_ AVEncVideoForceKeyFrame - proprietà

Forza il codificatore a codificare il fotogramma successivo come fotogramma chiave.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncVideoForceKeyFrame**

## <a name="property-value"></a>Valore proprietà

Se il valore è diverso da zero, il codificatore codifica il fotogramma successivo come fotogramma chiave. Se il valore è zero, il codificatore seleziona se codificare il fotogramma successivo come fotogramma chiave.

Questa proprietà si applica al fotogramma successivo ricevuto dal codificatore come input. Per una Media Foundation (MFT), questo è il frame successivo passato al [**metodo IMFTransform::P rocessInput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) L'impostazione viene reimpostata su zero dopo il fotogramma successivo.

## <a name="remarks"></a>Commenti

Questa proprietà viene usata anche con codificatori [di fotocamera H.264 UVC 1.5.](camera-encoder-h264-uvc-1-5.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                     |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

