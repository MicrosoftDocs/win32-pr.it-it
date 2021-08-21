---
description: I GUID seguenti definiscono i tipi per l'oggetto di esclusione reciproca per i flussi ASF (Advanced Systems Format).
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: GUID del tipo di esclusione reciproca ASF (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fc035248610c8f58928347093dad4470f58f9818dc99fee1d88ac3fc0d13d88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035539"
---
# <a name="asf-mutual-exclusion-type-guids"></a>GUID del tipo di esclusione reciproca di ASF

I GUID seguenti definiscono i tipi per l'oggetto di esclusione reciproca per i flussi ASF (Advanced Systems Format).



| Costante                                                                                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <dt>**Linguaggio MFASFMutexType \_**</dt> </dl>                 | I flussi si escludono a vicenda in base al linguaggio. Questo tipo di esclusione reciproca è simile alle tracce audio in un DVD.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <dt>**Velocità in bit MFASFMutexType \_**</dt> </dl>                     | I flussi si escludono a vicenda in base alla velocità in bit. Questo tipo di esclusione reciproca è detto anche esclusione MBR (Multiple Bit Rate).<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <dt>**Presentazione di MFASFMutexType \_**</dt> </dl> | I flussi si escludono a vicenda in base alla presentazione. Questo tipo può essere usato per molti scenari, ma deve essere usato solo quando il contenuto è lo stesso ma ha un formato diverso. Ad esempio, due flussi contenenti lo stesso video, uno formattato per riempire lo schermo e l'altro che mantiene le proporzioni widescreen originali, devono essere resi reciprocamente esclusivi usando questo tipo. Un altro esempio sono i flussi contenenti video della stessa scena ripresa da angolazioni diverse.<br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <dt>**MFASFMutexType \_ Unknown**</dt> </dl>                     | I flussi si escludono a vicenda in base a criteri personalizzati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFASFMutualExclusion::GetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[**IMFASFMutualExclusion::SetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[Media Foundation costanti](media-foundation-constants.md)
</dt> </dl>

 

 




