---
description: Criteri dei metadati delle foto per la proprietà System.GPS.Track.
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: Criteri dei metadati delle foto System.GPS.Track
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89aee05d0c55e78fe4e55d7eacd8a8d0992fcb8d9f56312164c652cbc0bd81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205532"
---
# <a name="systemgpstrack-photo-metadata-policy"></a>Criteri dei metadati delle foto System.GPS.Track

Criteri dei metadati delle foto per [la proprietà System.GPS.Track.](../properties/props-system-gps-track.md)

### <a name="pkey"></a>Chiave PKEY

Traccia GPS PKEY \_ \_

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System.GPS.TrackNumerator e System.GPS.TrackDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=15} |             |
| 2     | /xmp/exif:GPSTrack        |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=15} |             |
| 2     | /xmp/exif:GPSTrack        |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=15} |
| 2     | /xmp/exif:gpstrack        |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /ifd/gps/{ushort=15}   |             |
| 2     | /ifd/xmp/exif:GPSTrack |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /ifd/gps/{ushort=15}   |             |
| 2     | /ifd/xmp/exif:GPSTrack |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                   |
|-------|------------------------|
| 1     | /ifd/gps/{ushort=15}   |
| 2     | /ifd/xmp/exif:gpstrack |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.Track](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
