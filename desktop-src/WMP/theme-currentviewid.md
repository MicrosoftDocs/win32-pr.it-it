---
title: THEME.currentViewID
description: L'attributo currentViewID specifica o recupera l'elemento VIEW attualmente visualizzato.
ms.assetid: 94f23da9-cfda-4dc4-9804-b7daff5ebb8f
keywords:
- THEME.currentViewID Windows Media Player
topic_type:
- apiref
api_name:
- THEME.currentViewID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21bf3027b0249286689862e53fc2d616d1d33b19eca562c886e981bffb7f0267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117812"
---
# <a name="themecurrentviewid"></a>THEME.currentViewID

**L'attributo currentViewID** specifica o recupera l'oggetto **VIEW attualmente visualizzato.**

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura** che specifica **l'ID** dell'oggetto **VIEW corrente.** e non prevede alcun valore predefinito.

## <a name="remarks"></a>Commenti

Se si specifica **currentViewID,** l'oggetto **currentView esistente** (a cui punta l'attributo **globale della** visualizzazione) viene chiuso automaticamente e viene aperto l'oggetto **VIEW specificato.**

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
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> </dl>

 

 





