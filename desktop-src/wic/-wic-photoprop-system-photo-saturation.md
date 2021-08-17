---
description: Criteri dei metadati delle foto per la proprietà System.Photo.Saturation.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: Criteri dei metadati delle foto di System.Photo.Saturation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be1c5be7a0663d5f57823dcb704b843f56e6076713de3682e4b12d6b533ff48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087014"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a>Criteri dei metadati delle foto di System.Photo.Saturation

Criteri dei metadati delle foto [per la proprietà System.Photo.Saturation.](../properties/props-system-photo-saturation.md)

### <a name="pkey"></a>Chiave PKEY

\_Saturazione foto PKEY \_

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
| 1     | /app1/ifd/exif/{ushort=41993} | ushort      |
| 2     | /xmp/exif:Saturation          | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41993} | ushort      |
| 2     | /xmp/exif:Saturation          | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=41993} |
| 2     | /xmp/exif:saturation          |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41993} | ushort      |
| 2     | /ifd/xmp/exif:Saturazione | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41993} | ushort      |
| 2     | /ifd/xmp/exif:Saturazione | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort=41993} |
| 2     | /ifd/xmp/exif:saturazione |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.Saturation](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
