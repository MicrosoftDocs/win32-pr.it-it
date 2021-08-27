---
description: Contiene informazioni sui codec e i formati usati per codificare il contenuto in un file ASF (Advanced Systems Format). Questo attributo corrisponde all'oggetto Elenco codec nell'intestazione ASF, definito nella specifica ASF.
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: MF_PD_ASF_CODECLIST attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c512dee499dbd2d006fb695c89d59add449e64fb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471307"
---
# <a name="mf_pd_asf_codeclist-attribute"></a>Attributo MF \_ PD \_ ASF \_ CODECLIST

Contiene informazioni sui codec e i formati usati per codificare il contenuto in un file ASF (Advanced Systems Format). Questo attributo corrisponde all'oggetto Elenco codec nell'intestazione ASF, definito nella specifica ASF.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto asf.

Il [**metodo IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea il descrittore di presentazione e genera questo attributo dall'oggetto elenco codec nell'intestazione ASF. Un'applicazione che usa [l'origine multimediale ASF](asf-media-source.md) può ottenere questo attributo chiamando [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) e quindi ottenendo l'attributo dal descrittore di presentazione.

Nella tabella seguente viene illustrato il layout del BLOB di attributi.



| Campo Oggetto elenco codec | Tipo di dati    | Dimensione    | Descrizione                           |
|-------------------------|--------------|---------|---------------------------------------|
| Conteggio voci codec     | **DWORD**    | 4 byte | Numero di codec                      |
| Voci codec           | **BYTE**\[\] | Varia  | Matrice di strutture di informazioni sui codec |



 

Il campo Code Entries è una matrice di strutture. La tabella seguente illustra il formato di ogni voce:




| Campo Oggetto elenco codec | Tipo di dati | Dimensione | Descrizione | 
|-------------------------|-----------|------|-------------|
| Type | <strong>DWORD</strong> | 4 byte | Tipo di codec. I valori possibili sono i seguenti:<br /><ul><li>0x0001: codec audio</li><li>0x0002: codec video</li><li>0xFFFF: Sconosciuto</li></ul> | 
| Lunghezza nome codec | <strong>DWORD</strong> | 4 byte | Dimensioni della stringa Nome codec, in byte, incluso il <strong>carattere NULL.</strong> | 
| Nome codec | <strong>WCHAR</strong>[] | Varia | Stringa Unicode con terminazione Null che contiene il nome del codec, ad esempio "Windows Media Video 9". | 
| Lunghezza descrizione codec | <strong>DWORD</strong> | 4 byte | Dimensioni della stringa di descrizione del codec, in byte, incluso il <strong>carattere NULL.</strong> | 
| Descrizione codec | <strong>WCHAR</strong>[] | Varia | Stringa Unicode con terminazione Null che contiene una descrizione del codec. | 
| Lunghezza delle informazioni sul codec | <strong>DWORD</strong> | 4 byte | Dimensioni del campo Informazioni sul codec, in byte. | 
| Informazioni sui codec | <strong>BYTE</strong>[] | Varia | Dati del codec. Il significato di questi dati dipende dal codec. In genere, questi dati indicano il formato. | 




 

> [!Note]  
> Il layout del BLOB dell'attributo non corrisponde esattamente al layout dell'oggetto elenco codec nell'intestazione ASF. In particolare, le lunghezze delle stringhe sono specificate in byte e includono le dimensioni del terminatore **NULL.**

 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore di presentazione](presentation-descriptor-attributes.md)
</dt> <dt>

[Oggetto intestazione ASF](asf-file-structure.md)
</dt> <dt>

[Descrittori di presentazione](presentation-descriptors.md)
</dt> </dl>

 

 




