---
description: Criteri per i metadati delle foto per la proprietà System. GPS. Track.
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: Criteri di metadati di Photo System. GPS. Track
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 773c65eec8b165c51456f3871309644638c1e2da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319108"
---
# <a name="systemgpstrack-photo-metadata-policy"></a>Criteri di metadati di Photo System. GPS. Track

Criteri per i metadati delle foto per la proprietà [System. GPS. Track](../properties/props-system-gps-track.md) .

### <a name="pkey"></a>PKEY

\_Traccia GPS \_ pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System. GPS. TrackNumerator e System. GPS. TrackDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 15} |             |
| 2     | /XMP/EXIF: GPSTrack        |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 15} |             |
| 2     | /XMP/EXIF: GPSTrack        |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{ushort = 15} |
| 2     | /XMP/EXIF: Gpstrack        |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 15}   |             |
| 2     | /IFD/XMP/EXIF: GPSTrack |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                   | Formato disco |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 15}   |             |
| 2     | /IFD/XMP/EXIF: GPSTrack |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                   |
|-------|------------------------|
| 1     | /IFD/GPS/{ushort = 15}   |
| 2     | /IFD/XMP/EXIF: Gpstrack |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. Track](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
