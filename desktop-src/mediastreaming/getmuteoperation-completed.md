---
title: GetMuteOperation.Completed - proprietà
description: Ottiene o imposta un gestore eventi che viene richiamato al completamento dell'operazione asincrona avviata da GetMuteAsync.
ms.assetid: B8E1DE71-46AC-4F6A-B873-AE3239BE492C
keywords:
- Proprietà Completata API Streaming multimediale
- Proprietà Completata API Streaming multimediale, interfaccia GetMuteOperation
- Interfaccia GetMuteOperation API Streaming multimediale, proprietà Completed
topic_type:
- apiref
api_name:
- GetMuteOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb27715f284b96af4ba9e6cf8ff825a7237ba027d46d30d77859018d4d8b5574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100675"
---
# <a name="getmuteoperationcompleted-property"></a>GetMuteOperation.Completed - proprietà

Ottiene o imposta un gestore eventi che viene richiamato al completamento dell'operazione asincrona avviata da [**GetMuteAsync.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync)

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Completed(
  [in]  GetMuteCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetMuteCompletedHandler **value
);
```



## <a name="property-value"></a>Valore proprietà

Gestore eventi.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetMuteOperation**](getmuteoperation.md)
</dt> </dl>

 

 