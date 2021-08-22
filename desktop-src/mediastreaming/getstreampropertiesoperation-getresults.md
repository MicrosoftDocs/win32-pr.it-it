---
title: Metodo GetStreamPropertiesOperation.GetResults
description: Restituisce i risultati dell'operazione asincrona avviata da GetStreamPropertiesAsync.
ms.assetid: D09DCDF5-2B9E-4E03-908B-AEEC7DC228C1
keywords:
- Metodo GetResults API Streaming multimediale
- Metodo GetResults API Streaming multimediale, interfaccia GetStreamPropertiesOperation
- Interfaccia GetStreamPropertiesOperation API Streaming multimediale, metodo GetResults
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3520cc44919e9c606c6625c75193b5f1ab54f4005cc098316bd8769ad0e0fe7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735822"
---
# <a name="getstreampropertiesoperationgetresults-method"></a>Metodo GetStreamPropertiesOperation.GetResults

Restituisce i risultati dell'operazione asincrona avviata [**da GetStreamPropertiesAsync.**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))

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

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetStreamPropertiesOperation**](getstreampropertiesoperation.md)
</dt> </dl>

 

