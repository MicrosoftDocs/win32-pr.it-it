---
description: Il metodo BeginFlush indica al filtro proprietario di scaricare i filtri downstream. La classe derivata deve implementare questo metodo.
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: Metodo CPullPin.BeginFlush (Pullpin.h)
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
ms.openlocfilehash: d2c7998c1c38a533d67edcd2cc237188a627ec8258a8b0349066e31ecf0fbaf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687751"
---
# <a name="cpullpinbeginflush-method"></a>Metodo CPullPin.BeginFlush

Il `BeginFlush` metodo indica al filtro proprietario di scaricare i filtri downstream. La classe derivata deve implementare questo metodo.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Il [**metodo CPullPin::Seek**](cpullpin-seek.md) chiama questo metodo. Implementare questo metodo per chiamare il [**metodo IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) su ogni pin di input downstream che riceve dati da questo oggetto. Se i pin di output del filtro derivano da [**CBaseOutputPin,**](cbaseoutputpin.md)chiamare il metodo [**CBaseOutputPin::D eliverBeginFlush.**](cbaseoutputpin-deliverbeginflush.md)

Questa progettazione consente al filtro di cercare il flusso semplicemente chiamando **Seek sull'oggetto** **CPullPin.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




