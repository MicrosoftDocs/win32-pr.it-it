---
description: Il metodo ChangeRate viene chiamato quando cambia la velocità di riproduzione.
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: Metodo CSourceSeeking.ChangeRate (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee74c8eb39fbebab1e58442c3b12f8342610ed792f4eb80ee70e5f44c3cca236
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633941"
---
# <a name="csourceseekingchangerate-method"></a>Metodo CSourceSeeking.ChangeRate

Il `ChangeRate` metodo viene chiamato quando cambia la velocità di riproduzione.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Il [**metodo CSourceSeeking::SetRate**](csourceseeking-setrate.md) chiama questo metodo, che deve essere implementato dalla classe derivata. Il **metodo SetRate** aggiorna la variabile membro [**CSourceSeeking::m \_ dRateSeeking,**](csourceseeking-m-drateseeking.md) ma non convalida il nuovo valore. Una frequenza pari a zero deve sempre essere rifiutata. Le percentuali minori di zero indicano una riproduzione negativa. La maggior parte dei filtri non supporta i tassi negativi.

L'esempio seguente illustra una possibile implementazione:


```C++
HRESULT CMyStream::ChangeRate( )
{
    {   // Scope for critical section lock.
        CAutoLock cAutoLockSeeking(CSourceSeeking::m_pLock);
        if( m_dRateSeeking <= 0 ) {
            m_dRateSeeking = 1.0;  // Reset to a reasonable value.
            return E_FAIL;
        }
    }
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




