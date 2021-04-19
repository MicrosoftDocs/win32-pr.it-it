---
description: Il metodo pause sospende il filtro.
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: Metodo CBaseRenderer. pause (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e0b422882c07808f560f5256f67d01054d097726
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333344"
---
# <a name="cbaserendererpause-method"></a>CBaseRenderer. pause (metodo)

Il `Pause` metodo sospende il filtro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                             | Descrizione                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | La transizione è stata completata.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl> | La transizione non è completa.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBaseFilter::P ause**](cbasefilter-pause.md) . Esegue i passaggi seguenti:

-   Chiama il metodo **CBaseFilter::P ause** .
-   Viene eseguito il commit dell'allocatore. Vedere [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).
-   Se lo stato precedente è stato interrotto, il filtro rilascia tutti i campioni che contiene. (L'esempio non è più valido).
-   Chiama il metodo [**CBaseRenderer:: CompleteStateChange**](cbaserenderer-completestatechange.md) e restituisce il valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




