---
title: Controlli contenitore
description: Controlli contenitore
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69228bcc03017442880d41156f67397ee26bb13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471787"
---
# <a name="container-controls"></a><span data-ttu-id="7955b-103">Controlli contenitore</span><span class="sxs-lookup"><span data-stu-id="7955b-103">Container Controls</span></span>

<span data-ttu-id="7955b-104">Come descritto in precedenza, i controlli contenitore sono controlli ActiveX che contengono visivamente altri controlli.</span><span class="sxs-lookup"><span data-stu-id="7955b-104">As described above, container controls are ActiveX controls that visually contain other controls.</span></span> <span data-ttu-id="7955b-105">L'architettura dei controlli ActiveX specifica l'interfaccia [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) per abilitare i controlli contenitore.</span><span class="sxs-lookup"><span data-stu-id="7955b-105">The ActiveX controls architecture specifies the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface to enable container controls.</span></span> <span data-ttu-id="7955b-106">I contenitori possono inoltre supportare i controlli contenitore senza supportare **ISimpleFrameSite**, anche se non è possibile garantire il comportamento.</span><span class="sxs-lookup"><span data-stu-id="7955b-106">Containers may also support container controls without supporting **ISimpleFrameSite**, although the behavior cannot be guaranteed.</span></span> <span data-ttu-id="7955b-107">Per questo motivo, esiste una categoria di componenti per i controlli SimpleFrameSite in cui è necessaria la funzionalità completa di questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7955b-107">For this reason, a component category exists for SimpleFrameSite controls where the full functionality of this interface is required.</span></span>

<span data-ttu-id="7955b-108">Per supportare i controlli contenitore senza implementare [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), un contenitore di controlli ActiveX deve:</span><span class="sxs-lookup"><span data-stu-id="7955b-108">To support container controls without implementing [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), an ActiveX control container must:</span></span>

-   <span data-ttu-id="7955b-109">Attivare tutti i controlli in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="7955b-109">Activate all controls at all times.</span></span>
-   <span data-ttu-id="7955b-110">Eseguire un nuovo elemento padre dei controlli contenuti nell'hWnd del controllo che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="7955b-110">Reparent the contained controls to the hWnd of the containing control.</span></span>
-   <span data-ttu-id="7955b-111">Rimanere l'elemento padre del controllo contenitore.</span><span class="sxs-lookup"><span data-stu-id="7955b-111">Remain the parent of the container control.</span></span>

 

 




