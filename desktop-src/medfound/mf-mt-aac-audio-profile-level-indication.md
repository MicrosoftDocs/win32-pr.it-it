---
description: Specifica il profilo audio e il livello di un flusso AAC (Advanced Audio Coding).
ms.assetid: 87fa1127-46ca-4b83-a3b5-99253af22ba0
title: MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89934c55ff07124c28952c621513ddd4fd8db504c6e9df7cc6094f8ba7b875ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104567"
---
# <a name="mf_mt_aac_audio_profile_level_indication-attribute"></a>Attributo MF \_ MT \_ AAC \_ AUDIO PROFILE \_ \_ LEVEL \_ INDICATION

Specifica il profilo audio e il livello di un flusso AAC (Advanced Audio Coding).

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

Questo attributo contiene il valore del campo **audioProfileLevelIndication,** come definito da ISO/IEC 14496-3.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




