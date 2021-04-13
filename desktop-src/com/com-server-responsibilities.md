---
title: Responsabilità server COM
description: Responsabilità server COM
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86b9d3104af80a7b2dca49dbbd5b55e66a613ee7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399772"
---
# <a name="com-server-responsibilities"></a><span data-ttu-id="43e10-103">Responsabilità server COM</span><span class="sxs-lookup"><span data-stu-id="43e10-103">COM Server Responsibilities</span></span>

<span data-ttu-id="43e10-104">Uno dei modi più importanti per ottenere un puntatore a un oggetto da parte del client è che il client chieda che un server venga avviato e che sia stata creata e attivata un'istanza dell'oggetto fornito dal server.</span><span class="sxs-lookup"><span data-stu-id="43e10-104">One of the most important ways for a client to get a pointer to an object is for the client to ask that a server be launched and that an instance of the object provided by the server be created and activated.</span></span> <span data-ttu-id="43e10-105">Il server è responsabile della verifica del corretto funzionamento.</span><span class="sxs-lookup"><span data-stu-id="43e10-105">It is the responsibility of the server to ensure that this happens properly.</span></span> <span data-ttu-id="43e10-106">A questo punto sono disponibili diverse parti importanti.</span><span class="sxs-lookup"><span data-stu-id="43e10-106">There are several important parts to this.</span></span>

<span data-ttu-id="43e10-107">Il server deve implementare il codice per un oggetto classe tramite un'implementazione dell'interfaccia [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) o [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) .</span><span class="sxs-lookup"><span data-stu-id="43e10-107">The server must implement code for a class object through an implementation of either the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) or [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) interface.</span></span>

<span data-ttu-id="43e10-108">Il server deve registrare il proprio CLSID nel registro di sistema nel computer in cui si trova e ulteriormente, può scegliere di pubblicare il percorso del computer su altri sistemi in una rete per consentire ai client di chiamarlo senza richiedere al client di conoscerne la posizione.</span><span class="sxs-lookup"><span data-stu-id="43e10-108">The server must register its CLSID in the system registry on the machine on which it resides and further, has the option of publishing its machine location to other systems on a network to allow clients to call it without requiring the client to know the server's location.</span></span>

<span data-ttu-id="43e10-109">Il server è principalmente responsabile della sicurezza. ovvero, nella maggior parte dei casi, il server determina se fornirà un puntatore a uno dei relativi oggetti a un client.</span><span class="sxs-lookup"><span data-stu-id="43e10-109">The server is primarily responsible for security; that is, for the most part, the server determines whether it will provide a pointer to one of its objects to a client.</span></span>

<span data-ttu-id="43e10-110">I server in-process devono implementare ed esportare determinate funzioni che consentono al processo client di crearne un'istanza.</span><span class="sxs-lookup"><span data-stu-id="43e10-110">In-process servers should implement and export certain functions that allow the client process to instantiate them.</span></span>

<span data-ttu-id="43e10-111">Gli argomenti seguenti illustrano in dettaglio le responsabilità del server COM:</span><span class="sxs-lookup"><span data-stu-id="43e10-111">The following topics detail the responsibilities of the COM server:</span></span>

-   [<span data-ttu-id="43e10-112">Implementazione di IClassFactory</span><span class="sxs-lookup"><span data-stu-id="43e10-112">Implementing IClassFactory</span></span>](implementing-iclassfactory.md)
-   [<span data-ttu-id="43e10-113">Licenze e IClassFactory2</span><span class="sxs-lookup"><span data-stu-id="43e10-113">Licensing and IClassFactory2</span></span>](licensing-and-iclassfactory2.md)
-   [<span data-ttu-id="43e10-114">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="43e10-114">Registering COM Servers</span></span>](registering-com-servers.md)
-   [<span data-ttu-id="43e10-115">Helper di implementazione del server out-of-process</span><span class="sxs-lookup"><span data-stu-id="43e10-115">Out-of-Process Server Implementation Helpers</span></span>](out-of-process-server-implementation-helpers.md)
-   [<span data-ttu-id="43e10-116">Creazione e ottimizzazioni di GUID</span><span class="sxs-lookup"><span data-stu-id="43e10-116">GUID Creation and Optimizations</span></span>](guid-creation-and-optimizations.md)

## <a name="related-topics"></a><span data-ttu-id="43e10-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="43e10-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43e10-118">Client e server COM</span><span class="sxs-lookup"><span data-stu-id="43e10-118">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 