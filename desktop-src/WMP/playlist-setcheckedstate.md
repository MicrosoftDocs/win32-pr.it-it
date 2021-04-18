---
title: PLAYLIST. setCheckedState
description: Il metodo setCheckedState specifica che l'elemento indicizzato nella playlist è selezionato.
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- PLAYLIST. setCheckedState Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a8c86459dcf590b1ff1e884a8aa671dc1bba78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324459"
---
# <a name="playlistsetcheckedstate"></a>PLAYLIST. setCheckedState

Il metodo **setCheckedState** specifica che l'elemento indicizzato nella playlist è selezionato.

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*elemento*
</dt> <dd>

**Numero** (**Long**) che indica l'indice dell'elemento della playlist da verificare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore booleano**.

## <a name="remarks"></a>Commenti

È possibile impostare tutti gli elementi sullo stato selezionato specificando 1 nel parametro *Item* .

Questo metodo è stato sostituito da **setCheckedState2**, che supporta le playlist nidificate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. setCheckedState2**](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





