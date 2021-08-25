---
description: 'Metodo CDynamicOutputPin.CompleteConnect: il metodo CompleteConnect completa una connessione a un pin di input.'
ms.assetid: c23195e7-8d66-4217-bd59-8889459ce4f1
title: Metodo CDynamicOutputPin.CompleteConnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6d051bdd2757e37d3939616300ab0763ef2bebec727d48477f15a23e0f5178f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983171"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a>Metodo CDynamicOutputPin.CompleteConnect

Il `CompleteConnect` metodo completa una connessione a un pin di input.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntatore all'interfaccia [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S OK in caso di esito positivo o un \_ **valore HRESULT** che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBaseOutputPin::CompleteConnect.**](cbaseoutputpin-completeconnect.md) Per supportare le riconnessioni dinamiche, questo metodo esegue il commit dell'allocatore se il filtro è attivo. Nella classe di base le connessioni possono verificarsi solo quando il filtro viene arrestato, quindi viene sempre eseguito il commit dell'allocatore nel metodo [**CBaseOutputPin::Active.**](cbaseoutputpin-active.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




