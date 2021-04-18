---
description: Specifica il livello MPEG-2 o H. 264 in un tipo di supporto video. Si tratta di un alias di MF \_ mt \_ MPEG2 \_ level.
ms.assetid: 23786FC8-ACA4-4F6A-98BA-57A8C76BD4C6
title: Attributo MF_MT_VIDEO_LEVEL (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca2c5eb00390df1b5c18cab7e04a5f7449f84fc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318423"
---
# <a name="mf_mt_video_level-attribute"></a>\_ \_ Attributo livello video MF mt \_

Specifica il livello MPEG-2 o H. 264 in un tipo di supporto video. Si tratta di un alias di [MF \_ mt \_ MPEG2 \_ Level](mf-mt-mpeg2-level-attribute.md).

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

**Codificatori H. 264:**

I livelli supportati sono estesi in modo da includere [**eAVEncH264VLevel5 \_ 2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel).

Impostazione predefinita: il valore predefinito consigliato è quello di selezionare il livello minimo per la corrispondenza della configurazione della codifica video, inclusa la risoluzione, la frequenza dei fotogrammi

Impostazione predefinita consigliata: selezionare il livello minimo per la corrispondenza con la configurazione della codifica video, inclusi risoluzione, frequenza dei fotogrammi e così via.

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

 

 




