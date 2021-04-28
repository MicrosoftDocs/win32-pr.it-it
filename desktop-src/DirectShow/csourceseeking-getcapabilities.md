---
description: 'Metodo CSourceSeeking.GetCapabilities: il metodo GetCapabilities recupera tutte le funzionalità di ricerca del flusso. Questo metodo implementa il metodo IMediaSeeking::GetCapabilities.'
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: Metodo CSourceSeeking.GetCapabilities (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f1f354381c4c99cf880c75cbbc4b13355e386030
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098779"
---
# <a name="csourceseekinggetcapabilities-method"></a>Metodo CSourceSeeking.GetCapabilities

Il `GetCapabilities` metodo recupera tutte le funzionalità di ricerca del flusso. Questo metodo implementa il [**metodo IMediaSeeking::GetCapabilities.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCapabilities* 
</dt> <dd>

Puntatore a una variabile che riceve una combinazione bit per bit di [**flag AM \_ \_ SEEKING SEEKING \_ CAPABILITIES.**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Operazione riuscita<br/>                |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl> | **Valore del** puntatore NULL<br/> |



 

## <a name="remarks"></a>Commenti

Le funzionalità di ricerca vengono specificate dalla variabile membro [**CSourceSeeking::m \_ dwSeekingCaps.**](csourceseeking-m-dwseekingcaps.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




