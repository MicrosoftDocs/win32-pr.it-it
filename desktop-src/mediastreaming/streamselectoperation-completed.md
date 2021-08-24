---
title: StreamSelectOperation.Completed - proprietà
description: Ottiene o imposta un gestore eventi richiamato quando viene completata l'operazione asincrona avviata da SelectBestStreamAsync.
ms.assetid: 693CC002-2D91-4656-954D-8A556480155C
keywords:
- Proprietà Completata API Streaming multimediale
- Proprietà Completata API Streaming multimediale, interfaccia StreamSelectOperation
- Interfaccia StreamSelectOperation API Streaming multimediale, proprietà Completed
topic_type:
- apiref
api_name:
- StreamSelectOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 554874c19054f4b2ee46fbfe29fb4dfb8149e476ff96d040ffdbdd9b39de4612
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847581"
---
# <a name="streamselectoperationcompleted-property"></a>StreamSelectOperation.Completed - proprietà

Ottiene o imposta un gestore eventi richiamato quando viene completata l'operazione asincrona avviata da [**SelectBestStreamAsync.**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85))

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a>Valore proprietà

Gestore eventi.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**StreamSelectOperation**](streamselectoperation.md)
</dt> </dl>

 

 