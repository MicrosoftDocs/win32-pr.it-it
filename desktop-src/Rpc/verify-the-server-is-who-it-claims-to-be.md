---
title: Verificare che il server sia quello che dichiara di essere
description: È preferibile usare l'autenticazione reciproca e verificare quindi l'identità del server.
ms.assetid: 6636a865-0e3b-4e52-81bb-0df48285e928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e16ae6a87134a9fbc783d35216a1c4df56ce2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710576"
---
# <a name="verify-the-server-is-who-it-claims-to-be"></a><span data-ttu-id="0240e-103">Verificare che il server sia quello che dichiara di essere</span><span class="sxs-lookup"><span data-stu-id="0240e-103">Verify the Server is Who it Claims to Be</span></span>

<span data-ttu-id="0240e-104">È preferibile usare l'autenticazione reciproca e verificare quindi l'identità del server.</span><span class="sxs-lookup"><span data-stu-id="0240e-104">It is best to use mutual authentication, and thereby verify the identity of the server.</span></span> <span data-ttu-id="0240e-105">Un esempio di errore comune che non riesce a eseguire questa operazione è costituito dalle applicazioni che dispongono di un servizio locale in cui i client chiamano.</span><span class="sxs-lookup"><span data-stu-id="0240e-105">An example of a common mistake that fails to do this is applications that have a local service into which clients call.</span></span> <span data-ttu-id="0240e-106">In alcune configurazioni, un amministratore può decidere che il servizio di sistema non è molto utile e può scegliere di arrestarlo.</span><span class="sxs-lookup"><span data-stu-id="0240e-106">In some configurations an administrator may decide that the system service is not really useful and may chose to stop it.</span></span> <span data-ttu-id="0240e-107">Un utente malintenzionato inventivo in un computer Terminal Server può avviare un processo che rimane in ascolto sullo stesso endpoint e quando un client si connette a un endpoint, consentendo la rappresentazione sul server senza autenticare reciprocamente il server, l'autore dell'attacco può rappresentare il client e accedere ai dati del client oppure effettuare chiamate di rete per conto del client.</span><span class="sxs-lookup"><span data-stu-id="0240e-107">An inventive attacker on a terminal server computer may launch a process that listens on the same endpoint, and when a client connects to an endpoint, allowing impersonation on the server without mutually authenticating the server, the attacker can impersonate the client and access the client's data, or make network calls on behalf of the client.</span></span> <span data-ttu-id="0240e-108">La maggior parte dei servizi di sistema viene eseguita con un account noto, ad esempio LocalSysyem, LocalService o NetworkService, che può essere verificato utilizzando l'autenticazione reciproca.</span><span class="sxs-lookup"><span data-stu-id="0240e-108">Most system services run under a well-known account, such as LocalSysyem, LocalService, or NetworkService, which can be verified using mutual authentication.</span></span>

 

 




