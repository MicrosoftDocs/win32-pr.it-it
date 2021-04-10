---
description: Criteri per i metadati delle foto per la proprietà System. Photo. LensModel.
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: Criteri per i metadati delle foto di System. Photo. LensModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a5249136346407ab9fcd1e4802d6910d3e514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058050"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. LensModel

Criteri per i metadati delle foto per la proprietà [System. Photo. LensModel](../properties/props-system-photo-lensmodel.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ LensModel

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-type"></a>Tipo di input

Stringa.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="precedence-of-paths-jpeg"></a>Precedenza dei percorsi (JPEG)

Se il file è in formato JPEG, il gestore utilizzerà il percorso seguente durante la lettura o la scrittura dei dati.



| JSON | Percorso                          | Formato disco | Necessario |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:LensModel | Unicode     | Sì      |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, il gestore utilizzerà l'ordine di precedenza seguente durante la lettura o la scrittura dei dati.



| JSON | Percorso                              | Formato disco | Necessario |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:LensModel | Unicode     | Sì      |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. LensModel](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
