---
description: Imposta il formato della destinazione di rendering per il motore di contenuti multimediali.
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT attributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaa0dab3c3ea1c9ce23d767458df0b68a9b3c787f80ca1af786061536343a356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973730"
---
# <a name="mf_media_engine_video_output_format-attribute"></a>Attributo VIDEO OUTPUT FORMAT del MOTORE \_ \_ \_ \_ \_ MULTIMEDIALE MF

Imposta il formato della destinazione di rendering per il motore di contenuti multimediali.

## <a name="data-type"></a>Tipo di dati

**DXGI \_ FORMAT** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Impostare questo attributo se si crea il motore multimediale in modalità server frame. Per altre informazioni, vedere [**IMFMediaEngineClassFactory::CreateInstance.**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) Il valore dell'attributo è un [valore DXGI \_ FORMAT.](../direct3d9/d3dformat.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                          |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
