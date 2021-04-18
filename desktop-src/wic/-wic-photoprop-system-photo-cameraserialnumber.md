---
description: Criteri per i metadati delle foto per la proprietà System. Photo. CameraSerialNumber.
ms.assetid: 85f78f45-5e76-4d52-88a2-ac3c9e2b6a1e
title: Criteri per i metadati delle foto di System. Photo. CameraSerialNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c329cd4c56b49e39de5da97ac9d9f8b14bffb64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317247"
---
# <a name="systemphotocameraserialnumber-photo-metadata-policy"></a>Criteri per i metadati delle foto di System. Photo. CameraSerialNumber

Criteri per i metadati delle foto per la proprietà [System. Photo. CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ CameraSerialNumber

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

### <a name="precedence-of-paths-jpeg"></a>Precedenza dei percorsi (JPEG)

Se il file è in formato JPEG, i dati vengono letti, scritti e rimossi dal gestore dal percorso seguente:



| JSON | Percorso                                   | Formato disco | Necessario |
|-------|----------------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:CameraSerialNumber | Unicode     | Sì      |



 

### <a name="precedence-of-paths-tiff"></a>Precedenza dei percorsi (TIFF)

Se il file è in formato TIFF, i dati vengono letti, scritti e rimossi dal gestore dal percorso seguente



| JSON | Percorso                                       | Formato disco | Necessario |
|-------|--------------------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:CameraSerialNumber | Unicode     | Sì      |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. Photo. CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md)
</dt> </dl>

 

 
