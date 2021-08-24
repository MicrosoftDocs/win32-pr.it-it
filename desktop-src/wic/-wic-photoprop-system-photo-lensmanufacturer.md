---
description: Criteri dei metadati delle foto per la proprietà System.Photo.LensManufacturer.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: Criteri metadati foto System.Photo.LensManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f6beebc06ce690b05da62c023480bec25b675a7a9ec6093cec1752ac3a0e343
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881984"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a>Criteri metadati foto System.Photo.LensManufacturer

Criteri dei metadati delle foto [per la proprietà System.Photo.LensManufacturer.](../properties/props-system-photo-lensmanufacturer.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Photo \_ LensManufacturer

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ LPWSTR

### <a name="input-type"></a>Tipo di input

Stringa.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="precedence-of-paths-jpeg"></a>Precedenza dei percorsi (JPEG)

Se il file è in formato JPEG, il gestore utilizzerà il percorso seguente durante la lettura o la scrittura dei dati.



| JSON | Percorso                                 | Formato disco | Necessario |
|-------|--------------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:LensManufacturer | Unicode     | Sì      |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, il gestore userà l'ordine di precedenza seguente durante la lettura o la scrittura dei dati.



| JSON | Percorso                                     | Formato disco | Necessario |
|-------|------------------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:LensManufacturer | Unicode     | Sì      |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.LensManufacturer](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
