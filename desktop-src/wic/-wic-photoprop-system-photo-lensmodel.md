---
description: Criteri dei metadati delle foto per la proprietà System.Photo.LensModel.
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: Criteri dei metadati delle foto System.Photo.LensModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07fff44e14a04dab220f8dbce243a638710f30db253c43c1ff79a240bb32f3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441871"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a>Criteri dei metadati delle foto System.Photo.LensModel

Criteri dei metadati delle foto per [la proprietà System.Photo.LensModel.](../properties/props-system-photo-lensmodel.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Photo \_ LensModel

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



| JSON | Percorso                          | Formato disco | Necessario |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:LensModel | Unicode     | Sì      |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, il gestore userà l'ordine di precedenza seguente durante la lettura o la scrittura dei dati.



| JSON | Percorso                              | Formato disco | Necessario |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:LensModel | Unicode     | Sì      |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.LensModel](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
