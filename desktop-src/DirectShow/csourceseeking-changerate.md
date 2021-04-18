---
description: Il metodo ChangeRate viene chiamato quando cambia la velocità di riproduzione.
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: Metodo CSourceSeeking. ChangeRate (Ctlutil. h)
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
ms.openlocfilehash: 02fab05d65929233b97f7d53e497bae6593c472a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325925"
---
# <a name="csourceseekingchangerate-method"></a>CSourceSeeking. ChangeRate (metodo)

Il `ChangeRate` metodo viene chiamato quando viene modificata la velocità di riproduzione.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Il metodo [**CSourceSeeking::**](csourceseeking-setrate.md) SetValue chiama questo metodo, che deve essere implementato dalla classe derivata. Il metodo **serate** aggiorna la variabile membro [**CSourceSeeking:: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) , ma non convalida il nuovo valore. Una frequenza pari a zero deve essere sempre rifiutata. La velocità inferiore a zero indica una riproduzione negativa. La maggior parte dei filtri non supporta frequenze negative.

Nell'esempio seguente viene illustrata una possibile implementazione:


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
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




