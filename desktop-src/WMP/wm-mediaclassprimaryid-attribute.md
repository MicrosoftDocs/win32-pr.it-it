---
title: Attributo WM/MediaClassPrimaryID
description: L'attributo WM/MediaClassPrimaryID è un GUID che specifica una delle classi multimediali principali music, audio non musicale, video o altro.
ms.assetid: eb78f4a9-7c18-4cad-bb34-fd1ff15bad4f
keywords:
- Attributo WM/MediaClassPrimaryID Windows Media Player
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aebc52488ebcabfca843a8fdfdfbb51307cd96be4fe923386c718bab8752c61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506461"
---
# <a name="wmmediaclassprimaryid-attribute"></a>Attributo WM/MediaClassPrimaryID

**L'attributo WM/MediaClassPrimaryID** è un GUID che specifica una delle classi multimediali principali: musica, audio non musicale, video o altro.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi dei Windows file multimediali comunemente usati](commonly-used-windows-media-file-attributes.md)
-   [Altri elementi](other-item-attributes.md)
-   [Elementi foto](photo-item-attributes.md)
-   [Playlist](playlist-attributes-ref.md)
-   [Elementi radio](radio-item-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

**MediaClassPrimaryID è** un alias per questo attributo.

La Windows Media Format SDK per questo attributo è g \_ wszWMMediaClassPrimaryID.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successiva (l'elemento foto è supportato solo in Windows Media Player 10 o versioni successive)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> </dl>

 

 





