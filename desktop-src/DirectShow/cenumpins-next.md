---
description: Il metodo Next recupera un numero specificato di pin nella sequenza di enumerazione. Questo metodo implementa il metodo IEnumPins::Next.
ms.assetid: c38fbd32-7d83-43ec-a105-4a7cb515b471
title: Metodo CEnumPins.Next (Amfilter.h)
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
ms.openlocfilehash: 683b8eb5beb9946db7f37d4db53a84c96d5bff7fc91fa4864020fffde5554824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567081"
---
# <a name="cenumpinsnext-method"></a>Metodo CEnumPins.Next

Il metodo Next recupera un numero specificato di pin nella sequenza di enumerazione. Questo metodo implementa il [**metodo IEnumPins::Next.**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next)

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

Matrice di *oggetti cPin di* dimensioni riempiti con [**puntatori IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

</dd> <dt>

*pcFetched* 
</dt> <dd>

Puntatore a una variabile che riceve il numero di pin recuperati. Può essere **NULL** se *cPins* è 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Non è stato recuperato il numero di pin richiesto.<br/>                                 |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Operazione completata.<br/>                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Argomento non valido.<br/>                                                           |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>                  | Argomento del puntatore **NULL.**<br/>                                                  |
| <dl> <dt>**ENUMERAZIONE VFW \_ \_ NON \_ \_ \_ SINCRONIZZATA**</dt> </dl> | Lo stato del filtro è stato modificato ed è ora incoerente con l'enumeratore.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo recupera i puntatori al numero specificato di pin, a partire dalla posizione corrente nell'enumerazione , e li inserisce nella matrice specificata.

Questo metodo chiama il metodo [**CBaseFilter::GetPin**](cbasefilter-getpin.md) del filtro per recuperare i pin.

Se il metodo ha esito positivo, tutti **i puntatori IPin** hanno conteggi dei riferimenti in sospeso. Assicurarsi di rilasciarli al termine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




