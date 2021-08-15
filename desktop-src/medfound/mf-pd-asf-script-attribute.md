---
description: Specifica un elenco di comandi script e i parametri per un file ASF (Advanced Systems Format). Questo attributo corrisponde all'oggetto comando script nell'intestazione ASF, definito nella specifica ASF.
ms.assetid: c85c9da4-f0b5-4055-a645-2a71cabbe4a3
title: MF_PD_ASF_SCRIPT attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b98a078b0196add597ab184703306a7b2eba260082e3544ae84697b70bf71822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740722"
---
# <a name="mf_pd_asf_script-attribute"></a>Attributo \_ MF PD \_ ASF \_ SCRIPT

Specifica un elenco di comandi script e i parametri per un file ASF (Advanced Systems Format). Questo attributo corrisponde all'oggetto comando script nell'intestazione ASF, definito nella specifica ASF.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Questo attributo si applica ai descrittori di presentazione per il contenuto asf.

Il [**metodo IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea il descrittore di presentazione e genera questo attributo dall'intestazione Script Command Object. La tabella seguente illustra il formato del BLOB:



| Campo Oggetto comando script | Tipo di dati    | Dimensione    | Descrizione               |
|-----------------------------|--------------|---------|---------------------------|
| Conteggio comandi              | **Dword**    | 4 byte | Numero di comandi script |
| Tipo di comando, comandi      | **BYTE**\[\] | Varia  | Matrice di comandi script  |



 

Il primo **valore DWORD** è il numero di comandi script, seguito da una matrice di comandi. Ogni comando script ha il formato seguente:



| Campo Oggetto comando script | Tipo di dati     | Dimensione    | Descrizione                                                              |
|-----------------------------|---------------|---------|--------------------------------------------------------------------------|
| Lunghezza nome comando         | **Dword**     | 4 byte | Dimensioni della stringa di comando, in byte, incluso il carattere NULL.      |
| Nome comando                | **Wchar**\[\] | Varia  | Stringa con terminazione Null che contiene il comando script.                 |
| Lunghezza del nome del tipo di comando    | **Dword**     | 4 byte | Dimensioni della stringa del tipo di comando, in byte, incluso il carattere NULL. |
| Nome del tipo di comando           | **Wchar**\[\] | Varia  | Stringa con terminazione Null che contiene il tipo di comando.                   |
| Ora di presentazione           | **Dword**     | 4 byte | Ora di presentazione del comando in millisecondi.                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
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

 

 




