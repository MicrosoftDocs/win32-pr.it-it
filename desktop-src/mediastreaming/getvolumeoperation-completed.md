---
title: Proprietà GetVolumeOperation. Completed
description: Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da GetVolumeAsync.
ms.assetid: 34100EE7-C4CB-4AE0-BD3E-9E23A643F87E
keywords:
- API di streaming multimediale delle proprietà completate
- API di streaming multimediale delle proprietà completa, interfaccia GetVolumeOperation
- API di streaming multimediale dell'interfaccia GetVolumeOperation, proprietà Completed
topic_type:
- apiref
api_name:
- GetVolumeOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d21577d57e1e29aff1d2b12b92bcbef58a529eba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117622"
---
# <a name="getvolumeoperationcompleted-property"></a>Proprietà GetVolumeOperation. Completed

Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) .

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Completed(
  [in]  GetVolumeCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetVolumeCompletedHandler **value
);
```



## <a name="property-value"></a>Valore proprietà

Gestore eventi.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetVolumeOperation**](getvolumeoperation.md)
</dt> </dl>

 

 