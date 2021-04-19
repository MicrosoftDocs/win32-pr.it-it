---
title: Attributo Description (WMP SDK)
description: L'attributo Description è una descrizione del contenuto.
ms.assetid: 8bf76bf5-2bba-4ceb-bc98-f8b8ab2c8b6f
keywords:
- Attributo Description Media Player Windows
topic_type:
- apiref
api_name:
- Description
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4bc3562e7b807dc0e333c887aad1550d05b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326024"
---
# <a name="description-attribute"></a>Description (attributo)

L'attributo **Description** è una descrizione del contenuto.

## <a name="applies-to"></a>Si applica a

-   [File musicali](music-file-attributes.md)

## <a name="remarks"></a>Commenti

Questo attributo viene archiviato in file musicali, non nella libreria.

Questo attributo può avere più valori. Per recuperare tutti i valori per un attributo multivalore, è necessario usare il *supporto*. metodo **getItemInfoByType** , non il metodo *media*. GetItemInfo.

La costante Windows Media Format SDK per questo attributo è g \_ wszWMDescription.

Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





