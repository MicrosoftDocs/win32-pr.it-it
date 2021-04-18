---
title: attribute_onchange
description: Quando un attributo Skin cambia valore, si verifica un evento che può essere gestito da un gestore eventi. Il nome del gestore eventi è il nome dell'attributo seguito da un carattere di sottolineatura e da \ 0034; OnChange \ 0034;, ad esempio \ 0034; value \_ OnChange \ 0034;.
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
ms.openlocfilehash: 45c4955193507e258d055a3399fc565c569fd291
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330740"
---
# <a name="attribute_onchange"></a>attributo \_ OnChange

Quando un attributo Skin cambia valore, si verifica un evento che può essere gestito da un gestore eventi. Il nome del gestore eventi è il nome dell'attributo seguito da un carattere di sottolineatura e da "onChange", ad esempio "valore \_ OnChange".

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

 

 





