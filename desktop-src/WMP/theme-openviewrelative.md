---
title: THEME. openViewRelative
description: Il metodo openViewRelative apre una visualizzazione in una nuova finestra in corrispondenza della posizione iniziale specificata rispetto all'angolo superiore sinistro dell'interfaccia.
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- THEME. openViewRelative Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80ec93055535640b84c33dde2b61ee59cd5bfdcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328390"
---
# <a name="themeopenviewrelative"></a>THEME. openViewRelative

Il metodo **openViewRelative** apre una **visualizzazione** in una nuova finestra in corrispondenza della posizione iniziale specificata rispetto all'angolo superiore sinistro dell'interfaccia.

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*visualizzare*
</dt> <dd>

**Stringa** che specifica l' **ID** della **visualizzazione** da aprire.

</dd> <dt>

<span id="left"></span><span id="LEFT"></span>*sinistra*
</dt> <dd>

**Numero** (**Long**) che specifica la distanza iniziale, in pixel, del bordo sinistro della **visualizzazione** dal bordo sinistro dell'interfaccia. Un valore negativo indica una posizione iniziale a sinistra del bordo dell'interfaccia.

</dd> <dt>

<span id="top"></span><span id="TOP"></span>*In alto*
</dt> <dd>

**Numero** (**Long**) che specifica la posizione iniziale del bordo superiore della **visualizzazione** rispetto al bordo superiore dell'interfaccia. Un valore negativo indica una posizione iniziale sopra il bordo dell'interfaccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La posizione specificata per la **visualizzazione** viene utilizzata la prima volta che viene chiamato questo metodo, dopo il quale l'utente può trascinare la **visualizzazione** in un'altra posizione. La nuova posizione viene salvata e, nelle chiamate successive, viene usata la posizione più recente.

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
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**THEME. closeView**](theme-closeview.md)
</dt> <dt>

[**TEMA. openView**](theme-openview.md)
</dt> </dl>

 

 





