---
description: Il metodo GetReader restituisce un puntatore all'interfaccia IAsyncReader del PIN di output.
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: Metodo CPullPin. GetReader (Pullpin. h)
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
ms.openlocfilehash: 3a20bbb689c4ee5e3ac12c510098163d9fbb224e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331166"
---
# <a name="cpullpingetreader-method"></a>CPullPin. GetReader, metodo

Il `GetReader` metodo restituisce un puntatore all'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) del PIN di output.

## <a name="syntax"></a>Sintassi


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .

## <a name="remarks"></a>Commenti

Il conteggio dei riferimenti dell'interfaccia restituita è in attesa. Il chiamante deve rilasciare l'interfaccia.

Il metodo non verifica il valore del puntatore a interfaccia prima di chiamare **AddRef**, quindi non chiamarlo finché il metodo [**CPullPin:: Connect**](cpullpin-connect.md) non è stato chiamato correttamente. In caso contrario, il puntatore a interfaccia potrebbe essere **null** e la chiamata a **AddRef** genererà un'eccezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




