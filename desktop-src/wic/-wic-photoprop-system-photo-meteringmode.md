---
description: Criteri dei metadati della foto per la proprietà System.Photo.MeteringMode.
ms.assetid: cb0bf0d5-eccf-4345-a242-76769c34e02d
title: Criteri metadati foto System.Photo.MeteringMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424b14fa6216d5c88c350512d1583b311f92ef2f487e604760b1836b296d3bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964780"
---
# <a name="systemphotometeringmode-photo-metadata-policy"></a>Criteri metadati foto System.Photo.MeteringMode

Criteri dei metadati della foto per [la proprietà System.Photo.MeteringMode.](../properties/props-system-photo-meteringmode.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ MeteringMode

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

Interfaccia utente \_ VT 2

### <a name="input-type"></a>Tipo di input

UShort

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37383} | ushort      |
| 2     | /xmp/exif:MeteringMode        | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37383} | ushort      |
| 2     | /xmp/exif:MeteringMode        | unicode     |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37383} |
| 2     | /xmp/exif:meteringmode        |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /ifd/exif/{ushort=37383}   | ushort      |
| 2     | /ifd/xmp/exif:MeteringMode | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /ifd/exif/{ushort=37383}   | ushort      |
| 2     | /ifd/xmp/exif:MeteringMode | unicode     |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                       |
|-------|----------------------------|
| 1     | /ifd/exif/{ushort=37383}   |
| 2     | /ifd/xmp/exif:meteringmode |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.MeteringMode](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
