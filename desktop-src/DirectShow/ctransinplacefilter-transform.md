---
description: Il metodo Transform trasforma un campione sul posto.
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: Metodo CTransInPlaceFilter. Transform (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5b84f326807f730745268a217b6066dacb9aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333795"
---
# <a name="ctransinplacefiltertransform-method"></a>Metodo CTransInPlaceFilter. Transform

Il `Transform` metodo trasforma un campione sul posto.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Transform(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Non recapitare questo esempio.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                    |



 

## <a name="remarks"></a>Commenti

La classe derivata deve implementare questo metodo. Trasformare i dati di esempio sul posto. Se il filtro usa due allocatori, copia i dati dall'esempio di input in un nuovo esempio e passa la copia a questo metodo.

Se il filtro non deve fornire questo esempio (ad esempio per supportare il controllo di qualità), il metodo deve restituire S \_ false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




