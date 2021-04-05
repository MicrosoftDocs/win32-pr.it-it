---
title: Supporto host sicurezza RAS
description: Windows NT 4,0 fornisce un modo per una DLL di sicurezza RAS di terze parti per migliorare le funzionalità di protezione RAS predefinite. Windows 95 non fornisce questo supporto.
ms.assetid: 1cbacd7f-c9b9-4fb4-b505-a4b1d1b6f632
keywords:
- Supporto host, RAS
- Supporto host sicurezza, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99145f80d347ccd4ee9fbf4a4cdc23ca5af373e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711740"
---
# <a name="ras-security-host-support"></a><span data-ttu-id="f0e83-106">Supporto host sicurezza RAS</span><span class="sxs-lookup"><span data-stu-id="f0e83-106">RAS Security Host Support</span></span>

<span data-ttu-id="f0e83-107">Windows NT 4,0 fornisce un modo per una DLL di sicurezza RAS di terze parti per migliorare le funzionalità di protezione RAS predefinite.</span><span class="sxs-lookup"><span data-stu-id="f0e83-107">Windows NT 4.0 provides a way for a third-party RAS security DLL to enhance the built-in RAS security features.</span></span> <span data-ttu-id="f0e83-108">Windows 95 non fornisce questo supporto.</span><span class="sxs-lookup"><span data-stu-id="f0e83-108">Windows 95 does not provide this support.</span></span>

<span data-ttu-id="f0e83-109">Un server RAS Windows NT/Windows 2000 fornisce meccanismi di sicurezza per la convalida dell'accesso alla rete degli utenti remoti.</span><span class="sxs-lookup"><span data-stu-id="f0e83-109">A Windows NT/Windows 2000 RAS server provides security mechanisms for validating the network access of remote users.</span></span> <span data-ttu-id="f0e83-110">Quando un server RAS riceve una chiamata, convalida le credenziali dell'utente nel database di account locale o di dominio.</span><span class="sxs-lookup"><span data-stu-id="f0e83-110">When a RAS server receives a call, it validates the user's credentials against the local or domain account database.</span></span> <span data-ttu-id="f0e83-111">RAS supporta inoltre la sicurezza da richiamare, in cui il server RAS si blocca e quindi richiama l'utente remoto per stabilire la connessione.</span><span class="sxs-lookup"><span data-stu-id="f0e83-111">RAS also supports call-back security, in which the RAS server hangs up and then calls back to the remote user to establish the connection.</span></span> <span data-ttu-id="f0e83-112">Per le reti in cui questo livello di protezione non è sufficiente, è possibile installare una DLL di protezione RAS di terze parti.</span><span class="sxs-lookup"><span data-stu-id="f0e83-112">For networks in which this level of security is not enough, you can install a third-party RAS security DLL.</span></span> <span data-ttu-id="f0e83-113">La DLL di sicurezza può quindi autenticare un utente remoto leggendo le informazioni di sicurezza da un database diverso dal database degli account utente standard.</span><span class="sxs-lookup"><span data-stu-id="f0e83-113">The security DLL can then authenticate a remote user by reading security information from a database other than the standard user account database.</span></span>

<span data-ttu-id="f0e83-114">Quando il server RAS riceve una chiamata, richiama la DLL di sicurezza per autenticare l'utente remoto.</span><span class="sxs-lookup"><span data-stu-id="f0e83-114">When the RAS server receives a call, it invokes the security DLL to authenticate the remote user.</span></span> <span data-ttu-id="f0e83-115">Il supporto dell'host di sicurezza RAS fornisce un meccanismo per la comunicazione tra la DLL di sicurezza e l'utente remoto tramite una finestra del terminale nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="f0e83-115">The RAS security host support provides a mechanism for the security DLL to communicate with the remote user through a terminal window on the remote computer.</span></span> <span data-ttu-id="f0e83-116">In uno scenario tipico, la DLL di sicurezza richiede il nome di accesso dell'utente remoto.</span><span class="sxs-lookup"><span data-stu-id="f0e83-116">In a typical scenario, the security DLL asks for the logon name of the remote user.</span></span> <span data-ttu-id="f0e83-117">La DLL usa quindi il database di sicurezza privato per formulare una richiesta di invio al terminale remoto.</span><span class="sxs-lookup"><span data-stu-id="f0e83-117">The DLL then uses its private security database to formulate a challenge to send to the remote terminal.</span></span> <span data-ttu-id="f0e83-118">Ad esempio, la richiesta può essere un codice che l'utente deve fornire come input a un lettore cardkey.</span><span class="sxs-lookup"><span data-stu-id="f0e83-118">For example, the challenge could be a code that the user must provide as input to a cardkey reader.</span></span> <span data-ttu-id="f0e83-119">Il lettore cardkey Visualizza quindi una risposta che l'utente remoto digita nella finestra del terminale.</span><span class="sxs-lookup"><span data-stu-id="f0e83-119">The cardkey reader then displays a response that the remote user types in the terminal window.</span></span> <span data-ttu-id="f0e83-120">La DLL di sicurezza convalida quindi la risposta in base alle informazioni dell'utente nel database di sicurezza privata.</span><span class="sxs-lookup"><span data-stu-id="f0e83-120">The security DLL then validates the response against the user's information in the private security database.</span></span>

<span data-ttu-id="f0e83-121">Se la DLL di sicurezza autentica l'utente remoto, il server RAS esegue la propria autenticazione.</span><span class="sxs-lookup"><span data-stu-id="f0e83-121">If the security DLL authenticates the remote user, the RAS server performs its own authentication.</span></span> <span data-ttu-id="f0e83-122">In questo modo si garantisce che la sicurezza RAS esegua sempre l'autenticazione di un utente remoto, anche se è installata una DLL di sicurezza che concede l'accesso a tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="f0e83-122">This ensures that RAS security always authenticates a remote user, even if a security DLL is installed that grants access to all users.</span></span>

> [!Note]  
> <span data-ttu-id="f0e83-123">Windows NT/Windows 2000 fornisce attualmente il supporto per gli host di sicurezza RAS solo per le connessioni asincrone del modem. altri tipi di connessioni, ad esempio Ethernet (che non è una connessione modem), VPN (che non è anche una connessione modem) o ISDN (sincrono) non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="f0e83-123">Windows NT/Windows 2000 currently provides RAS security host support only for asynchronous modem connections; other types of connections such as Ethernet (which is not a modem connection), VPN (which is also not a modem connection), or ISDN (which is synchronous), are not supported.</span></span>

 

 

 




