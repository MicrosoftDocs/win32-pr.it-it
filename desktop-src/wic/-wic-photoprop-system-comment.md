---
description: Criteri dei metadati delle foto per la proprietà System.Comment.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: Criteri metadati foto System.Comment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa1a62fd5afa131a714c365ed2fda2c307bc955
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883911"
---
# <a name="systemcomment-photo-metadata-policy"></a>Criteri metadati foto System.Comment

Criteri dei metadati delle foto per [la proprietà System.Comment.](../properties/props-system-comment.md)

### <a name="pkey"></a>Chiave PKEY

Commento \_ PKEY

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT di input

VT \_ LPWSTR o VT \_ LPSTR

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                                | Formato disco    |
|-------|-------------------------------------|----------------|
| 1     | /app1/ifd/{ushort=40092}            | byte \_ Unicode |
| 2     | /app1/ifd/{ushort=37510}            | unicode        |
| 3     | /xmp/ &lt; xmpalt &gt; exif:UserComment | unicode        |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco    |
|-------|--------------------------|----------------|
| 1     | /app1/ifd/{ushort=40092} | byte \_ Unicode |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/{ushort=40092}      |
| 2     | /app1/ifd/exif/{ushort=37510} |
| 3     | /xmp/exif:UserComment         |



 

### <a name="tiff-policy"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                                    | Formato disco    |
|-------|-----------------------------------------|----------------|
| 1     | /ifd/{ushort=40092}                     | byte \_ Unicode |
| 2     | /ifd/{ushort=37510}                     | unicode        |
| 3     | /ifd/xmp/ &lt; xmpalt &gt; exif:UserComment | unicode        |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                | Formato disco    |
|-------|---------------------|----------------|
| 1     | /ifd/{ushort=40092} | byte \_ Unicode |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                      |
|-------|---------------------------|
| 1     | /ifd/{ushort=40092}       |
| 2     | /ifd/{ushort=37510}       |
| 3     | /ifd/xmp/exif:UserComment |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Comment](../properties/props-system-comment.md)
</dt> </dl>

 

 
