---
description: Criteri dei metadati della foto per la proprietà System.Photo.RelatedSoundFile.
ms.assetid: 3b212d90-7ae2-4b7c-b77a-2017490aca40
title: Criteri dei metadati della foto System.Photo.RelatedSoundFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aae80ad39b8d3dab271aacf4815836e8b386c150ec80be63a83a4ab5937635e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549431"
---
# <a name="systemphotorelatedsoundfile-photo-metadata-policy"></a>Criteri dei metadati della foto System.Photo.RelatedSoundFile

Criteri dei metadati della foto [per la proprietà System.Photo.RelatedSoundFile.](../properties/props-system-photo-relatedsoundfile.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ RelatedSoundFile

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



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=40964} | ascii       |
| 2     | /xmp/exif:RelatedSoundFile    | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=40964} | ascii       |
| 2     | /xmp/exif:RelatedSoundFile    | unicode     |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=40964} |
| 2     | /xmp/exif:RelatedSoundFile    |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                           | Formato disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort=40964}       | ascii       |
| 2     | /ifd/xmp/exif:RelatedSoundFile | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                           | Formato disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort=40964}       | ascii       |
| 2     | /ifd/xmp/exif:RelatedSoundFile | unicode     |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                           |
|-------|--------------------------------|
| 1     | /ifd/exif/{ushort=40964}       |
| 2     | /ifd/xmp/exif:RelatedSoundFile |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md)
</dt> </dl>

 

 
