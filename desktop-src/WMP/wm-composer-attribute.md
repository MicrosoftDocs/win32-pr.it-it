---
title: Attributo WM/Composer
description: L'attributo WM/Composer è il nome del compositore della musica.
ms.assetid: 48459027-ed80-46a2-ad5c-ace602144150
keywords:
- Attributi WM/Composer Windows Media Player
topic_type:
- apiref
api_name:
- WM/Composer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f41e92e1f343ecbd532769560a6d2d555c275e147ab2386ae574c2dea8bc411c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001171"
---
# <a name="wmcomposer-attribute"></a>Attributo WM/Composer

**L'attributo WM/Composer** è il nome del compositore della musica.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Playlist cd](cd-playlist-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [Attributi dei Windows file multimediali comunemente usati](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria (o cache) che nel file multimediale digitale.

Questo attributo può avere più valori. Per recuperare tutti i valori per un attributo multivalore, è necessario usare il metodo **Media.getItemInfoByType,** non il **metodo Media.getItemInfo.**

**Composer** è un alias per questo attributo.

La Windows Media Format SDK per questo attributo è g \_ wszWMComposer.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





