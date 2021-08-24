---
title: Metodo GetPositionInformationOperation.GetResults
description: Restituisce i risultati dell'operazione asincrona avviata da GetPositionInformationAsync.
ms.assetid: 1DC7CD65-1F0F-44A5-9836-C77A5C23F91E
keywords:
- Metodo GetResults API Streaming multimediale
- Metodo GetResults API Streaming multimediale, interfaccia GetPositionInformationOperation
- GetPositionInformationOperation interface Media Streaming API , Metodo GetResults
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e924227c37318a788f9c30aea5e5125a40c69175ac7c4449a54ebcc4cf61326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721061"
---
# <a name="getpositioninformationoperationgetresults-method"></a>Metodo GetPositionInformationOperation.GetResults

Restituisce i risultati dell'operazione asincrona avviata [**da GetPositionInformationAsync.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetResults(
  [out, retval] PositionInformation *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Riferimento a una [**struttura PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) che contiene i risultati dell'operazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Il **metodo GetResults** viene in genere chiamato dal gestore eventi registrato impostando la [**proprietà Completed.**](getpositioninformationoperation-completed.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetPositionInformationOperation**](getpositioninformationoperation.md)
</dt> </dl>

 

