---
description: Specifica un elenco di comandi di script e i parametri per un file di formato Advanced Systems (ASF). Questo attributo corrisponde all'oggetto comando script nell'intestazione ASF, definito nella specifica ASF.
ms.assetid: c85c9da4-f0b5-4055-a645-2a71cabbe4a3
title: Attributo MF_PD_ASF_SCRIPT (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03de86298d28183aa57cc80b451c4e46bb054de2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314545"
---
# <a name="mf_pd_asf_script-attribute"></a>\_ \_ Attributo script MF PD ASF \_

Specifica un elenco di comandi di script e i parametri per un file di formato Advanced Systems (ASF). Questo attributo corrisponde all'oggetto comando script nell'intestazione ASF, definito nella specifica ASF.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.

Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea il descrittore di presentazione e genera questo attributo dall'intestazione dell'oggetto del comando per script. La tabella seguente illustra il formato del BLOB:



| Campo oggetto comando script | Tipo di dati    | Dimensione    | Descrizione               |
|-----------------------------|--------------|---------|---------------------------|
| Conteggio comandi              | **DWORD**    | 4 byte | Numero di comandi script |
| Tipo di comando, comandi      | **BYTE**\[\] | Varia  | Matrice di comandi script  |



 

Il primo **valore DWORD** è il numero di comandi script, seguito da una matrice di comandi. Ogni comando di script ha il formato seguente:



| Campo oggetto comando script | Tipo di dati     | Dimensione    | Descrizione                                                              |
|-----------------------------|---------------|---------|--------------------------------------------------------------------------|
| Lunghezza del nome del comando         | **DWORD**     | 4 byte | Dimensione della stringa di comando, in byte, incluso il carattere NULL.      |
| Nome comando                | **WCHAR**\[\] | Varia  | Stringa con terminazione null che contiene il comando script.                 |
| Lunghezza del nome del tipo di comando    | **DWORD**     | 4 byte | Dimensione della stringa del tipo di comando, in byte, incluso il carattere NULL. |
| Nome tipo di comando           | **WCHAR**\[\] | Varia  | Stringa con terminazione null che contiene il tipo di comando.                   |
| Ora di presentazione           | **DWORD**     | 4 byte | Tempo di presentazione del comando in millisecondi.                        |



 

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

 

 




