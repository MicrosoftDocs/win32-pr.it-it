---
title: Proprietà GetMuteOperation. Completed
description: Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da GetMuteAsync.
ms.assetid: B8E1DE71-46AC-4F6A-B873-AE3239BE492C
keywords:
- API di streaming multimediale delle proprietà completate
- API di streaming multimediale delle proprietà completa, interfaccia GetMuteOperation
- API di streaming multimediale dell'interfaccia GetMuteOperation, proprietà Completed
topic_type:
- apiref
api_name:
- GetMuteOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40c360dc3597d8cf04d1a8c505e479a38136f592
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726578"
---
# <a name="getmuteoperationcompleted-property"></a>Proprietà GetMuteOperation. Completed

Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) .

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Completed(
  [in]  GetMuteCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetMuteCompletedHandler **value
);
```



## <a name="property-value"></a>Valore proprietà

Gestore eventi.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetMuteOperation**](getmuteoperation.md)
</dt> </dl>

 

 