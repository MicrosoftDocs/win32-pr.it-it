---
description: Il Metodo BeginFlush avvia un'operazione di svuotamento.
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: Metodo CBaseRenderer. BeginFlush (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e218e3b2d9c0cef8ce0fe052ad1b3c4b6f786858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329406"
---
# <a name="cbaserendererbeginflush-method"></a>CBaseRenderer. BeginFlush, metodo

Il `BeginFlush` metodo inizia un'operazione di svuotamento.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Il pin di input del filtro chiama questo metodo quando riceve una chiamata al metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) . Il filtro rilascia il thread di streaming e rilascia qualsiasi campione che era in attesa di rendering.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




