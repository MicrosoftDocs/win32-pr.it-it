---
description: Contiene il tag di formato WAVE originale per un flusso audio.
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: MF_MT_ORIGINAL_WAVE_FORMAT_TAG attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89f05086858f54c619e3896f5978cf81005e9b1e80e858bc89c71e951ab48b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741666"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a>Attributo \_ MF MT \_ ORIGINAL WAVE \_ FORMAT \_ \_ TAG

Contiene il tag di formato WAVE originale per un flusso audio.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

A seconda del file di origine, l'origine multimediale AVI potrebbe impostare questo attributo sui tipi di supporti che offre.

Un file AVI contiene un'intestazione di flusso per ogni flusso nel file. L'origine multimediale AVI converte l'intestazione del flusso in un tipo di supporto. Per i flussi audio, l'intestazione del flusso contiene un tag di formato che identifica il formato audio. Il tag di formato è contenuto nel **membro wFormatTag** della [**struttura WAVEFORMATEX.**](/previous-versions/dd757713(v=vs.85)) Nella maggior parte dei casi, l'origine multimediale AVI converte il tag di formato direttamente in un GUID di sottotipo, come descritto nell'argomento GUID del [**sottotipo audio**](audio-subtype-guids.md). In alcuni casi, tuttavia, esegue il mapping del tag di formato originale a un altro tag di formato equivalente. In questo caso, l'origine multimediale archivia il tag di formato originale nel tipo di supporto, usando l'attributo \_ MF MT \_ ORIGINAL WAVE \_ FORMAT \_ \_ TAG.

I mapping di formato vengono archiviati nel Registro di sistema nella chiave seguente:

**HKEY \_ CLASSES \_ ROOT** \\ **MediaFoundation** \\ **MapAudioFormatTag**

Ogni voce è un **valore DWORD.** Il nome della voce è la rappresentazione decimale del tag di formato. Il valore della voce è il tag di formato equivalente.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 
