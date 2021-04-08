---
description: Il reindirizzamento della sessione consente a un'applicazione di deflettere una sessione offerta in un altro indirizzo senza rispondere alla chiamata.
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: reindirizzamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ade9315c3b5e8e68c17bf34a0b6d54a9d9663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760808"
---
# <a name="redirect"></a><span data-ttu-id="414b0-103">reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="414b0-103">Redirect</span></span>

<span data-ttu-id="414b0-104">Il reindirizzamento della sessione consente a un'applicazione di deflettere una sessione offerta in un altro indirizzo senza rispondere alla chiamata.</span><span class="sxs-lookup"><span data-stu-id="414b0-104">Session redirection allows an application to deflect an offered session to another address without answering the call.</span></span> <span data-ttu-id="414b0-105">L'applicazione può eseguire il reindirizzamento in base a una chiamata.</span><span class="sxs-lookup"><span data-stu-id="414b0-105">The application can do redirection on a call-by-call basis.</span></span> <span data-ttu-id="414b0-106">Ad esempio, un'applicazione potrebbe consentire a un utente di specificare reindirizzamenti diversi in base alle informazioni sull'ID chiamante.</span><span class="sxs-lookup"><span data-stu-id="414b0-106">For example, an application might allow a user to specify different redirections based on caller ID information.</span></span> <span data-ttu-id="414b0-107">Dopo che una chiamata è stata reindirizzata correttamente, lo stato passa in genere a inattivo e le risorse associate devono essere rilasciate.</span><span class="sxs-lookup"><span data-stu-id="414b0-107">After a call has been successfully redirected, the state typically transitions to idle and associated resources must be released.</span></span>

<span data-ttu-id="414b0-108">Il reindirizzamento differisce [da quello](forward-ovr.md) che una volta impostato, l'operazione viene eseguita da TAPI, dal provider di servizi o dallo switch senza ulteriore coinvolgimento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="414b0-108">Redirect differs from [forward](forward-ovr.md) in that once forwarding has been set up, the operation is performed by TAPI, the service provider, or the switch without further involvement of the application.</span></span> <span data-ttu-id="414b0-109">Il reindirizzamento differisce dal [trasferimento](transfer-ovr.md) in quanto il reindirizzamento non richiede prima di tutto la risposta alla chiamata.</span><span class="sxs-lookup"><span data-stu-id="414b0-109">Redirect differs from [transfer](transfer-ovr.md) in that redirect does not require answering the call first.</span></span>

<span data-ttu-id="414b0-110">Non tutti i provider di servizi supportano l'utilizzo di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="414b0-110">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="414b0-111">**TAPI 2. x:** Vedere [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).</span><span class="sxs-lookup"><span data-stu-id="414b0-111">**TAPI 2.x:** See [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).</span></span>

 

 
