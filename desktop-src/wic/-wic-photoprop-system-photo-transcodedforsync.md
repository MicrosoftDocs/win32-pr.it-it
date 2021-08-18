---
description: Criteri dei metadati delle foto per la proprietà System.Photo.TranscodedForSync.
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: Criteri metadati foto System.Photo.TranscodedForSync
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e78086284e1ca13b01c5e7cd188b761afe7eeba8acb5f2bca103234f80955b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964760"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a>Criteri metadati foto System.Photo.TranscodedForSync

Criteri dei metadati delle foto [per la proprietà System.Photo.TranscodedForSync.](../properties/props-system-photo-transcodedforsync.md)

### <a name="pkey"></a>Chiave PKEY

PKEY \_ Photo \_ TranscodedForSync

### <a name="containers"></a>Contenitori

JPEG, TIFF

### <a name="read-only"></a>Read-Only

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT di output

VT \_ BOOL

### <a name="input-type"></a>Tipo di input

Proprietà di tipo Boolean.

### <a name="conflict-resolution-policy"></a>Criteri di risoluzione dei conflitti

I valori di schemi diversi vengono riconciliati.

### <a name="jpeg-policy"></a>Criteri JPEG

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                                  | Formato disco  |
|-------|---------------------------------------|--------------|
| 1     | /app1/ifd/{ushort=18248}              | bool \_ ushort |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                  | Formato disco  |
|-------|---------------------------------------|--------------|
| 1     | /app1/ifd/{ushort=18248}              | bool \_ ushort |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                  |
|-------|---------------------------------------|
| 1     | /app1/ifd/{ushort=18248}              |
| 2     | /xmp/microsoftphoto:transcodedforsync |



 

### <a name="tiff-policies"></a>Criteri TIFF

### <a name="read-paths"></a>Percorsi di lettura



| JSON | Percorso                                      | Formato disco  |
|-------|-------------------------------------------|--------------|
| 1     | /ifd/{ushort=18248}                       | bool \_ ushort |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>Percorsi di scrittura



| JSON | Percorso                                      | Formato disco  |
|-------|-------------------------------------------|--------------|
| 1     | /ifd/{ushort=18248}                       | bool \_ ushort |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>Rimuovi percorsi



| JSON | Percorso                                      |
|-------|-------------------------------------------|
| 1     | /ifd/{ushort=18248}                       |
| 2     | /ifd/xmp/microsoftphoto:transcodedforsync |



 

## <a name="remarks"></a>Commenti

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Photo.TranscodedForSync](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
