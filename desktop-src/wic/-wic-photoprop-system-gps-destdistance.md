---
description: Criteri per i metadati delle foto per la proprietà System. GPS. DestDistance.
ms.assetid: 1bd72acb-f462-454d-aec2-72d5b4517de3
title: Criteri per i metadati delle foto di System. GPS. DestDistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc71c89ae6270f5babf08637f54baaf2cb57aae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314465"
---
# <a name="systemgpsdestdistance-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. GPS. DestDistance

Criteri per i metadati delle foto per la proprietà [System. GPS. DestDistance](../properties/props-system-gps-destdistance.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestDistance

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System. GPS. DestDistanceNumerator e System. GPS. DestDistanceDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 26} |             |
| 2     | /xmp/exif:GPSDestDistance |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 26} |             |
| 2     | /xmp/exif:GPSDestDistance |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{ushort = 26} |
| 2     | /xmp/exif:gpsdestdistance |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 26}          |             |
| 2     | /ifd/xmp/exif:GPSDestDistance |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 26}          |             |
| 2     | /ifd/xmp/exif:GPSDestDistance |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /IFD/GPS/{ushort = 26}          |
| 2     | /ifd/xmp/exif:gpsdestdistance |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. DestDistance](../properties/props-system-gps-destdistance.md)
</dt> </dl>

 

 
