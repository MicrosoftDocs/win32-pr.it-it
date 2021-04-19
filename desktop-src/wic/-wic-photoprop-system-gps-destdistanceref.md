---
description: Criteri per i metadati delle foto per la proprietà System. GPS. DestDistanceRef.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: Criteri per i metadati delle foto di System. GPS. DestDistanceRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bba6e04bee00aaed868fcc02059403fe479f8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317882"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. GPS. DestDistanceRef

Criteri per i metadati delle foto per la proprietà [System. GPS. DestDistanceRef](../properties/props-system-gps-destdistanceref.md) .

### <a name="pkey"></a>PKEY

\_DESTDISTANCEREF pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-type"></a>Tipo di input

VT \_ LPWSTR o VT \_ LPSTR sono accettati.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policies"></a>Criteri di JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                         |
|-------|------------------------------|
| 1     | /App1/IFD/GPS/{ushort = 25}    |
| 2     | /xmp/exif:gpsdestdistanceref |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                             | Formato disco |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                             | Formato disco |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                             |
|-------|----------------------------------|
| 1     | /IFD/GPS/{ushort = 25}             |
| 2     | /ifd/xmp/exif:gpsdestdistanceref |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. DestDistanceRef](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
