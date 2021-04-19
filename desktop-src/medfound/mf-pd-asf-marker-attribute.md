---
description: Specifica i marcatori in un file di formato Advanced Systems (ASF). Questo attributo corrisponde all'oggetto marcatore nell'intestazione ASF, definito nella specifica ASF.
ms.assetid: 6458eb5f-72a2-4723-b26b-b63516aa2df3
title: Attributo MF_PD_ASF_MARKER (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ae9c5a6cfd79924b95a3b15a7146539d630aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318059"
---
# <a name="mf_pd_asf_marker-attribute"></a>\_ \_ \_ Attributo marcatore ASF MF PD

Specifica i marcatori in un file di formato Advanced Systems (ASF). Questo attributo corrisponde all'oggetto marcatore nell'intestazione ASF, definito nella specifica ASF.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.

Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea il descrittore di presentazione e genera questo attributo dall'oggetto marcatore. La tabella seguente illustra il formato del BLOB:



| Campo oggetto marcatore | Tipo di dati    | Dimensione    | Descrizione       |
|---------------------|--------------|---------|-------------------|
| Conteggio marcatori       | **DWORD**    | 4 byte | Numero di marcatori |
| Indicatori             | **BYTE**\[\] | Varia  | Matrice di marcatori  |



 

Il primo **valore DWORD** è il numero di marcatori, seguiti da una matrice di marcatori. Ogni marcatore ha il formato seguente:



| Campo oggetto marcatore       | Tipo di dati     | Dimensione    | Descrizione                                                                       |
|---------------------------|---------------|---------|-----------------------------------------------------------------------------------|
| Lunghezza Descrizione indicatore | **DWORD**     | 4 byte | Dimensione della stringa di descrizione, in byte, incluso il carattere NULL.           |
| Descrizione indicatore        | **WCHAR**\[\] | Varia  | Stringa con terminazione null che descrive il marcatore.                                 |
| Ora di presentazione         | **LONGLONG**  | 8 byte | Tempo di presentazione del marcatore, in unità di 100 nanosecondi.                         |
| Ora di invio                 | **LONGLONG**  | 8 byte | Tempo di invio della voce del marcatore, in millisecondi.                                   |
| Offset                    | **UINT64**    | 8 byte | Offset, in byte, nell'oggetto dati che specifica la posizione del mercato. |



 

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

 

 




