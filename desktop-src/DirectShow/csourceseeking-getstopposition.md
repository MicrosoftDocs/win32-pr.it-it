---
description: Il metodo GetStopPosition recupera l'ora di arresto della riproduzione, in relazione alla durata del flusso. Questo metodo implementa il metodo IMediaSeeking::GetStopPosition.
ms.assetid: 83928f62-7acc-43b9-9537-49131ed0b0d4
title: Metodo CSourceSeeking.GetStopPosition (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 870ddbf77d1a29a34703d4b43ee21d02b676e8fafac9ee688384246339465732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073325"
---
# <a name="csourceseekinggetstopposition-method"></a>Metodo CSourceSeeking.GetStopPosition

Il `GetStopPosition` metodo recupera l'ora di arresto della riproduzione, in relazione alla durata del flusso. Questo metodo implementa il [**metodo IMediaSeeking::GetStopPosition.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStop* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora di arresto, in unità del formato di ora corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Operazione riuscita<br/>                |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | **Valore del** puntatore NULL<br/> |



 

## <a name="remarks"></a>Commenti

L'ora di arresto viene specificata dalla [**variabile membro CSourceSeeking::m \_ rtStop.**](csourceseeking-m-rtstop.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




