---
description: Criteri dei metadati delle foto per la proprietà System.GPS.DestBearing.
ms.assetid: ccc31b3d-27fd-4a8c-a304-852cf6114ec5
title: Criteri dei metadati delle foto di System.GPS.DestBearing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598ef1e759f75dfb4851f2f3f435b53db1f875421c3d21446ae3de33f688cefd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205512"
---
# <a name="systemgpsdestbearing-photo-metadata-policy"></a>Criteri dei metadati delle foto di System.GPS.DestBearing

Criteri dei metadati delle foto per [la proprietà System.GPS.DestBearing.](../properties/props-system-gps-destbearing.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestBearing

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore può essere scritto in System.GPS.DestBearingNumerator e System.GPS.DestBearingDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=24} |             |
| 2     | /xmp/exif:GPSDestBearing  |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=24} |             |
| 2     | /xmp/exif:GPSDestBearing  |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                      | Formato del disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=24} |             |
| 2     | /xmp/exif:gpsdestbearing  |             |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=24}         |             |
| 2     | /ifd/xmp/exif:GPSDestBearing |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=24}         |             |
| 2     | /ifd/xmp/exif:GPSDestBearing |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                         |
|-------|------------------------------|
| 1     | /ifd/gps/{ushort=24}         |
| 2     | /ifd/xmp/exif:gpsdestbearing |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.DestBearing](../properties/props-system-gps-destbearing.md)
</dt> </dl>

 

 
