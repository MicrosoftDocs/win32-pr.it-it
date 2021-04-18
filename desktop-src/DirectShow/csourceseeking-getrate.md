---
description: 'Il metodo getrate recupera la velocità di riproduzione. Questo metodo implementa il metodo IMediaSeeking:: getrate.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: Metodo CSourceSeeking. getrate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b14cad0b043193f7ee410455aaa399e3bcb26715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329503"
---
# <a name="csourceseekinggetrate-method"></a>CSourceSeeking. getrate, metodo

Il `GetRate` metodo recupera la velocità di riproduzione. Questo metodo implementa il metodo [**IMediaSeeking:: getrate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdRate* 
</dt> <dd>

Puntatore a una variabile che riceve la velocità di riproduzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Operazione riuscita<br/>                |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Valore del puntatore **null**<br/> |



 

## <a name="remarks"></a>Commenti

La velocità di riproduzione è specificata dalla variabile membro [**CSourceSeeking:: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




