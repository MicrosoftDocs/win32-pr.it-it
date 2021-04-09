---
description: GUID del sottotipo per un tipo di supporto.
ms.assetid: 8e600943-92f1-4936-8c00-842fc7f4cb57
title: Attributo MF_MT_SUBTYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f156e356a0e80d6b2c4bff1ae6f266e4d64b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050093"
---
# <a name="mf_mt_subtype-attribute"></a>\_Attributo del \_ sottotipo MF mt

GUID del sottotipo per un tipo di supporto.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Il GUID del sottotipo definisce un tipo di formato multimediale specifico all'interno di un tipo principale. Ad esempio, all'interno di video, i sottotipi includono RGB-24, RGB-32, UYVY, AYUV e così via. All'interno di audio, i sottotipi includono audio PCM, Windows Media Audio 9 e così via.

Per i valori possibili, vedere gli argomenti seguenti:

-   [GUID del sottotipo audio](audio-subtype-guids.md)
-   [GUID del sottotipo video](video-subtype-guids.md)

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                              |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




