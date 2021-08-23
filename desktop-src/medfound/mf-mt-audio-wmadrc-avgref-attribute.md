---
description: Fare riferimento al livello medio di volume di Windows file audio multimediale.
ms.assetid: ea7d4ed1-2a96-4372-9936-abdd6473b57e
title: MF_MT_AUDIO_WMADRC_AVGREF attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a822046d368025bcfd068f7c1afd32f75d22b5d1ceab69d3e4b517595baa9b8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035289"
---
# <a name="mf_mt_audio_wmadrc_avgref-attribute"></a>Attributo \_ \_ \_ AVGREF WMADRC AUDIO MF \_ MT

Fare riferimento al livello medio di volume di Windows file audio multimediale.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai tipi di supporti audio per Windows codec Audio multimediali. Specifica il livello di volume medio originale del contenuto. Il decodificatore può usare questo valore per eseguire il controllo dinamico dell'intervallo.

Il [**metodo IMFASFContentInfo::P arseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) aggiunge questo attributo al tipo di supporto se l'intestazione ASF contiene l'attributo [**WM/WMADRCAverageReference.**](../wmformat/wm-wmadrcaveragereference.md) Questo attributo è documentato nella documentazione Windows Media Format SDK.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 \[ \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 
