---
description: Il metodo BreakConnect rilascia un pin da una connessione.
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: Metodo CTransformFilter. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec60322a4782d84e84dc2030b69f6c385783e98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325733"
---
# <a name="ctransformfilterbreakconnect-method"></a>CTransformFilter. BreakConnect, metodo

Il `BreakConnect` metodo rilascia un pin da una connessione.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT BreakConnect(
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dir* 
</dt> <dd>

Membro del tipo enumerato di [**\_ direzione del pin**](/windows/win32/api/strmif/ne-strmif-pin_direction) , che specifica quale connessione del PIN è stata interrotta (input o output).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

I metodi [**CTransformInputPin:: BreakConnect**](ctransforminputpin-breakconnect.md) e [**CTransformOutputPin:: BreakConnect**](ctransformoutputpin-breakconnect.md) chiamano questo metodo quando viene interruppe una connessione al pin. Questo metodo non esegue alcuna operazione nella classe di base. Se si esegue l'override del metodo [**CheckConnect**](ctransformfilter-checkconnect.md) , eseguire l'override di questo metodo per rilasciare tutte le risorse ottenute nel metodo **CheckConnect** , inclusi i puntatori di interfaccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




