---
description: Il metodo DecideAllocator negozia un allocatore con il pin di output.
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: Metodo CPullPin. DecideAllocator (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91ffa139b916b1594e0729a0f8d52f07c62eda12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331177"
---
# <a name="cpullpindecideallocator-method"></a>CPullPin. DecideAllocator, metodo

Il `DecideAllocator` Metodo negozia un allocatore con il pin di output.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT DecideAllocator(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAlloc* 
</dt> <dd>

Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore preferito del PIN di input o **null**.

</dd> <dt>

*pProps* 
</dt> <dd>

Puntatore a una struttura [**di \_ Proprietà allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) facoltativa che contiene i requisiti del buffer del PIN di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se l'esito è positivo o un codice di errore.

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**IAsyncReader:: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) per negoziare un allocatore. Passa il parametro *pAlloc* direttamente al metodo **RequestAllocator** . Passa il parametro *pProps* a **RequestAllocator** se *pProps* è diverso da **null**; in caso contrario, viene creata una struttura di **\_ proprietà dell'allocatore** con una richiesta predefinita di tre buffer 64K.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> <dt>

[**CPullPin:: Connect**](cpullpin-connect.md)
</dt> </dl>

 

 




