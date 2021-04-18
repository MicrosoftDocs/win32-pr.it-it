---
description: Il metodo ChangeStop viene chiamato quando viene modificata la posizione di arresto.
ms.assetid: 3d4a73a4-68e6-449c-9637-62cad937c4b4
title: Metodo CSourceSeeking. ChangeStop (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eefcc64b4692363c8caa8f39a3a0db9beb0d08b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327531"
---
# <a name="csourceseekingchangestop-method"></a>CSourceSeeking. ChangeStop, metodo

Il `ChangeStop` metodo viene chiamato quando viene modificata la posizione di arresto.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT ChangeStop() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Il metodo [**CSourceSeeking:: Sepositions**](csourceseeking-setpositions.md) chiama questo metodo se la posizione di arresto cambia. Questo metodo è virtuale puro; la classe derivata deve implementarla. Nell'esempio seguente viene illustrata una possibile implementazione:


```C++
HRESULT CMyStream::ChangeStop( )
{
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




