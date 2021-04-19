---
description: Il metodo iniziale viene chiamato quando cambia la posizione iniziale.
ms.assetid: d0a5497e-43e9-4d1f-9106-1f4cd8fcb372
title: Metodo CSourceSeeking. iniziale (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0a2751cf0ad1ecc6fddeeffd97b97c32b4a31b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333272"
---
# <a name="csourceseekingchangestart-method"></a>CSourceSeeking. iniziale, metodo

Il `ChangeStart` metodo viene chiamato quando viene modificata la posizione iniziale.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT ChangeStart() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Il metodo [**CSourceSeeking:: Sepositions**](csourceseeking-setpositions.md) chiama questo metodo se la posizione iniziale viene modificata. Questo metodo è virtuale puro; la classe derivata deve implementarla. Dopo un'operazione di ricerca, i timestamp devono essere riavviati da zero. I tempi dei supporti devono riflettere la nuova ora di inizio. Nell'esempio seguente viene illustrata una possibile implementazione:


```C++
HRESULT CMyStream::ChangeStart( )
{
    m_rtSampleTime = 0;          // Reset the time stamps.
    m_rtMediaTime = m_rtStart;   // Reset the media times.
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

 

 




