---
title: AmbientAttributes.height
description: L'attributo height specifica o recupera l'altezza del controllo.
ms.assetid: a5c85d86-15d4-451d-b8bc-ed3b6e0dfd7d
keywords:
- AmbientAttributes.height Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.height
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbc03f631fffc4d1544906721476f229cbeb926e5d56b08dc1647f2dfd3b243
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098951"
---
# <a name="ambientattributesheight"></a>AmbientAttributes.height

**L'attributo** height specifica o recupera l'altezza del controllo.

``` syntax
        elementID.height
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un numero **di** lettura/scrittura (**long**) che rappresenta l'altezza del controllo in pixel. Il valore predefinito è zero o l'altezza dell'immagine specificata nell'attributo **image del** controllo.

## <a name="remarks"></a>Commenti

Se l'altezza specificata è inferiore all'altezza dell'immagine specificata, l'immagine verrà ritagliata. Se l'altezza è maggiore dell'altezza dell'immagine, l'area di clic supera il limite dell'immagine. Indipendentemente dal valore assegnato a questo attributo, l'immagine non può aumentare oltre il valore **VIEW** o **SUBVIEW padre.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





