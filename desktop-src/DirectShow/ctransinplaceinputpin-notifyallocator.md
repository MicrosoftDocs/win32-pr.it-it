---
description: 'Metodo CTransInPlaceInputPin.NotifyAllocator : il metodo NotifyAllocator specifica un allocatore per la connessione. Questo metodo implementa il metodo IMemInputPin::NotifyAllocator.'
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: Metodo CTransInPlaceInputPin.NotifyAllocator (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca15be5dc1893a393e6052832cc7522f27355eeb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094749"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a>Metodo CTransInPlaceInputPin.NotifyAllocator

Il `NotifyAllocator` metodo specifica un allocatore per la connessione. Questo metodo implementa il [**metodo IMemInputPin::NotifyAllocator.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)

## <a name="syntax"></a>Sintassi


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAllocator* 
</dt> <dd>

Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.

</dd> <dt>

*bReadOnly* 
</dt> <dd>

Flag che specifica se i campioni di questo allocatore sono di sola lettura. Se **TRUE,** gli esempi sono di sola lettura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Operazione riuscita<br/>                   |
| <dl> <dt>**E \_ FAIL**</dt> </dl>    | Operazioni non riuscite<br/>                   |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | **Argomento puntatore NULL**<br/> |



 

## <a name="remarks"></a>Commenti

Il filtro tenta di usare lo stesso allocatore per entrambe le connessioni pin.

-   Se il pin di output non è connesso, il pin di input accetta automaticamente l'allocatore. Quando il pin di output è connesso, il filtro riconnetterà il pin di input. A questo punto, il filtro tenterà di nuovo di usare un singolo allocatore.
-   Se il pin di output è connesso, il pin di input accetta l'allocatore. Il pin di output usa anche lo stesso allocatore. Chiama sul `NotifyAllocator` pin di input downstream.

Il caso precedente presenta l'eccezione seguente:

-   Se l'allocatore proposto è di sola lettura, ovvero il parametro *bReadOnly* è **TRUE** e il filtro deve modificare gli esempi, il filtro deve usare due allocatori diversi. In questo caso, se il filtro upstream propone di usare l'allocatore del filtro downstream, il metodo restituisce E \_ FAIL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




