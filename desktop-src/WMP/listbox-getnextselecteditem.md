---
title: LISTBOX.getNextSelectedItem
description: Il metodo getNextSelectedItem recupera l'elemento selezionato successivo nel controllo casella di riepilogo a partire dall'elemento successivo a quello con l'indice specificato.
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- LISTBOX.getNextSelectedItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f4a5d95880b1300ebfb7f1732e7c20b6975ad82cf2d15514c58e68b9f9c42cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003401"
---
# <a name="listboxgetnextselecteditem"></a>LISTBOX.getNextSelectedItem

Il **metodo getNextSelectedItem** recupera l'elemento selezionato successivo nel controllo casella di riepilogo a partire dall'elemento successivo a quello con l'indice specificato.

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*Startindex*
</dt> <dd>

**Numero** (**long**) contenente l'indice dell'elemento che precede l'elemento recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore Number** (**long**) contenente l'indice dell'elemento selezionato successivo.

## <a name="remarks"></a>Commenti

Per avviare la ricerca dall'inizio, usare 1 per l'indice iniziale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





