---
title: Attributo WM/Provider
description: L'attributo WM/Provider è il nome del provider dei valori dell'attributo.
ms.assetid: 358651d3-5bcd-4a03-a9aa-a33745d0323a
keywords:
- Attributi wm/provider Windows Media Player
topic_type:
- apiref
api_name:
- WM/Provider
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7fa8312d095151145cfe33a139def23e20082aec2cd1d5f1c3344b9b565dfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735371"
---
# <a name="wmprovider-attribute"></a>Attributo WM/Provider

**L'attributo WM/Provider** è il nome del provider dei valori dell'attributo.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Playlist cd](cd-playlist-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [Attributi dei Windows file multimediali comunemente usati](commonly-used-windows-media-file-attributes.md)
-   [Elementi radio](radio-item-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria (o cache) che nel file multimediale digitale.

**MetadataSource** è un alias per questo attributo.

La Windows Media Format SDK per questo attributo è g \_ wszWMProvider.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successiva (l'elemento foto è supportato solo in Windows Media Player 10 o versioni successive)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> </dl>

 

 





