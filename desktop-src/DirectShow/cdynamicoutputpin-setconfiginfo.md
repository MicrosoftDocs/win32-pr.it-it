---
description: Il metodo SetConfigInfo specifica il puntatore IGraphConfig e l'evento Stop.
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: Metodo CDynamicOutputPin. SetConfigInfo (Amfilter. h)
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
ms.openlocfilehash: b0c14342a629a38a878649ac59d8f1f814874f12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327543"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a>CDynamicOutputPin. SetConfigInfo, metodo

Il `SetConfigInfo` metodo specifica il puntatore [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) e l'evento Stop.

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

Puntatore all'interfaccia [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) o **null**.

</dd> <dt>

*hStopEvent* 
</dt> <dd>

Handle per un evento segnalato quando il filtro viene arrestato o **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il filtro deve chiamare questo metodo quando viene aggiunto al grafo del filtro. Filter Graph Manager supporta **IGraphConfig**. Per il parametro *hStopEvent* , creare un evento di reimpostazione manuale. Quando il filtro lascia il grafico del filtro, chiamare nuovamente questo metodo con **null** per entrambi i parametri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




