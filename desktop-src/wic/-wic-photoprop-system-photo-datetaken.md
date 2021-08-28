---
description: Criteri dei metadati delle foto per la proprietà System.Photo.DateTaken.
ms.assetid: 800aa01b-6064-45df-a40e-6537819df4d7
title: Criteri metadati foto System.Photo.DateTaken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691476c704d3fdbc4ff5e01467031f2b41884ccb16be537904484a9d01c8fa18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087077"
---
# <a name="systemphotodatetaken-photo-metadata-policy"></a>Criteri metadati foto System.Photo.DateTaken

Criteri dei metadati delle foto per [la proprietà System.Photo.DateTaken.](../properties/props-system-photo-datetaken.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Photo \_ DateTaken

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ FILETIME

### <a name="input-type"></a>Tipo di input

Datetime

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                                  | Formato disco |
|-------|---------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=36867}         | ascii       |
| 2     | /app13/irb/8bimiptc/iptc/date created | unicode     |
| 3     | /xmp/xmp:CreateDate                   | unicode     |
| 4     | /app1/ifd/exif/{ushort=36868}         | ascii       |
| 5     | /app13/irb/8bimiptc/iptc/date created | unicode     |
| 6     | /xmp/exif:DateTimeOriginal            | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                  | Formato disco |
|-------|---------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=36867}         | ascii       |
| 2     | /app13/irb/8bimiptc/iptc/date created | unicode     |
| 3     | /xmp/xmp:CreateDate                   | unicode     |
| 4     | /app1/ifd/exif/{ushort=36868}         | ascii       |
| 5     | /xmp/exif:DateTimeOriginal            | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                  |
|-------|---------------------------------------|
| 1     | /app1/ifd/exif/{ushort=36867}         |
| 2     | /app1/ifd/exif/{ushort=37521}         |
| 3     | /app1/ifd/exif/{ushort=36868}         |
| 4     | /app1/ifd/exif/{ushort=37522}         |
| 5     | /xmp/exif:DateTimeOriginal            |
| 6     | /xmp/xmp:CreateDate                   |
| 7     | /app13/irb/8bimiptc/iptc/date created |
| 8     | /app13/irb/8bimiptc/iptc/time created |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                                | Formato disco |
|-------|-------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=36867}            | ascii       |
| 2     | /ifd/iptc/date created              | unicode     |
| 3     | /ifd/xmp/xmp:CreateDate             | unicode     |
| 4     | /ifd/exif/{ushort=36868}            | ascii       |
| 5     | /ifd/iptc/date created              | unicode     |
| 6     | /ifd/irb/8bimiptc/iptc/date created | unicode     |
| 7     | /ifd/xmp/exif:DateTimeOriginal      | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                | Formato disco |
|-------|-------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=36867}            | ascii       |
| 2     | /ifd/iptc/date created              | unicode     |
| 3     | /ifd/xmp/xmp:CreateDate             | unicode     |
| 4     | /ifd/exif/{ushort=36868}            | ascii       |
| 5     | /ifd/irb/8bimiptc/iptc/date created | unicode     |
| 6     | /ifd/xmp/exif:DateTimeOriginal      | unicode     |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                                |
|-------|-------------------------------------|
| 1     | /ifd/exif/{ushort=36867}            |
| 2     | /ifd/exif/{ushort=37521}            |
| 3     | /ifd/exif/{ushort=36868}            |
| 4     | /ifd/exif/{ushort=37522}            |
| 5     | /ifd/xmp/exif:DateTimeOriginal      |
| 6     | /ifd/xmp/xmp:CreateDate             |
| 7     | /ifd/iptc/date created              |
| 8     | /ifd/iptc/time created              |
| 9     | /ifd/irb/8bimiptc/iptc/date created |
| 10    | /ifd/irb/8bimiptc/iptc/time created |



 

### <a name="png-policy"></a>Criteri PNG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /\[\*\]tEXt/Creation Time | ascii       |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 2     | /\[\*\]tEXt/Creation Time | ascii       |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 3     | /\[\*\]tEXt/Creation Time |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.DateTaken](../properties/props-system-photo-datetaken.md)
</dt> </dl>

 

 
