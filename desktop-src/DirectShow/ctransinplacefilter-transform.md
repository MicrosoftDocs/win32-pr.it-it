---
description: Il metodo Transform trasforma un esempio sul posto.
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: Metodo CTransInPlaceFilter.Transform (Transip.h)
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
ms.openlocfilehash: 224052bc882792f57eedf9ea58842b953e5853012d3581ef14cad58467b614b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953400"
---
# <a name="ctransinplacefiltertransform-method"></a>Metodo CTransInPlaceFilter.Transform

Il `Transform` metodo trasforma un esempio sul posto.

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

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Non recapitare questo esempio.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>                    |



 

## <a name="remarks"></a>Commenti

La classe derivata deve implementare questo metodo. Trasformare i dati di esempio sul posto. Se il filtro usa due allocatori, copia i dati dall'esempio di input in un nuovo esempio e passa la copia a questo metodo.

Se il filtro non deve recapitare questo esempio (ad esempio, per supportare il controllo di qualità), il metodo deve restituire S \_ FALSE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




