---
description: Criteri per i metadati delle foto per la proprietà System. GPS. satellites.
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: Criteri dei metadati delle foto di System. GPS. Satellites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980393accdb1bee3d2a44dd539f3c9fb169c648b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312967"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a>Criteri dei metadati delle foto di System. GPS. Satellites

Criteri per i metadati delle foto per la proprietà [System. GPS. Satellites](../properties/props-system-gps-satellites.md) .

### <a name="pkey"></a>PKEY

\_ \_ Satelliti GPS pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-type"></a>Tipo di input

Stringa.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policies"></a>Criteri di JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 8} | ascii       |
| 2     | /xmp/exif:GPSSatellites  | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 8} | ascii       |
| 2     | /xmp/exif:GPSSatellites  | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{ushort = 8} |
| 2     | /xmp/exif:gpssatellites  |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                        | Formato disco |
|-------|-----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 8}         | ascii       |
| 2     | /ifd/xmp/exif:GPSSatellites | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                        | Formato disco |
|-------|-----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 8}         | ascii       |
| 2     | /ifd/xmp/exif:GPSSatellites | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                        |
|-------|-----------------------------|
| 1     | /IFD/GPS/{ushort = 8}         |
| 2     | /ifd/xmp/exif:gpssatellites |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. Satellites](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
