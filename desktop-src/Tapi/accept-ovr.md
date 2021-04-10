---
description: In alcuni ambienti, un utente non viene avvisato automaticamente di una chiamata a un'offerta, ad esempio tramite suoneria o un messaggio sullo schermo del computer.
ms.assetid: 50684e2a-0799-458b-9402-0958e35026d7
title: Accetta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd23d8ca1ed483b23d1b56fe98721b9fc53fb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226002"
---
# <a name="accept"></a><span data-ttu-id="be35d-103">Accetta</span><span class="sxs-lookup"><span data-stu-id="be35d-103">Accept</span></span>

<span data-ttu-id="be35d-104">In alcuni ambienti, un utente non viene avvisato automaticamente di una chiamata a un'offerta, ad esempio tramite suoneria o un messaggio sullo schermo del computer.</span><span class="sxs-lookup"><span data-stu-id="be35d-104">In some environments, a user is not automatically alerted to an offering call, such as by ringing or by a message on their computer screen.</span></span> <span data-ttu-id="be35d-105">L'operazione Accept avvia il processo di avviso (in genere squillante) e l'operazione di [risposta](answer-ovr.md) viene eseguita in seguito.</span><span class="sxs-lookup"><span data-stu-id="be35d-105">The accept operation starts the process of alerting (usually ringing), and the [answer](answer-ovr.md) operation takes place afterward.</span></span> <span data-ttu-id="be35d-106">L'applicazione può [eliminare](drop-ovr.md) la sessione, [reindirizzarla](redirect-ovr.md) o accettarla.</span><span class="sxs-lookup"><span data-stu-id="be35d-106">The application may [drop](drop-ovr.md) the session, [redirect](redirect-ovr.md) it, or accept it.</span></span>

<span data-ttu-id="be35d-107">Se il provider di servizi corrente lo supporta, l'applicazione ha la possibilità di inviare informazioni utente utente al momento dell'accettazione.</span><span class="sxs-lookup"><span data-stu-id="be35d-107">If the current service provider supports it, the application has the option to send user-user information at the time of the accept.</span></span> <span data-ttu-id="be35d-108">Non esiste alcuna garanzia che la rete fornisca tali informazioni alla parte chiamante.</span><span class="sxs-lookup"><span data-stu-id="be35d-108">There is no guarantee that the network will deliver this information to the calling party.</span></span>

<span data-ttu-id="be35d-109">Non tutti i provider di servizi supportano l'utilizzo di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="be35d-109">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="be35d-110">**TAPI 2. x:** Vedere [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept).</span><span class="sxs-lookup"><span data-stu-id="be35d-110">**TAPI 2.x:** See [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept).</span></span>

 

 
