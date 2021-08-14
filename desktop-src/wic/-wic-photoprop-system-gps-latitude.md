---
description: Criteri dei metadati delle foto per la proprietà System.GPS.Latitude.
ms.assetid: 0f8cea07-da96-4d2a-8444-6073b51e1236
title: Criteri dei metadati delle foto di System.GPS.Latitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41dd1eb0ee21ab02eeb8c83d5ea84f28c07c2811929f2b8c973cace4a4a06fd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710625"
---
# <a name="systemgpslatitude-photo-metadata-policy"></a>Criteri dei metadati delle foto di System.GPS.Latitude

Criteri dei metadati delle foto per [la proprietà System.GPS.Latitude.](../properties/props-system-gps-latitude.md)

### <a name="pkey"></a>PKEY

\_Latitudine GPS \_ PKEY

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ VECTOR \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore può essere scritto in System.GPS.LatitudeNumerator e System.GPS.LatitudeDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=2} |             |
| 2     | /xmp/exif:GPSLatitude    |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=2} |             |
| 2     | /xmp/exif:GPSLatitude    |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=2} |
| 2     | /xmp/exif:gpslatitude    |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=2}       |             |
| 2     | /ifd/xmp/exif:GPSLatitude |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=2}       |             |
| 2     | /ifd/xmp/exif:GPSLatitude |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /ifd/gps/{ushort=2}       |
| 2     | /ifd/xmp/exif:gpslatitude |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.Latitude](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
