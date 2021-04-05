---
title: Contenimento semplice del sito di frame
description: Contenimento semplice del sito di frame
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0106bc88d9f69f380590e808741e0b1a0bdc2f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955323"
---
# <a name="simple-frame-site-containment"></a><span data-ttu-id="db67c-103">Contenimento semplice del sito di frame</span><span class="sxs-lookup"><span data-stu-id="db67c-103">Simple Frame Site Containment</span></span>

<span data-ttu-id="db67c-104">Un controllo contenitore è un controllo ActiveX in grado di contenere altri controlli.</span><span class="sxs-lookup"><span data-stu-id="db67c-104">A container control is an ActiveX control that is capable of containing other controls.</span></span> <span data-ttu-id="db67c-105">Una casella di gruppo che contiene una raccolta di pulsanti di opzione è un esempio di un controllo contenitore.</span><span class="sxs-lookup"><span data-stu-id="db67c-105">A group box that contains a collection of radio buttons is an example of a container control.</span></span> <span data-ttu-id="db67c-106">I controlli contenitore devono impostare il \_ bit di stato SIMPLEFRAME di OLEMISC e chiamare l'implementazione [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) del relativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="db67c-106">Container controls should set the OLEMISC\_SIMPLEFRAME status bit, and should call its container's [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) implementation.</span></span> <span data-ttu-id="db67c-107">Un contenitore di controlli ActiveX che supporta i controlli contenitore deve implementare **ISimpleFrameSite**.</span><span class="sxs-lookup"><span data-stu-id="db67c-107">An ActiveX control container that supports container controls must implement **ISimpleFrameSite**.</span></span>

<span data-ttu-id="db67c-108">CATId-{157083E0-2368-11cf-87B9-00AA006C8166} CATId \_ SimpleFrameControl</span><span class="sxs-lookup"><span data-stu-id="db67c-108">CATID - {157083E0-2368-11cf-87B9-00AA006C8166} CATID\_SimpleFrameControl</span></span>

## <a name="related-topics"></a><span data-ttu-id="db67c-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="db67c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db67c-110">Categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="db67c-110">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




