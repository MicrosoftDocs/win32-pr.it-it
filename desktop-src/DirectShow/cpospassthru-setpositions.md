---
description: 'Metodo CPosPassThru.SetPositions: il metodo SetPositions imposta la posizione corrente e la posizione di arresto. Questo metodo implementa il metodo IMediaSeeking::SetPositions.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: Metodo CPosPassThru.SetPositions (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8c61f24ab51ffe7fa161830ef9a0c8bdd167256
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085479"
---
# <a name="cpospassthrusetpositions-method"></a>Metodo CPosPassThru.SetPositions

Il `SetPositions` metodo imposta la posizione corrente e la posizione di arresto. Questo metodo implementa il [**metodo IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCurrent* 
</dt> <dd>

Puntatore a una variabile che specifica la posizione corrente, in unità del formato di ora corrente.

</dd> <dt>

*dwCurrentFlags* 
</dt> <dd>

Combinazione bit per bit di flag. Per [**altre informazioni, vedere IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)

</dd> <dt>

*pStop* 
</dt> <dd>

Puntatore a una variabile che specifica l'ora di arresto, in unità del formato di ora corrente.

</dd> <dt>

*dwStopFlags* 
</dt> <dd>

Combinazione bit per bit di flag. Per [**altre informazioni, vedere IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il **valore HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




