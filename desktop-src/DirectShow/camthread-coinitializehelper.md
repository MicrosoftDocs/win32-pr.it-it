---
description: Il metodo CoInitializeHelper chiama la funzione CoInitializeEx all'inizio del thread.
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: Metodo CAMThread.CoInitializeHelper (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CoInitializeHelper
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 41a763a4b9151f22615aa0af3dae57af8281751209a016dc3135f3572e9d8ef3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768291"
---
# <a name="camthreadcoinitializehelper-method"></a>Metodo CAMThread.CoInitializeHelper

Il `CoInitializeHelper` metodo chiama la funzione CoInitializeEx all'inizio del thread.

## <a name="syntax"></a>Sintassi


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Di seguito sono riportati i valori possibili.



| Codice restituito                                                                             | Descrizione                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | La funzione CoInitializeEx non è disponibile.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>                                      |
| <dl> <dt>**E \_ FAIL**</dt> </dl>  | Esito negativo.<br/>                                      |



 

## <a name="remarks"></a>Commenti

Il [**metodo CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) chiama questo metodo helper, che chiama la funzione CoInitializeEx. Usa il flag COINIT \_ DISABLE \_ OLE1DDE per disabilitare Dynamic Data Exchange (DDE). Per altre informazioni, vedere Platform SDK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




