---
description: Criteri dei metadati delle foto per la proprietà System.GPS.VersionID.
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: Criteri dei metadati foto system.GPS.VersionID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857ecb6b172dafa2a771d9e81f8b570a89f458c79b7630a2f231ce84dbec4f9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706361"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a>Criteri dei metadati foto system.GPS.VersionID

Criteri dei metadati delle foto per [la proprietà System.GPS.VersionID.](../properties/props-system-gps-versionid.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ GPS \_ VersionID

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

Interfaccia utente \_ VT VECTOR \| VT \_

### <a name="input-type"></a>Tipo di input

Buffer

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policies"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=0} |             |
| 2     | /xmp/exif:GPSVersionID   | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=0} |             |
| 2     | /xmp/exif:GPSVersionID   | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=0} |
| 2     | /xmp/exif:gpsversionid   |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /ifd/gps/{ushort=0}        |             |
| 2     | /ifd/xmp/exif:GPSVersionID | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /ifd/gps/{ushort=0}        |             |
| 2     | /ifd/xmp/exif:GPSVersionID | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                       |
|-------|----------------------------|
| 1     | /ifd/gps/{ushort=0}        |
| 2     | /ifd/xmp/exif:gpsversionid |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.VersionID](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
