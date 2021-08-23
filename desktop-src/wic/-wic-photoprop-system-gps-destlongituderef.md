---
description: Criteri dei metadati delle foto per la proprietà System.GPS.DestLongitudeRef.
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: Criteri metadati foto System.GPS.DestLongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fca1095138b35767da94e2eeed85a11892ba6edea3fa32f37ea6bd85fb76462
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964950"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a>Criteri metadati foto System.GPS.DestLongitudeRef

Criteri dei metadati delle foto per [la proprietà System.GPS.DestLongitudeRef.](../properties/props-system-gps-destlongituderef.md)

### <a name="pkey"></a>Chiave PKEY

GPS \_ PKEY. DestLongitudeRef

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT di input

VT \_ LPWSTR è preferibile, ma viene accettato anche \_ VT LPSTR.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="precedence-of-paths-jpeg"></a>Precedenza dei percorsi (JPEG)

Se il file è in formato JPEG, il gestore leggerà, scriverà e rimuoverà i dati nell'ordine seguente:



| JSON | Percorso                          | Formato disco | Necessario |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSDestLongitudeRef | Unicode     | Sì      |
| 2     | /app1/ifd/gps/ \\ {ushort=21 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, il gestore leggerà, scriverà e rimuoverà i dati nell'ordine seguente:



| JSON | Percorso                              | Formato disco | Necessario |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSDestLongitudeRef | Unicode     | Sì      |
| 2     | /ifd/gps/ \\ {ushort=21 \\ }          | ASCII       | No       |



 

## <a name="remarks"></a>Osservazioni

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.DestLongitudeRef](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
