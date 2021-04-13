---
description: Criteri per i metadati delle foto per la proprietà System. rating.
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: Criteri per i metadati delle foto System. rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4f7d89b1ff1ea8326c2d26fba0d331db1eab1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347176"
---
# <a name="systemrating-photo-metadata-policy"></a>Criteri per i metadati delle foto System. rating

Criteri per i metadati delle foto per la proprietà [System. rating](../properties/props-system-rating.md) .

### <a name="pkey"></a>PKEY

\_Classificazione pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_UI4 VT

### <a name="input-propvariant-type"></a>Tipo di PROPVARIANT di input

Può essere VT \_ Ui1, VT \_ UI2 o VT \_ UI4. Il valore può essere compreso tra 0 e 99.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /App1/IFD/{ushort = 18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto: valutazione | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /App1/IFD/{ushort = 18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto: valutazione | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                       |
|-------|----------------------------|
| 1     | /App1/IFD/{ushort = 18249}   |
| 2     | /XMP/microsoftphoto: valutazione |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                           | Formato disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/{ushort = 18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto: valutazione | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                           | Formato disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/{ushort = 18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto: valutazione | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                           |
|-------|--------------------------------|
| 1     | /IFD/{ushort = 18249}            |
| 2     | /IFD/XMP/microsoftphoto: valutazione |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. rating](../properties/props-system-rating.md)
</dt> </dl>

 

 
