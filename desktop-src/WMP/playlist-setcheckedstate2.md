---
title: PLAYLIST.setCheckedState2
description: Il metodo setCheckedState2 imposta lo stato selezionato dell'elemento con l'indice specificato nell'elemento PLAYLIST.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- PLAYLIST.setCheckedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b6b95cb332c5f5a9d86e6f49484b27c1ab5802f28b18195f610395a1c732e369
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336220"
---
# <a name="playlistsetcheckedstate2"></a>PLAYLIST.setCheckedState2

Il **metodo setCheckedState2** imposta lo stato selezionato dell'elemento con l'indice specificato nell'elemento **PLAYLIST.**

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Elemento*
</dt> <dd>

**Numero** (**long**) che indica l'indice dell'elemento della playlist da controllare o deselezionare.

</dd> <dt>

<span id="checked"></span><span id="CHECKED"></span>*Controllato*
</dt> <dd>

**Valore** booleano che indica se l'elemento specificato deve essere controllato (true) o deselezionato (false).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un valore **booleano.**

## <a name="remarks"></a>Commenti

Questo metodo può essere utilizzato con playlist annidate e sostituisce il **metodo setCheckedState,** che non può. È possibile impostare tutti gli elementi sullo stato richiesto specificando 1 nel *parametro item.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.setCheckedState**](playlist-setcheckedstate.md)
</dt> </dl>

 

 





