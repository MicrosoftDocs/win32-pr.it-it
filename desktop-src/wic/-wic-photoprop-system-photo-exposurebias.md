---
description: Criteri per i metadati delle foto per la proprietà System. Photo. ExposureBias.
ms.assetid: 00ebe037-0116-4d75-868b-d75b3e58a84d
title: Criteri per i metadati delle foto di System. Photo. ExposureBias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709aa21da7cec56d36b5de643681a592873717bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314459"
---
# <a name="systemphotoexposurebias-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. ExposureBias

Criteri per i metadati delle foto per la proprietà [System. Photo. ExposureBias](../properties/props-system-photo-exposurebias.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ ExposureBias

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

Sì

### <a name="output-propvariant-type"></a>Tipo di PROPVARIANT di output

VT \_ R8

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

Questo valore viene generato da System. Photo. ExposureBiasNumerator e System. Photo. ExposureBiasDenominator. Non può essere scritto direttamente. I valori di schemi diversi vengono risolti.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37380} |             |
| 2     | /xmp/exif:ExposureBiasValue   |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                          | Formato disco |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37380} |             |
| 2     | /xmp/exif:ExposureBiasValue   |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37380} |
| 2     | /xmp/exif:exposurebiasvalue   |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Leggi percorsi



| JSON | Percorso                            | Formato disco |
|-------|---------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37380}        |             |
| 2     | /ifd/xmp/exif:ExposureBiasValue |             |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                            | Formato disco |
|-------|---------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37380}        |             |
| 2     | /ifd/xmp/exif:ExposureBiasValue |             |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                            |
|-------|---------------------------------|
| 1     | /IFD/EXIF/{ushort = 37380}        |
| 2     | /ifd/xmp/exif:exposurebiasvalue |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. ExposureBias](../properties/props-system-photo-exposurebias.md)
</dt> </dl>

 

 
