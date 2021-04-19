---
description: 'Il metodo sepositions imposta la posizione corrente e la posizione di arresto. Questo metodo implementa il metodo IMediaSeeking:: sepositions.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: Metodo CPosPassThru. sepositions (Ctlutil. h)
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
ms.openlocfilehash: 409b4a63f02e6751f987a53dad2836adecd27607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333194"
---
# <a name="cpospassthrusetpositions-method"></a>Metodo CPosPassThru. sepositions

Il `SetPositions` metodo imposta la posizione corrente e la posizione di arresto. Questo metodo implementa il metodo [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

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

Puntatore a una variabile che specifica la posizione corrente, in unità del formato dell'ora corrente.

</dd> <dt>

*dwCurrentFlags* 
</dt> <dd>

Combinazione bit per bit di flag. Per ulteriori informazioni, vedere [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

</dd> <dt>

*pStop* 
</dt> <dd>

Puntatore a una variabile che specifica l'ora di arresto, in unità del formato dell'ora corrente.

</dd> <dt>

*dwStopFlags* 
</dt> <dd>

Combinazione bit per bit di flag. Per ulteriori informazioni, vedere [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore **HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




