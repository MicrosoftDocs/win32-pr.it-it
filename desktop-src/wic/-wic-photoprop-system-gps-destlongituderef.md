---
description: Criteri per i metadati delle foto per la proprietà System. GPS. DestLongitudeRef.
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: Criteri per i metadati delle foto di System. GPS. DestLongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8139fcf5218d9863393888d7ab7b188a53e7f55f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317252"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. GPS. DestLongitudeRef

Criteri per i metadati delle foto per la proprietà [System. GPS. DestLongitudeRef](../properties/props-system-gps-destlongituderef.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS. DestLongitudeRef

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-propvariant-type"></a>Tipo di PROPVARIANT di input

VT \_ LPWSTR è preferibile, ma \_ viene accettato anche VT LPSTR.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="precedence-of-paths-jpeg"></a>Precedenza dei percorsi (JPEG)

Se il file è in formato JPEG, i dati vengono letti, scritti e rimossi dal gestore nell'ordine seguente:



| JSON | Percorso                          | Formato disco | Necessario |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSDestLongitudeRef | Unicode     | Sì      |
| 2     | /App1/IFD/GPS/ \\ {ushort = 21 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, i dati vengono letti, scritti e rimossi nell'ordine seguente:



| JSON | Percorso                              | Formato disco | Necessario |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSDestLongitudeRef | Unicode     | Sì      |
| 2     | /IFD/GPS/ \\ {ushort = 21 \\ }          | ASCII       | No       |



 

## <a name="remarks"></a>Osservazioni

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. DestLongitudeRef](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
