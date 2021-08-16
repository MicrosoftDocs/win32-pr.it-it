---
description: Criteri dei metadati delle foto per la proprietà System.Photo.FlashModel.
ms.assetid: ef322823-1b87-40ea-a5e3-e7551f14e44d
title: Criteri dei metadati delle foto System.Photo.FlashModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c9e45e1ef759f2bee0d383cde3bcdabe8be67dc55a463ab6c9f7e6e05889a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204882"
---
# <a name="systemphotoflashmodel-photo-metadata-policy"></a>Criteri dei metadati delle foto System.Photo.FlashModel

Criteri dei metadati delle foto per [la proprietà System.Photo.FlashModel.](../properties/props-system-photo-flashmodel.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Photo \_ FlashModel

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



| JSON | Percorso                           | Formato disco | Formato dati | Necessario |
|-------|--------------------------------|-------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:FlashModel | Unicode     |             | Sì      |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, il gestore userà l'ordine di precedenza seguente durante la lettura o la scrittura dei dati.



| JSON | Percorso                               | Formato disco | Formato dati | Necessario |
|-------|------------------------------------|-------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:FlashModel | Unicode     |             | Sì      |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.FlashModel](../properties/props-system-photo-flashmodel.md)
</dt> </dl>

 

 
