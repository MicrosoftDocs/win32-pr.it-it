---
title: Evento TransportParametersUpdate
description: Si verifica ogni volta che un set di parametri di trasporto viene aggiornato nella dmr.
ms.assetid: df9256ca-6c59-462c-b32f-4653546db384
keywords:
- Api di streaming multimediale dell'evento TransportParametersUpdate
topic_type:
- apiref
api_name:
- TransportParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e3a600b7345b2cf05b5fb76f20b968e1af9ddecfb72f8442ada34dfd98ae3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034519"
---
# <a name="transportparametersupdate-event"></a>Evento TransportParametersUpdate

Si verifica ogni volta che un set di parametri di trasporto viene aggiornato nella dmr.

## <a name="syntax"></a>Sintassi


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a>Parametri

Questo evento non ha parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Per gestire le notifiche da questo evento, registrare una funzione del gestore eventi [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) usando [**il metodo add \_ TransportParametersUpdate.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) Per annullare la registrazione del gestore eventi, usare [**il metodo \_ remove TransportParametersUpdate.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate)

 

 