---
description: Il metodo GetReader restituisce un puntatore all'interfaccia IAsyncReader del pin di output.
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: Metodo CPullPin.GetReader (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.GetReader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7880cba8e910c3da8ade049e18ae22e403c0c616246e4dfde94e587a1fcdeab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055001"
---
# <a name="cpullpingetreader-method"></a>Metodo CPullPin.GetReader

Il `GetReader` metodo restituisce un puntatore all'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) del pin di output.

## <a name="syntax"></a>Sintassi


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore [**all'interfaccia IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)

## <a name="remarks"></a>Commenti

L'interfaccia restituita ha un conteggio dei riferimenti in sospeso. Il chiamante deve rilasciare l'interfaccia .

Il metodo non controlla il valore del puntatore a interfaccia prima di chiamare **AddRef,** quindi non chiamare questo metodo fino a quando non viene chiamato correttamente il metodo [**CPullPin::Connessione.**](cpullpin-connect.md) In caso contrario, il puntatore a interfaccia **potrebbe essere NULL** e la chiamata di **AddRef** genererà un'eccezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




