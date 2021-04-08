---
description: Criteri per i metadati delle foto per la proprietà System. Photo. FlashManufacturer.
ms.assetid: f62e85ec-2dc6-456b-a43b-7b76d162b608
title: Criteri per i metadati delle foto di System. Photo. FlashManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1e785dfd00662acf065021a3c80de5c587586c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058189"
---
# <a name="systemphotoflashmanufacturer-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. FlashManufacturer

Criteri per i metadati delle foto per la proprietà [System. Photo. FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ FlashManufacturer

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



| JSON | Percorso                                  | Formato disco | Formato dati | Necessario |
|-------|---------------------------------------|-------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:FlashManufacturer | Unicode     |             | Sì      |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, il gestore utilizzerà l'ordine di precedenza seguente durante la lettura o la scrittura dei dati.



| JSON | Percorso                                      | Formato disco | Formato dati | Necessario |
|-------|-------------------------------------------|-------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:FlashManufacturer | Unicode     |             | Sì      |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md)
</dt> </dl>

 

 
