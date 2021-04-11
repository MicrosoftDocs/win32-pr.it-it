---
description: Criteri per i metadati delle foto per la proprietà System. GPS. LatitudeRef.
ms.assetid: 057015fd-38b7-4053-b611-72565975cc58
title: Criteri per i metadati delle foto di System. GPS. LatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782fbcecbed90c9c75c1ae5fe9d5409496f842a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233022"
---
# <a name="systemgpslatituderef-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. GPS. LatitudeRef

Criteri per i metadati delle foto per la proprietà [System. GPS. LatitudeRef](../properties/props-system-gps-latitude.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ LatitudeRef

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-type"></a>Tipo di input

VT \_ LPWSTR è preferibile, ma \_ viene accettato anche VT LPSTR.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="precedence-of-paths-jpeg"></a>Precedenza dei percorsi (JPEG)

Se il file è in formato JPEG, i dati vengono letti, scritti e rimossi dal gestore nell'ordine seguente:



| JSON | Percorso                         | Formato disco | Necessario |
|-------|------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSLatitudeRef     | Unicode     | Sì      |
| 2     | /App1/IFD/GPS/ \\ {ushort = 1 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, i dati vengono letti, scritti e rimossi nell'ordine seguente:



| JSON | Percorso                         | Formato disco | Necessario |
|-------|------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSLatitudeRef | Unicode     | Sì      |
| 2     | /IFD/GPS/ \\ {ushort = 1 \\ }      | ASCII       | No       |



 

## <a name="remarks"></a>Osservazioni

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. LatitudeRef](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
