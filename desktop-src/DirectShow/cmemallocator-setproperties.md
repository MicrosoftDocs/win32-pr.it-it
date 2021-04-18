---
description: Il metodo seproperties specifica il numero di buffer da allocare e le dimensioni di ogni buffer.
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: Metodo CMemAllocator. seproperties (Amfilter. h)
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
ms.openlocfilehash: 8505916245cca81fdd84132e4523fe9dd03b971b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328845"
---
# <a name="cmemallocatorsetproperties-method"></a>Metodo CMemAllocator. seproperties

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

Puntatore a una struttura di [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che contiene i requisiti del buffer.

</dd> <dt>

*pActual* 
</dt> <dd>

Puntatore a una struttura di **\_ proprietà dell'allocatore** che riceve le proprietà effettive del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                                 | Descrizione                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                        | Esito positivo.<br/>                                                   |
| <dl> <dt>**\_puntatore E**</dt> </dl>                   | Argomento puntatore **null** .<br/>                                 |
| <dl> <dt>**è \_ \_ già stato \_ eseguito il commit di VFW**</dt> </dl>   | Non è possibile modificare la memoria allocata mentre il filtro è attivo.<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | È stato specificato un allineamento non valido.<br/>                        |
| <dl> <dt>**\_buffer VFW E in \_ \_ attesa**</dt> </dl> | Uno o più buffer sono ancora attivi.<br/>                      |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBaseAllocator::**](cbaseallocator-setproperties.md) SetValue.

L'allineamento del buffer, specificato dal membro **cbAlign** della struttura **delle \_ proprietà dell'allocatore** , deve essere una potenza pari di due.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




