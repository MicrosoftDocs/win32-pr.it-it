---
description: Criteri per i metadati delle foto per la proprietà System. GPS. AreaInformation.
ms.assetid: d9ecb00b-1f97-4f53-909f-30231104d398
title: Criteri per i metadati delle foto di System. GPS. AreaInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e14837da9ffa8b688caf1a544e222043988cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346416"
---
# <a name="systemgpsareainformation-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. GPS. AreaInformation

Criteri per i metadati delle foto per la proprietà [System. GPS. AreaInformation](../properties/props-system-gps-areainformation.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ AreaInformation

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

\_LPWSTR VT

### <a name="input-type"></a>Tipo di input

Stringa.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono risolti.

### <a name="jpeg-policies"></a>Criteri di JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 28}    |             |
| 2     | /xmp/exif:GPSAreaInformation | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                         | Formato disco |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 28}    |             |
| 2     | /xmp/exif:GPSAreaInformation | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                         |
|-------|------------------------------|
| 1     | /App1/IFD/GPS/{ushort = 28}    |
| 2     | /xmp/exif:GPSAreaInformation |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                             | Formato disco |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 28}             |             |
| 2     | /ifd/xmp/exif:GPSAreaInformation | unicode     |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                             | Formato disco |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 28}             |             |
| 2     | /ifd/xmp/exif:GPSAreaInformation | unicode     |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                             |
|-------|----------------------------------|
| 1     | /IFD/GPS/{ushort = 28}             |
| 2     | /ifd/xmp/exif:GPSAreaInformation |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. GPS. AreaInformation](../properties/props-system-gps-areainformation.md)
</dt> </dl>

 

 
