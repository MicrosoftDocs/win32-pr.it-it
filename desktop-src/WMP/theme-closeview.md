---
title: THEME. closeView
description: Il metodo closeView chiude una visualizzazione aperta.
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- THEME. closeView Windows Media Player
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b39083979809fc2e747c54569db8d03298a951c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327284"
---
# <a name="themecloseview"></a>THEME. closeView

Il metodo **closeView** chiude una **visualizzazione** aperta.

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*theView*
</dt> <dd>

**Stringa** che specifica l' **ID** della **visualizzazione** da chiudere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="examples"></a>Esempio


```C++
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openView('newView')"/>
    <TEXT top="30" value="close"
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**TEMA. openView**](theme-openview.md)
</dt> </dl>

 

 





