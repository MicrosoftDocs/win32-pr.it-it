---
description: Criteri dei metadati delle foto per la proprietà System.GPS.DestLongitude.
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: Criteri dei metadati delle foto di System.GPS.DestLongitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 917c65dbd580b00cf25603e04050386383967e3a70c1896405346652667ef5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087842"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a>Criteri dei metadati delle foto di System.GPS.DestLongitude

Criteri dei metadati delle foto per [la proprietà System.GPS.DestLongitude.](../properties/props-system-gps-destlongitude.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestLongitude

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ VECTOR \| VT \_ R8

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT di input

VT \_ VECTOR \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System.GPS.DestLongitudeNumerator e System.GPS.DestLongitudeDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=22}  |             |
| 2     | /xmp/exif:GPSDestLongitude |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=22}  |             |
| 2     | /xmp/exif:GPSDestLongitude |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                       |
|-------|----------------------------|
| 1     | /app1/ifd/gps/{ushort=22}  |
| 2     | /xmp/exif:gpsdestlongitude |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                           | Formato disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/gps/{ushort=22}           |             |
| 2     | /ifd/xmp/exif:GPSDestLongitude |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                           | Formato disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/gps/{ushort=22}           |             |
| 2     | /ifd/xmp/exif:GPSDestLongitude |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                           |
|-------|--------------------------------|
| 1     | /ifd/gps/{ushort=22}           |
| 2     | /ifd/xmp/exif:gpsdestlongitude |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.DestLongitude](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
