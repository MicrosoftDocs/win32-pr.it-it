---
title: Visualizza. Restore
description: Il metodo Restore ripristina la visualizzazione.
ms.assetid: 8005c14e-771b-4f20-8039-fc09869dc726
keywords:
- Visualizza. ripristino di Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: db92fc5e796acc55fe9c4faf93417d648652415e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329066"
---
# <a name="viewrestore"></a>Visualizza. Restore

Il metodo **Restore ripristina** la **visualizzazione**.

``` syntax
        elementID.restore()
```

## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="examples"></a>Esempio


```JScript
<THEME>
  <VIEW id="View1">
    <BUTTON id="Open" image="Open.png" 
        onclick="jscript:View1.restore()">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> </dl>

 

 





