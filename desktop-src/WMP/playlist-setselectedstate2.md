---
title: PLAYLIST. setSelectedState2
description: Il metodo setSelectedState2 imposta lo stato selezionato dell'elemento con l'indice specificato nell'elemento PLAYLIST.
ms.assetid: 990b834a-f7ed-45b8-99e1-3efd7f4447f4
keywords:
- PLAYLIST. setSelectedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1a4e317543765fb24755516a0637b16958ad679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333834"
---
# <a name="playlistsetselectedstate2"></a>PLAYLIST. setSelectedState2

Il metodo **setSelectedState2** imposta lo stato selezionato dell'elemento con l'indice specificato nell'elemento **playlist** .

``` syntax
        elementID.setSelectedState2(item, selected)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*elemento*
</dt> <dd>

**Numero** (**Long**) che indica l'indice di un elemento nella playlist.

</dd> <dt>

<span id="selected"></span><span id="SELECTED"></span>*selezionato*
</dt> <dd>

**Valore booleano** che indica se l'elemento specificato deve essere selezionato (true) o deselezionato (false).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo può funzionare con playlist annidate e sostituisce il metodo **setSelectedState** che non può. È possibile impostare tutti gli elementi sullo stato richiesto specificando 1 nel parametro *Item* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. setSelectedState**](playlist-setselectedstate.md)
</dt> </dl>

 

 





