---
description: Il metodo CheckInputType controlla se un tipo di supporto specificato è accettabile per l'input.
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: Metodo CTransformFilter. CheckInputType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckInputType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63c48a0502ee074b0940f85386dca0619a3ad12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325731"
---
# <a name="ctransformfiltercheckinputtype-method"></a>CTransformFilter. CheckInputType, metodo

Il `CheckInputType` metodo controlla se un tipo di supporto specificato è accettabile per l'input.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CheckInputType(
   const CMediaType *mtIn
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mtIn* 
</dt> <dd>

Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Il tipo di supporto è accettabile.<br/>     |
| <dl> <dt>**\_tipo VFW \_ E \_ non \_ accettato**</dt> </dl> | Il tipo di supporto non è accettabile.<br/> |



 

## <a name="remarks"></a>Commenti

La classe derivata deve implementare questo metodo. Restituisce \_ OK se il formato di input proposto è accettabile o in caso contrario un codice di errore.

Questo metodo non deve verificare che il formato di input sia compatibile con il formato di output (se presente). Il pin di input verifica che chiamando il metodo [**CheckTransform**](ctransformfilter-checktransform.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




