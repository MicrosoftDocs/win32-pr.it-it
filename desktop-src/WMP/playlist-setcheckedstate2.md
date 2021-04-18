---
title: PLAYLIST. setCheckedState2
description: Il metodo setCheckedState2 imposta lo stato di selezione dell'elemento con l'indice specificato nell'elemento PLAYLIST.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- PLAYLIST. setCheckedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37cc9c821ae783e79d327e93b0c2f297fb75eab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324528"
---
# <a name="playlistsetcheckedstate2"></a>PLAYLIST. setCheckedState2

Il metodo **setCheckedState2** imposta lo stato di selezione dell'elemento con l'indice specificato nell'elemento **playlist** .

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*elemento*
</dt> <dd>

**Numero** (**Long**) che indica l'indice dell'elemento della playlist da controllare o deselezionare.

</dd> <dt>

<span id="checked"></span><span id="CHECKED"></span>*selezionata*
</dt> <dd>

**Valore booleano** che indica se l'elemento specificato deve essere selezionato (true) o deselezionato (false).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore booleano**.

## <a name="remarks"></a>Commenti

Questo metodo può funzionare con playlist annidate e sostituisce il metodo **setCheckedState** , che non può. È possibile impostare tutti gli elementi sullo stato richiesto specificando 1 nel parametro *Item* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. setCheckedState**](playlist-setcheckedstate.md)
</dt> </dl>

 

 





