---
title: Metodo IReferenceClock AdviseTime
description: Il metodo AdviseTime richiede una notifica asincrona che è trascorso un periodo di tempo.
ms.assetid: 8f3f8713-b53c-4110-ac7a-724bbc49368e
keywords:
- Metodo AdviseTime Windows Media Format
- Metodo AdviseTime Windows Media Format, interfaccia IReferenceClock
- Interfaccia IReferenceClock-formato Windows Media, metodo AdviseTime
topic_type:
- apiref
api_name:
- IReferenceClock.AdviseTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fa91338b4bff8f925f00e7159a36089e0de0aa8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299129"
---
# <a name="ireferenceclockadvisetime-method"></a>Metodo IReferenceClock:: AdviseTime

Il metodo **AdviseTime** richiede una notifica asincrona che è trascorso un periodo di tempo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AdviseTime(
  [in]  REFERENCE_TIME rtBaseTime,
  [in]  REFERENCE_TIME rtStreamTime,
  [in]  HEVENT         hEvent,
  [out] DWORD          *pdwAdviseCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rtBaseTime* \[ in\]
</dt> <dd>

Tempo di riferimento di base, in unità 100-nanosecondi.

</dd> <dt>

*rtStreamTime* \[ in\]
</dt> <dd>

Tempo di offset del flusso, in unità di 100 nanosecondi.

</dd> <dt>

*hEvent* \[ in\]
</dt> <dd>

Handle per un evento, creato dal chiamante. Questo evento verrà segnalato al termine dell'intervallo di tempo specificato.

</dd> <dt>

*pdwAdviseCookie* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve un identificatore per la richiesta. Viene usato per identificare la chiamata a **AdviseTime** in futuro, ad esempio, per annullare la richiesta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Il metodo è riuscito.<br/>                        |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Il parametro *pdwAdviseCookie* è **null**.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>    | Errore non specificato.<br/>                         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IReferenceClock**](ireferenceclock.md)
</dt> </dl>

 

 





