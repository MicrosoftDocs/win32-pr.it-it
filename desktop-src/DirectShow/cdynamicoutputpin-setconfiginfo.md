---
description: Il metodo SetConfigInfo specifica il puntatore IGraphConfig e l'evento di arresto.
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: Metodo CDynamicOutputPin.SetConfigInfo (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SetConfigInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23b492eaf4b5f712a51132eefcceac12a772b17b8285d8c6edb1a6cec268b1c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074235"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a>Metodo CDynamicOutputPin.SetConfigInfo

Il `SetConfigInfo` metodo specifica il puntatore [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) e l'evento di arresto.

## <a name="syntax"></a>Sintassi


```C++
void SetConfigInfo(
   IGraphConfig *pGraphConfig,
   HANDLE       hStopEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGraphConfig* 
</dt> <dd>

Puntatore [**all'interfaccia IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) o **NULL.**

</dd> <dt>

*hStopEvent* 
</dt> <dd>

Handle a un evento segnalato all'arresto del filtro oppure **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il filtro deve chiamare questo metodo quando si unisce al grafico dei filtri. Il gestore del grafo del filtro supporta **IGraphConfig.** Per il *parametro hStopEvent* creare un evento di reimpostazione manuale. Quando il filtro esce dal grafico dei filtri, chiamare di nuovo questo metodo con **NULL** per entrambi i parametri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




