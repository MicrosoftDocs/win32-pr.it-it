---
description: 'Il metodo sepositions imposta la posizione corrente e la posizione di arresto. Questo metodo implementa il metodo IMediaSeeking:: sepositions.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: Metodo CSourceSeeking. sepositions (Ctlutil. h)
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
ms.openlocfilehash: 342ca7d85fe9358b914709b7887216b62e03521d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328486"
---
# <a name="csourceseekingsetpositions-method"></a>Metodo CSourceSeeking. sepositions

Il `SetPositions` metodo imposta la posizione corrente e la posizione di arresto. Questo metodo implementa il metodo [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

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

Puntatore a una variabile che specifica l'ora di arresto, in unità del formato dell'ora corrente.

</dd> <dt>

*StopFlags* 
</dt> <dd>

Combinazione bit per bit di flag. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Operazione riuscita<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Flag non validi<br/>             |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Argomento puntatore **null**<br/> |



 

## <a name="remarks"></a>Commenti

Sono supportati i flag seguenti:

-   \_Ricerca di \_ nopositioning
-   \_Ricerca di \_ AbsolutePositioning
-   \_Ricerca di \_ RelativePositioning
-   \_Cerco \_ IncrementalPositioning (solo *pStop* )

Per altre informazioni, vedere [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

Questo metodo aggiorna i valori delle variabili [**membro CSourceSeeking:: m \_ RtStart**](csourceseeking-m-rtstart.md) e [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) , quindi chiama i metodi virtuali puri [**CSourceSeeking:: iniziale**](csourceseeking-changestart.md) e [**CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




