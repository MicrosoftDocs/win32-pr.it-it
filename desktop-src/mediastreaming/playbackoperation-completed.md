---
title: Proprietà PlaybackOperation. Completed
description: Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da uno dei metodi di riproduzione MediaRenderer.
ms.assetid: E8F8D3FC-C31F-485C-A30B-2457F4B1DE82
keywords:
- API di streaming multimediale delle proprietà completate
- API di streaming multimediale delle proprietà completa, interfaccia PlaybackOperation
- API di streaming multimediale dell'interfaccia PlaybackOperation, proprietà Completed
topic_type:
- apiref
api_name:
- PlaybackOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bf305b4028e223c36df0c8a59c5246228c5b8d40
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299047"
---
# <a name="playbackoperationcompleted-property"></a>Proprietà PlaybackOperation. Completed

Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da uno dei metodi di riproduzione [**MediaRenderer**](mediarenderer.md) .

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Completed(
  [in]  PlaybackOperationCompletedHandler *value
);

HRESULT get_Completed(
  [out] PlaybackOperationCompletedHandler **value
);
```



## <a name="property-value"></a>Valore proprietà

Gestore eventi.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PlaybackOperation**](playbackoperation.md)
</dt> </dl>

 

 




