---
title: PLAYLIST.setCheckedState
description: Il metodo setCheckedState specifica che l'elemento indicizzato nella playlist è selezionato.
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- PLAYLIST.setCheckedState Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 93e143f738197524e1555f18aedf84aa606626de645a98149c65507b71291cde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336248"
---
# <a name="playlistsetcheckedstate"></a>PLAYLIST.setCheckedState

Il **metodo setCheckedState** specifica che l'elemento indicizzato nella playlist è selezionato.

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*Elemento*
</dt> <dd>

**Numero** (**long**) che indica l'indice dell'elemento della playlist da controllare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un valore **booleano**.

## <a name="remarks"></a>Commenti

È possibile impostare tutti gli elementi sullo stato selezionato specificando 1 nel *parametro item.*

Questo metodo è stato sostituito da **setCheckedState2**, che supporta playlist annidate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.setCheckedState2**](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





