---
description: "Il metodo Clone crea una copia dell'enumeratore con lo stesso stato di enumerazione. Questo metodo implementa il metodo IEnumPins:: clone."
ms.assetid: 6e44c970-b90a-4bdb-8c60-dd8f31516249
title: Metodo CEnumPins. Clone (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2aa3e4604b260779a5d203e75e8e0790a7378b11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329838"
---
# <a name="cenumpinsclone-method"></a>Metodo CEnumPins. Clone

Il `Clone` metodo crea una copia dell'enumeratore con lo stesso stato di enumerazione. Questo metodo implementa il metodo [**IEnumPins:: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clone(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnum* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) del nuovo enumeratore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Esito positivo.<br/>                                                                    |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>              | Memoria insufficiente.<br/>                                                        |
| <dl> <dt>**\_puntatore E**</dt> </dl>                  | Argomento puntatore **null** .<br/>                                                  |
| <dl> <dt>**non \_ \_ \_ \_ sincronizzato con VFW E enum \_**</dt> </dl> | Lo stato del filtro è stato modificato ed è ora incoerente con l'enumeratore.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




