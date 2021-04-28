---
description: 'Metodo CSourceSeeking.GetRate: il metodo GetRate recupera la velocità di riproduzione. Questo metodo implementa il metodo IMediaSeeking::GetRate.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: Metodo CSourceSeeking.GetRate (Ctlutil.h)
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
ms.openlocfilehash: fef379ef06cd0982f1eb5742ac2624d706ed73a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085229"
---
# <a name="csourceseekinggetrate-method"></a>Metodo CSourceSeeking.GetRate

Il `GetRate` metodo recupera la velocità di riproduzione. Questo metodo implementa il [**metodo IMediaSeeking::GetRate.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate)

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

Restituisce uno dei **valori HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Operazione riuscita<br/>                |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | **Valore del** puntatore NULL<br/> |



 

## <a name="remarks"></a>Commenti

La velocità di riproduzione viene specificata dalla [**variabile membro CSourceSeeking::m \_ dRateSeeking.**](csourceseeking-m-drateseeking.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




