---
description: Il metodo ResetEndOfStream Reimposta i flag di fine del flusso.
ms.assetid: 80f6d49b-a825-4c3c-b693-7b1d9298f541
title: Metodo CBaseRenderer. ResetEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0269ee2dfafea9265b5eeb82caa4c39f8d91320c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333331"
---
# <a name="cbaserendererresetendofstream-method"></a>CBaseRenderer. ResetEndOfStream, metodo

Il `ResetEndOfStream` metodo reimposta i flag di fine del flusso.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT ResetEndOfStream();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo cancella la condizione di fine del flusso precedente. A questo punto, il filtro può ricevere nuovi dati. I metodi [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) e [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) chiamano questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




