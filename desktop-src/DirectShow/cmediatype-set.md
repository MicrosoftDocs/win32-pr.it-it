---
description: Il metodo CMediaType.Set (Mtype.h) imposta il tipo di supporto da un altro tipo di supporto. Il metodo usa il parametro 'cmtype'.
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: Metodo CMediaType.Set (Mtype.h) - parametro cmtype [ref]
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
ms.openlocfilehash: 0a317b23b4870ad6e68032ed23f846a81019be358974ebbe75e2a5859db71303
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585881"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a>Metodo CMediaType.Set (Mtype.h) - parametro cmtype [ref]

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

Riferimento a un [**oggetto CMediaType.**](cmediatype.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questo metodo copia l'intero tipo di supporto da *cmtype*.

## <a name="requirements"></a>Requisiti

| Requisito                   | Valore                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione  | Mtype.h (includere Flussi.h)                                                                                     |
| Libreria | Strmbase.lib (build di vendita al dettaglio); Strmbasd.lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




