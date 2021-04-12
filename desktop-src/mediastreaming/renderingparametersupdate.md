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
# <a name="renderingparametersupdate-event"></a><span data-ttu-id="47236-104">Evento RenderingParametersUpdate</span><span class="sxs-lookup"><span data-stu-id="47236-104">RenderingParametersUpdate event</span></span>

<span data-ttu-id="47236-105">Si verifica ogni volta che un set di parametri del controllo di rendering viene aggiornato in ricevitore.</span><span class="sxs-lookup"><span data-stu-id="47236-105">Occurs whenever any of a set of rendering control parameters are updated on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="47236-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47236-106">Syntax</span></span>


```C++
void RenderingParametersUpdate();
```



## <a name="parameters"></a><span data-ttu-id="47236-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="47236-107">Parameters</span></span>

<span data-ttu-id="47236-108">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="47236-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47236-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47236-109">Return value</span></span>

<span data-ttu-id="47236-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="47236-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="47236-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="47236-111">Remarks</span></span>

<span data-ttu-id="47236-112">Per gestire le notifiche da questo evento, registrare una funzione del gestore eventi [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) usando il metodo [**Add \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="47236-112">To handle notifications from this event, register a [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) event handler function using the [**add\_RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) method.</span></span> <span data-ttu-id="47236-113">Per annullare la registrazione del gestore eventi, usare il metodo [**Remove \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="47236-113">To unregister the event handler, use the [**remove\_RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) method.</span></span>

 

 