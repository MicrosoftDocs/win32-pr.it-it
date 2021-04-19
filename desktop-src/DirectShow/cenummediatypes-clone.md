---
description: "Il metodo Clone crea una copia dell'enumeratore con lo stesso stato di enumerazione. Questo metodo implementa il metodo IEnumMediaTypes:: clone."
ms.assetid: 3b4eb29e-48fc-4f00-a5f3-597b9aa94ce1
title: Metodo CEnumMediaTypes. Clone (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43f051bf90afa231d3b677045468f26d06d55150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329853"
---
# <a name="cenummediatypesclone-method"></a>Metodo CEnumMediaTypes. Clone

Il `Clone` metodo crea una copia dell'enumeratore con lo stesso stato di enumerazione. Questo metodo implementa il metodo [**IEnumMediaTypes:: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clone(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnum* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) del nuovo enumeratore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Esito positivo.<br/>                                                                 |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>              | Memoria insufficiente.<br/>                                                     |
| <dl> <dt>**\_puntatore E**</dt> </dl>                  | Argomento puntatore **null** .<br/>                                               |
| <dl> <dt>**non \_ \_ \_ \_ sincronizzato con VFW E enum \_**</dt> </dl> | Lo stato del PIN è stato modificato ed è ora incoerente con l'enumeratore.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CEnumMediaTypes**](cenummediatypes.md)
</dt> </dl>

 

 




