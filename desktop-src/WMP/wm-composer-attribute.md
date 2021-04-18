---
title: Attributo WM/Composer
description: L'attributo WM/Composer è il nome del compositore di Music.
ms.assetid: 48459027-ed80-46a2-ad5c-ace602144150
keywords:
- Windows Media Player attributo WM/Composer
topic_type:
- apiref
api_name:
- WM/Composer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f206b1a23126612f3f7c875b9a9b4badca8339
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327030"
---
# <a name="wmcomposer-attribute"></a>Attributo WM/Composer

L'attributo **WM/Composer** è il nome del compositore di Music.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Playlist CD](cd-playlist-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato nella libreria o nella cache e nel file multimediale digitale.

Questo attributo può avere più valori. Per recuperare tutti i valori per un attributo multivalore, è necessario usare il metodo **Media. getItemInfoByType** , non il metodo **Media. GetItemInfo** .

**Composer** è un alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMComposer.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





