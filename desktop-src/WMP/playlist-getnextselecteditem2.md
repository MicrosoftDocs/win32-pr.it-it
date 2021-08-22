---
title: PLAYLIST.getNextSelectedItem2
description: Il metodo getNextSelectedItem2 recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- PLAYLIST.getNextSelectedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6d1f98a418da1d8b21345598999f847cbf2142e9ca575bcfdc7047e2f9fd524
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415281"
---
# <a name="playlistgetnextselecteditem2"></a>PLAYLIST.getNextSelectedItem2

Il **metodo getNextSelectedItem2** recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.

``` syntax
        elementID.getNextSelectedItem2(item)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Elemento*
</dt> <dd>

**Numero** (**long**) che indica l'indice dell'elemento in base al quale eseguire la ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore Number** (**long**).

## <a name="remarks"></a>Commenti

Questo metodo può funzionare con playlist annidate e sostituisce il **metodo getNextSelectedItem,** che non può. Passare 1 nel parametro *item* per trovare il primo elemento selezionato. Quando non sono presenti altri elementi selezionati, viene restituito -1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.getNextSelectedItem**](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





