---
description: Il metodo SetProperties specifica il numero di buffer da allocare e le dimensioni di ogni buffer.
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: Metodo CMemAllocator.SetProperties (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5c5a145e630101bda4d060058cde7bfd91796386f0915e9e5329f63ced43ef19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821966"
---
# <a name="cmemallocatorsetproperties-method"></a>Metodo CMemAllocator.SetProperties

Il `SetProperties` metodo specifica il numero di buffer da allocare e le dimensioni di ogni buffer.

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

Puntatore a una **struttura ALLOCATOR \_ PROPERTIES** che riceve le proprietà del buffer effettive.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                                 | Descrizione                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                        | Operazione completata.<br/>                                                   |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>                   | Argomento del puntatore **NULL.**<br/>                                 |
| <dl> <dt>**VFW \_ E GIÀ DI CUI È GIÀ STATO ESEGUITO IL \_ \_ COMMIT**</dt> </dl>   | Impossibile modificare la memoria allocata mentre il filtro è attivo.<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | È stato specificato un allineamento non valido.<br/>                        |
| <dl> <dt>**BUFFER \_ VFW E \_ IN \_ SOSPESO**</dt> </dl> | Uno o più buffer sono ancora attivi.<br/>                      |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBaseAllocator::SetProperties.**](cbaseallocator-setproperties.md)

L'allineamento del buffer, specificato dal membro **cbAlign** della struttura **ALLOCATOR \_ PROPERTIES,** deve essere una potenza pari a due.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




