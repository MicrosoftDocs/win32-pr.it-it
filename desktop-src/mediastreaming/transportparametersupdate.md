---
title: Evento TransportParametersUpdate
description: Si verifica ogni volta che un set di parametri di trasporto viene aggiornato in ricevitore.
ms.assetid: df9256ca-6c59-462c-b32f-4653546db384
keywords:
- API di streaming multimediale per gli eventi TransportParametersUpdate
topic_type:
- apiref
api_name:
- TransportParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58df04862275af5da8714f8a954dc5b127f833f2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872477"
---
# <a name="transportparametersupdate-event"></a>Evento TransportParametersUpdate

Si verifica ogni volta che un set di parametri di trasporto viene aggiornato in ricevitore.

## <a name="syntax"></a>Sintassi


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a>Parametri

Questo evento non contiene parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Per gestire le notifiche da questo evento, registrare una funzione del gestore eventi [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) usando il metodo [**Add \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) . Per annullare la registrazione del gestore eventi, usare il metodo [**Remove \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) .

 

 