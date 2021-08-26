---
description: Criteri dei metadati della foto per la proprietà System.Photo.EXIFVersion.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: Criteri metadati foto System.Photo.EXIFVersion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eee0fdac7ba8e86321d4a055cb6c37c4e9c7bad3f5bcfced548cc2485b3347c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882031"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a>Criteri metadati foto System.Photo.EXIFVersion

Criteri dei metadati della foto per [la proprietà System.Photo.EXIFVersion.](../properties/props-system-photo-exifversion.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ EXIFVersion

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ LPWSTR

### <a name="input-type"></a>Tipo di input

Stringa.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco   |
|-------|-------------------------------|---------------|
| 1     | /app1/ifd/exif/{ushort=36864} | Versione di \_ exif |
| 2     | /xmp/exif:ExifVersion         | unicode       |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco   |
|-------|-------------------------------|---------------|
| 1     | /app1/ifd/exif/{ushort=36864} | Versione di \_ exif |
| 2     | /xmp/exif:ExifVersion         | unicode       |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=36864} |
| 2     | /xmp/exif:ExifVersion         |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                      | Formato disco   |
|-------|---------------------------|---------------|
| 1     | /ifd/exif/{ushort=36864}  | Versione di \_ exif |
| 2     | /ifd/xmp/exif:ExifVersion | unicode       |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco   |
|-------|---------------------------|---------------|
| 1     | /ifd/exif/{ushort=36864}  | Versione di \_ exif |
| 2     | /ifd/xmp/exif:ExifVersion | unicode       |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort=36864}  |
| 2     | /ifd/xmp/exif:ExifVersion |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.EXIFVersion](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
