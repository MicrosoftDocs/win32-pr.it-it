---
description: "Il metodo QueryId recupera l'identificatore del PIN. Questo metodo implementa il metodo IPin:: QueryId."
ms.assetid: b365a574-61b4-454c-b062-8826cbe10f03
title: Metodo CBasePin. QueryId (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa14fb933c89da0b0b6d2eebfab480b5508a3666
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328262"
---
# <a name="cbasepinqueryid-method"></a>CBasePin. QueryId, metodo

Il `QueryId` metodo recupera l'identificatore del PIN. Questo metodo implementa il metodo [**Ipin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Id* 
</dt> <dd>

Puntatore all'identificatore del PIN.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Esito positivo.<br/>                   |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>       |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Argomento puntatore **null** .<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo restituisce una copia della variabile membro [**CBasePin:: m \_ pname**](cbasepin-m-pname.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




