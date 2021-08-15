---
description: Criteri dei metadati delle foto per la proprietà System.Image.ColorSpace.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: Criteri metadati foto System.Image.ColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c7d7c9134a8bd93a12ba6cfb6bd8605e228cb6b745ad4401a94f91a2ba9ff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710421"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a>Criteri metadati foto System.Image.ColorSpace

Criteri dei metadati delle foto per [la proprietà System.Image.ColorSpace.](../properties/props-system-image-colorspace.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Image \_ ColorSpace

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

Interfaccia utente \_ VT2

### <a name="input-type"></a>Tipo di input

UShort

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=40961} | ushort      |
| 2     | /xmp/exif:ColorSpace          | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=40961} | ushort      |
| 2     | /xmp/exif:ColorSpace          | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=40961} |
| 2     | /xmp/exif:colorspace          |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=40961} | ushort      |
| 2     | /ifd/xmp/exif:ColorSpace | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=40961} | ushort      |
| 2     | /ifd/xmp/exif:ColorSpace | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort=40961} |
| 2     | /ifd/xmp/exif:colorspace |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Image.ColorSpace](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
