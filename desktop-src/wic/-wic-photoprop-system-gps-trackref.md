---
description: Criteri dei metadati delle foto per la proprietà System.GPS.TrackRef.
ms.assetid: e6912177-8add-4520-b396-c28060b359c7
title: Criteri dei metadati delle foto System.GPS.TrackRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a523f801b8e82fc4191b54bf0bb5fee659ab4f5b09c326d5d1adf14c713f13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087179"
---
# <a name="systemgpstrackref-photo-metadata-policy"></a>Criteri dei metadati delle foto System.GPS.TrackRef

Criteri dei metadati delle foto per [la proprietà System.GPS.TrackRef.](../properties/props-system-gps-trackref.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ GPS \_ TrackRef

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ LPWSTR

### <a name="input-type"></a>Tipo di input

string

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policies"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=14} | ascii       |
| 2     | /xmp/exif:GPSTrackRef     | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=14} | ascii       |
| 2     | /xmp/exif:GPSTrackRef     | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=14} |
| 2     | /xmp/exif:gpstrackref     |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=14}      | ascii       |
| 2     | /ifd/xmp/exif:GPSTrackRef | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=14}      | ascii       |
| 2     | /ifd/xmp/exif:GPSTrackRef | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /ifd/gps/{ushort=14}      |
| 2     | /ifd/xmp/exif:gpstrackref |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.TrackRef](../properties/props-system-gps-trackref.md)
</dt> </dl>

 

 
