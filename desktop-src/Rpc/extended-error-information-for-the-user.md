---
title: Informazioni estese sull'errore per l'utente
description: Se sono disponibili informazioni estese sugli errori, i componenti che partecipano alla creazione delle informazioni sugli errori estesi devono facilitare l'individuazione del problema.
ms.assetid: 10c54f53-f449-4e7d-ba84-7b000beaee22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f52e45e3f181c5aaa0db196f9ce791581cc38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856302"
---
# <a name="extended-error-information-for-the-user"></a><span data-ttu-id="68ef5-103">Informazioni estese sull'errore per l'utente</span><span class="sxs-lookup"><span data-stu-id="68ef5-103">Extended Error Information for the User</span></span>

<span data-ttu-id="68ef5-104">Se sono disponibili informazioni estese sugli errori, i componenti che partecipano alla creazione delle informazioni sugli errori estesi devono facilitare l'individuazione del problema.</span><span class="sxs-lookup"><span data-stu-id="68ef5-104">If extended error information is available, the components participating in the creation of the extended error information must make it easy to find the problem.</span></span> <span data-ttu-id="68ef5-105">Il primo passaggio consiste nel rivedere l'ultimo record degli errori esteso e determinare in quale computer e in quale processo ha avuto origine il problema.</span><span class="sxs-lookup"><span data-stu-id="68ef5-105">The first step is to review the last extended error record, and determine on which computer and which process the problem originated.</span></span> <span data-ttu-id="68ef5-106">Si tratta spesso della cause dell'errore della \_ RPC \_ \* .</span><span class="sxs-lookup"><span data-stu-id="68ef5-106">This is often the cause of the RPC\_S\_\* error.</span></span> <span data-ttu-id="68ef5-107">Trovare il percorso di rilevamento e determinare quali sono i parametri per la posizione di rilevamento.</span><span class="sxs-lookup"><span data-stu-id="68ef5-107">Find the detection location, and determine what the parameters for this detection location mean.</span></span> <span data-ttu-id="68ef5-108">In genere indicano un errore di una chiamata di funzione o di un particolare controllo.</span><span class="sxs-lookup"><span data-stu-id="68ef5-108">Usually they indicate a failure of a function call or particular check.</span></span> <span data-ttu-id="68ef5-109">Da qui, determinare il motivo per cui la funzione o il controllo ha esito negativo e intraprendere un'azione correttiva.</span><span class="sxs-lookup"><span data-stu-id="68ef5-109">From there, determine why the function or check fails, and take corrective action.</span></span>

<span data-ttu-id="68ef5-110">I record prima dell'ultimo record indicano il percorso in base al quale è arrivato l'errore e in genere vengono usati come controllo di integrità anziché come un assistente nel processo di risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="68ef5-110">The records before the last record indicate the path by which the error arrived, and generally serve as a sanity check rather than an aide in the troubleshooting process.</span></span>

 

 




