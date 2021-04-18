---
description: Valore HRESULT che indica se l'oggetto accetterà esempi. Se il valore è \_ OK, l'oggetto accetterà esempi. In caso contrario, rifiuta gli esempi.
ms.assetid: e05d4d2e-cc3e-4b83-8531-bc4bd6d665ac
title: 'Membro COutputQueue:: m_hr (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hr
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b786afa24f974d5eab7e13062105f26386da1c30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327342"
---
# <a name="coutputqueuem_hr-member"></a>Membro HR COutputQueue:: m \_

Valore **HRESULT** che indica se l'oggetto accetterà esempi. Se il valore è \_ OK, l'oggetto accetterà esempi. In caso contrario, rifiuta gli esempi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT m_hr;
```



## <a name="remarks"></a>Osservazioni

Questa variabile membro viene utilizzata per coordinare le attività tra thread. Se il pin di input downstream rifiuta un campione o se l'oggetto inizia lo scaricamento, il valore viene impostato su S \_ false o su un codice di errore. L'oggetto non fornirà altri esempi fino al completamento dello scaricamento oppure fino a quando non viene chiamato il metodo [**COutputQueue:: Reset**](coutputqueue-reset.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




