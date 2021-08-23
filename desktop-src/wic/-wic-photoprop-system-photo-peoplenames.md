---
description: Criteri dei metadati delle foto per la proprietà System.Photo.PeopleNames.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: Criteri metadati foto System.Photo.PeopleNames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4118cc8242d6dfe8a91d0bcd2b6039095fdf180037f51205d3541b9aefa2cc0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087050"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a>Criteri metadati foto System.Photo.PeopleNames

Criteri dei metadati delle foto [per la proprietà System.Photo.PeopleNames.](../properties/props-system-photo-peoplenames.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Photo \_ PeopleNames

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ VECTOR \| VT \_ LPWSTR

### <a name="input-type"></a>Tipo di input

StringMulti

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                                                           | Formato disco |
|-------|----------------------------------------------------------------|-------------|
| 1     | /xmp/ <xmpstruct> MP:RegionInfo/ <xmpbag> MPRI:Regions | ushort      |



 

### <a name="write-paths"></a>Percorsi di scrittura

Questa proprietà non può essere scritta usando i criteri dei metadati.

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                |
|-------|-------------------------------------|
| 1     | /xmp/ <xmpstruct> MP:RegionInfo |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                                                               | Formato disco |
|-------|--------------------------------------------------------------------|-------------|
| 1     | /ifd/xmp/ <xmpstruct> MP:RegionInfo/ <xmpbag> MPRI:Regions | ushort      |



 

### <a name="write-paths"></a>Percorsi di scrittura

Questa proprietà non può essere scritta usando i criteri dei metadati.

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                    |
|-------|-----------------------------------------|
| 1     | /ifd/xmp/ <xmpstruct> MP:RegionInfo |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
