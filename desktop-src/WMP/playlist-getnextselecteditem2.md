---
title: PLAYLIST. getNextSelectedItem2
description: Il metodo getNextSelectedItem2 recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- PLAYLIST. getNextSelectedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 27d166887bb2fa98e184e1f64f4aaceb89930d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324726"
---
# <a name="playlistgetnextselecteditem2"></a>PLAYLIST. getNextSelectedItem2

Il metodo **getNextSelectedItem2** recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.

``` syntax
        elementID.getNextSelectedItem2(item)
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

Questo metodo può funzionare con playlist annidate e sostituisce il metodo **getNextSelectedItem** , che non può. Passare 1 nel parametro *Item* per trovare il primo elemento selezionato. Quando non sono presenti altri elementi selezionati, viene restituito-1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. getNextSelectedItem**](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





