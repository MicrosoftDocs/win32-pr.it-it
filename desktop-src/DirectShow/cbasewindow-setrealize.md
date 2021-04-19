---
description: Il metodo sealize specifica se la finestra realizza le tavolozze.
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: Metodo CBaseWindow. sealize (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetRealize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 587e54cdbbbf57ddb4cf52e2d5dfb916acaee22d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333326"
---
# <a name="cbasewindowsetrealize-method"></a>Metodo CBaseWindow. sealize

Il `SetRealize` metodo specifica se la finestra realizza le tavolozze.

## <a name="syntax"></a>Sintassi


```C++
void SetRealize(
   BOOL bRealize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bRealize* 
</dt> <dd>

Valore booleano che specifica se realizzare le tavolozze. Se **true**, il metodo [**CBaseWindow:: sepalette**](cbasewindow-setpalette.md) realizza le tavolozze.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il metodo **sepalette** realizza la tavolozza specificata. Chiamare questo metodo per modificare il comportamento predefinito, in modo che le tavolozze vengano selezionate ma non realizzate. Questo metodo imposta la variabile membro [**CBaseWindow:: m \_ bNoRealize**](cbasewindow-m-bnorealize.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




