---
title: Metodo IReferenceClock GetTime
description: Il metodo GetTime recupera l'ora di riferimento corrente.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- Metodo GetTime per Windows Media Format
- Metodo GetTime windows Media Format , interfaccia IReferenceClock
- Interfaccia IReferenceClock windows Media Format, metodo GetTime
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f7756240e8987199e1f1b5d79e3f0b676d4808520781fbac18dfa18dd75e88d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055441"
---
# <a name="ireferenceclockgettime-method"></a>Metodo IReferenceClock::GetTime

Il **metodo GetTime** recupera l'ora di riferimento corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTime* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve l'ora corrente, in unità di 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Il metodo è riuscito.<br/>              |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | Il *parametro pTime* è **NULL.**<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IReferenceClock**](ireferenceclock.md)
</dt> </dl>

 

 





