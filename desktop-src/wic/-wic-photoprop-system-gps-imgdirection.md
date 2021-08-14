---
description: Criteri dei metadati delle foto per la proprietà System.GPS.ImgDirection.
ms.assetid: c9a0f5de-4010-4251-a5d5-8728b7ae6d33
title: Criteri dei metadati delle foto di System.GPS.ImgDirection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43544458c4b6a64df1d396426ebbe487d80324d24dd10c2f8f6f0e548d9eca99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710671"
---
# <a name="systemgpsimgdirection-photo-metadata-policy"></a>Criteri dei metadati delle foto di System.GPS.ImgDirection

Criteri dei metadati delle foto per [la proprietà System.GPS.ImgDirection.](../properties/props-system-gps-imgdirection.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ ImgDirection

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore può essere scritto in System.GPS.ImgDirectionNumerator e System.GPS.ImgDirectionDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=17} |             |
| 2     | /xmp/exif:GPSImgDirection |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=17} |             |
| 2     | /xmp/exif:GPSImgDirection |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=17} |
| 2     | /xmp/exif:gpsimgdirection |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=17}          |             |
| 2     | /ifd/xmp/exif:GPSImgDirection |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=17}          |             |
| 2     | /ifd/xmp/exif:GPSImgDirection |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /ifd/gps/{ushort=17}          |
| 2     | /ifd/xmp/exif:gpsimgdirection |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.ImgDirection](../properties/props-system-gps-imgdirection.md)
</dt> </dl>

 

 
