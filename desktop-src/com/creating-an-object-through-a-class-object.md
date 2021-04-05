---
title: Creazione di un oggetto tramite un oggetto classe
description: Creazione di un oggetto tramite un oggetto classe
ms.assetid: cecf21b0-e509-425f-8dd6-ca6b1ac04f5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38787e7bc32151446cda6ff0a4cfe3f23a0f6eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955821"
---
# <a name="creating-an-object-through-a-class-object"></a><span data-ttu-id="03286-103">Creazione di un oggetto tramite un oggetto classe</span><span class="sxs-lookup"><span data-stu-id="03286-103">Creating an Object Through a Class Object</span></span>

<span data-ttu-id="03286-104">Con la crescente importanza delle reti informatiche, è necessario che i client e i server interagiscano in modo semplice ed efficiente, indipendentemente dal fatto che si trovino nello stesso computer o in una rete.</span><span class="sxs-lookup"><span data-stu-id="03286-104">With the increasing importance of computer networks, it has become necessary for clients and servers to interact easily and efficiently, whether they reside on the same machine or across a network.</span></span> <span data-ttu-id="03286-105">Fondamentale per questo è la capacità di un client di avviare un server, creare un'istanza dell'oggetto del server e accedere ai metodi delle interfacce sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="03286-105">Crucial to this is a client's ability to launch a server, create an instance of the server's object, and have access to the methods of the interfaces on the object.</span></span>

<span data-ttu-id="03286-106">COM fornisce estensioni a questo processo COM di base che lo rendono virtualmente trasparente in una rete.</span><span class="sxs-lookup"><span data-stu-id="03286-106">COM provides extensions to this basic COM process that make it virtually seamless across a network.</span></span> <span data-ttu-id="03286-107">Se un client è in grado di identificare il server tramite il relativo CLSID, chiamando alcune funzioni semplici si consente a COM di eseguire tutte le operazioni di individuazione e avvio del server e di attivazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="03286-107">If a client is able to identify the server through its CLSID, calling a few simple functions permit COM to do all the work of locating and launching the server and activating the object.</span></span> <span data-ttu-id="03286-108">Le sottochiavi nel registro di sistema consentono ai server remoti di registrare il proprio percorso, in modo che il client non richieda tali informazioni.</span><span class="sxs-lookup"><span data-stu-id="03286-108">Subkeys in the registry allow remote servers to register their location, so the client does not require that information.</span></span> <span data-ttu-id="03286-109">Per le applicazioni che desiderano sfruttare le funzionalità di rete, le funzioni di creazione di oggetti COM consentono una maggiore flessibilità ed efficienza.</span><span class="sxs-lookup"><span data-stu-id="03286-109">For applications that want to take advantage of networking features, the COM object creation functions allow more flexibility and efficiency.</span></span>

<span data-ttu-id="03286-110">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="03286-110">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="03286-111">Oggetti classe COM e CLSID</span><span class="sxs-lookup"><span data-stu-id="03286-111">COM Class Objects and CLSIDs</span></span>](com-class-objects-and-clsids.md)
-   [<span data-ttu-id="03286-112">Individuazione di un oggetto remoto</span><span class="sxs-lookup"><span data-stu-id="03286-112">Locating a Remote Object</span></span>](locating-a-remote-object.md)
-   [<span data-ttu-id="03286-113">Funzioni di supporto per la creazione di istanze</span><span class="sxs-lookup"><span data-stu-id="03286-113">Instance Creation Helper Functions</span></span>](instance-creation-helper-functions.md)

## <a name="related-topics"></a><span data-ttu-id="03286-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03286-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03286-115">Client e server COM</span><span class="sxs-lookup"><span data-stu-id="03286-115">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




