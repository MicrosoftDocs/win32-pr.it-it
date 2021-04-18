---
title: PLAYLIST. setSelectedState
description: Il metodo setSelectedState specifica che l'elemento indicizzato nella playlist è selezionato.
ms.assetid: 61770053-733f-40b5-8b1f-92b6975d3ad3
keywords:
- PLAYLIST. setSelectedState Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a7bb545330710ae4fe2c39eae4556207061203
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333838"
---
# <a name="playlistsetselectedstate"></a>PLAYLIST. setSelectedState

Il metodo **setSelectedState** specifica che l'elemento indicizzato nella playlist è selezionato.

``` syntax
        elementID.setSelectedState(item)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*elemento*
</dt> <dd>

**Numero** (**Long**) che indica l'indice di un elemento nella playlist.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

È possibile impostare tutti gli elementi sullo stato selezionato specificando 1 nel parametro *Item* .

Questo metodo è stato sostituito da **setSelectedState2**, che supporta le playlist nidificate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. setSelectedState2**](playlist-setselectedstate2.md)
</dt> </dl>

 

 





