---
description: Criteri dei metadati delle foto per la proprietà System.Image.CompressedBitsPerPixel.
ms.assetid: e97a5c68-6d4a-44af-8096-22680f8b16b8
title: Criteri dei metadati della foto System.Image.CompressedBitsPerPixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a18cc76e22c5c409e19e08fc5a2e667ad374348bc753ffa85cd09003a8bdaf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032710"
---
# <a name="systemimagecompressedbitsperpixel-photo-metadata-policy"></a>Criteri dei metadati della foto System.Image.CompressedBitsPerPixel

Criteri dei metadati delle foto per [la proprietà System.Image.CompressedBitsPerPixel.](../properties/props-system-image-compressedbitsperpixel.md)

### <a name="pkey"></a>PKEY

Immagine PKEY \_ \_ CompressedBitsPerPixel

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System.Image.CompressedBitsPerPixelNumerator e System.Image.CompressedBitsPerPixelDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                             | Formato disco |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37122}    |             |
| 2     | /xmp/exif:CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                             |
|-------|----------------------------------|
| 1     | /app1/ifd/exif/{ushort=37122}    |
| 2     | /xmp/exif:compressedbitsperpixel |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                                 | Formato disco |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37122}             |             |
| 2     | /ifd/xmp/exif:CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                                 |
|-------|--------------------------------------|
| 1     | /ifd/exif/{ushort=37122}             |
| 2     | /ifd/xmp/exif:compressedbitsperpixel |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Image.CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md)
</dt> </dl>

 

 
