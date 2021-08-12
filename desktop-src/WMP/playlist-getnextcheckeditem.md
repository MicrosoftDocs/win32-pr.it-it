---
title: PLAYLIST.getNextCheckedItem
description: Il metodo getNextCheckedItem recupera l'indice dell'elemento selezionato successivo nella playlist che segue l'indice specificato.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- PLAYLIST.getNextCheckedItem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54b6e598737d1aac09754b15c037c27a435deb5fff34c729aa48c51019e12982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571451"
---
# <a name="playlistgetnextcheckeditem"></a>PLAYLIST.getNextCheckedItem

Il **metodo getNextCheckedItem** recupera l'indice dell'elemento selezionato successivo nella playlist che segue l'indice specificato.

``` syntax
        elementID.getNextCheckedItem(item)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Elemento*
</dt> <dd>

**Numero** (**long**) che indica l'indice dell'elemento in cui eseguire la ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore Number** (**long**).

## <a name="remarks"></a>Commenti

Quando non sono presenti altri elementi controllati, questo metodo restituisce 1.

Questo metodo è stato sostituito da **getNextCheckedItem2**, che supporta playlist annidate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.getNextCheckedItem2**](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





