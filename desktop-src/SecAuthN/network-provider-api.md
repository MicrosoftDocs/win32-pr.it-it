---
description: Un provider di rete è una DLL che consente al sistema operativo Windows di interagire con altri tipi di reti, ad esempio Novell. Si tratta di un client del driver WNet di Windows.
ms.assetid: d316f159-4fe3-4b78-9efc-177906875918
title: API provider di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc68184f60639a603614cbaf71631a2521012cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315864"
---
# <a name="network-provider-api"></a><span data-ttu-id="d14b3-104">API provider di rete</span><span class="sxs-lookup"><span data-stu-id="d14b3-104">Network Provider API</span></span>

<span data-ttu-id="d14b3-105">Un provider di rete è una DLL che consente al sistema operativo Windows di interagire con altri tipi di reti, ad esempio Novell.</span><span class="sxs-lookup"><span data-stu-id="d14b3-105">A network provider is a DLL that enables the Windows operating system to interact with other kinds of networks, such as Novell.</span></span> <span data-ttu-id="d14b3-106">Si tratta di un client del driver WNet di Windows.</span><span class="sxs-lookup"><span data-stu-id="d14b3-106">It is a client of the Windows WNet driver.</span></span> <span data-ttu-id="d14b3-107">Un provider di rete implementa azioni specifiche della rete, ad esempio la creazione di una connessione, ed espone un'interfaccia comune a Windows.</span><span class="sxs-lookup"><span data-stu-id="d14b3-107">A network provider implements network-specific actions, such as making a connection, and exposes a common interface to Windows.</span></span> <span data-ttu-id="d14b3-108">Questa interfaccia è chiamata API del provider di rete ed è costituita da funzioni implementate dal provider di rete.</span><span class="sxs-lookup"><span data-stu-id="d14b3-108">This interface is called the Network Provider API and consists of functions implemented by the network provider.</span></span> <span data-ttu-id="d14b3-109">È possibile creare una DLL del provider di rete per supportare nuovi protocolli di rete.</span><span class="sxs-lookup"><span data-stu-id="d14b3-109">You can create a network provider DLL to support new network protocols.</span></span>

<span data-ttu-id="d14b3-110">Poiché ogni rete espone un'interfaccia comune tramite il provider, Windows può interagire con diversi tipi di reti senza conoscere i dettagli di implementazione specifici della rete.</span><span class="sxs-lookup"><span data-stu-id="d14b3-110">Because each network exposes a common interface through its provider, Windows can interact with several types of networks without knowing their network-specific implementation details.</span></span>

<span data-ttu-id="d14b3-111">Il [*router multi-provider*](../secgloss/m-gly.md) (MPR) gestisce la comunicazione con tutti i diversi provider di rete del sistema e presenta una rete integrata all'utente.</span><span class="sxs-lookup"><span data-stu-id="d14b3-111">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) handles communication with all of the various network providers on the system and presents an integrated network to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d14b3-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d14b3-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d14b3-113">Provider di rete</span><span class="sxs-lookup"><span data-stu-id="d14b3-113">Network Providers</span></span>](network-providers.md)
</dt> <dt>

[<span data-ttu-id="d14b3-114">Gestione credenziali</span><span class="sxs-lookup"><span data-stu-id="d14b3-114">Credential Manager</span></span>](credential-manager.md)
</dt> <dt>

[<span data-ttu-id="d14b3-115">Router per più provider</span><span class="sxs-lookup"><span data-stu-id="d14b3-115">Multiple Provider Router</span></span>](multiple-provider-router.md)
</dt> <dt>

[<span data-ttu-id="d14b3-116">Funzioni implementate dai provider di rete</span><span class="sxs-lookup"><span data-stu-id="d14b3-116">Functions Implemented by Network Providers</span></span>](functions-implemented-by-network-providers.md)
</dt> <dt>

[<span data-ttu-id="d14b3-117">API di gestione delle credenziali</span><span class="sxs-lookup"><span data-stu-id="d14b3-117">Credential Management API</span></span>](credential-management-api.md)
</dt> <dt>

[<span data-ttu-id="d14b3-118">API di notifica della connessione</span><span class="sxs-lookup"><span data-stu-id="d14b3-118">Connection Notification API</span></span>](connection-notification-api.md)
</dt> </dl>

 

 
