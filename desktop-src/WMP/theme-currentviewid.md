---
title: THEME. currentViewID
description: L'attributo currentViewID specifica o recupera la visualizzazione attualmente visualizzata.
ms.assetid: 94f23da9-cfda-4dc4-9804-b7daff5ebb8f
keywords:
- THEME. currentViewID Windows Media Player
topic_type:
- apiref
api_name:
- THEME.currentViewID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c0c1b52ffdc35abf846987ed459565904938d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328548"
---
# <a name="themecurrentviewid"></a>THEME. currentViewID

L'attributo **currentViewID** specifica o recupera la **visualizzazione** attualmente visualizzata.

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura che specifica l' **ID** della **visualizzazione** corrente. e non prevede alcun valore predefinito.

## <a name="remarks"></a>Commenti

Se si specifica **currentViewID** , il **currentView** esistente (a cui fa riferimento l'attributo **View** Global) viene chiuso automaticamente e viene aperta la **visualizzazione** specificata.

## <a name="examples"></a>Esempio


```C++
<THEME currentViewID="startView">
  <VIEW>
    <TEXT value="this would have been the default view"/>
  </VIEW>
  <VIEW id="startView">
    <TEXT value="go to new view"
        onclick="jscript:theme.currentViewID='newView'"/>
  </VIEW>
  <VIEW id="newView">
    <TEXT value="new view"/>
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> </dl>

 

 





