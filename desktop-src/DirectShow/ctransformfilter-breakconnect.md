---
description: Il metodo BreakConnect rilascia un pin da una connessione.
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: Metodo CTransformFilter.BreakConnect (Transfrm.h)
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
ms.openlocfilehash: 3c4e77e28548c1f181cb5f8a6c106572d243314c5afd9d9126024e9b84fbe02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053811"
---
# <a name="ctransformfilterbreakconnect-method"></a>Metodo CTransformFilter.BreakConnect

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

Membro del tipo [**enumerato \_ PIN DIRECTION,**](/windows/win32/api/strmif/ne-strmif-pin_direction) che specifica quale connessione pin è stata interrotta (input o output).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

I [**metodi CTransformInputPin::BreakConnect**](ctransforminputpin-breakconnect.md) e [**CTransformOutputPin::BreakConnect**](ctransformoutputpin-breakconnect.md) chiamano questo metodo quando viene interrotta una connessione pin. Questo metodo non esegue alcuna operazione nella classe di base. Se si esegue l'override [**del metodo CheckConnect,**](ctransformfilter-checkconnect.md) eseguire l'override di questo metodo per rilasciare tutte le risorse ottenute nel **metodo CheckConnect,** inclusi i puntatori a interfaccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




