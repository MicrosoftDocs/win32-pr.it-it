---
title: Considerazioni sulla programmazione MGM
description: Quando si sviluppano client di gestione dei gruppi multicast, osservare le linee guida seguenti
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- Multicast, considerazioni sulla programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e442de1dcb2da5a8664648587a88f05feaee970
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856505"
---
# <a name="mgm-programming-considerations"></a><span data-ttu-id="c08b7-104">Considerazioni sulla programmazione MGM</span><span class="sxs-lookup"><span data-stu-id="c08b7-104">MGM Programming Considerations</span></span>

<span data-ttu-id="c08b7-105">Quando si sviluppano client di gestione dei gruppi multicast, attenersi alle linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="c08b7-105">When you are developing multicast group manager clients, observe the following guidelines:</span></span>

-   <span data-ttu-id="c08b7-106">Le chiamate di funzione devono essere eseguite all'interno del processo del router.</span><span class="sxs-lookup"><span data-stu-id="c08b7-106">Function calls must be made from within the router process.</span></span> <span data-ttu-id="c08b7-107">Se le funzioni vengono chiamate da un altro processo, i risultati non saranno validi. il client non interagisce con il gestore del gruppo multicast.</span><span class="sxs-lookup"><span data-stu-id="c08b7-107">If functions are called from another process, their results will not be valid; the client will not interact with the multicast group manager.</span></span>
-   <span data-ttu-id="c08b7-108">I client che usano l'API MGM devono fornire il proprio controllo degli errori, assicurando che solo i dati validi vengano passati al gestore del gruppo multicast.</span><span class="sxs-lookup"><span data-stu-id="c08b7-108">Clients that use the MGM API must provide their own error checking, ensuring that only valid data is passed to the multicast group manager.</span></span> <span data-ttu-id="c08b7-109">Le funzioni MGM non restituiscono messaggi di errore dettagliati sui parametri non validi. il \_ valore del parametro error non valido \_ viene restituito senza spiegazione.</span><span class="sxs-lookup"><span data-stu-id="c08b7-109">MGM functions do not return detailed error messages about invalid parameters; the ERROR\_INVALID\_PARAMETER value is returned without explanation.</span></span>
-   <span data-ttu-id="c08b7-110">I client devono prestare attenzione nell'uso dei blocchi durante la chiamata di funzioni MGM.</span><span class="sxs-lookup"><span data-stu-id="c08b7-110">Clients should exercise caution in using locks while calling MGM functions.</span></span> <span data-ttu-id="c08b7-111">Questa operazione può impedire i deadlock.</span><span class="sxs-lookup"><span data-stu-id="c08b7-111">Doing so can prevent deadlocks.</span></span> <span data-ttu-id="c08b7-112">Quando si chiamano le funzioni MGM, i client non devono contenere blocchi che possono essere mantenuti contemporaneamente in un callback da Gestione gruppi multicast.</span><span class="sxs-lookup"><span data-stu-id="c08b7-112">When calling MGM functions, clients should not hold any locks that might simultaneously be held in a callback from the multicast group manager.</span></span>

 

 




