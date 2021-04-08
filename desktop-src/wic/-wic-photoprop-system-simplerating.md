---
description: Criteri per i metadati delle foto per la proprietà System. SimpleRating.
ms.assetid: d932a251-f238-4582-a1c4-cf4855f26fb3
title: Criteri per i metadati delle foto System. SimpleRating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b91e41a0684c8e395992683e0a1d4fe43306a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058044"
---
# <a name="systemsimplerating-photo-metadata-policy"></a>Criteri per i metadati delle foto System. SimpleRating

Criteri per i metadati delle foto per la proprietà [System. SimpleRating](../properties/props-system-simplerating.md) .

### <a name="pkey"></a>PKEY

\_SIMPLERATING pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_UI4 VT

### <a name="input-propvariant-type"></a>Tipo di PROPVARIANT di input

Può essere VT \_ Ui1, VT \_ UI2 o VT \_ UI4. Il valore integer può variare da 0 a 5.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/{ushort = 18246} | ushort      |
| 2     | /XMP/XMP: valutazione          | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/{ushort = 18246} | ushort      |
| 2     | /XMP/XMP: valutazione          | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /App1/IFD/{ushort = 18246} |
| 2     | /XMP/XMP: valutazione          |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                | Formato disco |
|-------|---------------------|-------------|
| 1     | /IFD/{ushort = 18246} | ushort      |
| 2     | /IFD/XMP/XMP: valutazione | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                | Formato disco |
|-------|---------------------|-------------|
| 1     | /IFD/{ushort = 18246} | ushort      |
| 2     | /IFD/XMP/XMP: valutazione | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                |
|-------|---------------------|
| 1     | /IFD/{ushort = 18246} |
| 2     | /IFD/XMP/XMP: valutazione |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. SimpleRating](../properties/props-system-simplerating.md)
</dt> </dl>

 

 
