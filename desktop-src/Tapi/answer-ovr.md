---
description: L'operazione di risposta è una risposta tipica delle applicazioni a una sessione di comunicazione offerta. Se ha esito positivo, questa operazione causa la transizione di una sessione nello stato connesso.
ms.assetid: 34ac0b34-1d1b-4657-a737-27a4ed9326af
title: Risposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e08081b32b7ba3a3a24cde3ec37c1a6118582cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529221"
---
# <a name="answer"></a><span data-ttu-id="c7b49-104">Risposta</span><span class="sxs-lookup"><span data-stu-id="c7b49-104">Answer</span></span>

<span data-ttu-id="c7b49-105">L'operazione di risposta è la risposta tipica di un'applicazione a una sessione di comunicazione offerta.</span><span class="sxs-lookup"><span data-stu-id="c7b49-105">The answer operation is an application's typical response to an offered communications session.</span></span> <span data-ttu-id="c7b49-106">Se ha esito positivo, questa operazione causa la transizione di una sessione nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="c7b49-106">If successful, this operation causes a session to transition into the connected state.</span></span>

<span data-ttu-id="c7b49-107">In alcuni ambienti di telefonia (ad esempio ISDN), in cui gli avvisi utente sono separati dall'offerta di chiamata, l'applicazione ha la possibilità di [accettare](accept-ovr.md) una chiamata prima di rispondere o rifiutare ([eliminare](drop-ovr.md)) o [reindirizzare](redirect-ovr.md) la chiamata all' *offerta* .</span><span class="sxs-lookup"><span data-stu-id="c7b49-107">In some telephony environments (like ISDN), where user alerting is separate from call offering, the application has the option to [accept](accept-ovr.md) a call prior to answering or to reject ([drop](drop-ovr.md)) or [redirect](redirect-ovr.md) the *offering* call.</span></span>

<span data-ttu-id="c7b49-108">Se viene eseguita un'operazione di risposta per una nuova sessione quando una sessione è già attiva, l'effetto della sessione attiva esistente dipende dalle funzionalità del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="c7b49-108">If an answer operation is performed for a new session when a session is already active, the effect this has on the existing active session depends on the service provider's capabilities.</span></span> <span data-ttu-id="c7b49-109">La prima chiamata può non essere interessata, può essere eliminata automaticamente oppure può essere automaticamente messa in attesa.</span><span class="sxs-lookup"><span data-stu-id="c7b49-109">The first call can be unaffected, it can automatically be dropped, or it can automatically be placed on hold.</span></span> <span data-ttu-id="c7b49-110">TAPI invierà le notifiche degli eventi appropriate per entrambe le chiamate.</span><span class="sxs-lookup"><span data-stu-id="c7b49-110">TAPI will send the appropriate event notifications concerning both calls.</span></span>

<span data-ttu-id="c7b49-111">In una situazione con Bridge, se una chiamata è connessa ma nello stato attivo, è possibile aggiungerla usando l'operazione di risposta.</span><span class="sxs-lookup"><span data-stu-id="c7b49-111">In a bridged situation, if a call is connected but in the active state, it can be joined using the answer operation.</span></span>

<span data-ttu-id="c7b49-112">Se il provider di servizi lo supporta, l'applicazione ha la possibilità di inviare informazioni utente utente al momento della risposta.</span><span class="sxs-lookup"><span data-stu-id="c7b49-112">The application has the option to send user-user information at the time of the answer, if the service provider supports it.</span></span>

<span data-ttu-id="c7b49-113">**TAPI 2. x:** Vedere [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="c7b49-113">**TAPI 2.x:** See [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).</span></span>

<span data-ttu-id="c7b49-114">**TAPI 3. x:** Vedere [**ITBasicCallControl:: Answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).</span><span class="sxs-lookup"><span data-stu-id="c7b49-114">**TAPI 3.x:** See [**ITBasicCallControl::Answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).</span></span>

 

 
