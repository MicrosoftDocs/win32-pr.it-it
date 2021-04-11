---
description: Criteri per i metadati delle foto per la proprietà System. keywords.
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: Criteri per i metadati di Photo System. Keywords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5d25e7f1919527d474395397d6df62863f7b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233334"
---
# <a name="systemkeywords-photo-metadata-policy"></a>Criteri per i metadati di Photo System. Keywords

Criteri per i metadati delle foto per la proprietà [System. Keywords](../properties/props-system-keywords.md) .

### <a name="pkey"></a>PKEY

\_Parole chiave pkey

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ vettore \| VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo di PROPVARIANT di input

\_ \| \_ È preferibile il vettore VT LPWSTR. \_Viene anche accettato un LPWSTR VT contenente una stringa delimitata da punti e virgola.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono uniti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                              | Formato disco    |
|-------|-----------------------------------|----------------|
| 1     | /XMP/ <xmpbag> DC: oggetto     | unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords |                |
| 3     | /App1/IFD/{ushort = 18247}          | \_byte Unicode |
| 4     | /App1/IFD/{ushort = 40094}          | \_byte Unicode |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                              | Formato disco    |
|-------|---------------------------------------------------|----------------|
| 1     | /XMP/ <xmpbag> DC: oggetto                     | unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |                |
| 3     | /App1/IFD/{ushort = 18247}                          | \_byte Unicode |
| 4     | /App1/IFD/{ushort = 40094}                          | \_byte Unicode |
| 5     | /XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP  | unicode        |
| 6     | /XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC | unicode        |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                              |
|-------|---------------------------------------------------|
| 1     | /XMP/DC: oggetto                                   |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |
| 3     | /App1/IFD/{ushort = 18247}                          |
| 4     | /App1/IFD/{ushort = 40094}                          |
| 5     | /XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP  |
| 6     | /XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                              | Formato disco    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/XMP/ <xmpbag> DC: oggetto | unicode        |
| 2     | /ifd/iptc/keywords                |                |
| 3     | /IFD/{ushort = 18247}               | \_byte Unicode |
| 4     | /IFD/{ushort = 40094}               | \_byte Unicode |
| 5     | /ifd/irb/8bimiptc/iptc/keywords   |                |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                                             | Formato disco    |
|-------|------------------------------------------------------------------|----------------|
| 1     | /IFD/XMP/ <xmpbag> DC: oggetto                                | unicode        |
| 2     | /ifd/iptc/keywords                                               |                |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |                |
| 4     | /IFD/{ushort = 18247}                                              | \_byte Unicode |
| 5     | /IFD/{ushort = 40094}                                              | \_byte Unicode |
| 6     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP             | unicode        |
| 7     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC            | unicode        |
| 8     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC \_ TIFF \_ IRB | unicode        |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                                             |
|-------|------------------------------------------------------------------|
| 1     | /IFD/XMP/DC: oggetto                                              |
| 2     | /ifd/iptc/keywords                                               |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |
| 4     | /IFD/{ushort = 18247}                                              |
| 5     | /IFD/{ushort = 40094}                                              |
| 6     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP             |
| 7     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC            |
| 8     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC \_ TIFF \_ IRB |



 

### <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Keywords](../properties/props-system-keywords.md)
</dt> </dl>

 

 
