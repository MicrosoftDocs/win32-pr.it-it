---
title: Attributo WM/MediaClassSecondaryID
description: L'attributo WM/MediaClassSecondaryID è un GUID che specifica la classe multimediale secondaria, ovvero una sottoclasse della classe di supporti primaria.
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- Attributo WM/MediaClassSecondaryID Windows Media Player
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9582fc3db713b8db945ec17534f1dc9c951402eea88489285526d6a3cfbdf147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000991"
---
# <a name="wmmediaclasssecondaryid-attribute"></a>Attributo WM/MediaClassSecondaryID

**L'attributo WM/MediaClassSecondaryID** è un GUID che specifica la classe multimediale secondaria, ovvero una sottoclasse della classe di supporti primaria.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi dei file multimediali Windows comunemente usati](commonly-used-windows-media-file-attributes.md)
-   [Altri elementi](other-item-attributes.md)
-   [Elementi foto](photo-item-attributes.md)
-   [Playlist](playlist-attributes-ref.md)
-   [Elementi radio](radio-item-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

Nella tabella seguente sono elencati i GUID supportati e le relative descrizioni.



| GUID                                 | Descrizione                                    |
|--------------------------------------|------------------------------------------------|
| D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC | L'oggetto multimediale rappresenta una playlist statica. |
| EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D | L'oggetto multimediale rappresenta una playlist automatica.  |



 

**MediaClassSecondaryID è** un alias per questo attributo.

La Windows Media Format SDK per questo attributo è g \_ wszWMMediaClassSecondaryID.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | L'elemento foto è supportato solo in Windows Media Player 10 o versioni successive L'elemento radio è supportato solo nella serie Windows Media Player 9 Tutti gli altri elementi sono supportati nella serie Windows Media Player 9 e versioni successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento all'attributo**](attribute-reference.md)
</dt> </dl>

 

 





