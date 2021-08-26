---
description: Specifica il livello MPEG-2 o H.264 in un tipo di supporto video. Si tratta di un alias di MF \_ MT \_ MPEG2 \_ LEVEL.
ms.assetid: 23786FC8-ACA4-4F6A-98BA-57A8C76BD4C6
title: MF_MT_VIDEO_LEVEL attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40f1ebc6834373e00253f494e3fc76c20c343af17d754c7c4fe642b802d16ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012771"
---
# <a name="mf_mt_video_level-attribute"></a>Attributo MF \_ MT \_ VIDEO \_ LEVEL

Specifica il livello MPEG-2 o H.264 in un tipo di supporto video. Si tratta di un alias di [MF \_ MT \_ MPEG2 \_ LEVEL.](mf-mt-mpeg2-level-attribute.md)

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

**Codificatori H.264:**

I livelli supportati sono estesi per includere [**eAVEncH264VLevel5 \_ 2.**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel)

Impostazione predefinita: l'impostazione predefinita consigliata è selezionare il livello minimo per la configurazione della codifica video, tra cui risoluzione, frequenza dei fotogrammi e così via.

Impostazione predefinita consigliata: selezionare il livello minimo per la configurazione della codifica video, tra cui risoluzione, frequenza dei fotogrammi e così via.

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

 

 




