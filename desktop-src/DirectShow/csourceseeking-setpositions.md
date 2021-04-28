---
description: 'Metodo CSourceSeeking.SetPositions: il metodo SetPositions imposta la posizione corrente e la posizione di arresto. Questo metodo implementa il metodo IMediaSeeking::SetPositions.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: Metodo CSourceSeeking.SetPositions (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b09dd92b97166b8d973328ec95e466abbda116bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085169"
---
# <a name="csourceseekingsetpositions-method"></a>Metodo CSourceSeeking.SetPositions

Il `SetPositions` metodo imposta la posizione corrente e la posizione di arresto. Questo metodo implementa il [**metodo IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCurrent* 
</dt> <dd>

Puntatore a una variabile che specifica la posizione corrente.

</dd> <dt>

*CurrentFlags* 
</dt> <dd>

Combinazione bit per bit di flag. Vedere la sezione Osservazioni.

</dd> <dt>

*pStop* 
</dt> <dd>

Puntatore a una variabile che specifica l'ora di arresto, in unità del formato di ora corrente.

</dd> <dt>

*StopFlags* 
</dt> <dd>

Combinazione bit per bit di flag. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione riuscita<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Flag non validi<br/>             |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>    | **Argomento puntatore NULL**<br/> |



 

## <a name="remarks"></a>Commenti

Sono supportati i flag seguenti:

-   AM \_ SEEKING \_ NoPositioning
-   AM \_ SEEKING \_ AbsolutePositioning
-   AM \_ SEEKING \_ RelativePositioning
-   AM \_ SEEKING \_ IncrementalPositioning *(solo pStop)*

Per altre informazioni, vedere [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

Questo metodo aggiorna i valori delle variabili membro [**CSourceSeeking::m \_ rtStart**](csourceseeking-m-rtstart.md) e [**CSourceSeeking::m \_ rtStop**](csourceseeking-m-rtstop.md) e quindi chiama i metodi virtuali puri [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) e [**CSourceSeeking::ChangeSeeking::ChangeStop**](csourceseeking-changestop.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




