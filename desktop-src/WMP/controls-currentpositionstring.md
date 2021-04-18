---
title: Controls. currentPositionString
description: La proprietà currentPositionString recupera la posizione corrente nell'elemento multimediale come stringa formattata come HH MM SS (ore, minuti e secondi).
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- Media Player di Windows Controls. currentPositionString
topic_type:
- apiref
api_name:
- Controls.currentPositionString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf3472d71afc543c596485d10f0d7e59dde90a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331760"
---
# <a name="controlscurrentpositionstring"></a>Controls. currentPositionString

La proprietà **currentPositionString** recupera la posizione corrente nell'elemento multimediale come **stringa** formattata come HH: mm: SS (ore, minuti e secondi).

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di sola lettura.

## <a name="remarks"></a>Commenti

Se la lunghezza dell'elemento multimediale è inferiore a un'ora, la parte HH: non è inclusa.

> [!Note]  
> È necessario includere il codice per arrestare il timer quando l'elemento multimediale viene arrestato o sospeso.

 

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene avviato un timer HTML che visualizza la posizione corrente del file multimediale a intervalli di un secondo. È stato creato un elemento di testo HTML denominato testo per visualizzare la posizione corrente. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> </dl>

 

 





