---
description: Criteri dei metadati delle foto per la proprietà System.Rating.
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: Criteri dei metadati delle foto System.Rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25278ad7d881a0acadc5199fd07227bb650aaae4da2b6342070a64d69fd75240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086984"
---
# <a name="systemrating-photo-metadata-policy"></a>Criteri dei metadati delle foto System.Rating

Criteri dei metadati delle foto per [la proprietà System.Rating.](../properties/props-system-rating.md)

### <a name="pkey"></a>Chiave PKEY

Classificazione \_ PKEY

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ UI4

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT di input

Può essere VT \_ UI1, VT \_ UI2 o VT \_ UI4. Il valore può essere compreso tra 0 e 99.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/{ushort=18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto:Rating | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/{ushort=18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto:Rating | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                       |
|-------|----------------------------|
| 1     | /app1/ifd/{ushort=18249}   |
| 2     | /xmp/microsoftphoto:rating |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                           | Formato disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/{ushort=18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto:Rating | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                           | Formato disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/{ushort=18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto:Rating | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                           |
|-------|--------------------------------|
| 1     | /ifd/{ushort=18249}            |
| 2     | /ifd/xmp/microsoftphoto:rating |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Rating](../properties/props-system-rating.md)
</dt> </dl>

 

 
