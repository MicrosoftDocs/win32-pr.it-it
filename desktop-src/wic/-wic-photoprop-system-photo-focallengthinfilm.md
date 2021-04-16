---
description: Criteri per i metadati delle foto per la proprietà System. Photo. FocalLengthInFilm.
ms.assetid: 3ad63a7a-5ced-4e7f-a4a0-e1463f3d3fa3
title: Criteri per i metadati delle foto di System. Photo. FocalLengthInFilm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df46f3e52c447cb7902fe3cce2da201dae16d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485701"
---
# <a name="systemphotofocallengthinfilm-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. FocalLengthInFilm

Criteri per i metadati delle foto per la proprietà [System. Photo. FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md) .

### <a name="pkey"></a>PKEY

\_FOCALLENGTHINFILM pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_UI4 VT

### <a name="input-type"></a>Tipo di input

UShort

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                            | Formato disco |
|-------|---------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41989}   | ushort      |
| 2     | /xmp/exif:FocalLengthIn35mmFilm | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                            | Formato disco |
|-------|---------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41989}   | ushort      |
| 2     | /xmp/exif:FocalLengthIn35mmFilm | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                            |
|-------|---------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 41989}   |
| 2     | /xmp/exif:focallengthin35mmfilm |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                | Formato disco |
|-------|-------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41989}            | ushort      |
| 2     | /ifd/xmp/exif:FocalLengthIn35mmFilm | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                | Formato disco |
|-------|-------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41989}            | ushort      |
| 2     | /ifd/xmp/exif:FocalLengthIn35mmFilm | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                |
|-------|-------------------------------------|
| 1     | /IFD/EXIF/{ushort = 41989}            |
| 2     | /ifd/xmp/exif:focallengthin35mmfilm |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
