---
title: Conversione delle coordinate degli eventi
description: Conversione delle coordinate degli eventi
ms.assetid: e7de8af1-a409-4140-9e85-e035bd583912
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c40a742ead8fc8d7e431c1caa5210f0978168cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713219"
---
# <a name="event-coordinate-translation"></a><span data-ttu-id="6f2a1-103">Conversione delle coordinate degli eventi</span><span class="sxs-lookup"><span data-stu-id="6f2a1-103">Event Coordinate Translation</span></span>

<span data-ttu-id="6f2a1-104">La specifica 96 per i controlli richiede che le coordinate passate per gli eventi generati dal controllo cambino HIMETRIC in base ai punti.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-104">The 96 specification for controls requires that coordinates passed for events fired by the control change from being HIMETRIC to being points based.</span></span> <span data-ttu-id="6f2a1-105">Questa modifica consente di passare gli eventi delle coordinate in linea con proprietà e metodi e quindi la traduzione delle coordinate non è più la responsabilità del contenitore.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-105">This change brings the event passing of coordinates in line with properties and methods and thus coordinate translation is no longer the responsibility of the container.</span></span> <span data-ttu-id="6f2a1-106">In questo modo si verificano alcuni problemi di compatibilità in cui un controllo genera eventi usando una base di coordinate non prevista. dovrebbe trattarsi solo di un problema per cui un contenitore di controlli 96 ospita un controllo precedente a 96 precedente, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="6f2a1-106">This raises certain compatibility issues where a control fires events using a coordinate base that it is not expecting, this should only be an issue where a 96 control container is hosting an older pre-96 control as follows:</span></span>

-   <span data-ttu-id="6f2a1-107">Quando un contenitore precedente a 96 precedente ospita un controllo 96, il controllo presenta le coordinate dell'evento come punti, questo non dovrebbe causare problemi al contenitore poiché il contenitore deve riconoscere il tipo di parametro.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-107">When an older pre-96 container hosts a 96 control the control will present the event coordinates as points, this should not cause the container any problems as the container should recognize the parameter type.</span></span>
-   <span data-ttu-id="6f2a1-108">Quando un contenitore 96 ospita un controllo precedente a 96, il controllo presenterà il contenitore con le coordinate e si aspetterà che il contenitore debba eseguire una traduzione necessaria.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-108">When a 96 container hosts a pre-96 control the control will present the container with coordinates and expect the container to any translation necessary.</span></span> <span data-ttu-id="6f2a1-109">Tuttavia, il contenitore 96 prevede che un controllo sia conforme alla specifica dei controlli 96 e presenti le coordinate come punti.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-109">However the 96 container will be expecting a control to conform to the 96 controls specification and present its coordinates as points.</span></span> <span data-ttu-id="6f2a1-110">Il controllo Usa il metodo [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) sull'interfaccia [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) fornita dal contenitore in modo analogo a quanto accade per le proprietà e i metodi per ottenere questo risultato.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-110">The control uses the [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) method on the [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interface provided by the container in the same way as it does for properties and methods to achieve this.</span></span>

<span data-ttu-id="6f2a1-111">Di conseguenza, l'utente di un contenitore 96 che ospita i controlli precedenti a 96 dovrà tenere presente che, quando vengono attivati gli eventi, potrebbe essere necessaria una conversione aggiuntiva delle coordinate.</span><span class="sxs-lookup"><span data-stu-id="6f2a1-111">As a result the user of a 96 container hosting pre-96 controls will need to be aware that further translation of coordinates may be necessary when events are fired.</span></span>

 

 




