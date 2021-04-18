---
title: AmbientAttributes. Height
description: L'attributo Height specifica o recupera l'altezza del controllo.
ms.assetid: a5c85d86-15d4-451d-b8bc-ed3b6e0dfd7d
keywords:
- Media Player Windows AmbientAttributes. Height
topic_type:
- apiref
api_name:
- AmbientAttributes.height
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662268bfeaf00b3185d531ff10d8dd17c9127a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331405"
---
# <a name="ambientattributesheight"></a>AmbientAttributes. Height

L'attributo **Height** specifica o recupera l'altezza del controllo.

``` syntax
        elementID.height
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**Long**) che rappresenta l'altezza del controllo in pixel. Il valore predefinito è zero o l'altezza dell'immagine specificata nell'attributo **Image** del controllo.

## <a name="remarks"></a>Commenti

Se l'altezza specificata è inferiore all'altezza dell'immagine specificata, l'immagine verrà ritagliata. Se l'altezza è maggiore dell'altezza dell'immagine, l'area di clic andrà oltre il limite dell'immagine. Indipendentemente dal valore assegnato a questo attributo, l'immagine non può superare la **visualizzazione** padre o la relativa **visualizzazione**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





