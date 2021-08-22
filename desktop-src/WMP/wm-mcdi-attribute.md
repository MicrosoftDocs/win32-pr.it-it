---
title: Attributo WM/MCDI
description: L'attributo WM/MCDI è l'identificatore CD musicale del CD da cui è stato copiato il file o la traccia.
ms.assetid: f0bec14d-416c-477f-98df-dece0bf85ea4
keywords:
- Attributi WM/MCDI Windows Media Player
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 738ce8d5af7351b30fd986323db01d4dd335fa7307d2da88e48f4b2456eba1f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053849"
---
# <a name="wmmcdi-attribute"></a>Attributo WM/MCDI

**L'attributo WM/MCDI** è l'identificatore CD musicale del CD da cui è stato copiato il file o la traccia.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Tracce CD](cd-track-attributes.md)
-   [Attributi dei Windows file multimediali comunemente usati](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria (o cache) che nel file multimediale digitale.

**ToC** è un alias per questo attributo.

La Windows Media Format SDK per questo attributo è g \_ wszWMMCDI.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> </dl>

 

 





