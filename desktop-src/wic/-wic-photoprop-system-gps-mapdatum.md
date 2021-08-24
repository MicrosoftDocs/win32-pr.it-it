---
description: Criteri dei metadati delle foto per la proprietà System.GPS.MapDatum.
ms.assetid: be31e98f-5114-4693-a9ef-37fea334875b
title: Criteri dei metadati foto di System.GPS.MapDatum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8bbd3671ec9e025dd2c5ea98fc36f4937abab315b09a2227fb6249d74e577da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882341"
---
# <a name="systemgpsmapdatum-photo-metadata-policy"></a>Criteri dei metadati foto di System.GPS.MapDatum

Criteri dei metadati delle foto per [la proprietà System.GPS.MapDatum.](../properties/props-system-gps-mapdatum.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ GPS \_ MapDatum

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ LPWSTR

### <a name="input-type"></a>Tipo di input

VT \_ LPWSTR è preferibile, ma viene accettata anche \_ LPSTR VT

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="precedence-of-paths-jpeg"></a>Precedenza dei percorsi (JPEG)

Se il file è in formato JPEG, il gestore leggerà, scriverà e rimuoverà i dati nell'ordine seguente:



| JSON | Percorso                          | Formato disco | Necessario |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSMapDatum         | Unicode     | Sì      |
| 2     | /app1/ifd/gps/ \\ {ushort=18 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, il gestore leggerà, scriverà e rimuoverà i dati nell'ordine seguente:



| JSON | Percorso                      | Formato disco | Necessario |
|-------|---------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSMapDatum | Unicode     | Sì      |
| 2     | /ifd/gps/ \\ {ushort=18 \\ }  | ASCII       | No       |



 

## <a name="remarks"></a>Osservazioni

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.MapDatum](../properties/props-system-gps-mapdatum.md)
</dt> </dl>

 

 
