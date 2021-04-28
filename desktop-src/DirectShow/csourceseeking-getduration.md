---
description: 'Metodo CSourceSeeking.GetDuration: il metodo GetDuration recupera la durata del flusso. Questo metodo implementa il metodo IMediaSeeking::GetDuration.'
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: Metodo CSourceSeeking.GetDuration (Ctlutil.h)
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
ms.openlocfilehash: 3d5b961ad62d65c1f728af71e82de1373ea20b1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098769"
---
# <a name="csourceseekinggetduration-method"></a>Metodo CSourceSeeking.GetDuration

Il `GetDuration` metodo recupera la durata del flusso. Questo metodo implementa il [**metodo IMediaSeeking::GetDuration.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration)

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

Puntatore a una variabile che riceve la durata, in unità del formato di ora corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Operazione riuscita<br/>                |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | **Valore del** puntatore NULL<br/> |



 

## <a name="remarks"></a>Commenti

La durata viene specificata dalla [**variabile membro CSourceSeeking::m \_ rtDuration.**](csourceseeking-m-rtduration.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




