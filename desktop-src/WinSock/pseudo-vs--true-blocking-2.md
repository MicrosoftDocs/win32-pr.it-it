---
description: Pseudoblocking operazioni pseudo-blocco in Windows Sockets (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Pseudo-blocco e vero blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082992aba884aebec30d35bc65d2cb6c49e29051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309943"
---
# <a name="pseudo-blocking-and-true-blocking"></a><span data-ttu-id="8f1e9-103">Pseudo-blocco e vero blocco</span><span class="sxs-lookup"><span data-stu-id="8f1e9-103">Pseudo Blocking and True Blocking</span></span>

<span data-ttu-id="8f1e9-104">In 16 ambienti Windows il blocco effettivo non è supportato dal sistema operativo. Pertanto, un'operazione di blocco che non può essere completata immediatamente viene gestita come segue:</span><span class="sxs-lookup"><span data-stu-id="8f1e9-104">In 16 Windows environments, true blocking is not supported by the operating system; therefore, a blocking operation that cannot be completed immediately is handled as follows:</span></span>

-   <span data-ttu-id="8f1e9-105">Il provider di servizi avvia l'operazione e quindi immette un ciclo durante il quale invia tutti i messaggi di Windows (cedendo il processore a un altro thread, se necessario)</span><span class="sxs-lookup"><span data-stu-id="8f1e9-105">The service provider initiates the operation, and then enters a loop during which it dispatches any Windows messages (yielding the processor to another thread if necessary)</span></span>
-   <span data-ttu-id="8f1e9-106">Viene quindi verificato il completamento della funzione Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="8f1e9-106">It then checks for the completion of the Windows Sockets function.</span></span>
-   <span data-ttu-id="8f1e9-107">Se la funzione è stata completata o se [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) è stato richiamato, il ciclo viene terminato e la funzione di blocco viene completata con un risultato appropriato.</span><span class="sxs-lookup"><span data-stu-id="8f1e9-107">If the function has completed, or if [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) has been invoked, the loop is terminated and the blocking function completes with an appropriate result.</span></span>

<span data-ttu-id="8f1e9-108">Questo è ciò che si intende con il termine pseudo-blocco e il ciclo a cui si fa riferimento è noto come hook di blocco predefinito.</span><span class="sxs-lookup"><span data-stu-id="8f1e9-108">This is what is meant by the term pseudo blocking, and the loop referred to above is known as the default blocking hook.</span></span>

 

 
