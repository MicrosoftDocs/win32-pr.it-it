---
description: Criteri per i metadati delle foto per la proprietà System. GPS. ProcessingMethod.
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: Criteri per i metadati delle foto di System. GPS. ProcessingMethod
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bf1484eb8e8a53c65a9cd43c54b076e418d4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319109"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. GPS. ProcessingMethod

Criteri per i metadati delle foto per la proprietà [System. GPS. ProcessingMethod](../properties/props-system-gps-processingmethod.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ ProcessingMethod

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-propvariant-type"></a>Tipo di PROPVARIANT di input

VT \_ LPWSTR è preferibile, ma \_ viene accettato anche VT LPSTR.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policies"></a>Criteri di JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 27}     |             |
| 2     | /xmp/exif:GPSProcessingMethod | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 27}     |             |
| 2     | /xmp/exif:GPSProcessingMethod | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/GPS/{ushort = 27}     |
| 2     | /xmp/exif:gpsprocessingmethod |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                              | Formato disco |
|-------|-----------------------------------|-------------|
| 1     | /ifd/xmp/exif:GPSProcessingMethod | unicode     |
| 2     | /IFD/GPS/{ushort = 27}              |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                              | Formato disco |
|-------|-----------------------------------|-------------|
| 1     | /ifd/xmp/exif:GPSProcessingMethod | unicode     |
| 2     | /IFD/GPS/{ushort = 27}              |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                              |
|-------|-----------------------------------|
| 1     | /ifd/xmp/exif:gpsprocessingmethod |
| 2     | /IFD/GPS/{ushort = 27}              |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. ProcessingMethod](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
