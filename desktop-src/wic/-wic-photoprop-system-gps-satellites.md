---
description: Criteri dei metadati delle foto per la proprietà System.GPS.Satellites.
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: Criteri dei metadati foto di System.GPS.Satellites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65bdc244324df513b5029c682e9c2cb355da58f2c95d13910fe093ce2521c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964840"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a>Criteri dei metadati foto di System.GPS.Satellites

Criteri dei metadati delle foto [per la proprietà System.GPS.Satellites.](../properties/props-system-gps-satellites.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ GPS \_ Satellites

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ LPWSTR

### <a name="input-type"></a>Tipo di input

Stringa.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policies"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=8} | ascii       |
| 2     | /xmp/exif:GPSSatellites  | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=8} | ascii       |
| 2     | /xmp/exif:GPSSatellites  | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=8} |
| 2     | /xmp/exif:gpssatellites  |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                        | Formato disco |
|-------|-----------------------------|-------------|
| 1     | /ifd/gps/{ushort=8}         | ascii       |
| 2     | /ifd/xmp/exif:GPSSatellites | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                        | Formato disco |
|-------|-----------------------------|-------------|
| 1     | /ifd/gps/{ushort=8}         | ascii       |
| 2     | /ifd/xmp/exif:GPSSatellites | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                        |
|-------|-----------------------------|
| 1     | /ifd/gps/{ushort=8}         |
| 2     | /ifd/xmp/exif:gpssatellites |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.Satellites](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
