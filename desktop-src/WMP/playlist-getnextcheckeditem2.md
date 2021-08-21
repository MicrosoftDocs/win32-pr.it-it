---
title: PLAYLIST.getNextCheckedItem2
description: Il metodo getNextCheckedItem2 recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- PLAYLIST.getNextCheckedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9bd39ba95aff88bccfa43885f8c15fba6bb0beef20d51dd3ca4cf6f36bda05b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118834868"
---
# <a name="playlistgetnextcheckeditem2"></a>PLAYLIST.getNextCheckedItem2

Il **metodo getNextCheckedItem2** recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.

``` syntax
        elementID.getNextCheckedItem2(item)
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

Questo metodo può funzionare con playlist annidate e sostituisce il **metodo getNextCheckedItem,** che non può. Passare 1 nel parametro *item* per trovare il primo elemento selezionato. Quando non sono presenti altri elementi selezionati, questo metodo restituisce 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.getNextCheckedItem**](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





