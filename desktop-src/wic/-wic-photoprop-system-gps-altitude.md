---
description: Criteri per i metadati delle foto per la proprietà System. GPS. Altitude.
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: Criteri dei metadati della foto System. GPS. Altitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003d39d135c625a01035c023b5d7dc8d890b3b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317886"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a>Criteri dei metadati della foto System. GPS. Altitude

Criteri per i metadati delle foto per la proprietà [System. GPS. Altitude](../properties/props-system-gps-altitude.md) .

### <a name="pkey"></a>PKEY

\_Altitudine GPS \_ pkey

### <a name="description"></a>Descrizione

L'altitudine è indicata come un valore assoluto a cui si fa riferimento in metri.

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ R8

### <a name="input-propvariant-type"></a>Tipo di PROPVARIANT di input

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore può essere scritto scrivendo in System. GPS. Altitude. numerator e System. GPS. Altitude. denominator. Non può essere scritto direttamente. I percorsi di scrittura nelle tabelle seguenti indicano la posizione in cui il valore può essere salvato quando viene generato e non quando viene scritto direttamente. Quando viene letto il valore, i valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{ushort = 6} |
| 2     | /xmp/exif:gpsaltitude    |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |     |
|-------|---------------------------|-----|
| 1     | /IFD/GPS/{ushort = 6}       |     |
| 2     | /ifd/xmp/exif:gpsaltitude |     |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. Altitude](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
