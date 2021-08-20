---
title: Attributo WM/ProviderRating
description: L'attributo WM/ProviderRating è la classificazione dell'elemento assegnato dal provider dei valori di attributo.
ms.assetid: a1a76560-a8d9-486a-badc-56d7bf488c10
keywords:
- Attributi WM/ProviderRating Windows Media Player
topic_type:
- apiref
api_name:
- WM/ProviderRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddcff262f21b4f31daff6f704dba1cb096f54bb295a21a3ae9a7c90f574af34f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116608"
---
# <a name="wmproviderrating-attribute"></a>Attributo WM/ProviderRating

**L'attributo WM/ProviderRating** è la classificazione dell'elemento assegnato dal provider dei valori di attributo.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Playlist cd](cd-playlist-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [Attributi di file multimediali Windows comunemente usati](commonly-used-windows-media-file-attributes.md)
-   [DVD](dvd-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria (o cache) che nel file multimediale digitale.

**Rating** è un alias per questo attributo.

La Windows media format SDK costante per questo attributo è g \_ wszWMProviderRating.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento all'attributo**](attribute-reference.md)
</dt> </dl>

 

 





