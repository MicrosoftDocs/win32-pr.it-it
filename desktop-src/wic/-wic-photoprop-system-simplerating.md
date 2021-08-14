---
description: Criteri dei metadati delle foto per la proprietà System.SimpleRating.
ms.assetid: d932a251-f238-4582-a1c4-cf4855f26fb3
title: Criteri dei metadati delle foto di System.SimpleRating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c65c9e49d7e905a4cefe890b6c5aab257250baa41171470666ba38b3fb5c96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709965"
---
# <a name="systemsimplerating-photo-metadata-policy"></a>Criteri dei metadati delle foto di System.SimpleRating

Criteri dei metadati delle foto per [la proprietà System.SimpleRating.](../properties/props-system-simplerating.md)

### <a name="pkey"></a>PKEY

PKEY \_ SimpleRating

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

Interfaccia utente \_ VT4

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT di input

Può essere VT \_ UI1, VT \_ UI2 o VT \_ UI4. Il valore intero può essere compreso tra 0 e 5.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/{ushort=18246} | ushort      |
| 2     | /xmp/xmp:Rating          | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/{ushort=18246} | ushort      |
| 2     | /xmp/xmp:Rating          | unicode     |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /app1/ifd/{ushort=18246} |
| 2     | /xmp/xmp:rating          |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                | Formato disco |
|-------|---------------------|-------------|
| 1     | /ifd/{ushort=18246} | ushort      |
| 2     | /ifd/xmp/xmp:Rating | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                | Formato disco |
|-------|---------------------|-------------|
| 1     | /ifd/{ushort=18246} | ushort      |
| 2     | /ifd/xmp/xmp:Rating | unicode     |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                |
|-------|---------------------|
| 1     | /ifd/{ushort=18246} |
| 2     | /ifd/xmp/xmp:rating |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.SimpleRating](../properties/props-system-simplerating.md)
</dt> </dl>

 

 
