---
title: PLAYLIST. getNextCheckedItem2
description: Il metodo getNextCheckedItem2 recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- PLAYLIST. getNextCheckedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50bb2fd6ed6e3328df29a59381571204ebd28369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324732"
---
# <a name="playlistgetnextcheckeditem2"></a>PLAYLIST. getNextCheckedItem2

Il metodo **getNextCheckedItem2** recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.

``` syntax
        elementID.getNextCheckedItem2(item)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*elemento*
</dt> <dd>

**Numero** (**Long**) che indica l'indice dell'elemento in cui eseguire la ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **numero** (**Long**).

## <a name="remarks"></a>Commenti

Questo metodo può funzionare con playlist annidate e sostituisce il metodo **getNextCheckedItem** , che non può. Passare 1 nel parametro *Item* per trovare il primo elemento selezionato. Quando non sono presenti altri elementi controllati, questo metodo restituisce 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. getNextCheckedItem**](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





