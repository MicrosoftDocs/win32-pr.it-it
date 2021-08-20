---
description: GUID del sottotipo per un tipo di supporto.
ms.assetid: 8e600943-92f1-4936-8c00-842fc7f4cb57
title: MF_MT_SUBTYPE attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e739bba5acc4816b8f8b9c2e9506496de3468865afca2d262cf56379c600889
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060013"
---
# <a name="mf_mt_subtype-attribute"></a>Attributo \_ MF MT \_ SUBTYPE

GUID del sottotipo per un tipo di supporto.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Il GUID del sottotipo definisce un tipo di formato multimediale specifico all'interno di un tipo principale. Ad esempio, all'interno del video, i sottotipi includono RGB-24, RGB-32, UYVY, AYUV e così via. All'interno dell'audio, i sottotipi includono l'audio PCM, Windows Media Audio 9 e così via.

Per i valori possibili, vedere gli argomenti seguenti:

-   [GUID del sottotipo audio](audio-subtype-guids.md)
-   [GUID del sottotipo video](video-subtype-guids.md)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop Di Vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 \[ \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




