---
description: Specifica il profilo della codifica video nel tipo di supporto di output. Si tratta di un alias di MF \_ mt \_ MPEG2 \_ profile Attribute.
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: Attributo MF_MT_VIDEO_PROFILE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6dbf8d324c7a451c1d2affb9f348a3ef2e1806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318063"
---
# <a name="mf_mt_video_profile-attribute"></a>\_ \_ Attributo profilo video MF mt \_

Specifica il profilo della codifica video nel tipo di supporto di output. Si tratta di un alias di [MF \_ mt \_ MPEG2 \_ profile](mf-mt-mpeg2-profile-attribute.md) Attribute.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

**Codificatori H. 264:**

Sono stati superati i profili supportati per includere [**eAVEncH264VProfile \_ ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) e **eAVEncH264VProfile \_ ConstrainedHigh**.

I codificatori devono supportare sia [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) che [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) per questo attributo.

Questo è statico, quindi i codificatori video devono essere configurati prima dell'avvio del flusso. Se l'applicazione imposta un profilo che non è supportato dal codificatore, il codificatore rifiuterà il tipo di supporto.

Impostazione predefinita consigliata: profilo [**\_ principale eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                       |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
