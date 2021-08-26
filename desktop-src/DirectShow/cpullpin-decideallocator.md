---
description: Il metodo DecideAllocator negozia un allocatore con il pin di output.
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: Metodo CPullPin.DecideAllocator (Pullpin.h)
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
ms.openlocfilehash: e02fe78631c6ddee01b7acc96d761f71b80e8d3e1738d2ed6f6ae40d70b0c5d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055061"
---
# <a name="cpullpindecideallocator-method"></a>Metodo CPullPin.DecideAllocator

Il `DecideAllocator` metodo negozia un allocatore con il pin di output.

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

Puntatore [**all'interfaccia IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore preferito del pin di input o **NULL.**

</dd> <dt>

*pProps* 
</dt> <dd>

Puntatore a una struttura [**ALLOCATOR \_ PROPERTIES facoltativa**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che contiene i requisiti del buffer del pin di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo oppure un codice di errore in caso contrario.

## <a name="remarks"></a>Commenti

Questo metodo chiama il [**metodo IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) per negoziare un allocatore. Passa il *parametro pAlloc* direttamente al **metodo RequestAllocator.** Passa il *parametro pProps* a **RequestAllocator** se *pProps* è diverso da **NULL;** In caso contrario, crea **una struttura ALLOCATOR \_ PROPERTIES** con una richiesta predefinita di tre buffer da 64 KB.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> <dt>

[**CPullPin::Connessione**](cpullpin-connect.md)
</dt> </dl>

 

 




