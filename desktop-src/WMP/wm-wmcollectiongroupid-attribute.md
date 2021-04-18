---
title: Attributo WM/WMCollectionGroupID
description: L'attributo WM/WMCollectionGroupID è un GUID che identifica il gruppo che contiene la raccolta a cui appartiene l'elemento.
ms.assetid: 5383fb12-fc16-474e-b9a0-c1e69b86a057
keywords:
- Media Player Windows per gli attributi WM/WMCollectionGroupID
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681ad7049520ed77de3ebb385e74efcfef66b4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329693"
---
# <a name="wmwmcollectiongroupid-attribute"></a>Attributo WM/WMCollectionGroupID

L'attributo **WM/WMCollectionGroupID** è un GUID che identifica il gruppo che contiene la raccolta a cui appartiene l'elemento.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Playlist CD](cd-playlist-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato nella libreria o nella cache e nel file multimediale digitale.

**WMCollectionGroupID** è un alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMCollectionGroupID.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





