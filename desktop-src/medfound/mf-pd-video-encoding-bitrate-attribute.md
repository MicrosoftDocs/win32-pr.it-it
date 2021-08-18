---
description: Specifica la velocità in bit di codifica video per la presentazione, in bit al secondo. Questo attributo si applica ai descrittori di presentazione.
ms.assetid: 0fe8cf64-2256-4e48-9853-2c734f97f3c7
title: MF_PD_VIDEO_ENCODING_BITRATE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de8c7e250ab446714a3d9afb2c7d07e0d3ac76a671bb50dcd46785368a77cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102907"
---
# <a name="mf_pd_video_encoding_bitrate-attribute"></a>Attributo MF \_ PD \_ VIDEO ENCODING \_ \_ BITRATE

Specifica la velocità in bit di codifica video per la presentazione, in bit al secondo. Questo attributo si applica ai descrittori di presentazione.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Alcuni formati hanno schemi di codifica più complessi che non possono essere riepilogati usando questo attributo. Per i file ASF (Advanced Systems Format), gli attributi seguenti descrivono collettivamente la velocità in bit di codifica:

-   [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MAX \_ BITRATE**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ VELOCITÀ IN BIT MASSIMA DEI \_ \_ DATI**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ STREAMBITRATES \_ BITRATES**](mf-sd-asf-streambitrates-bitrate-attribute.md)

I formati di terze parti potrebbero usare altri attributi personalizzati.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop Di Vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 \[ \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore di presentazione](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




