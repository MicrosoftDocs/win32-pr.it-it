---
title: Metodo GetTransportInformationOperation GetResults
description: Restituisce i risultati dell'operazione asincrona avviata da GetTransportInformationAsync.
ms.assetid: 8CC6641E-C1E6-4C64-90EC-4120ECB54135
keywords:
- Metodo GetResults API Streaming multimediale
- Metodo GetResults API Streaming multimediale, interfaccia GetTransportInformationOperation
- GetTransportInformationOperation interface Media Streaming API , Metodo GetResults
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbcc6345a09d0553df240c57e50b4498618be76cc75814f268892aa6e0b4dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100635"
---
# <a name="gettransportinformationoperationgetresults-method"></a>Metodo GetTransportInformationOperation::GetResults

Restituisce i risultati dell'operazione asincrona avviata da [**GetTransportInformationAsync.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetResults(
  [out, retval] TransportInformation *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Riferimento a una [**struttura TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) che contiene i risultati dell'operazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Il **metodo GetResults** viene in genere chiamato dal gestore eventi registrato impostando la [**proprietà Completed.**](gettransportinformationoperation-completed.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetTransportInformationOperation**](gettransportinformationoperation.md)
</dt> </dl>

 

