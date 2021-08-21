---
description: Criteri dei metadati delle foto per la proprietà System.GPS.DestDistance.
ms.assetid: 1bd72acb-f462-454d-aec2-72d5b4517de3
title: System.GPS.DestDistance Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ff376752d6d97a9a6c0c84e583f0a65521c130dc3ce382ab549e3a6b1f5fb33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033007"
---
# <a name="systemgpsdestdistance-photo-metadata-policy"></a>System.GPS.DestDistance Photo Metadata Policy

Criteri dei metadati delle foto per [la proprietà System.GPS.DestDistance.](../properties/props-system-gps-destdistance.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ GPS \_ DestDistance

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System.GPS.DestDistanceNumerator e System.GPS.DestDistanceDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=26} |             |
| 2     | /xmp/exif:GPSDestDistance |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=26} |             |
| 2     | /xmp/exif:GPSDestDistance |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=26} |
| 2     | /xmp/exif:gpsdestdistance |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=26}          |             |
| 2     | /ifd/xmp/exif:GPSDestDistance |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=26}          |             |
| 2     | /ifd/xmp/exif:GPSDestDistance |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /ifd/gps/{ushort=26}          |
| 2     | /ifd/xmp/exif:gpsdestdistance |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.DestDistance](../properties/props-system-gps-destdistance.md)
</dt> </dl>

 

 
