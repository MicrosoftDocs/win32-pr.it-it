---
description: Criteri per i metadati delle foto per la proprietà System. GPS. DOP.
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: Criteri dei metadati delle foto di System. GPS. DOP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c33f3bfc6b958593748396124a8cfd1a7de73fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968412"
---
# <a name="systemgpsdop-photo-metadata-policy"></a>Criteri dei metadati delle foto di System. GPS. DOP

Criteri per i metadati delle foto per la proprietà [System. GPS. DOP](../properties/props-system-gps-dop.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DOP

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore può essere scritto scrivendo in System. GPS. DOPNumerator e System. GPS. DOPDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono risolti.

### <a name="precedence-of-paths-jpeg"></a>Precedenza dei percorsi (JPEG)

Se il file è in formato JPEG, i dati vengono letti, scritti e rimossi dal gestore nell'ordine seguente:



| JSON | Percorso                          | Formato disco   | Necessario |
|-------|-------------------------------|---------------|----------|
| 1     | /xmp/exif:GPSDOP              | Razionale XMP  | Sì      |
| 2     | /App1/IFD/GPS/ \\ {ushort = 11 \\ } | Razionale EXIF | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, i dati vengono letti, scritti e rimossi nell'ordine seguente:



| JSON | Percorso                     | Formato disco   | Necessario |
|-------|--------------------------|---------------|----------|
| 1     | /ifd/xmp/exif:GPSDop     | Razionale XMP  | Sì      |
| 2     | /IFD/GPS/ \\ {ushort = 11 \\ } | Razionale EXIF | No       |



 

## <a name="remarks"></a>Osservazioni

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. DOP](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
