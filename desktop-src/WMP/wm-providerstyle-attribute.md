---
title: Attributo WM/ProviderStyle
description: L'attributo WM/ProviderStyle è lo stile dell'elemento assegnato dal provider dei valori dell'attributo.
ms.assetid: 43994d6b-0d71-4f2c-834a-47bbcd32b461
keywords:
- Media Player Windows per gli attributi WM/ProviderStyle
topic_type:
- apiref
api_name:
- WM/ProviderStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a18af02254e7ce476ffc9c1e427465966cd66c84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329713"
---
# <a name="wmproviderstyle-attribute"></a>Attributo WM/ProviderStyle

L'attributo **WM/ProviderStyle** è lo stile dell'elemento assegnato dal provider dei valori dell'attributo.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Playlist CD](cd-playlist-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato nella libreria o nella cache e nel file multimediale digitale.

**Style** è un alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMProviderStyle.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





