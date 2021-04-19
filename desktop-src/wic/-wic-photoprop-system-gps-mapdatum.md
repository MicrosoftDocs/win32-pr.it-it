---
description: Criteri per i metadati delle foto per la proprietà System. GPS. MapDatum.
ms.assetid: be31e98f-5114-4693-a9ef-37fea334875b
title: Criteri per i metadati delle foto di System. GPS. MapDatum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb7a279c79da3d2b1dd20563af35bd34233a1a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317870"
---
# <a name="systemgpsmapdatum-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. GPS. MapDatum

Criteri per i metadati delle foto per la proprietà [System. GPS. MapDatum](../properties/props-system-gps-mapdatum.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ MapDatum

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-type"></a>Tipo di input

VT \_ LPWSTR è preferibile, ma \_ viene accettato anche VT LPSTR

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="precedence-of-paths-jpeg"></a>Precedenza dei percorsi (JPEG)

Se il file è in formato JPEG, i dati vengono letti, scritti e rimossi dal gestore nell'ordine seguente:



| JSON | Percorso                          | Formato disco | Necessario |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSMapDatum         | Unicode     | Sì      |
| 2     | /App1/IFD/GPS/ \\ {ushort = 18 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, i dati vengono letti, scritti e rimossi nell'ordine seguente:



| JSON | Percorso                      | Formato disco | Necessario |
|-------|---------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSMapDatum | Unicode     | Sì      |
| 2     | /IFD/GPS/ \\ {ushort = 18 \\ }  | ASCII       | No       |



 

## <a name="remarks"></a>Osservazioni

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. MapDatum](../properties/props-system-gps-mapdatum.md)
</dt> </dl>

 

 
