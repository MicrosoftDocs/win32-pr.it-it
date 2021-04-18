---
title: TEMA. openView
description: Il metodo openView apre una visualizzazione in una nuova finestra.
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- TEMA. openView Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d66ff2cf47004c7687a37f1f22a87bdeb534d344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328391"
---
# <a name="themeopenview"></a>TEMA. openView

Il metodo **openView** apre una **visualizzazione** in una nuova finestra.

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*visualizzare*
</dt> <dd>

**Stringa** che specifica l' **ID** della **visualizzazione** da aprire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="examples"></a>Esempio


```JScript
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

[**THEME. closeView**](theme-closeview.md)
</dt> <dt>

[**THEME. openViewRelative**](theme-openviewrelative.md)
</dt> </dl>

 

 





