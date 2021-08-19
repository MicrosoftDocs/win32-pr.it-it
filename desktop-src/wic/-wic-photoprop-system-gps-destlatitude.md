---
description: Criteri dei metadati delle foto per la proprietà System.GPS.DestLatitude.
ms.assetid: 05284291-977d-49b8-ad92-365f68384960
title: Criteri dei metadati delle foto di System.GPS.DestLatitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57cce67b13235933816e244e17b5c761e1f0d230055eb82d683eb610579e5aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882351"
---
# <a name="systemgpsdestlatitude-photo-metadata-policy"></a>Criteri dei metadati delle foto di System.GPS.DestLatitude

Criteri dei metadati delle foto per [la proprietà System.GPS.DestLatitude.](../properties/props-system-gps-destlatitude.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestLatitude

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ VECTOR \| VT \_ R8

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT di input

VT \_ VECTOR \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System.GPS.DestLatitudeNumerator e System.GPS.DestLatitudeDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=20} |             |
| 2     | /xmp/exif:GPSDestLatitude |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=20} |             |
| 2     | /xmp/exif:GPSDestLatitude |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=20} |
| 2     | /xmp/exif:gpsdestlatitude |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=20}          |             |
| 2     | /ifd/xmp/exif:GPSDestLatitude |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=20}          |             |
| 2     | /ifd/xmp/exif:GPSDestLatitude |             |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /ifd/gps/{ushort=20}          |
| 2     | /ifd/xmp/exif:gpsdestlatitude |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.DestLatitude](../properties/props-system-gps-destlatitude.md)
</dt> </dl>

 

 
