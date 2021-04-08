---
title: Metodo GetPositionInformationOperation. GetResults
description: Restituisce i risultati dell'operazione asincrona avviata da GetPositionInformationAsync.
ms.assetid: 1DC7CD65-1F0F-44A5-9836-C77A5C23F91E
keywords:
- API di streaming multimediale metodo GetResults
- API di streaming multimediale del metodo GetResults, interfaccia GetPositionInformationOperation
- API di streaming multimediale dell'interfaccia GetPositionInformationOperation, metodo GetResults
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a0b4311c3be814a73ddb1e2a9b18d8e19aea9ee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726759"
---
# <a name="getpositioninformationoperationgetresults-method"></a>Metodo GetPositionInformationOperation. GetResults

Restituisce i risultati dell'operazione asincrona avviata da [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetResults(
  [out, retval] PositionInformation *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out, retval\]
</dt> <dd>

Riferimento a una struttura [**PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) che contiene i risultati dell'operazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Il metodo **GetResults** viene in genere chiamato dal gestore eventi registrato impostando la proprietà [**Completed**](getpositioninformationoperation-completed.md) .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetPositionInformationOperation**](getpositioninformationoperation.md)
</dt> </dl>

 

