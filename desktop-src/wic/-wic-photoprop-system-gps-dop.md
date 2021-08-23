---
description: Criteri dei metadati delle foto per la proprietà System.GPS.DOP.
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: Criteri dei metadati foto di System.GPS.DOP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c414b7cb8648210175953e4c7b5f51a66f026cb45a06fd4d62918f2f8ac369
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087789"
---
# <a name="systemgpsdop-photo-metadata-policy"></a>Criteri dei metadati foto di System.GPS.DOP

Criteri dei metadati delle foto per [la proprietà System.GPS.DOP.](../properties/props-system-gps-dop.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ GPS \_ DOP

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore può essere scritto in System.GPS.DOPNumerator e System.GPS.DOPDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono riconciliati.

### <a name="precedence-of-paths-jpeg"></a>Precedenza dei percorsi (JPEG)

Se il file è in formato JPEG, il gestore leggerà, scriverà e rimuoverà i dati nell'ordine seguente:



| JSON | Percorso                          | Formato disco   | Necessario |
|-------|-------------------------------|---------------|----------|
| 1     | /xmp/exif:GPSDOP              | XMP razionale  | Sì      |
| 2     | /app1/ifd/gps/ \\ {ushort=11 \\ } | ExIF razionale | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, il gestore leggerà, scriverà e rimuoverà i dati nell'ordine seguente:



| JSON | Percorso                     | Formato disco   | Necessario |
|-------|--------------------------|---------------|----------|
| 1     | /ifd/xmp/exif:GPSDop     | XMP razionale  | Sì      |
| 2     | /ifd/gps/ \\ {ushort=11 \\ } | ExIF razionale | No       |



 

## <a name="remarks"></a>Osservazioni

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.DOP](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
