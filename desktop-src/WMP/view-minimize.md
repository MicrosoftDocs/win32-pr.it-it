---
title: Visualizza. Riduci a icona
description: Il metodo di riduzione a icona riduce al minimo la visualizzazione.
ms.assetid: 97c257fa-aa4f-4e6f-bc49-fa54db63b59b
keywords:
- Visualizza. ridurre a icona Media Player Windows
topic_type:
- apiref
api_name:
- VIEW.minimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e01c35ad5a77c5a78a705d0188f771e0466a761
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330991"
---
# <a name="viewminimize"></a>Visualizza. Riduci a icona

Il metodo di **riduzione** a icona riduce al minimo la **visualizzazione**.

``` syntax
        elementID.minimize()
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
        onclick="jscript:View1.minimize()">
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
</dt> <dt>

[**Visualizza. ingrandisce**](view-maximize.md)
</dt> </dl>

 

 





