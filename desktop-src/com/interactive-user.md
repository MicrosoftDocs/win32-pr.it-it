---
title: Utente interattivo
description: L'utente interattivo è l'utente attualmente connesso al computer in cui è in esecuzione il server COM.
ms.assetid: 6d43842c-0ad1-4563-b50c-5024bda480f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7fc8aeb5fd9674c09b40f6c46e4e173f5965a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339319"
---
# <a name="interactive-user"></a><span data-ttu-id="cdf2b-103">Utente interattivo</span><span class="sxs-lookup"><span data-stu-id="cdf2b-103">Interactive User</span></span>

<span data-ttu-id="cdf2b-104">L' *utente interattivo* è l'utente attualmente connesso al computer in cui è in esecuzione il server com.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-104">The *interactive user* is the user that is currently logged on to the computer where the COM server is running.</span></span> <span data-ttu-id="cdf2b-105">Se l'identità è impostata come utente interattivo, tutti i client utilizzeranno la stessa istanza del server se il server ne registrerà il class factory come multiutilizzo.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-105">If the identity is set to be the interactive user, all clients use the same instance of the server if the server registers its class factory as multi-use.</span></span> <span data-ttu-id="cdf2b-106">Se nessun utente è connesso, il server non verrà eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-106">If no user is logged on, the server will not run.</span></span> <span data-ttu-id="cdf2b-107">Se il server dispone di un'interfaccia utente grafica (GUI) che il client deve visualizzare, è necessario usare l'utente interattivo per l'identità del server.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-107">If the server has a graphical user interface (GUI) that the client needs to see, you should use interactive user for the server's identity.</span></span> <span data-ttu-id="cdf2b-108">Tuttavia, la scelta di questa identità comporta alcuni rischi per la sicurezza perché il server viene eseguito con l'identità dell'utente che ha effettuato l'accesso senza la conoscenza o il consenso dell'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-108">However, choosing this identity carries some security risks because the server runs under the identity of the logged on user without the logged on user's knowledge or consent.</span></span> <span data-ttu-id="cdf2b-109">Inoltre, un'applicazione di servizio non è in grado di visualizzare un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-109">In addition, a service application cannot display a user interface.</span></span> <span data-ttu-id="cdf2b-110">Per ulteriori informazioni, vedere [servizi interattivi](/windows/desktop/Services/interactive-services).</span><span class="sxs-lookup"><span data-stu-id="cdf2b-110">For more information, see [Interactive Services](/windows/desktop/Services/interactive-services).</span></span>

<span data-ttu-id="cdf2b-111">Se un server COM è configurato per l'esecuzione come utente interattivo, in un ambiente di Servizi terminal, il server verrà avviato nella sessione interattiva corrispondente all'identità utente del client.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-111">If a COM server is configured to run as the interactive user, in a terminal services environment, the server will be launched in the interactive session that matches the client's user identity.</span></span> <span data-ttu-id="cdf2b-112">Tuttavia, l'applicazione client può utilizzare il moniker della sessione per fare riferimento a un oggetto fornito dal server in una sessione che non corrisponde all'identità del client.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-112">However, the client application can use the session moniker to reference an object provided by the server in a session that does not match the client identity.</span></span> <span data-ttu-id="cdf2b-113">Quando si utilizza questo, l'applicazione client può specificare qualsiasi sessione, nel qual caso il server verrà eseguito con l'utente proprietario della sessione e non con l'utente di avvio.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-113">When this is used, the client application can specify any session, in which case the server will run as the user who owns the session, not the launching user.</span></span> <span data-ttu-id="cdf2b-114">Le autorizzazioni di accesso predefinite in questo scenario non consentono all'utente di avviare di chiamare i metodi sul server.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-114">The default access permissions in this scenario would not allow the launching user to call methods on the server.</span></span> <span data-ttu-id="cdf2b-115">Tuttavia, vengono mantenuti i rischi di sicurezza seguenti:</span><span class="sxs-lookup"><span data-stu-id="cdf2b-115">However, the following security risks remain:</span></span>

-   <span data-ttu-id="cdf2b-116">Se il server COM espone interfacce che non sono controllate da COM, ad esempio porte TCP, named pipe, porte LPC, sezioni Shared Memory e così via, possono essere usate dall'utente che ha avviato l'avvio per influenzare il server.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-116">If the COM server exposes interfaces that are not controlled by COM, such as TCP ports, named pipes, LPC ports, shared memory sections, and so on, these could be used by the launching user to influence the server.</span></span> <span data-ttu-id="cdf2b-117">Gli oggetti COM configurati per l'esecuzione come utente interattivo dovrebbero ridurre al massimo la superficie di attacco.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-117">COM objects configured to run as the interactive user should reduce this attack surface as much as possible.</span></span>
-   <span data-ttu-id="cdf2b-118">Gli oggetti COM sono gratuiti per impostare le proprie autorizzazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-118">COM objects are free to set their own access permissions.</span></span> <span data-ttu-id="cdf2b-119">Se l'oggetto imposta le autorizzazioni di accesso, nella registrazione AppID o chiamando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), per consentire all'utente di avviare l'accesso, l'utente può avviare il server per l'esecuzione con un altro utente, quindi accedere all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-119">If the object sets access permissions, either in its AppID registration or by calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), to allow the launching user access, the user would be able to launch the server to run as another user, then access the object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdf2b-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cdf2b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdf2b-121">Identità applicazione</span><span class="sxs-lookup"><span data-stu-id="cdf2b-121">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="cdf2b-122">Avvio dell'utente</span><span class="sxs-lookup"><span data-stu-id="cdf2b-122">Launching User</span></span>](launching-user.md)
</dt> <dt>

[<span data-ttu-id="cdf2b-123">Identità del servizio</span><span class="sxs-lookup"><span data-stu-id="cdf2b-123">Service Identity</span></span>](service-identity.md)
</dt> <dt>

[<span data-ttu-id="cdf2b-124">Utente specificato</span><span class="sxs-lookup"><span data-stu-id="cdf2b-124">Specified User</span></span>](specified-user.md)
</dt> </dl>

 

 