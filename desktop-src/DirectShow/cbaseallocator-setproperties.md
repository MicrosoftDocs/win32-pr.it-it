---
description: Il metodo SetProperties specifica il numero di buffer da allocare e le dimensioni di ogni buffer. Questo metodo implementa il metodo IMemAllocator::SetProperties.
ms.assetid: f53c22a4-c01d-4d2f-81f0-bedf8f2ae5f0
title: Metodo CBaseAllocator.SetProperties (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d81ee1c29f1c9e2cc9927f926144a7427b5e94f72406f94ce65f7d4a20e2ab32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057481"
---
# <a name="cbaseallocatorsetproperties-method"></a>Metodo CBaseAllocator.SetProperties

Il `SetProperties` metodo specifica il numero di buffer da allocare e le dimensioni di ogni buffer. Questo metodo implementa il [**metodo IMemAllocator::SetProperties.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRequest* 
</dt> <dd>

Puntatore a una [**struttura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che contiene i requisiti del buffer.

</dd> <dt>

*pActual* 
</dt> <dd>

Puntatore a **una struttura ALLOCATOR \_ PROPERTIES** che riceve le proprietà effettive del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti.



| Codice restituito                                                                                                 | Descrizione                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                        | Operazione completata.<br/>                                                   |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>                   | Argomento del puntatore **NULL.**<br/>                                 |
| <dl> <dt>**VFW \_ E \_ ALREADY \_ COMMITTED**</dt> </dl>   | Impossibile modificare la memoria allocata mentre il filtro è attivo.<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | È stato specificato un allineamento non valido.<br/>                        |
| <dl> <dt>**BUFFER E VFW \_ \_ IN \_ SOSPESO**</dt> </dl> | Uno o più buffer sono ancora attivi.<br/>                      |



 

## <a name="remarks"></a>Commenti

Questo metodo specifica i requisiti del buffer, ma non alloca alcun buffer. Chiamare il [**metodo CBaseAllocator::Commit**](cbaseallocator-commit.md) per allocare buffer.

Il chiamante alloca due strutture \_ ALLOCATOR PROPERTIES. Il *parametro pRequest* contiene i requisiti del buffer del chiamante, inclusi il numero di buffer e le dimensioni di ogni buffer. Quando il metodo viene restituito, *il parametro pActual* contiene le proprietà effettive del buffer, come impostato dall'allocatore. Nella classe di base, supponendo che il metodo abbia esito positivo, le proprietà effettive corrispondono sempre alle proprietà richieste. Le classi derivate potrebbero eseguire l'override di questo comportamento.

Non è necessario eseguire il commit dell'allocatore e non devono essere in attesa di buffer. Nella classe di base l'allineamento deve essere uguale a 1. La [**classe CMemAllocator**](cmemallocator.md) esegue l'override di questo requisito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




