---
description: Il Metodo BeginFlush informa il filtro proprietario per scaricare i filtri downstream. La classe derivata deve implementare questo metodo.
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: Metodo CPullPin. BeginFlush (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2e4c26b99c78794449077e73040d98b5481fb91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328489"
---
# <a name="cpullpinbeginflush-method"></a>CPullPin. BeginFlush, metodo

Il `BeginFlush` metodo informa il filtro proprietario per scaricare i filtri downstream. La classe derivata deve implementare questo metodo.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Il metodo [**CPullPin:: Seek**](cpullpin-seek.md) chiama questo metodo. Implementare questo metodo per chiamare il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) su ogni pin di input downstream che riceve i dati da questo oggetto. Se i pin di output del filtro derivano da [**CBaseOutputPin**](cbaseoutputpin.md), chiamare il metodo [**CBaseOutputPin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .

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

 

 




