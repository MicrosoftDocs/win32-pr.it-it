---
description: 'Il metodo successivo recupera un numero specificato di pin nella sequenza di enumerazione. Questo metodo implementa il metodo IEnumPins:: Next.'
ms.assetid: c38fbd32-7d83-43ec-a105-4a7cb515b471
title: Metodo CEnumPins. Next (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 612dcd638939b34803b7296babf7445a07cdad22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329837"
---
# <a name="cenumpinsnext-method"></a>Metodo CEnumPins. Next

Il metodo successivo recupera un numero specificato di pin nella sequenza di enumerazione. Questo metodo implementa il metodo [**IEnumPins:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Next(
   ULONG cPins,
   IPin  **ppPins,
   ULONG *pcFetched
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cPins* 
</dt> <dd>

Numero di pin da recuperare.

</dd> <dt>

*ppPins* 
</dt> <dd>

Matrice di dimensioni *cPins* riempite con puntatori [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

</dd> <dt>

*pcFetched* 
</dt> <dd>

Puntatore a una variabile che riceve il numero di pin recuperati. Può essere **null** se *cPins* è 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                    | Non è stato possibile recuperare tutti i pin richiesti.<br/>                                 |
| <dl> <dt>**\_OK**</dt> </dl>                       | Esito positivo.<br/>                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Argomento non valido.<br/>                                                           |
| <dl> <dt>**\_puntatore E**</dt> </dl>                  | Argomento puntatore **null** .<br/>                                                  |
| <dl> <dt>**non \_ \_ \_ \_ sincronizzato con VFW E enum \_**</dt> </dl> | Lo stato del filtro è stato modificato ed è ora incoerente con l'enumeratore.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo recupera i puntatori al numero di PIN specificato, a partire dalla posizione corrente nell'enumerazione e li inserisce nella matrice specificata.

Questo metodo chiama il metodo [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) del filtro per recuperare i pin.

Se il metodo ha esito positivo, i puntatori **Ipin** hanno tutti i conteggi dei riferimenti in attesa. Assicurarsi di rilasciarli al termine dell'operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




