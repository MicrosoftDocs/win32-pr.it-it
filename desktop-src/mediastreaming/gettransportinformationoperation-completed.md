---
title: Proprietà GetTransportInformationOperation Completed
description: Ottiene o imposta un gestore eventi che viene richiamato al completamento dell'operazione asincrona avviata da GetTransportInformationAsync.
ms.assetid: 11E60E00-75B5-4412-B115-4438255AEB8A
keywords:
- Proprietà Completata API Streaming multimediale
- Proprietà Completata API Streaming multimediale, interfaccia GetTransportInformationOperation
- Interfaccia GetTransportInformationOperation API Streaming multimediale , proprietà Completed
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.Completed
- GetTransportInformationOperation.get_Completed
- GetTransportInformationOperation.put_Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 389d7b281c10458e854407f9ce02bd2656fe6d4b16574408d75ae06ccc06d7f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735784"
---
# <a name="gettransportinformationoperationcompleted-property"></a>Proprietà GetTransportInformationOperation::Completed

Ottiene o imposta un gestore eventi che viene richiamato al completamento dell'operazione asincrona avviata da [**GetTransportInformationAsync.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync)

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Completed(
  [in]  GetTransportInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetTransportInformationCompletedHandler **value
);
```



## <a name="property-value"></a>Valore proprietà

Gestore eventi.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetTransportInformationOperation**](gettransportinformationoperation.md)
</dt> </dl>

 

 