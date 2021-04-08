---
description: Livello di picco del volume di destinazione di un file di Windows Media Audio.
ms.assetid: 73f4e763-dcb7-48cd-ab80-37635d973da0
title: Attributo MF_MT_AUDIO_WMADRC_PEAKTARGET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48391adfaa19dcc00ea4d7a30b909b4573f67222
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968165"
---
# <a name="mf_mt_audio_wmadrc_peaktarget-attribute"></a>\_Attributo PEAKTARGET di MF mt \_ audio \_ WMADRC \_

Livello di picco del volume di destinazione di un file di Windows Media Audio.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai tipi di supporti audio per Windows Media Audio codec. Specifica il livello di picco del volume di destinazione del contenuto. Il decodificatore può usare questo valore per eseguire il controllo dinamico degli intervalli.

Il metodo [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) aggiunge questo attributo al tipo di supporto se l'intestazione ASF contiene l'attributo [**WM/WMADRCPeakTarget**](../wmformat/wm-wmadrcpeaktarget.md) . Questo attributo è descritto nella documentazione di Windows Media Format SDK.

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

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 
