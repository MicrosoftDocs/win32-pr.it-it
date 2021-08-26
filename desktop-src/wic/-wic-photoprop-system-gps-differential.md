---
description: Criteri dei metadati delle foto per la proprietà System.GPS.Differential.
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: System.GPS.Differential Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728df47fd8e6e9748b7208b79444ba8fa257fa49c92587df199441de941f4fdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931801"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a>System.GPS.Differential Photo Metadata Policy

Criteri dei metadati delle foto per [la proprietà System.GPS.Differential.](../properties/props-system-gps-differential.md)

### <a name="pkey"></a>Chiave PKEY

Differenziale \_ GPS \_ PKEY

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

Interfaccia utente \_ VT2

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT di input

VT \_ UI1, VT \_ UI2 e VT \_ UI4 sono tutti accettati.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policies"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=30} | ushort      |
| 2     | /xmp/exif:GPSDifferential | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                      | Formato disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=30} | ushort      |
| 2     | /xmp/exif:GPSDifferential | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=30} |
| 2     | /xmp/exif:gpsdifferential |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=30}          | ushort      |
| 2     | /ifd/xmp/exif:GPSDifferential | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=30}          | ushort      |
| 2     | /ifd/xmp/exif:GPSDifferential | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /ifd/gps/{ushort=30}          |
| 2     | /ifd/xmp/exif:gpsdifferential |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.GPS.Differential](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
