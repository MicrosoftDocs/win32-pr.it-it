---
description: "Il metodo GetPreroll recupera l'ora di preroll. Questo metodo implementa il metodo IMediaSeeking:: GetPreroll."
ms.assetid: 2395d5b2-8c1f-40cd-8d4a-48620debe7a7
title: Metodo CSourceSeeking. GetPreroll (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 097af089a7221f005cf7f3aac74953166af3cb2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329504"
---
# <a name="csourceseekinggetpreroll-method"></a>CSourceSeeking. GetPreroll, metodo

Il `GetPreroll` metodo recupera l'ora di preregistrazione. Questo metodo implementa il metodo [**IMediaSeeking:: GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPreroll(
   LONGLONG *pPreroll
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPreroll* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora di preregistrazione. Il valore è impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Operazione riuscita<br/>                |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Valore del puntatore **null**<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




