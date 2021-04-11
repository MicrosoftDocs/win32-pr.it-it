---
title: Moniker
description: Un moniker in COM non è solo un modo per identificare un oggetto \ 8212; anche un moniker viene implementato come un oggetto.
ms.assetid: ae0cd2f3-8ac0-4388-8781-e86fc4a26b3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf148d63611b5252eec9f5f5f69eacbcece8c65f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044147"
---
# <a name="monikers"></a><span data-ttu-id="3875b-103">Moniker</span><span class="sxs-lookup"><span data-stu-id="3875b-103">Monikers</span></span>

<span data-ttu-id="3875b-104">Un moniker in COM non è solo un modo per identificare un oggetto; un moniker viene inoltre implementato come un oggetto.</span><span class="sxs-lookup"><span data-stu-id="3875b-104">A moniker in COM is not only a way to identify an object—a moniker is also implemented as an object.</span></span> <span data-ttu-id="3875b-105">Questo oggetto fornisce servizi che consentono a un componente di ottenere un puntatore all'oggetto identificato dal moniker.</span><span class="sxs-lookup"><span data-stu-id="3875b-105">This object provides services allowing a component to obtain a pointer to the object identified by the moniker.</span></span> <span data-ttu-id="3875b-106">Questo processo è denominato *Binding*.</span><span class="sxs-lookup"><span data-stu-id="3875b-106">This process is referred to as *binding*.</span></span>

<span data-ttu-id="3875b-107">I moniker sono oggetti che implementano l'interfaccia [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) e vengono in genere implementati nelle DLL come oggetti componente.</span><span class="sxs-lookup"><span data-stu-id="3875b-107">Monikers are objects that implement the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface and are generally implemented in DLLs as component objects.</span></span> <span data-ttu-id="3875b-108">Esistono due modi per visualizzare l'uso dei moniker: come client moniker, un componente che usa un moniker per ottenere un puntatore a un altro oggetto; e come provider di moniker, un componente che fornisce moniker che identificano i relativi oggetti ai client moniker.</span><span class="sxs-lookup"><span data-stu-id="3875b-108">There are two ways of viewing the use of monikers: as a moniker client, a component that uses a moniker to get a pointer to another object; and as a moniker provider, a component that supplies monikers identifying its objects to moniker clients.</span></span>

<span data-ttu-id="3875b-109">OLE utilizza i moniker per connettersi e attivare gli oggetti, sia che si trovino nello stesso computer o in una rete.</span><span class="sxs-lookup"><span data-stu-id="3875b-109">OLE uses monikers to connect to and activate objects, whether they are in the same machine or across a network.</span></span> <span data-ttu-id="3875b-110">Un uso molto importante riguarda le connessioni di rete.</span><span class="sxs-lookup"><span data-stu-id="3875b-110">A very important use is for network connections.</span></span> <span data-ttu-id="3875b-111">Vengono usati anche per identificare, connettersi ed eseguire oggetti di collegamento al documento composito OLE.</span><span class="sxs-lookup"><span data-stu-id="3875b-111">They are also used to identify, connect to, and run OLE compound document link objects.</span></span> <span data-ttu-id="3875b-112">In questo caso, l'origine del collegamento funge da provider del moniker e il contenitore che contiene l'oggetto collegamento funge da client del moniker.</span><span class="sxs-lookup"><span data-stu-id="3875b-112">In this case, the link source acts as the moniker provider and the container holding the link object acts as the moniker client.</span></span>

<span data-ttu-id="3875b-113">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="3875b-113">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="3875b-114">Client moniker</span><span class="sxs-lookup"><span data-stu-id="3875b-114">Moniker Clients</span></span>](moniker-clients.md)
-   [<span data-ttu-id="3875b-115">Provider moniker</span><span class="sxs-lookup"><span data-stu-id="3875b-115">Moniker Providers</span></span>](moniker-providers.md)
-   [<span data-ttu-id="3875b-116">Implementazioni del moniker OLE</span><span class="sxs-lookup"><span data-stu-id="3875b-116">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)

## <a name="related-topics"></a><span data-ttu-id="3875b-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3875b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3875b-118">Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="3875b-118">The Component Object Model</span></span>](the-component-object-model.md)
</dt> </dl>

 

 




