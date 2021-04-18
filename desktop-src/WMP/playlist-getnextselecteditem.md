---
title: PLAYLIST. getNextSelectedItem
description: Il metodo getNextSelectedItem recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- PLAYLIST. getNextSelectedItem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c5e37ad5109066a11cf28a593ed69f8c86b8b639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324730"
---
# <a name="playlistgetnextselecteditem"></a>PLAYLIST. getNextSelectedItem

Il metodo **getNextSelectedItem** recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.

``` syntax
        elementID.getNextSelectedItem(item)
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

Quando non sono presenti altri elementi selezionati, questo metodo restituisce 1.

Questo metodo è stato sostituito da **getNextSelectedItem2**, che supporta le playlist nidificate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. getNextSelectedItem2**](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





