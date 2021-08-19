---
title: Attributo WM/UniqueFileIdentifier
description: L'attributo WM/UniqueFileIdentifier è una stringa che identifica in modo univoco l'elemento.
ms.assetid: 8196fc38-05dc-4c9e-98cb-1e160ce28a9a
keywords:
- Attributo WM/UniqueFileIdentifier Windows Media Player
topic_type:
- apiref
api_name:
- WM/UniqueFileIdentifier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf29b5f4a0c2bf6e2642ce13f190a4734a2fb4ff395481b1ba93bc5feeb6db89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930817"
---
# <a name="wmuniquefileidentifier-attribute"></a>Attributo WM/UniqueFileIdentifier

**L'attributo WM/UniqueFileIdentifier** è una stringa che identifica in modo univoco l'elemento.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Playlist cd](cd-playlist-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [Attributi dei Windows file multimediali comunemente usati](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria (o cache) che nel file multimediale digitale.

**UniqueFileIdentifier** è un alias per questo attributo.

La Windows Media Format SDK per questo attributo è g \_ wszWMUniqueFileIdentifier.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> </dl>

 

 





