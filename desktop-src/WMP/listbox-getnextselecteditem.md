---
title: LISTBOX. getNextSelectedItem
description: Il metodo getNextSelectedItem Recupera il successivo elemento selezionato nel controllo casella di riepilogo a partire dall'elemento dopo quello con l'indice specificato.
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- Media Player di Windows LISTBOX. getNextSelectedItem
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afb3df1f1b6a6adc528e02dd6531ac4fc1a9a3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327742"
---
# <a name="listboxgetnextselecteditem"></a>LISTBOX. getNextSelectedItem

Il metodo **getNextSelectedItem** Recupera il successivo elemento selezionato nel controllo casella di riepilogo a partire dall'elemento dopo quello con l'indice specificato.

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*
</dt> <dd>

**Numero** (**Long**) che contiene l'indice dell'elemento che precede l'elemento recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **numero** (**Long**) che contiene l'indice del successivo elemento selezionato.

## <a name="remarks"></a>Commenti

Per avviare la ricerca dall'inizio, utilizzare 1 per l'indice iniziale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LISTBOX (elemento)**](listbox-element.md)
</dt> </dl>

 

 





