---
description: Contiene dati di formato aggiuntivi per un tipo di supporto.
ms.assetid: 020832c4-40a1-4d8b-ada0-7a04ce097bce
title: MF_MT_USER_DATA attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0196e8fea06bb84fe5a78a8b486f95864e0c6d889692dfa6f3ee9b1103da518a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012782"
---
# <a name="mf_mt_user_data-attribute"></a>Attributo MF \_ MT \_ USER \_ DATA

Contiene dati di formato aggiuntivi per un tipo di supporto.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Il significato dei dati in questo attributo dipende dal formato descritto dal tipo di supporto.



| Tipo di formato                                                                                                           | Dati di formato aggiuntivi                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Codec multimediale.                                                                                                  | Codec di dati privati.                                                                                                                       |
| Struttura [**VIDEOINFOHEADER o**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) convertita.   | Dati aggiuntivi visualizzati dopo la struttura [**BITMAPINFOHEADER,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) senza includere la tabella dei colori o le maschere di colore. |
| Struttura [**WAVEFORMATEX o**](/previous-versions/dd757713(v=vs.85)) [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) convertita. | Dati aggiuntivi visualizzati dopo la struttura del formato audio.                                                                                 |



 

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

[**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 
