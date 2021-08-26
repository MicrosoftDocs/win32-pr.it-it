---
description: Il metodo SetAllocator specifica un allocatore per la connessione.
ms.assetid: 6b8e80f9-3b0d-498f-b1b0-bae491c25e81
title: Metodo CTransInPlaceOutputPin.SetAllocator (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.SetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 568a95df0d0cee39245c268fa1c49505531ddc84e1fd1542a1eae170e5c7d0da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053181"
---
# <a name="ctransinplaceoutputpinsetallocator-method"></a>Metodo CTransInPlaceOutputPin.SetAllocator

Il `SetAllocator` metodo specifica un allocatore per la connessione.

## <a name="syntax"></a>Sintassi


```C++
void SetAllocator(
   IMemAllocator *pAllocator
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAllocator* 
</dt> <dd>

Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il pin di output per questo filtro non fornisce mai un allocatore. Questo metodo specifica l'allocatore per il pin di output. Imposta il valore della variabile [**membro CBaseOutputPin::m \_ pAllocator.**](cbaseoutputpin-m-pallocator.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




