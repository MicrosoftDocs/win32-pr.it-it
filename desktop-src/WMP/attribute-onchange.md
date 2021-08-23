---
title: attribute_onchange
description: Quando un attributo dell'interfaccia cambia valore, si verifica un evento che può essere gestito da un gestore eventi. Il nome del gestore eventi è il nome dell'attributo seguito da un carattere di sottolineatura e \ 0034;onchange \ 0034;, ad esempio \ 0034;value \_ onchange \ 0034;.
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange Windows Media Player
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c707b04587b6e975f81c8a0d0918b14c8e193d303f82c61b5220796bb6975b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573761"
---
# <a name="attribute_onchange"></a>onchange \_ dell'attributo

Quando un attributo dell'interfaccia cambia valore, si verifica un evento che può essere gestito da un gestore eventi. Il nome del gestore eventi è il nome dell'attributo seguito da un carattere di sottolineatura e da "onchange", ad esempio "value \_ onchange".

``` syntax
        attribute_onchange
```

## <a name="examples"></a>Esempio


```JScript
<SLIDER 
  thumbImage = "thumb.gif"
  value_onchange = "JScript: if (value == 100) backgroundColor = 'green';"
/>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------|
| Versione<br/> | Windows Media Player versione 70 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Gestori eventi di ambiente**](ambient-event-handlers.md)
</dt> </dl>

 

 





