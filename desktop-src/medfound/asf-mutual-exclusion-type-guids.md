---
description: I GUID seguenti definiscono i tipi per l'oggetto di esclusione reciproca per i flussi ASF (Advanced Systems Format).
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: GUID del tipo di esclusione reciproca ASF (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a6fedc766e26c35bb967054a704b732ca03e8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225839"
---
# <a name="asf-mutual-exclusion-type-guids"></a>GUID del tipo di esclusione reciproca ASF

I GUID seguenti definiscono i tipi per l'oggetto di esclusione reciproca per i flussi ASF (Advanced Systems Format).



| Costante                                                                                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <dt>**\_Lingua MFASFMutexType**</dt> </dl>                 | I flussi si escludono reciprocamente in base alla lingua. Questo tipo di esclusione reciproca è simile alle tracce audio di un DVD.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <dt>**\_Velocità in bit MFASFMutexType**</dt> </dl>                     | I flussi si escludono a vicenda in base alla velocità in bit. Questo tipo di esclusione reciproca viene anche definito esclusione di velocità in bit multipli (MBR).<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <dt>**Presentazione di MFASFMutexType \_**</dt> </dl> | I flussi si escludono a vicenda dalla presentazione. Questo tipo può essere usato per molti scenari, ma deve essere usato solo quando il contenuto è lo stesso, ma assume un formato diverso. Ad esempio, due flussi che contengono lo stesso video, uno formattato in modo da riempire lo schermo e l'altro che mantiene le proporzioni widescreen originali, devono essere resi esclusi a vicenda usando questo tipo. Un altro esempio è costituito da flussi che contengono video della stessa scena ripresi da diverse angolazioni.<br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <dt>**MFASFMutexType \_ sconosciuto**</dt> </dl>                     | I flussi si escludono a vicenda in base a criteri personalizzati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFASFMutualExclusion:: GetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[**IMFASFMutualExclusion:: seTYPE**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[Costanti Media Foundation](media-foundation-constants.md)
</dt> </dl>

 

 




