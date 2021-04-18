---
description: Contiene il tag di formato WAVE originale per un flusso audio.
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: Attributo MF_MT_ORIGINAL_WAVE_FORMAT_TAG (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba89171f9ae2bf3ab99df05bd3ae64b7d52be6d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319174"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a>\_ \_ \_ \_ Attributo tag formato Wave originale MF mt \_

Contiene il tag di formato WAVE originale per un flusso audio.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

A seconda del file di origine, l'origine multimediale AVI potrebbe impostare questo attributo sui tipi di supporto che offre.

Un file AVI contiene un'intestazione del flusso per ogni flusso del file. L'origine multimediale AVI Converte l'intestazione del flusso in un tipo di supporto. Per i flussi audio, l'intestazione del flusso contiene un tag di formato che identifica il formato audio. Il tag di formato è contenuto nel membro **wFormatTag** della struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) . Nella maggior parte dei casi, l'origine multimediale AVI Converte il tag di formato direttamente in un GUID di sottotipo, come descritto nell'argomento [**GUID del sottotipo audio**](audio-subtype-guids.md). In alcuni casi, tuttavia, il tag di formato originale viene mappato a un altro tag di formato equivalente a. In tal caso, l'origine multimediale archivia il tag di formato originale nel tipo di supporto, usando \_ l' \_ attributo di tag di formato Original Wave di MF mt \_ \_ \_ .

I mapping del formato vengono archiviati nel registro di sistema con la seguente chiave:

**HKEY \_ Classi \_ radice** \\ **MediaFoundation** \\ **MapAudioFormatTag**

Ogni voce è un valore **DWORD** . Il nome della voce è la rappresentazione decimale del tag di formato. Il valore della voce è il tag di formato equivalente.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 
