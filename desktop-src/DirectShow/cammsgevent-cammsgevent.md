---
description: Metodo del costruttore.
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: Costruttore CAMMsgEvent. CAMMsgEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0d207afae53a715728d8307656b0c2427ce9574c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332708"
---
# <a name="cammsgeventcammsgevent-constructor"></a>Costruttore CAMMsgEvent. CAMMsgEvent

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PHR* 
</dt> <dd>

Puntatore a un valore **HRESULT** . Se il costruttore ha esito negativo, questo parametro riceve un codice di errore. In tal caso, lo stato dell'oggetto non è valido.

Per la compatibilità con le versioni precedenti di strmbase. lib, il valore predefinito di questo parametro è **null**. Tuttavia, è preferibile passare un valore non **null** , in modo che il chiamante possa controllare lo stato dell'oggetto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMMsgEvent**](cammsgevent.md)
</dt> </dl>

 

 




