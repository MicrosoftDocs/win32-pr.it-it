---
title: Evento RenderingParametersUpdate
description: Si verifica ogni volta che un set di parametri del controllo di rendering viene aggiornato in ricevitore.
ms.assetid: 863ca879-a420-43d6-9ac8-94f8303bb759
keywords:
- API di streaming multimediale per gli eventi RenderingParametersUpdate
topic_type:
- apiref
api_name:
- RenderingParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35e4898bae876babb0e5fbc1c4b9760eec6a9b62
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337094"
---
# <a name="renderingparametersupdate-event"></a>Evento RenderingParametersUpdate

Si verifica ogni volta che un set di parametri del controllo di rendering viene aggiornato in ricevitore.

## <a name="syntax"></a>Sintassi


```C++
void RenderingParametersUpdate();
```



## <a name="parameters"></a>Parametri

Questo evento non contiene parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Per gestire le notifiche da questo evento, registrare una funzione del gestore eventi [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) usando il metodo [**Add \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) . Per annullare la registrazione del gestore eventi, usare il metodo [**Remove \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) .

 

 