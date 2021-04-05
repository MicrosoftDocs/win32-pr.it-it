---
title: Proprietà CreateMediaRendererOperation. Completed
description: Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da CreateMediaRendererAsync o CreateMediaRendererFromBasicDeviceAsync.
ms.assetid: B62CF929-13D0-4665-89E4-DEC48A38DDF7
keywords:
- API di streaming multimediale delle proprietà completate
- API di streaming multimediale delle proprietà completa, interfaccia CreateMediaRendererOperation
- API di streaming multimediale dell'interfaccia CreateMediaRendererOperation, proprietà Completed
topic_type:
- apiref
api_name:
- CreateMediaRendererOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3b4ebafc1441741a352f4573709495228bf13e4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718418"
---
# <a name="createmediarendereroperationcompleted-property"></a>Proprietà CreateMediaRendererOperation. Completed

Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) o [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) .

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Completed(
  [in]  ICreateMediaRendererCompletedHandler value
);

HRESULT get_Completed(
  [out] ICreateMediaRendererCompletedHandler *value
);
```



## <a name="property-value"></a>Valore proprietà

Gestore eventi.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CreateMediaRendererOperation**](createmediarendereroperation.md)
</dt> </dl>

 

 




