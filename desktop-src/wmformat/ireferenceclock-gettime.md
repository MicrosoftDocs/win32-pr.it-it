---
title: Metodo getTime IReferenceClock
description: Il metodo getTime recupera l'ora di riferimento corrente.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- Metodo getTime per Windows Media Format
- Metodo getTime, formato Windows Media, interfaccia IReferenceClock
- Interfaccia IReferenceClock-formato Windows Media, metodo getTime
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c679ce0adbbc6cc7ddc014c12f1b0ace4be6b4b0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104398046"
---
# <a name="ireferenceclockgettime-method"></a>Metodo IReferenceClock:: getTime

Il metodo **getTime** recupera l'ora di riferimento corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTime* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve l'ora corrente, in unità di 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Il metodo è riuscito.<br/>              |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Il parametro *pTime* è **null**.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IReferenceClock**](ireferenceclock.md)
</dt> </dl>

 

 





