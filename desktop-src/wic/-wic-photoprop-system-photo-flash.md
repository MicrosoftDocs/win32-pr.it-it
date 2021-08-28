---
description: Criteri dei metadati delle foto per la proprietà System.Photo.Flash.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: Criteri dei metadati delle foto System.Photo.Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7798e88c40193cac5c577f1960eee96fc2d868
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880074"
---
# <a name="systemphotoflash-photo-metadata-policy"></a>Criteri dei metadati delle foto System.Photo.Flash

Criteri dei metadati delle foto per [la proprietà System.Photo.Flash.](../properties/props-system-photo-exposuretime.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Photo \_ Flash

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ UI1 (se lo schema di origine era XMP) o VT \_ UI2 (se lo schema di origine era EXIF)

\\lang1036

### <a name="input-type"></a>Tipo di input

VT \_ UI1, VTUI2, VT \_ UI4

\\lang1033

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                             | Formato disco |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37385}    | ushort      |
| 2     | /xmp/ &lt; xmpstruct &gt; exif:Flash |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                             | Formato disco |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37385}    | ushort      |
| 2     | /xmp/ &lt; xmpstruct &gt; exif:Flash |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                             |
|-------|----------------------------------|
| 1     | /app1/ifd/exif/{ushort=37385}    |
| 2     | /xmp/ &lt; xmpstruct &gt; exif:flash |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                                 | Formato disco |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37385}             | ushort      |
| 2     | /ifd/xmp/ &lt; xmpstruct &gt; exif:Flash |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                 | Formato disco |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37385}             | ushort      |
| 2     | /ifd/xmp/ &lt; xmpstruct &gt; exif:Flash |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                 |
|-------|--------------------------------------|
| 1     | /ifd/exif/{ushort=37385}             |
| 2     | /ifd/xmp/ &lt; xmpstruct &gt; exif:flash |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.Flash](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
