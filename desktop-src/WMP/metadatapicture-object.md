---
title: Oggetto MetadataPicture
description: L'oggetto MetadataPicture consente di recuperare i valori dell'attributo dei metadati WM/Picture. Questo attributo corrisponde alla grafica degli album contenuta in un file multimediale digitale, non alla grafica degli album scaricata su Internet.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- Oggetto MetadataPicture Windows Media Player
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 261ed17a156e1b5563b52744490e2ed014803eb9f1e75c182f44d5bd228b11c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996211"
---
# <a name="metadatapicture-object"></a>Oggetto MetadataPicture

**L'oggetto MetadataPicture** consente di recuperare i valori dell'attributo dei metadati [**WM/Picture.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) Questo attributo corrisponde alla grafica degli album contenuta in un file multimediale digitale, non alla grafica degli album scaricata su Internet.

**L'oggetto MetadataPicture** supporta le proprietà seguenti.



| Proprietà                                           | Descrizione                                       |
|----------------------------------------------------|---------------------------------------------------|
| [**description**](metadatapicture-description.md) | Recupera una descrizione dell'immagine dei metadati.    |
| [**Mimetype**](metadatapicture-mimetype.md)       | Recupera il tipo MIME dell'immagine dei metadati.    |
| [**tipo di immagine**](metadatapicture-picturetype.md) | Recupera il tipo di immagine dell'immagine dei metadati. |
| [**URL**](metadatapicture-url.md)                 | Solo per uso interno.                                |



 

È **possibile accedere all'oggetto MetadataPicture** tramite il metodo seguente.



| Oggetto                        | Metodo                                               |
|-------------------------------|------------------------------------------------------|
| [**File multimediali**](media-object.md) | [**getItemInfoByType**](media-getiteminfobytype.md) |



 

A scopo illustrativo, `player.currentMedia.getItemInfoByType(name, language, index)` viene usato nelle sezioni relative alla sintassi di riferimento.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento sul modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 