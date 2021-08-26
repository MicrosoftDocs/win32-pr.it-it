---
title: Attributo WM/ParentRating
description: L'attributo WM/ParentRating è la classificazione dei genitori del contenuto.
ms.assetid: 9cbe5ae7-96b9-41f2-bdfd-8043f4cbd82d
keywords:
- Attributi WM/ParentRating Windows Media Player
topic_type:
- apiref
api_name:
- WM/ParentalRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5808156e73620f775c2aa91feceaed4e06961f8e974c53a1595cdc739185062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000881"
---
# <a name="wmparentalrating-attribute"></a>Attributo WM/ParentRating

**L'attributo WM/ParentRating** è la classificazione dei genitori del contenuto.

## <a name="applies-to"></a>Si applica a

-   [Elementi audio](audio-item-attributes.md)
-   [Attributi di file multimediali Windows comunemente usati](commonly-used-windows-media-file-attributes.md)
-   [DVD](dvd-attributes.md)
-   [Elementi video](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato sia nella libreria (o cache) che nel file multimediale digitale.

La Windows media format SDK costante per questo attributo è g \_ wszWMParentalRating.

**MPAARating** è un alias per questo attributo.

Per determinare se è possibile modificare il valore di questo attributo, usare il [metodo Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento all'attributo**](attribute-reference.md)
</dt> </dl>

 

 





