---
description: Criteri dei metadati delle foto per la proprietà System.GPS.AltitudeRef.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: Criteri dei metadati delle foto System.GPS.AltitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca49213754f605dcf6df40dfa3ff00e2b7aeaf765008037c23da21e35ab9ddee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710698"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a>Criteri dei metadati delle foto System.GPS.AltitudeRef

Criteri dei metadati delle foto per [la proprietà System.GPS.AltitudeRef.](../properties/props-system-gps-altituderef.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ GPS \_ AltitudineRef

### <a name="description"></a>Descrizione

Indica l'altitudine utilizzata come altitudine di riferimento. Il valore 0 indica che l'altitudine si trova sopra il livello del mare. Il valore 1 indica un'altitudine sotto il livello del mare.

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ UI1

### <a name="input-type"></a>Tipo di input

Byte.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policies"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=5} |
| 2     | /xmp/exif:gpsaltituderef |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                         |
|-------|------------------------------|
| 1     | /ifd/gps/{ushort=5}          |
| 2     | /ifd/xmp/exif:gpsaltituderef |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.AltitudeRef](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
