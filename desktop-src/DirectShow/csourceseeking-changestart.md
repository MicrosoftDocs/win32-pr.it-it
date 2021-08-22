---
description: Il metodo ChangeStart viene chiamato quando cambia la posizione iniziale.
ms.assetid: d0a5497e-43e9-4d1f-9106-1f4cd8fcb372
title: Metodo CSourceSeeking.ChangeStart (Ctlutil.h)
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
ms.openlocfilehash: 7f7c0d9a86d33d13c95295c5ef1ef46a3e6c02371d1b6520572750450320b1f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073365"
---
# <a name="csourceseekingchangestart-method"></a>Metodo CSourceSeeking.ChangeStart

Il `ChangeStart` metodo viene chiamato quando cambia la posizione iniziale.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT ChangeStart() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Il [**metodo CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) chiama questo metodo se la posizione iniziale cambia. Questo metodo è virtuale puro. la classe derivata deve implementarla. Dopo un'operazione di ricerca, i timestamp devono essere riavviati da zero. Gli orari dei supporti devono riflettere la nuova ora di inizio. L'esempio seguente illustra una possibile implementazione:


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
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




