---
title: THEME.closeView
description: Il metodo closeView chiude un elemento VIEW aperto.
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- Theme.closeView Windows Media Player
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e66a0c56ab2f5fc3d5d6a27d996d8b3f3cf7834c61e62113a40af3c42aeb4d59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117932546"
---
# <a name="themecloseview"></a>THEME.closeView

Il **metodo closeView** chiude un oggetto **VIEW aperto.**

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*Visualizzazione*
</dt> <dd>

Valore **String** che specifica **l'ID** dell'oggetto **VIEW** da chiudere.

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
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**THEME.openView**](theme-openview.md)
</dt> </dl>

 

 





