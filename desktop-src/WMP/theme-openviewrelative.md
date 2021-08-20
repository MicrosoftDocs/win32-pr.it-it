---
title: THEME.openViewRelative
description: Il metodo openViewRelative apre un elemento VIEW in una nuova finestra in una posizione iniziale specificata rispetto all'angolo superiore sinistro dell'interfaccia.
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- THEME.openViewRelative Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a26040bb8f47d85be99f0d8df602bdd69835cfa648ac6d5898f786e4518acdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117775"
---
# <a name="themeopenviewrelative"></a>THEME.openViewRelative

Il **metodo openViewRelative** apre un elemento **VIEW** in una nuova finestra in una posizione iniziale specificata rispetto all'angolo superiore sinistro dell'interfaccia.

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*Mostra*
</dt> <dd>

Valore **String** che specifica **l'ID** dell'oggetto **VIEW** da aprire.

</dd> <dt>

<span id="left"></span><span id="LEFT"></span>*Sinistra*
</dt> <dd>

Valore **Number** (**long**) che specifica la distanza iniziale in pixel del bordo sinistro dell'oggetto **VIEW** dal bordo sinistro dell'interfaccia. Un valore negativo indica una posizione iniziale a sinistra del bordo dell'interfaccia.

</dd> <dt>

<span id="top"></span><span id="TOP"></span>*In alto*
</dt> <dd>

Valore **Number** (**long**) che specifica la posizione iniziale del bordo superiore dell'elemento **VIEW** rispetto al bordo superiore dell'interfaccia. Un valore negativo indica una posizione iniziale sopra il bordo dell'interfaccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La posizione specificata per **VIEW viene** utilizzata la prima volta che viene chiamato questo metodo, dopo il quale l'utente può trascinare **view** in un'altra posizione. La nuova posizione viene salvata e nelle chiamate successive viene usata la posizione più recente.

## <a name="examples"></a>Esempio


```JScript
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openViewRelative('newView', 50, 50)"/>
    <TEXT top="30" value="close" 
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**THEME.closeView**](theme-closeview.md)
</dt> <dt>

[**THEME.openView**](theme-openview.md)
</dt> </dl>

 

 





