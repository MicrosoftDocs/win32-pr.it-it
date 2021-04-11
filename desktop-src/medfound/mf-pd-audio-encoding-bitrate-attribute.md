---
description: Specifica la velocità in bit per la codifica audio per la presentazione, in bit al secondo. Questo attributo si applica ai descrittori di presentazione.
ms.assetid: 700f61f4-a0d7-4b69-ace5-356e4e29b93d
title: Attributo MF_PD_AUDIO_ENCODING_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49566ecb225482ef6513e056de8ba11763de603e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232385"
---
# <a name="mf_pd_audio_encoding_bitrate-attribute"></a>\_ \_ \_ Attributo velocità in bit codifica audio MF PD \_

Specifica la velocità in bit per la codifica audio per la presentazione, in bit al secondo. Questo attributo si applica ai descrittori di presentazione.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

L'attributo è facoltativo. Per alcuni formati sono disponibili schemi di codifica più complessi che non possono essere riepilogati utilizzando questo attributo. Per i file di formato Advanced Systems (ASF), i seguenti attributi descrivono collettivamente la velocità in bit di codifica:

-   [**\_velocità in \_ \_ \_ bit max PD ASF FileProperties \_**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [**\_velocità in \_ \_ \_ \_ bit dei dati media \_ di MF SD ASF EXTSTRMPROP**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [**\_velocità in \_ \_ \_ \_ bit massima dei dati di EXTSTRMPROP \_ MF SD ASF**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [**\_velocità in bit MF SD \_ ASF \_ STREAMBITRATES \_**](mf-sd-asf-streambitrates-bitrate-attribute.md)

I formati di terze parti potrebbero usare altri attributi personalizzati.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                              |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore della presentazione](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




