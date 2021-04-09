---
title: Autenticazione della sicurezza del server RAS
description: Quando un server RAS Windows NT/Windows 2000 riceve una chiamata, richiama la funzione RasSecurityDialogBegin della DLL di sicurezza RAS registrata, se disponibile.
ms.assetid: dd9469ec-9bb1-4444-af5b-72e3ba8b4cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27184388b418e0fec2a1988fd9e693e942c08e03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044622"
---
# <a name="ras-server-security-authentication"></a><span data-ttu-id="aa2fb-103">Autenticazione della sicurezza del server RAS</span><span class="sxs-lookup"><span data-stu-id="aa2fb-103">RAS Server Security Authentication</span></span>

<span data-ttu-id="aa2fb-104">Quando un server RAS Windows NT/Windows 2000 riceve una chiamata, richiama la funzione [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) della DLL di sicurezza RAS registrata, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-104">When a Windows NT/Windows 2000 RAS server receives a call, it invokes the [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) function of the registered RAS security DLL, if there is one.</span></span> <span data-ttu-id="aa2fb-105">Questa chiamata notifica alla DLL di sicurezza di iniziare l'autenticazione dell'utente remoto.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-105">This call notifies the security DLL to begin its authentication of the remote user.</span></span> <span data-ttu-id="aa2fb-106">Il server RAS chiama **RasSecurityDialogBegin** prima di eseguire l'autenticazione PPP o RAS.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-106">The RAS server calls **RasSecurityDialogBegin** before performing its PPP or RAS authentication.</span></span>

<span data-ttu-id="aa2fb-107">La chiamata [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) passa le informazioni seguenti alla DLL di sicurezza:</span><span class="sxs-lookup"><span data-stu-id="aa2fb-107">The [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) call passes the following information to the security DLL:</span></span>

-   <span data-ttu-id="aa2fb-108">Handle di porta per identificare la connessione.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-108">A port handle to identify the connection.</span></span>
-   <span data-ttu-id="aa2fb-109">Puntatori ai buffer da usare durante la comunicazione con l'utente remoto.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-109">Pointers to buffers to use when communicating with the remote user.</span></span>
-   <span data-ttu-id="aa2fb-110">Puntatore a una funzione [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) da chiamare al termine dell'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-110">A pointer to a [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) function to call when the authentication has been completed.</span></span>

<span data-ttu-id="aa2fb-111">Il punto di controllo della porta e i puntatori del buffer sono validi finché la DLL di sicurezza non chiama [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) per terminare la transazione di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-111">The port handle and buffer pointers are valid until the security DLL calls [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) to terminate the authentication transaction.</span></span>

<span data-ttu-id="aa2fb-112">Il [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) notifica al server RAS i risultati dell'autenticazione della DLL di sicurezza dell'utente remoto.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-112">The [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) notifies the RAS server of the results of the security DLL's authentication of the remote user.</span></span> <span data-ttu-id="aa2fb-113">Se la DLL di sicurezza segnala l'esito positivo, il server RAS procede con l'autenticazione PPP e RAS dell'utente remoto.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-113">If the security DLL reports success, the RAS server proceeds with its PPP and RAS authentication of the remote user.</span></span> <span data-ttu-id="aa2fb-114">Se la DLL di sicurezza segnala che l'utente remoto non è riuscito a eseguire l'autenticazione o si è verificato un errore, il server RAS si blocca e registra l'errore o l'autenticazione non riuscita nel registro eventi.</span><span class="sxs-lookup"><span data-stu-id="aa2fb-114">If the security DLL reports that the remote user failed the authentication, or that an error occurred, the RAS server hangs up and logs the error or failed authentication in the event log.</span></span>

 

 




