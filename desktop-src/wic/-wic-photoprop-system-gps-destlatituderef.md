---
description: Criteri per i metadati delle foto per la proprietà System. GPS. DestLatitudeRef.
ms.assetid: 8a13642a-0d29-4193-9784-f716bc428c72
title: Criteri per i metadati delle foto di System. GPS. DestLatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838e4688f0c3342091e5995885689a44fab38739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314461"
---
# <a name="systemgpsdestlatituderef-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. GPS. DestLatitudeRef

Criteri per i metadati delle foto per la proprietà [System. GPS. DestLatitudeRef](../properties/props-system-gps-destlatituderef.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestLatitudeRef

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-type"></a>Tipo di input

\_È preferibile LPWSTR VT, ma \_ viene accettato il LPSTR VT.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="precedence-of-paths-jpeg"></a>Precedenza dei percorsi (JPEG)

Se il file è in formato JPEG, i dati vengono letti, scritti e rimossi dal gestore nell'ordine seguente:



| JSON | Percorso                          | Formato disco | Necessario |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSDestLatitudeRef  | Unicode     | Sì      |
| 2     | /App1/IFD/GPS/ \\ {ushort = 19 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, i dati vengono letti, scritti e rimossi nell'ordine seguente:



| JSON | Percorso                             | Formato disco | Necessario |
|-------|----------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSDestLatitudeRef | Unicode     | Sì      |
| 2     | /IFD/GPS/ \\ {ushort = 19 \\ }         | ASCII       | No       |



 

## <a name="remarks"></a>Osservazioni

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. DestLatitudeRef](../properties/props-system-gps-destlatituderef.md)
</dt> </dl>

 

 
