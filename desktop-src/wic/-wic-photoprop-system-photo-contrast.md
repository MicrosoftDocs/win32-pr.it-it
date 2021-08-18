---
description: Criteri dei metadati delle foto per la proprietà System.Photo.Contrast.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: Criteri dei metadati delle foto System.Photo.Contrast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a9309ecab96a2244e08ebf05ff8896c792f7366c9db21d41072d2d94aacf47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087097"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a>Criteri dei metadati delle foto System.Photo.Contrast

Criteri dei metadati delle foto per [la proprietà System.Photo.Contrast.](../properties/props-system-photo-contrast.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Photo \_ Contrast

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
| 1     | /app1/ifd/exif/{ushort=41992} | ushort      |
| 2     | /xmp/exif:Contrast            | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41992} | ushort      |
| 2     | /xmp/exif:Contrast            | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=41992} |
| 2     | /xmp/exif:contrast            |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41992} | ushort      |
| 2     | /ifd/xmp/exif:Contrast   | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41992} | ushort      |
| 2     | /ifd/xmp/exif:Contrast   | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort=41992} |
| 2     | /ifd/xmp/exif:contrast   |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.Contrast](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
