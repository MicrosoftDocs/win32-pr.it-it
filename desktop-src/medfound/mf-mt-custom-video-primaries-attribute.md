---
description: Specifica le primarie colore personalizzate per un tipo di supporto video.
ms.assetid: dc5df755-53cf-4910-af42-309f1f46b1ed
title: Attributo MF_MT_CUSTOM_VIDEO_PRIMARIES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d63e39638f74cacafa1b4376b28c7703f7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318424"
---
# <a name="mf_mt_custom_video_primaries-attribute"></a>\_ \_ \_ Attributo primari video personalizzati MF mt \_

Specifica le primarie colore personalizzate per un tipo di supporto video.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Matrice di byte

## <a name="remarks"></a>Commenti

I dati dell'attributo sono una struttura di [**\_ \_ \_ primari video personalizzati di mt**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) .

Questo attributo specifica il volume di colori effettivo del contenuto o una visualizzazione. Le informazioni di master del volume dei colori CEA-861,3/SMPTE ST. 2086 vengono archiviate in questo attributo dai decodificatori. Si noti che questo attributo non sostituisce l'attributo delle [**\_ \_ \_ primarie del video MF mt**](mf-mt-video-primaries-attribute.md). Questo attributo descrive un suggerimento sul volume di colori del contenuto, mentre le **\_ \_ \_ primarie del video MF mt** descrivono le primarie di colore in cui il contenuto è effettivamente codificato (ad esempio, il significato di 1,0 nei canali R/g/B di una rappresentazione a virgola mobile).

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: seblob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

 




