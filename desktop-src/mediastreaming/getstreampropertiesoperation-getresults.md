---
title: Metodo GetStreamPropertiesOperation. GetResults
description: Restituisce i risultati dell'operazione asincrona avviata da GetStreamPropertiesAsync.
ms.assetid: D09DCDF5-2B9E-4E03-908B-AEEC7DC228C1
keywords:
- API di streaming multimediale metodo GetResults
- API di streaming multimediale del metodo GetResults, interfaccia GetStreamPropertiesOperation
- API di streaming multimediale dell'interfaccia GetStreamPropertiesOperation, metodo GetResults
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 312703c28f5cdbb888b46d6ccd312dd358aa6b6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398943"
---
# <a name="getstreampropertiesoperationgetresults-method"></a>Metodo GetStreamPropertiesOperation. GetResults

Restituisce i risultati dell'operazione asincrona avviata da [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out, retval\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetStreamPropertiesOperation**](getstreampropertiesoperation.md)
</dt> </dl>

 

