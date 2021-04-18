---
description: Il metodo QueryId recupera un identificatore per il PIN.
ms.assetid: 6050292e-6203-4a79-87bf-47394624cb32
title: Metodo CSourceStream. QueryId (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 267748fe4ce1eeec4650544a2f72069df897a366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330662"
---
# <a name="csourcestreamqueryid-method"></a>CSourceStream. QueryId, metodo

Il `QueryId` metodo recupera un identificatore per il PIN.

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

Puntatore a una variabile che riceve una stringa che contiene l'identificatore del PIN.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                       | Descrizione                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Esito positivo.<br/>                         |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>     | Memoria insufficiente.<br/>             |
| <dl> <dt>**\_puntatore E**</dt> </dl>         | Argomento puntatore **null** .<br/>       |
| <dl> <dt>**VFW \_ E \_ non \_ trovato**</dt> </dl> | Il PIN non è stato trovato nel filtro.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo implementa il metodo [**Ipin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) . Per costruire una stringa dell'identificatore, il pin chiama il metodo [**CSource:: FindPinNumber**](csource-findpinnumber.md) con se stesso come parametro. Il metodo **FindPinNumber** restituisce il numero del PIN, indicizzato da zero. `QueryId` incrementa il valore restituito di uno e converte il risultato in una stringa. Ad esempio, il primo pin diventa "1"; il secondo pin diventa "2"; e così via.

Se questo metodo restituisce VFW \_ E \_ non \_ trovato, significa che la matrice di pin del filtro non è valida, presumibilmente causata da un bug nel filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




