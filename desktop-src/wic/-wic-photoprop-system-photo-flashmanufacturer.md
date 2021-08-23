---
description: Criteri dei metadati delle foto per la proprietà System.Photo.FlashManufacturer.
ms.assetid: f62e85ec-2dc6-456b-a43b-7b76d162b608
title: Criteri metadati foto System.Photo.FlashManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d81a57967e5b3f1139b0efabd85266bec80d10e06fb18251b0a6b9ef61a1e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964808"
---
# <a name="systemphotoflashmanufacturer-photo-metadata-policy"></a>Criteri metadati foto System.Photo.FlashManufacturer

Criteri dei metadati delle foto [per la proprietà System.Photo.FlashManufacturer.](../properties/props-system-photo-flashmanufacturer.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Photo \_ FlashManufacturer

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



| JSON | Percorso                                  | Formato disco | Formato dati | Necessario |
|-------|---------------------------------------|-------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:FlashManufacturer | Unicode     |             | Sì      |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, il gestore userà l'ordine di precedenza seguente durante la lettura o la scrittura dei dati.



| JSON | Percorso                                      | Formato disco | Formato dati | Necessario |
|-------|-------------------------------------------|-------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:FlashManufacturer | Unicode     |             | Sì      |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md)
</dt> </dl>

 

 
