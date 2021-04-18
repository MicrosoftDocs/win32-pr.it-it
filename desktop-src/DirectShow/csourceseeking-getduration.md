---
description: 'Il metodo GetDuration recupera la durata del flusso. Questo metodo implementa il metodo IMediaSeeking:: GetDuration.'
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: Metodo CSourceSeeking. GetDuration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8368f655394089c1155d848bc53d2ba2375e3320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329512"
---
# <a name="csourceseekinggetduration-method"></a>CSourceSeeking. GetDuration, metodo

Il `GetDuration` metodo recupera la durata del flusso. Questo metodo implementa il metodo [**IMediaSeeking:: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDuration* 
</dt> <dd>

Puntatore a una variabile che riceve la durata, in unità del formato dell'ora corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Operazione riuscita<br/>                |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Valore del puntatore **null**<br/> |



 

## <a name="remarks"></a>Commenti

La durata è specificata dalla variabile membro [**CSourceSeeking:: m \_ rtDuration**](csourceseeking-m-rtduration.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




