---
description: Criteri dei metadati della foto per la proprietà System.Author.
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: Criteri dei metadati delle foto di System.Author
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b898f450fe1d370f94a9be2922eb650db47ac8c2e414c27d9eede23f0dada276
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088003"
---
# <a name="systemauthor-photo-metadata-policy"></a>Criteri dei metadati delle foto di System.Author

Criteri dei metadati della foto per [la proprietà System.Author.](../properties/props-system-author.md)

### <a name="pkey"></a>PKEY

Autore \_ PKEY

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ VECTOR \| VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT di input

VT \_ VECTOR \| VT \_ LPWSTR è preferibile, ma viene accettato anche VT \_ LPWSTR.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                             | Formato disco    |
|-------|----------------------------------|----------------|
| 1     | /app1/ifd/{ushort=315}           | ascii          |
| 2     | /app13/irb/8bimiptc/iptc/by-line |                |
| 3     | /xmp/ <xmpseq> dc:creator    | unicode        |
| 4     | /app13/irb/8bimiptc/iptc/by-line |                |
| 5     | /app1/ifd/{ushort=40093}         | byte \_ unicode |
| 6     | /xmp/tiff:artist                 | unicode        |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                             | Formato disco    |
|-------|----------------------------------|----------------|
| 1     | /xmp/ <xmpseq> dc:creator    | unicode        |
| 2     | /xmp/tiff:artist                 | unicode        |
| 3     | /app13/irb/8bimiptc/iptc/by-line |                |
| 4     | /app1/ifd/{ushort=315}           | ascii          |
| 5     | /app1/ifd/{ushort=40093}         | byte \_ unicode |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                             |
|-------|----------------------------------|
| 1     | /xmp/dc:creator                  |
| 2     | /xmp/tiff:artist                 |
| 3     | /app13/irb/8bimiptc/iptc/by-line |
| 4     | /app1/ifd/{ushort=315}           |
| 5     | /app1/ifd/{ushort=40093}         |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                              | Formato disco    |
|-------|-----------------------------------|----------------|
| 1     | /ifd/{ushort=315}                 | ascii          |
| 2     | /ifd/iptc/by-line                 |                |
| 3     | /ifd/xmp/ <xmpseq> dc:creator | unicode        |
| 4     | /ifd/iptc/by-line                 |                |
| 5     | /ifd/{ushort=40093}               | byte \_ unicode |
| 6     | /ifd/irb/8bimiptc/iptc/by-line    |                |
| 7     | /ifd/xmp/tiff:artist              | unicode        |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                              | Formato disco    |
|-------|-----------------------------------|----------------|
| 1     | /ifd/xmp/ <xmpseq> dc:creator | unicode        |
| 2     | /ifd/xmp/tiff:artist              | unicode        |
| 3     | /ifd/iptc/by-line                 |                |
| 4     | /ifd/{ushort=315}                 | vettore \_ ascii  |
| 5     | /ifd/{ushort=40093}               | byte \_ Unicode |
| 6     | /ifd/iptc/by-line                 |                |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                           |
|-------|--------------------------------|
| 1     | /ifd/xmp/dc:creator            |
| 2     | /ifd/xmp/tiff:artista           |
| 3     | /ifd/iptc/by-line              |
| 4     | /ifd/irb/8bimiptc/iptc/by-line |
| 5     | /ifd/{ushort=315}              |
| 6     | /ifd/{ushort=40093}            |



 

### <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Author](../properties/props-system-author.md)
</dt> </dl>

 

 
