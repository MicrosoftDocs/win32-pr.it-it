---
description: Il metodo QueryId recupera un identificatore per il pin.
ms.assetid: 6050292e-6203-4a79-87bf-47394624cb32
title: Metodo CSourceStream.QueryId (Source.h)
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
ms.openlocfilehash: 1bd8582d16022c9d5dfd60eb87847d564ef69203e329ff37eaa9c2964a11794c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317511"
---
# <a name="csourcestreamqueryid-method"></a>Metodo CSourceStream.QueryId

Il `QueryId` metodo recupera un identificatore per il pin.

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

Puntatore a una variabile che riceve una stringa contenente l'identificatore pin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                       | Descrizione                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Operazione completata.<br/>                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>     | Memoria insufficiente.<br/>             |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>         | Argomento del puntatore **NULL.**<br/>       |
| <dl> <dt>**VFW \_ E \_ NON \_ TROVATO**</dt> </dl> | Il pin non è stato trovato nel filtro.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo implementa il [**metodo IPin::QueryId.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) Per costruire una stringa identificatore, il pin chiama il metodo [**CSource::FindPinNumber**](csource-findpinnumber.md) con se stesso come parametro. Il **metodo FindPinNumber** restituisce il numero pin, indicizzato da zero. `QueryId` incrementa di uno il valore restituito e converte il risultato in una stringa. Ad esempio, il primo pin diventa "1"; il secondo pin diventa "2"; e così via.

Se questo metodo restituisce VFW E NOT FOUND, indica che la matrice di pin del filtro non è valida, presumibilmente causata da un \_ \_ bug nel \_ filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (include Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




