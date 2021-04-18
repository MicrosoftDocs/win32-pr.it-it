---
title: PLAYLIST. getNextCheckedItem
description: Il metodo getNextCheckedItem recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- PLAYLIST. getNextCheckedItem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b4a85fdccc5de227ab8aea3d0ee4f93d46eed50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324733"
---
# <a name="playlistgetnextcheckeditem"></a>PLAYLIST. getNextCheckedItem

Il metodo **getNextCheckedItem** recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.

``` syntax
        elementID.getNextCheckedItem(item)
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

Quando non sono presenti altri elementi controllati, questo metodo restituisce 1.

Questo metodo è stato sostituito da **getNextCheckedItem2**, che supporta le playlist nidificate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. getNextCheckedItem2**](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





