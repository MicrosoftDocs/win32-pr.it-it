---
description: Criteri per i metadati delle foto per la proprietà System. GPS. AltitudeRef.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: Criteri per i metadati delle foto di System. GPS. AltitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db600d218d72014c49fd3f0a8b5eb11dd4c467d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317885"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. GPS. AltitudeRef

Criteri per i metadati delle foto per la proprietà [System. GPS. AltitudeRef](../properties/props-system-gps-altituderef.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ AltitudeRef

### <a name="description"></a>Descrizione

Indica l'altitudine utilizzata come altitudine di riferimento. Il valore 0 indica che l'altitudine è superiore al livello del mare. Il valore 1 indica un'altitudine sotto il livello Sea.

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_Ui1 VT

### <a name="input-type"></a>Tipo di input

Byte.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policies"></a>Criteri di JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{ushort = 5} |
| 2     | /xmp/exif:gpsaltituderef |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                         |
|-------|------------------------------|
| 1     | /IFD/GPS/{ushort = 5}          |
| 2     | /ifd/xmp/exif:gpsaltituderef |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. AltitudeRef](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
