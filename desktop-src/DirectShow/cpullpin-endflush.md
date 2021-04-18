---
description: Il metodo EndFlush comunica al filtro proprietario di terminare un'operazione di svuotamento. La classe derivata deve implementare questo metodo.
ms.assetid: 5b178b09-019c-4b5b-9794-5176b5402e1c
title: Metodo CPullPin. EndFlush (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e58cb9a903f0841de2442216fab0e360007206b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331169"
---
# <a name="cpullpinendflush-method"></a>CPullPin. EndFlush, metodo

Il `EndFlush` Metodo comunica al filtro proprietario di terminare un'operazione di svuotamento. La classe derivata deve implementare questo metodo.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT EndFlush() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Il metodo [**CPullPin:: Seek**](cpullpin-seek.md) chiama questo metodo. Implementare questo metodo per chiamare il metodo [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) su ogni pin di input downstream che riceve i dati da questo oggetto. Se i pin di output del filtro derivano da **CBaseOutputPin**, chiamare il metodo **CBaseOutputPin::D eliverendflush** .

Questa progettazione consente al filtro di cercare il flusso semplicemente chiamando **Seek** sull'oggetto **CPullPin** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




