---
description: Numero di campioni audio contenuti in un blocco compresso di dati audio. Questo attributo può essere usato in formati audio compressi con un numero fisso di campioni all'interno di ogni blocco.
ms.assetid: 6ae31548-4d78-4e38-9cfc-01b611a6022d
title: Attributo MF_MT_AUDIO_SAMPLES_PER_BLOCK (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c453fa4daeaa310b5e41add44b63b0fb45372d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315036"
---
# <a name="mf_mt_audio_samples_per_block-attribute"></a>\_ \_ Esempi audio MF \_ mt \_ per \_ blocco

Numero di campioni audio contenuti in un blocco compresso di dati audio. Questo attributo può essere usato in formati audio compressi con un numero fisso di campioni all'interno di ogni blocco.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo corrisponde al membro **wSamplesPerBlock** della struttura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .

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

 

 
