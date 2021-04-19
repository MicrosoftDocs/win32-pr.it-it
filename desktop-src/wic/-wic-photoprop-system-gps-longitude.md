---
description: Criteri per i metadati delle foto per la proprietà System. GPS. longitudine.
ms.assetid: 36539e20-d00c-4bbb-b9ee-1cf5e4b8df4b
title: Criteri dei metadati della foto System. GPS. Longitudine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25eb9869bc536f97adfc8f3c0f5b1f70c8bf030f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317873"
---
# <a name="systemgpslongitude-photo-metadata-policy"></a>Criteri dei metadati della foto System. GPS. Longitudine

Criteri per i metadati delle foto per la proprietà [System. GPS. Longitudine](../properties/props-system-gps-longitude.md) .

### <a name="pkey"></a>PKEY

\_Longitudine GPS \_ pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ vettore \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore può essere scritto scrivendo in System. GPS. LongitudeNumerator e System. GPS. LongitudeDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 4} |             |
| 2     | /xmp/exif:GPSLongitude   |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 4} |             |
| 2     | /xmp/exif:GPSLongitude   |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{ushort = 4} |
| 2     | /xmp/exif:gpslongitude   |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 4}        |             |
| 2     | /ifd/xmp/exif:GPSLongitude |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 4}        |             |
| 2     | /ifd/xmp/exif:GPSLongitude |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                       |
|-------|----------------------------|
| 1     | /IFD/GPS/{ushort = 4}        |
| 2     | /ifd/xmp/exif:gpslongitude |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. Longitudine](../properties/props-system-gps-longitude.md)
</dt> </dl>

 

 
