---
description: Quando le applicazioni di disegno complesse eseguono operazioni grafiche lunghe, utilizzano risorse di sistema valide.
ms.assetid: 3beef852-27fe-4ee2-b38b-3dc50e5d2fcf
title: Annullamento delle operazioni di disegno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e3bdb7a57c7c427e7cd15ffddb62b1c492c25b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994104"
---
# <a name="cancellation-of-drawing-operations"></a><span data-ttu-id="f7fd0-103">Annullamento delle operazioni di disegno</span><span class="sxs-lookup"><span data-stu-id="f7fd0-103">Cancellation of Drawing Operations</span></span>

<span data-ttu-id="f7fd0-104">Quando le applicazioni di disegno complesse eseguono operazioni grafiche lunghe, utilizzano risorse di sistema valide.</span><span class="sxs-lookup"><span data-stu-id="f7fd0-104">When complex drawing applications perform lengthy graphics operations, they consume valuable system resources.</span></span> <span data-ttu-id="f7fd0-105">Sfruttando le funzionalità multitasking del sistema, un'applicazione può utilizzare i thread e la funzione [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc) per gestire queste operazioni.</span><span class="sxs-lookup"><span data-stu-id="f7fd0-105">By taking advantage of the system's multitasking features, an application can use threads and the [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc) function to manage these operations.</span></span> <span data-ttu-id="f7fd0-106">Se, ad esempio, l'operazione grafica eseguita dal thread A sta utilizzando le risorse necessarie, il thread B può chiamare la funzione CancelDC per arrestare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="f7fd0-106">For example, if the graphics operation performed by thread A is consuming needed resources, thread B can call the CancelDC function to halt that operation.</span></span>

 

 



