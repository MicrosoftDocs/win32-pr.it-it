---
description: Criteri per i metadati delle foto per la proprietà System. Photo. RelatedSoundFile.
ms.assetid: 3b212d90-7ae2-4b7c-b77a-2017490aca40
title: Criteri per i metadati delle foto di System. Photo. RelatedSoundFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07a29adb71f572868f21b1b8427e71b09616b24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968115"
---
# <a name="systemphotorelatedsoundfile-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. RelatedSoundFile

Criteri per i metadati delle foto per la proprietà [System. Photo. RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ RelatedSoundFile

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-type"></a>Tipo di input

Stringa.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 40964} | ascii       |
| 2     | /xmp/exif:RelatedSoundFile    | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 40964} | ascii       |
| 2     | /xmp/exif:RelatedSoundFile    | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 40964} |
| 2     | /xmp/exif:RelatedSoundFile    |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                           | Formato disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 40964}       | ascii       |
| 2     | /ifd/xmp/exif:RelatedSoundFile | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                           | Formato disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 40964}       | ascii       |
| 2     | /ifd/xmp/exif:RelatedSoundFile | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                           |
|-------|--------------------------------|
| 1     | /IFD/EXIF/{ushort = 40964}       |
| 2     | /ifd/xmp/exif:RelatedSoundFile |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md)
</dt> </dl>

 

 
