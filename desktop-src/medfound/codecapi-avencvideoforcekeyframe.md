---
description: Impone al codificatore di codificare il fotogramma successivo come fotogramma chiave.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: Proprietà CODECAPI_AVEncVideoForceKeyFrame (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72c555d5680e822e9a8308b3e143a754eb22b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305489"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a>Proprietà AVEncVideoForceKeyFrame di codecapi \_

Impone al codificatore di codificare il fotogramma successivo come fotogramma chiave.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoForceKeyFrame**

## <a name="property-value"></a>Valore proprietà

Se il valore è diverso da zero, il codificatore codifica il frame successivo come fotogramma chiave. Se il valore è zero, il codificatore seleziona se codificare il fotogramma successivo come fotogramma chiave.

Questa proprietà si applica al frame successivo che il codificatore riceve come input. Per un Media Foundation Transform (MFT), questo è il frame successivo passato al metodo [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) . L'impostazione viene reimpostata su zero dopo il frame successivo.

## <a name="remarks"></a>Commenti

Questa proprietà viene usata anche con [codificatori della fotocamera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

