---
description: Fare riferimento al livello di volume massimo di Windows file audio multimediale.
ms.assetid: bb762f9c-cf08-4d32-991e-490eb7b1f579
title: MF_MT_AUDIO_WMADRC_PEAKREF attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 712c09d5cffc79c20122cf26211d1e63c0de495333ff5e349bbe7436a9b34bc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060283"
---
# <a name="mf_mt_audio_wmadrc_peakref-attribute"></a>Attributo MF \_ MT \_ AUDIO \_ WMADRC \_ PEAKREF

Fare riferimento al livello di volume massimo di Windows file audio multimediale.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai tipi di supporti audio per Windows codec Audio multimediali. Specifica il livello di volume di picco originale del contenuto. Il decodificatore può usare questo valore per eseguire il controllo dinamico dell'intervallo.

Il [**metodo IMFASFContentInfo::P arseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) aggiunge questo attributo al tipo di supporto se l'intestazione ASF contiene l'attributo [**WM/WMADRCPeakReference.**](../wmformat/wm-wmadrcpeakreference.md) Questo attributo è documentato nella documentazione Windows Media Format SDK.

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

 

 
