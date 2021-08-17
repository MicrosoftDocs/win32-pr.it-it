---
title: GetVolumeOperation.Completed - proprietà
description: Ottiene o imposta un gestore eventi che viene richiamato al completamento dell'operazione asincrona avviata da GetVolumeAsync.
ms.assetid: 34100EE7-C4CB-4AE0-BD3E-9E23A643F87E
keywords:
- Proprietà Completata API Streaming multimediale
- Proprietà completata API Di streaming multimediale, interfaccia GetVolumeOperation
- Interfaccia GetVolumeOperation API Streaming multimediale, proprietà Completed
topic_type:
- apiref
api_name:
- GetVolumeOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 84668f41f12c4920ec45bf70a3a931e6fc9234e213fe0a359ab93f3e34aac724
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735757"
---
# <a name="getvolumeoperationcompleted-property"></a>GetVolumeOperation.Completed - proprietà

Ottiene o imposta un gestore eventi che viene richiamato al completamento dell'operazione asincrona avviata da [**GetVolumeAsync.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync)

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Completed(
  [in]  GetVolumeCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetVolumeCompletedHandler **value
);
```



## <a name="property-value"></a>Valore proprietà

Gestore eventi.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetVolumeOperation**](getvolumeoperation.md)
</dt> </dl>

 

 