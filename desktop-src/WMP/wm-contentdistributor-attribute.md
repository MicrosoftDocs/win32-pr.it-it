---
title: Attributo WM/ContentDistributor
description: L'attributo WM/ContentDistributor è il nome del server di distribuzione dell'elemento.
ms.assetid: 45f548a4-4059-464c-af93-1ba09e6b8d1e
keywords:
- Media Player Windows per gli attributi WM/ContentDistributor
topic_type:
- apiref
api_name:
- WM/ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420e3e05a68f89d8e37b8ef95dd1247802442700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327026"
---
# <a name="wmcontentdistributor-attribute"></a>Attributo WM/ContentDistributor

L'attributo **WM/contentdistributor** è il nome del server di distribuzione dell'elemento.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi di file di Windows Media usati di frequente](commonly-used-windows-media-file-attributes.md)
-   [Playlist](playlist-attributes-ref.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria che nel file multimediale digitale.

**Contentdistributor** è un alias per questo attributo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMContentDistributor.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





