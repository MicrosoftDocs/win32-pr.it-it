---
description: Criteri dei metadati delle foto per la proprietà System.GPS.LatitudeRef.
ms.assetid: 057015fd-38b7-4053-b611-72565975cc58
title: Criteri dei metadati delle foto system.GPS.LatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04412af5359e39eaf8e033b059b1c5460e33f6d7537c4763b009b11010fbe87a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087249"
---
# <a name="systemgpslatituderef-photo-metadata-policy"></a>Criteri dei metadati delle foto system.GPS.LatitudeRef

Criteri dei metadati delle foto per [la proprietà System.GPS.LatitudeRef.](../properties/props-system-gps-latitude.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ LatitudeRef

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ LPWSTR

### <a name="input-type"></a>Tipo di input

VT \_ LPWSTR è preferibile, ma viene accettato anche \_ VT LPSTR.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="precedence-of-paths-jpeg"></a>Precedenza dei percorsi (JPEG)

Se il file è in formato JPEG, il gestore leggerà, scriverà e rimuoverà i dati nell'ordine seguente:



| JSON | Percorso                         | Formato disco | Necessario |
|-------|------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSLatitudeRef     | Unicode     | Sì      |
| 2     | /app1/ifd/gps/ \\ {ushort=1 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, il gestore leggerà, scriverà e rimuoverà i dati nell'ordine seguente:



| JSON | Percorso                         | Formato disco | Necessario |
|-------|------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSLatitudeRef | Unicode     | Sì      |
| 2     | /ifd/gps/ \\ {ushort=1 \\ }      | ASCII       | No       |



 

## <a name="remarks"></a>Osservazioni

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.LatitudeRef](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
