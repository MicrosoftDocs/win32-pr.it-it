---
description: Contiene informazioni sui codec e i formati utilizzati per codificare il contenuto in un file di formato Advanced Systems (ASF). Questo attributo corrisponde all'oggetto elenco di codec nell'intestazione ASF, definito nella specifica ASF.
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: Attributo MF_PD_ASF_CODECLIST (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402c53c082ae57fed444168c559f99718322f8a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316440"
---
# <a name="mf_pd_asf_codeclist-attribute"></a>\_ \_ \_ Attributo codecs MF PD ASF

Contiene informazioni sui codec e i formati utilizzati per codificare il contenuto in un file di formato Advanced Systems (ASF). Questo attributo corrisponde all'oggetto elenco di codec nell'intestazione ASF, definito nella specifica ASF.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.

Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea il descrittore di presentazione e genera questo attributo dall'oggetto elenco di codec nell'intestazione ASF. Un'applicazione che usa l' [origine dei supporti ASF](asf-media-source.md) può ottenere questo attributo chiamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) e quindi recuperando l'attributo dal descrittore di presentazione.

La tabella seguente illustra il layout del BLOB dell'attributo.



| Campo oggetto elenco di codec | Tipo di dati    | Dimensione    | Descrizione                           |
|-------------------------|--------------|---------|---------------------------------------|
| Conteggio voci codec     | **DWORD**    | 4 byte | Numero di codec                      |
| Voci di codec           | **BYTE**\[\] | Varia  | Matrice di strutture di informazioni sui codec |



 

Il campo voci di codice è una matrice di strutture. La tabella seguente mostra il formato di ogni voce:



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo oggetto elenco di codec</th>
<th>Tipo di dati</th>
<th>Dimensione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Type</td>
<td><strong>DWORD</strong></td>
<td>4 byte</td>
<td>Tipo di codec. I valori possibili sono i seguenti:<br/>
<ul>
<li>0x0001: codec audio</li>
<li>0x0002: codec video</li>
<li>0xFFFF: sconosciuto</li>
</ul></td>
</tr>
<tr class="even">
<td>Lunghezza del nome del codec</td>
<td><strong>DWORD</strong></td>
<td>4 byte</td>
<td>Dimensione della stringa del nome del codec, in byte, incluso il carattere <strong>null</strong> .</td>
</tr>
<tr class="odd">
<td>Nome codec</td>
<td><strong>WCHAR</strong>[]</td>
<td>Varia</td>
<td>Stringa Unicode con terminazione null che contiene il nome del codec, ad esempio &quot; Windows Media video 9 &quot; .</td>
</tr>
<tr class="even">
<td>Lunghezza Descrizione codec</td>
<td><strong>DWORD</strong></td>
<td>4 byte</td>
<td>Dimensione della stringa di descrizione del codec, in byte, incluso il carattere <strong>null</strong> .</td>
</tr>
<tr class="odd">
<td>Descrizione codec</td>
<td><strong>WCHAR</strong>[]</td>
<td>Varia</td>
<td>Stringa Unicode con terminazione null che contiene una descrizione del codec.</td>
</tr>
<tr class="even">
<td>Lunghezza informazioni codec</td>
<td><strong>DWORD</strong></td>
<td>4 byte</td>
<td>Dimensioni in byte del campo informazioni sul codec.</td>
</tr>
<tr class="odd">
<td>Informazioni sui codec</td>
<td><strong>Byte</strong>[]</td>
<td>Varia</td>
<td>Dati di codec. Il significato di questi dati dipende dal codec. In genere, questi dati indicano il formato.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Il layout del BLOB dell'attributo non corrisponde esattamente al layout dell'oggetto elenco di codec nell'intestazione ASF. In particolare, le lunghezze di stringa sono specificate in byte e includono le dimensioni del carattere di terminazione **null** .

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: seblob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore della presentazione](presentation-descriptor-attributes.md)
</dt> <dt>

[Oggetto intestazione ASF](asf-file-structure.md)
</dt> <dt>

[Descrittori di presentazione](presentation-descriptors.md)
</dt> </dl>

 

 




