---
title: Attributo WM/PartOfSet
description: L'attributo WM/PartOfSet è il numero di parte e il numero totale di parti del set a cui appartiene l'elemento.
ms.assetid: c6827c31-c625-4283-a50d-f08eccf87271
keywords:
- Media Player Windows per gli attributi WM/PartOfSet
topic_type:
- apiref
api_name:
- WM/PartOfSet
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27d6297931c503c95c8ef0462bf7b119a0ffb75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331208"
---
# <a name="wmpartofset-attribute"></a>Attributo WM/PartOfSet

L'attributo **WM/PartOfSet** è il numero di parte e il numero totale di parti del set a cui appartiene l'elemento.

## <a name="applies-to"></a>Si applica a

-   [File musicali](music-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato solo in un file musicale non presente nella libreria.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMPartOfSet.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





