---
description: Il metodo CoInitializeHelper chiama la funzione CoInitializeEx all'inizio del thread.
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: Metodo CAMThread. CoInitializeHelper (Wxutil. h)
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
ms.openlocfilehash: a6c3eb7fbcb9e4abada43098339a29d208ded0d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326943"
---
# <a name="camthreadcoinitializehelper-method"></a>CAMThread. CoInitializeHelper, metodo

Il `CoInitializeHelper` metodo chiama la funzione CoInitializeEx all'inizio del thread.

## <a name="syntax"></a>Sintassi


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono riportati i valori possibili.



| Codice restituito                                                                             | Descrizione                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | La funzione CoInitializeEx non è disponibile.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                                      |
| <dl> <dt>**E \_ non riescono**</dt> </dl>  | Esito negativo.<br/>                                      |



 

## <a name="remarks"></a>Commenti

Il metodo [**CAMThread:: InitialThreadProc**](camthread-initialthreadproc.md) chiama questo metodo helper, che chiama la funzione CoInitializeEx. Usa il flag CoInit \_ Disable \_ OLE1DDE per disabilitare Dynamic Data Exchange (DDE). Per ulteriori informazioni, vedere Platform SDK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




