---
description: Criteri dei metadati delle foto per la proprietà System.Keywords.
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: Criteri dei metadati foto di System.Keywords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa5387bfb8cca7fffe83f7615a979d8e23ae890
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886649"
---
# <a name="systemkeywords-photo-metadata-policy"></a>Criteri dei metadati foto di System.Keywords

Criteri dei metadati delle foto per [la proprietà System.Keywords.](../properties/props-system-keywords.md)

### <a name="pkey"></a>Chiave PKEY

Parole chiave \_ PKEY

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ VECTOR \| VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT di input

VT \_ VECTOR \| VT \_ LPWSTR è preferibile. Viene accettato anche un LPWSTR VT contenente una stringa delimitata da \_ punto e virgola.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono uniti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                              | Formato disco    |
|-------|-----------------------------------|----------------|
| 1     | /xmp/ &lt; xmpbag &gt; dc:subject     | unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords |                |
| 3     | /app1/ifd/{ushort=18247}          | byte \_ Unicode |
| 4     | /app1/ifd/{ushort=40094}          | byte \_ Unicode |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                              | Formato disco    |
|-------|---------------------------------------------------|----------------|
| 1     | /xmp/ &lt; xmpbag &gt; dc:subject                     | unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |                |
| 3     | /app1/ifd/{ushort=18247}                          | byte \_ Unicode |
| 4     | /app1/ifd/{ushort=40094}                          | byte \_ Unicode |
| 5     | /xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordXMP  | unicode        |
| 6     | /xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC | unicode        |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                              |
|-------|---------------------------------------------------|
| 1     | /xmp/dc:subject                                   |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |
| 3     | /app1/ifd/{ushort=18247}                          |
| 4     | /app1/ifd/{ushort=40094}                          |
| 5     | /xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordXMP  |
| 6     | /xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                              | Formato disco    |
|-------|-----------------------------------|----------------|
| 1     | /ifd/xmp/ &lt; xmpbag &gt; dc:subject | unicode        |
| 2     | /ifd/iptc/keywords                |                |
| 3     | /ifd/{ushort=18247}               | byte \_ Unicode |
| 4     | /ifd/{ushort=40094}               | byte \_ Unicode |
| 5     | /ifd/irb/8bimiptc/iptc/keywords   |                |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                                             | Formato disco    |
|-------|------------------------------------------------------------------|----------------|
| 1     | /ifd/xmp/ &lt; xmpbag &gt; dc:subject                                | unicode        |
| 2     | /ifd/iptc/keywords                                               |                |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |                |
| 4     | /ifd/{ushort=18247}                                              | byte \_ unicode |
| 5     | /ifd/{ushort=40094}                                              | byte \_ unicode |
| 6     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordXMP             | unicode        |
| 7     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC            | unicode        |
| 8     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC \_ TIFF \_ IRB | unicode        |



 

### <a name="remove-paths"></a>Rimuovere i percorsi



| JSON | Percorso                                                             |
|-------|------------------------------------------------------------------|
| 1     | /ifd/xmp/dc:subject                                              |
| 2     | /ifd/iptc/keywords                                               |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |
| 4     | /ifd/{ushort=18247}                                              |
| 5     | /ifd/{ushort=40094}                                              |
| 6     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordXMP             |
| 7     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC            |
| 8     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC \_ TIFF \_ IRB |



 

### <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Keywords](../properties/props-system-keywords.md)
</dt> </dl>

 

 
