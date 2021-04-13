---
title: Oggetto MetadataPicture
description: L'oggetto MetadataPicture fornisce un modo per recuperare i valori dell'attributo di metadati WM/Picture. Questo attributo corrisponde agli album Art contenuti in un file multimediale digitale, non all'Art album scaricato tramite Internet.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- Media Player di Windows oggetto MetadataPicture
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 892b162ba05ab43740565c849b00bc4e3c52aad6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473934"
---
# <a name="metadatapicture-object"></a>Oggetto MetadataPicture

L'oggetto **MetadataPicture** fornisce un modo per recuperare i valori dell'attributo di metadati [**WM/Picture**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) . Questo attributo corrisponde agli album Art contenuti in un file multimediale digitale, non all'Art album scaricato tramite Internet.

L'oggetto **MetadataPicture** supporta le proprietà seguenti.



| Proprietà                                           | Descrizione                                       |
|----------------------------------------------------|---------------------------------------------------|
| [**Descrizione**](metadatapicture-description.md) | Recupera una descrizione dell'immagine dei metadati.    |
| [**mimeType**](metadatapicture-mimetype.md)       | Recupera il tipo MIME dell'immagine dei metadati.    |
| [**pictureType**](metadatapicture-picturetype.md) | Recupera il tipo di immagine dell'immagine dei metadati. |
| [**URL**](metadatapicture-url.md)                 | Solo per uso interno.                                |



 

È possibile accedere all'oggetto **MetadataPicture** tramite il metodo seguente.



| Oggetto                        | Metodo                                               |
|-------------------------------|------------------------------------------------------|
| [**File multimediali**](media-object.md) | [**getItemInfoByType**](media-getiteminfobytype.md) |



 

Ai fini dell'illustrazione, `player.currentMedia.getItemInfoByType(name, language, index)` viene usato nelle sezioni della sintassi di riferimento.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 