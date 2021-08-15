---
description: Criteri dei metadati delle foto per la proprietà System.GPS.Status.
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: Criteri dei metadati delle foto system.GPS.Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a99237b9fe14d9adbc97dd5de95158a8aa714caaa4a0a8440d9f3798a2155d20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710516"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a>Criteri dei metadati delle foto system.GPS.Status

Criteri dei metadati delle foto per [la proprietà System.GPS.Status.](../properties/props-system-gps-status.md)

### <a name="pkey"></a>Chiave PKEY

Stato GPS PKEY \_ \_

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT di input

VT \_ LPWSTR è preferibile, ma viene accettato anche \_ VT LPSTR.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policies"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=9} | ascii       |
| 2     | /xmp/exif:GPSStatus      | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=9} | ascii       |
| 2     | /xmp/exif:GPSStatus      | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=9} |
| 2     | /xmp/exif:gpsstatus      |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                    | Formato disco |
|-------|-------------------------|-------------|
| 1     | /ifd/gps/{ushort=9}     | ascii       |
| 2     | /ifd/xmp/exif:GPSStatus | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                    | Formato disco |
|-------|-------------------------|-------------|
| 1     | /ifd/gps/{ushort=9}     | ascii       |
| 2     | /ifd/xmp/exif:GPSStatus | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                    |
|-------|-------------------------|
| 1     | /ifd/gps/{ushort=9}     |
| 2     | /ifd/xmp/exif:gpsstatus |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.Status](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
