---
description: Criteri per i metadati delle foto per la proprietà System. GPS. VersionId.
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: Criteri per i metadati delle foto System. GPS. VersionId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ca5bd1885f0ac5c3dc14dbb5e859de3f8a26cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312959"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a>Criteri per i metadati delle foto System. GPS. VersionId

Criteri per i metadati delle foto per la proprietà [System. GPS. VersionId](../properties/props-system-gps-versionid.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ VersionId

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_ \| interfaccia utente VT vettore VT \_

### <a name="input-type"></a>Tipo di input

Buffer

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policies"></a>Criteri di JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 0} |             |
| 2     | /xmp/exif:GPSVersionID   | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                     | Formato disco |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 0} |             |
| 2     | /xmp/exif:GPSVersionID   | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{ushort = 0} |
| 2     | /xmp/exif:gpsversionid   |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 0}        |             |
| 2     | /ifd/xmp/exif:GPSVersionID | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                       | Formato disco |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 0}        |             |
| 2     | /ifd/xmp/exif:GPSVersionID | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                       |
|-------|----------------------------|
| 1     | /IFD/GPS/{ushort = 0}        |
| 2     | /ifd/xmp/exif:gpsversionid |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. VersionId](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
