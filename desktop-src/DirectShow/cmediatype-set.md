---
description: Il metodo CMediaType. set (mtype. h) imposta il tipo di supporto da un altro tipo di supporto. Il metodo usa il parametro ' cmtype '.
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: Metodo CMediaType. set (mtype. h)-cmtype [Ref] parametro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9bf14132660045afbd171173a38d3ea320ba1aa
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323815"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a>Metodo CMediaType. set (mtype. h)-cmtype [Ref] parametro

Il `Set` metodo imposta il tipo di supporto da un altro tipo di supporto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Set(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cmtype* \[ Ref\]
</dt> <dd>

Riferimento a un oggetto [**CMediaType**](cmediatype.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o e \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questo metodo copia l'intero tipo di supporto da *cmtype*.

## <a name="requirements"></a>Requisiti

| Requisito                   | Valore                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione  | Mtype. h (include Streams. h)                                                                                     |
| Libreria | Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




