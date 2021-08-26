---
title: Metodo StreamSelectOperation.GetResults
description: Restituisce i risultati dell'operazione asincrona avviata da SelectBestStreamAsync.
ms.assetid: 2D9887E7-17C8-4161-984F-FA44591D2052
keywords:
- Metodo GetResults API Streaming multimediale
- Metodo GetResults API Streaming multimediale, interfaccia StreamSelectOperation
- Interfaccia StreamSelectOperation API Streaming multimediale, metodo GetResults
topic_type:
- apiref
api_name:
- StreamSelectOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 022e75a57b9b38cff2a1e477d78a164767ab8cbcd4e1d3a159e8f61c8972fb95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952481"
---
# <a name="streamselectoperationgetresults-method"></a>Metodo StreamSelectOperation.GetResults

Restituisce i risultati dell'operazione asincrona avviata [**da SelectBestStreamAsync.**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**StreamSelectOperation**](streamselectoperation.md)
</dt> </dl>

 

