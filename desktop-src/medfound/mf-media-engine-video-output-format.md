---
description: Imposta il formato di destinazione di rendering per il motore multimediale.
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: Attributo MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004025da1ad5258e5b04a3afba4a359f50f7444c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761386"
---
# <a name="mf_media_engine_video_output_format-attribute"></a>\_ \_ \_ Attributo formato video di \_ output del motore multimediale \_ MF

Imposta il formato di destinazione di rendering per il motore multimediale.

## <a name="data-type"></a>Tipo di dati

**DXGI \_ FORMATO** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Impostare questo attributo se si crea il motore multimediale in modalità frame-server. Per altre informazioni, vedere [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance). Il valore dell'attributo è un valore [di \_ formato DXGI](../direct3d9/d3dformat.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                          |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
