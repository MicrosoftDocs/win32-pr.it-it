---
description: Criteri per i metadati delle foto per la proprietà System. Photo. DateTaken.
ms.assetid: 800aa01b-6064-45df-a40e-6537819df4d7
title: Criteri per i metadati delle foto di System. Photo. DateTaken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc1d3fb50a9a94e4bb13b35a0a5726572d78429f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319107"
---
# <a name="systemphotodatetaken-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. DateTaken

Criteri per i metadati delle foto per la proprietà [System. Photo. DateTaken](../properties/props-system-photo-datetaken.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ DateTaken

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

FILETIME VT \_

### <a name="input-type"></a>Tipo di input

Datetime

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                  | Formato disco |
|-------|---------------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 36867}         | ascii       |
| 2     | /App13/IRB/8bimiptc/IPTC/date creato | unicode     |
| 3     | /XMP/XMP: creato                   | unicode     |
| 4     | /App1/IFD/EXIF/{ushort = 36868}         | ascii       |
| 5     | /App13/IRB/8bimiptc/IPTC/date creato | unicode     |
| 6     | /xmp/exif:DateTimeOriginal            | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                  | Formato disco |
|-------|---------------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 36867}         | ascii       |
| 2     | /App13/IRB/8bimiptc/IPTC/date creato | unicode     |
| 3     | /XMP/XMP: creato                   | unicode     |
| 4     | /App1/IFD/EXIF/{ushort = 36868}         | ascii       |
| 5     | /xmp/exif:DateTimeOriginal            | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                  |
|-------|---------------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 36867}         |
| 2     | /App1/IFD/EXIF/{ushort = 37521}         |
| 3     | /App1/IFD/EXIF/{ushort = 36868}         |
| 4     | /App1/IFD/EXIF/{ushort = 37522}         |
| 5     | /xmp/exif:DateTimeOriginal            |
| 6     | /XMP/XMP: creato                   |
| 7     | /App13/IRB/8bimiptc/IPTC/date creato |
| 8     | /App13/IRB/8bimiptc/IPTC/time creato |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                | Formato disco |
|-------|-------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 36867}            | ascii       |
| 2     | /IFD/IPTC/date creato              | unicode     |
| 3     | /IFD/XMP/XMP: creato             | unicode     |
| 4     | /IFD/EXIF/{ushort = 36868}            | ascii       |
| 5     | /IFD/IPTC/date creato              | unicode     |
| 6     | /IFD/IRB/8bimiptc/IPTC/date creato | unicode     |
| 7     | /ifd/xmp/exif:DateTimeOriginal      | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                | Formato disco |
|-------|-------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 36867}            | ascii       |
| 2     | /IFD/IPTC/date creato              | unicode     |
| 3     | /IFD/XMP/XMP: creato             | unicode     |
| 4     | /IFD/EXIF/{ushort = 36868}            | ascii       |
| 5     | /IFD/IRB/8bimiptc/IPTC/date creato | unicode     |
| 6     | /ifd/xmp/exif:DateTimeOriginal      | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                |
|-------|-------------------------------------|
| 1     | /IFD/EXIF/{ushort = 36867}            |
| 2     | /IFD/EXIF/{ushort = 37521}            |
| 3     | /IFD/EXIF/{ushort = 36868}            |
| 4     | /IFD/EXIF/{ushort = 37522}            |
| 5     | /ifd/xmp/exif:DateTimeOriginal      |
| 6     | /IFD/XMP/XMP: creato             |
| 7     | /IFD/IPTC/date creato              |
| 8     | /IFD/IPTC/time creato              |
| 9     | /IFD/IRB/8bimiptc/IPTC/date creato |
| 10    | /IFD/IRB/8bimiptc/IPTC/time creato |



 

### <a name="png-policy"></a>Criteri PNG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /\[\*\]Tempo di creazione/testo | ascii       |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 2     | /\[\*\]Tempo di creazione/testo | ascii       |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 3     | /\[\*\]Tempo di creazione/testo |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. DateTaken](../properties/props-system-photo-datetaken.md)
</dt> </dl>

 

 
