---
description: Criteri dei metadati delle foto per la proprietà System.Photo.ProgramMode.
ms.assetid: f1954dc7-d4df-4675-ab3b-a65f2354e57a
title: Criteri metadati foto System.Photo.ProgramMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260bf4ae5ca26fa26848765a76f5fdbc36eef48e2806909f46e5ab256f5acd7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032501"
---
# <a name="systemphotoprogrammode-photo-metadata-policy"></a>Criteri metadati foto System.Photo.ProgramMode

Criteri dei metadati delle foto per [la proprietà System.Photo.ProgramMode.](../properties/props-system-photo-programmode.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Photo \_ ProgramMode

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ UI4

### <a name="input-type"></a>Tipo di input

UShort

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=34850} | ushort      |
| 2     | /xmp/exif:ExposureProgram     | unicode     |
| 3     | /xmp/exif:ProgramMode         | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=34850} | ushort      |
| 2     | /xmp/exif:ExposureProgram     | unicode     |
| 3     | /xmp/exif:ProgramMode         | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=34850} |
| 2     | /xmp/exif:exposureprogram     |
| 3     | /xmp/exif:programmode         |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort=34850}      | ushort      |
| 2     | /ifd/xmp/exif:ExposureProgram | unicode     |
| 3     | /ifd/xmp/exif:ProgramMode     | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort=34850}      | ushort      |
| 2     | /ifd/xmp/exif:ExposureProgram | unicode     |
| 3     | /ifd/xmp/exif:ProgramMode     | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /ifd/exif/{ushort=34850}      |
| 2     | /ifd/xmp/exif:exposureprogram |
| 3     | /ifd/xmp/exif:programmode     |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
