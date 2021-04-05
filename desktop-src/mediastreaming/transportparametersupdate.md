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
# <a name="transportparametersupdate-event"></a><span data-ttu-id="37cf9-104">Evento TransportParametersUpdate</span><span class="sxs-lookup"><span data-stu-id="37cf9-104">TransportParametersUpdate event</span></span>

<span data-ttu-id="37cf9-105">Si verifica ogni volta che un set di parametri di trasporto viene aggiornato in ricevitore.</span><span class="sxs-lookup"><span data-stu-id="37cf9-105">Occurs whenever any of a set of transport parameters are updated on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="37cf9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37cf9-106">Syntax</span></span>


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a><span data-ttu-id="37cf9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="37cf9-107">Parameters</span></span>

<span data-ttu-id="37cf9-108">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="37cf9-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="37cf9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37cf9-109">Return value</span></span>

<span data-ttu-id="37cf9-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="37cf9-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37cf9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="37cf9-111">Remarks</span></span>

<span data-ttu-id="37cf9-112">Per gestire le notifiche da questo evento, registrare una funzione del gestore eventi [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) usando il metodo [**Add \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="37cf9-112">To handle notifications from this event, register a [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) event handler function using the [**add\_TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) method.</span></span> <span data-ttu-id="37cf9-113">Per annullare la registrazione del gestore eventi, usare il metodo [**Remove \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="37cf9-113">To unregister the event handler, use the [**remove\_TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) method.</span></span>

 

 