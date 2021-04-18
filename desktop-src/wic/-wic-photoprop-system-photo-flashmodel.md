---
description: Criteri per i metadati delle foto per la proprietà System. Photo. FlashModel.
ms.assetid: ef322823-1b87-40ea-a5e3-e7551f14e44d
title: Criteri per i metadati delle foto di System. Photo. FlashModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ade3769cb0d852239af84b769b85d5b3849589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314450"
---
# <a name="systemphotoflashmodel-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. FlashModel

Criteri per i metadati delle foto per la proprietà [System. Photo. FlashModel](../properties/props-system-photo-flashmodel.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ FlashModel

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



| JSON | Percorso                           | Formato disco | Formato dati | Necessario |
|-------|--------------------------------|-------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:FlashModel | Unicode     |             | Sì      |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, il gestore utilizzerà l'ordine di precedenza seguente durante la lettura o la scrittura dei dati.



| JSON | Percorso                               | Formato disco | Formato dati | Necessario |
|-------|------------------------------------|-------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:FlashModel | Unicode     |             | Sì      |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. FlashModel](../properties/props-system-photo-flashmodel.md)
</dt> </dl>

 

 
