---
description: Criteri dei metadati delle foto per la proprietà System.GPS.DestLatitudeRef.
ms.assetid: 8a13642a-0d29-4193-9784-f716bc428c72
title: Criteri metadati foto System.GPS.DestLatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7abdd7cb7332a15040f329469ec774214840b8eb1a4a8d67ba42662ce3c2c3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032885"
---
# <a name="systemgpsdestlatituderef-photo-metadata-policy"></a>Criteri metadati foto System.GPS.DestLatitudeRef

Criteri dei metadati delle foto per [la proprietà System.GPS.DestLatitudeRef.](../properties/props-system-gps-destlatituderef.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ GPS \_ DestLatitudeRef

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ LPWSTR

### <a name="input-type"></a>Tipo di input

VT \_ LPWSTR è preferibile, ma VT \_ LPSTR è accettato.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="precedence-of-paths-jpeg"></a>Precedenza dei percorsi (JPEG)

Se il file è in formato JPEG, il gestore leggerà, scriverà e rimuoverà i dati nell'ordine seguente:



| JSON | Percorso                          | Formato disco | Necessario |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSDestLatitudeRef  | Unicode     | Sì      |
| 2     | /app1/ifd/gps/ \\ {ushort=19 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, il gestore leggerà, scriverà e rimuoverà i dati nell'ordine seguente:



| JSON | Percorso                             | Formato disco | Necessario |
|-------|----------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSDestLatitudeRef | Unicode     | Sì      |
| 2     | /ifd/gps/ \\ {ushort=19 \\ }         | ASCII       | No       |



 

## <a name="remarks"></a>Osservazioni

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.DestLatitudeRef](../properties/props-system-gps-destlatituderef.md)
</dt> </dl>

 

 
