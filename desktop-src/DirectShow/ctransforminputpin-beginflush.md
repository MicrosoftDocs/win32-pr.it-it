---
description: "Il Metodo BeginFlush avvia un'operazione di svuotamento. Questo metodo implementa il metodo IPin:: BeginFlush."
ms.assetid: 7c76ca06-dc3c-4f9a-9761-32aea7db4c7e
title: Metodo CTransformInputPin. BeginFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4d028634364ca59ae293d9ebb60a464974ccd74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328479"
---
# <a name="ctransforminputpinbeginflush-method"></a>CTransformInputPin. BeginFlush, metodo

Il `BeginFlush` metodo inizia un'operazione di svuotamento. Questo metodo implementa il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Esito positivo.<br/>                     |
| <dl> <dt>**VFW \_ E \_ non \_ connesso**</dt> </dl> | Il pin di output non è connesso.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**CBaseInputPin:: BeginFlush**](cbaseinputpin-beginflush.md) del PIN. Chiama quindi il metodo [**CTransformFilter:: BeginFlush**](ctransformfilter-beginflush.md) del filtro per recapitare la chiamata downstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




