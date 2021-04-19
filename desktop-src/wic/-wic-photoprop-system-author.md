---
description: Criteri per i metadati delle foto per la proprietà System. Author.
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: Criteri per i metadati delle foto di System. Author
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90345257ef1623f7cda1ce4318af7a9f472df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317891"
---
# <a name="systemauthor-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Author

Criteri per i metadati delle foto per la proprietà [System. Author](../properties/props-system-author.md) .

### <a name="pkey"></a>PKEY

Autore di PKEY \_

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ vettore \| VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo di PROPVARIANT di input

\_ \| \_ È preferibile il vettore VT LPWSTR, ma \_ è anche accettato VT LPWSTR.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                             | Formato disco    |
|-------|----------------------------------|----------------|
| 1     | /App1/IFD/{ushort = 315}           | ascii          |
| 2     | /app13/irb/8bimiptc/iptc/by-line |                |
| 3     | /XMP/ <xmpseq> DC: Creator    | unicode        |
| 4     | /app13/irb/8bimiptc/iptc/by-line |                |
| 5     | /App1/IFD/{ushort = 40093}         | \_byte Unicode |
| 6     | /XMP/TIFF: artista                 | unicode        |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                             | Formato disco    |
|-------|----------------------------------|----------------|
| 1     | /XMP/ <xmpseq> DC: Creator    | unicode        |
| 2     | /XMP/TIFF: artista                 | unicode        |
| 3     | /app13/irb/8bimiptc/iptc/by-line |                |
| 4     | /App1/IFD/{ushort = 315}           | ascii          |
| 5     | /App1/IFD/{ushort = 40093}         | \_byte Unicode |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                             |
|-------|----------------------------------|
| 1     | /XMP/DC: creatore                  |
| 2     | /XMP/TIFF: artista                 |
| 3     | /app13/irb/8bimiptc/iptc/by-line |
| 4     | /App1/IFD/{ushort = 315}           |
| 5     | /App1/IFD/{ushort = 40093}         |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                              | Formato disco    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/{ushort = 315}                 | ascii          |
| 2     | /ifd/iptc/by-line                 |                |
| 3     | /IFD/XMP/ <xmpseq> DC: Creator | unicode        |
| 4     | /ifd/iptc/by-line                 |                |
| 5     | /IFD/{ushort = 40093}               | \_byte Unicode |
| 6     | /ifd/irb/8bimiptc/iptc/by-line    |                |
| 7     | /IFD/XMP/TIFF: artista              | unicode        |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                              | Formato disco    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/XMP/ <xmpseq> DC: Creator | unicode        |
| 2     | /IFD/XMP/TIFF: artista              | unicode        |
| 3     | /ifd/iptc/by-line                 |                |
| 4     | /IFD/{ushort = 315}                 | \_vettore ASCII  |
| 5     | /IFD/{ushort = 40093}               | \_byte Unicode |
| 6     | /ifd/iptc/by-line                 |                |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                           |
|-------|--------------------------------|
| 1     | /IFD/XMP/DC: creatore            |
| 2     | /IFD/XMP/TIFF: artista           |
| 3     | /ifd/iptc/by-line              |
| 4     | /ifd/irb/8bimiptc/iptc/by-line |
| 5     | /IFD/{ushort = 315}              |
| 6     | /IFD/{ushort = 40093}            |



 

### <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Author](../properties/props-system-author.md)
</dt> </dl>

 

 
