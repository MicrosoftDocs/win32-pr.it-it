---
description: Specifica la velocità in bit di codifica audio per la presentazione, in bit al secondo. Questo attributo si applica ai descrittori di presentazione.
ms.assetid: 700f61f4-a0d7-4b69-ace5-356e4e29b93d
title: MF_PD_AUDIO_ENCODING_BITRATE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041e92eb71621d1f42d2b800557d204215bbca40f346a2afa4627863fc1a2206
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102878"
---
# <a name="mf_pd_audio_encoding_bitrate-attribute"></a>Attributo MF \_ PD \_ AUDIO ENCODING \_ \_ BITRATE

Specifica la velocità in bit di codifica audio per la presentazione, in bit al secondo. Questo attributo si applica ai descrittori di presentazione.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

L'attributo è facoltativo. Alcuni formati hanno schemi di codifica più complessi che non possono essere riepilogati usando questo attributo. Per i file ASF (Advanced Systems Format), gli attributi seguenti descrivono collettivamente la velocità in bit di codifica:

-   [**FILE \_ ASF PD \_ \_ MFPROPRIETÀ \_ VELOCITÀ \_ IN BIT MASSIMA**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ STREAMBITRATES \_ BITRATES**](mf-sd-asf-streambitrates-bitrate-attribute.md)

I formati di terze parti potrebbero usare altri attributi personalizzati.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 \[ \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore di presentazione](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




