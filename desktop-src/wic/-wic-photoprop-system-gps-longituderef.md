---
description: Criteri dei metadati delle foto per la proprietà System.GPS.LongitudeRef.
ms.assetid: 6e7b3b87-70e5-4c6a-a9b3-959eab38f1f0
title: Criteri metadati foto System.GPS.LongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00908f0c76305c745e1146677f32bee7b9724c08510f273c1627ed56e139d02b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931731"
---
# <a name="systemgpslongituderef-photo-metadata-policy"></a>Criteri metadati foto System.GPS.LongitudeRef

Criteri dei metadati delle foto per [la proprietà System.GPS.LongitudeRef.](../properties/props-system-gps-longituderef.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ LongitudeRef

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ LPWSTR

### <a name="input-type"></a>Tipo di input

Stringa.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="precedence-of-paths-jpeg"></a>Precedenza dei percorsi (JPEG)

Se il file è in formato JPEG, il gestore leggerà, scriverà e rimuoverà i dati nell'ordine seguente:



| JSON | Percorso                         | Formato disco | Necessario |
|-------|------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSLongitudeRef    | Unicode     | Sì      |
| 2     | /app1/ifd/gps/ \\ {ushort=3 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, il gestore leggerà, scriverà e rimuoverà i dati nell'ordine seguente:



| JSON | Percorso                          | Formato disco | Necessario |
|-------|-------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSLongitudeRef | Unicode     | Sì      |
| 2     | /ifd/gps/ \\ {ushort=3 \\ }       | ASCII       | No       |



 

## <a name="remarks"></a>Osservazioni

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.LongitudeRef](../properties/props-system-gps-longituderef.md)
</dt> </dl>

 

 
