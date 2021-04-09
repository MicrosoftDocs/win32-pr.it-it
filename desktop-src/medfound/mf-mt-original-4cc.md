---
description: Contiene il codec originale FOURCC per un flusso video.
ms.assetid: 2e6ef198-5754-4ded-9fe3-61edd0742a17
title: Attributo MF_MT_ORIGINAL_4CC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b374ba3ef74cb98925edcc5d809e1fd5e0b7fbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968164"
---
# <a name="mf_mt_original_4cc-attribute"></a>\_ \_ Attributo 4cc originale MF mt \_

Contiene il codec originale FOURCC per un flusso video.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

A seconda del file di origine, l'origine multimediale AVI potrebbe impostare questo attributo sui tipi di supporto che offre.

Un file AVI contiene un'intestazione del flusso per ogni flusso del file. L'origine multimediale AVI Converte l'intestazione del flusso in un tipo di supporto. Per i flussi video compressi, l'intestazione del flusso contiene un FOURCC che identifica il codec video. Nella maggior parte dei casi, l'origine multimediale AVI Converte questo FOURCC direttamente in un GUID di sottotipo, come descritto nell'argomento [GUID del sottotipo video](video-subtype-guids.md). In alcuni casi, tuttavia, esegue il mapping del FOURCC originale a un altro FOURCC equivalente. In tal caso, l'origine multimediale archivia il FOURCC originale nel tipo di supporto, usando l' \_ \_ attributo 4cc originale MF mt \_ .

I mapping di FOURCC vengono archiviati nel registro di sistema con la seguente chiave:

**HKEY \_ Classi \_ radice** \\ **MediaFoundation** \\ **MapVideo4cc**

Ogni voce è un valore **DWORD** . Il nome della voce è la rappresentazione esadecimale di FOURCC, senza un prefisso "0x" e con il primo carattere visualizzato per primo nella stringa. Il codice FOURCC ' abcd ', ad esempio, verrebbe visualizzato come "61626364". Il valore della voce è il codice FOURCC equivalente.

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

 

 




