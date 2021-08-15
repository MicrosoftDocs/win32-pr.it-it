---
description: Specifica il profilo della codifica video nel tipo di supporto di output. Si tratta di un alias dell'attributo \_ MF MT \_ MPEG2 \_ PROFILE.
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: MF_MT_VIDEO_PROFILE attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d2af7c6ebbbbb78626e96385a6eda5a25c38a3ae8473fac866866248570cc48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741394"
---
# <a name="mf_mt_video_profile-attribute"></a>Attributo \_ MF MT \_ VIDEO \_ PROFILE

Specifica il profilo della codifica video nel tipo di supporto di output. Si tratta di un alias [dell'attributo \_ MF MT \_ MPEG2 \_ PROFILE.](mf-mt-mpeg2-profile-attribute.md)

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

**Codificatori H.264:**

I profili supportati sono stati superati per includere [**eAVEncH264VProfile \_ ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) ed **eAVEncH264VProfile \_ ConstrainedHigh.**

I codificatori devono supportare [**sia GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) che [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) per questo attributo.

Si tratta di una configurazione statica, quindi i codificatori video devono essere configurati prima dell'avvio dello streaming. Se l'applicazione imposta un profilo non supportato dal codificatore, il codificatore deve rifiutare il tipo di supporto.

Impostazione predefinita consigliata: [**profilo principale \_ eAVEncH264VProfile.**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                       |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
