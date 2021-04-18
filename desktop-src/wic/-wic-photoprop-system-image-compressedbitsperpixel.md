---
description: Criteri per i metadati delle foto per la proprietà System. image. CompressedBitsPerPixel.
ms.assetid: e97a5c68-6d4a-44af-8096-22680f8b16b8
title: Criteri per i metadati delle foto di System. image. CompressedBitsPerPixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45b3b1e8b29cdf992cd3b451a2e8a43947139a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312956"
---
# <a name="systemimagecompressedbitsperpixel-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. image. CompressedBitsPerPixel

Criteri per i metadati delle foto per la proprietà [System. image. CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md) .

### <a name="pkey"></a>PKEY

Immagine di PKEY \_ \_ CompressedBitsPerPixel

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System. image. CompressedBitsPerPixelNumerator e System. image. CompressedBitsPerPixelDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                             | Formato disco |
|-------|----------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37122}    |             |
| 2     | /xmp/exif:CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                             |
|-------|----------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37122}    |
| 2     | /xmp/exif:compressedbitsperpixel |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                                 | Formato disco |
|-------|--------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37122}             |             |
| 2     | /ifd/xmp/exif:CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                 |
|-------|--------------------------------------|
| 1     | /IFD/EXIF/{ushort = 37122}             |
| 2     | /ifd/xmp/exif:compressedbitsperpixel |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. image. CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md)
</dt> </dl>

 

 
