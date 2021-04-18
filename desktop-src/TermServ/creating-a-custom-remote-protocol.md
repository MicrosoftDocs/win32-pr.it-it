---
title: Creazione di un provider di Remote Desktop Protocol
description: Informazioni sulla creazione di un provider di Remote Desktop Protocol. Gestione protocolli viene implementato come server COM e registrato in un percorso in cui viene eseguita la ricerca all'avvio del servizio Servizi Desktop remoto.
ms.assetid: 9a3e6d5c-464f-4227-a06f-16eb8ed1079e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41265a350b4d5c559731a09abc21aa4c81b9b29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297632"
---
# <a name="creating-a-remote-desktop-protocol-provider"></a><span data-ttu-id="ae713-104">Creazione di un provider di Remote Desktop Protocol</span><span class="sxs-lookup"><span data-stu-id="ae713-104">Creating a Remote Desktop Protocol Provider</span></span>

<span data-ttu-id="ae713-105">Le sezioni seguenti contengono informazioni sulla creazione di un provider di Remote Desktop Protocol.</span><span class="sxs-lookup"><span data-stu-id="ae713-105">The following sections contain information about creating a Remote Desktop Protocol Provider.</span></span> <span data-ttu-id="ae713-106">Gestione protocolli viene implementato come server COM e registrato in un percorso in cui viene eseguita la ricerca all'avvio del servizio Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="ae713-106">The protocol manager is implemented as a COM server and registered in a location searched when the Remote Desktop Services service starts.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ae713-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="ae713-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="ae713-108">Registrazione di gestione protocolli</span><span class="sxs-lookup"><span data-stu-id="ae713-108">Registering the Protocol Manager</span></span>](registering-the-custom-protocol.md)
</dt> <dd>

<span data-ttu-id="ae713-109">È necessario creare almeno una voce del valore del registro di sistema per gestione protocolli, in modo che il servizio Servizi Desktop remoto possa crearne un'istanza.</span><span class="sxs-lookup"><span data-stu-id="ae713-109">You must create at least one registry value entry for your protocol manager so that the Remote Desktop Services service can instantiate it.</span></span>

</dd> <dt>

[<span data-ttu-id="ae713-110">Sequenza di chiamate al metodo</span><span class="sxs-lookup"><span data-stu-id="ae713-110">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dd>

<span data-ttu-id="ae713-111">Il servizio Servizi Desktop remoto e il provider di protocollo si chiamano reciprocamente in sequenze chiaramente definite.</span><span class="sxs-lookup"><span data-stu-id="ae713-111">The Remote Desktop Services service and your protocol provider call each other in clearly defined sequences.</span></span>

</dd> </dl>

-   [<span data-ttu-id="ae713-112">Registrazione di gestione protocolli</span><span class="sxs-lookup"><span data-stu-id="ae713-112">Registering the Protocol Manager</span></span>](registering-the-custom-protocol.md)
-   [<span data-ttu-id="ae713-113">Sequenza di chiamate al metodo</span><span class="sxs-lookup"><span data-stu-id="ae713-113">Method Call Sequence</span></span>](method-call-sequence.md)

## <a name="related-topics"></a><span data-ttu-id="ae713-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ae713-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae713-115">API del provider Remote Desktop Protocol</span><span class="sxs-lookup"><span data-stu-id="ae713-115">Remote Desktop Protocol Provider API</span></span>](custom-remote-desktop-protocols.md)
</dt> <dt>

[<span data-ttu-id="ae713-116">Utilizzo di Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="ae713-116">Using Remote Desktop Services</span></span>](using-terminal-services.md)
</dt> </dl>

 

 




