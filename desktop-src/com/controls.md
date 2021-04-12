---
title: Controlli (COM)
description: Controlli
ms.assetid: 73947c81-6727-4112-9da0-efa60360f458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f440fff8f855f70c1a5ab3df78a6f6f6ed365ea
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104339993"
---
# <a name="controls-com"></a><span data-ttu-id="f1c6d-103">Controlli (COM)</span><span class="sxs-lookup"><span data-stu-id="f1c6d-103">Controls (COM)</span></span>

<span data-ttu-id="f1c6d-104">Un controllo ActiveX è in realtà un altro termine per l'oggetto OLE o più specificamente un oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="f1c6d-104">An ActiveX control is really just another term for OLE object or more specifically, COM object.</span></span> <span data-ttu-id="f1c6d-105">In altre parole, un controllo, almeno, è un oggetto COM che supporta l'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) ed è anche autoregistrato.</span><span class="sxs-lookup"><span data-stu-id="f1c6d-105">In other words, a control, at the very least, is some COM object that supports the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface and is also self-registering.</span></span> <span data-ttu-id="f1c6d-106">Tramite [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) un contenitore può gestire la durata del controllo e individuare in modo dinamico l'entità completa della funzionalità di un controllo in base alle interfacce disponibili.</span><span class="sxs-lookup"><span data-stu-id="f1c6d-106">Through [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) a container can manage the lifetime of the control as well as dynamically discover the full extent of a control's functionality based on the available interfaces.</span></span> <span data-ttu-id="f1c6d-107">Questo consente a un controllo di implementare il minor numero di funzionalità necessario, anziché supportare un numero elevato di interfacce che in realtà non eseguono alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="f1c6d-107">This allows a control to implement as little functionality as it needs to, instead of supporting a large number of interfaces that actually don't do anything.</span></span> <span data-ttu-id="f1c6d-108">In breve, questo requisito minimo per nient'altro che **IUnknown** consente a qualsiasi controllo di essere il più leggero possibile.</span><span class="sxs-lookup"><span data-stu-id="f1c6d-108">In short, this minimal requirement for nothing more than **IUnknown** allows any control to be as lightweight as it can.</span></span>

<span data-ttu-id="f1c6d-109">In breve, oltre a [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) e registrazione automatica, non sono previsti altri requisiti per un controllo.</span><span class="sxs-lookup"><span data-stu-id="f1c6d-109">In short, other than [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and self-registration, there are no other requirements for a control.</span></span> <span data-ttu-id="f1c6d-110">Esistono, tuttavia, le convenzioni che devono essere seguite per quanto riguarda il supporto di un'interfaccia in termini di funzionalità fornite al contenitore dal controllo.</span><span class="sxs-lookup"><span data-stu-id="f1c6d-110">There are, however, conventions that should be followed about what the support of an interface means in terms of functionality provided to the container by the control.</span></span> <span data-ttu-id="f1c6d-111">Questa sezione descrive quindi il significato di un controllo per supportare effettivamente un'interfaccia, oltre a metodi, proprietà ed eventi che un controllo deve fornire come linea di base se ha l'opportunità di supportare metodi, proprietà ed eventi.</span><span class="sxs-lookup"><span data-stu-id="f1c6d-111">This section then describes what it means for a control to actually support an interface, as well as methods, properties, and events that a control should provide as a baseline if it has occasion to support methods, properties, and events.</span></span>

<span data-ttu-id="f1c6d-112">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="f1c6d-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="f1c6d-113">Registrazione automatica per i controlli</span><span class="sxs-lookup"><span data-stu-id="f1c6d-113">Self Registration for Controls</span></span>](self-registration-for-controls.md)
-   [<span data-ttu-id="f1c6d-114">Quale supporto per un'interfaccia significa</span><span class="sxs-lookup"><span data-stu-id="f1c6d-114">What Support for an Interface Means</span></span>](what-support-for-an-interface-means.md)
-   [<span data-ttu-id="f1c6d-115">Interfacce di persistenza</span><span class="sxs-lookup"><span data-stu-id="f1c6d-115">Persistence Interfaces</span></span>](persistence-interfaces.md)
-   [<span data-ttu-id="f1c6d-116">Metodi facoltativi nelle interfacce di controllo</span><span class="sxs-lookup"><span data-stu-id="f1c6d-116">Optional Methods in Control Interfaces</span></span>](optional-methods-in-control-interfaces.md)
-   [<span data-ttu-id="f1c6d-117">Opzioni di class factory</span><span class="sxs-lookup"><span data-stu-id="f1c6d-117">Class Factory Options</span></span>](class-factory-options.md)
-   [<span data-ttu-id="f1c6d-118">Esposizione di proprietà tramite IDispatch</span><span class="sxs-lookup"><span data-stu-id="f1c6d-118">Exposing Properties through IDispatch</span></span>](properties.md)
-   [<span data-ttu-id="f1c6d-119">Esposizione di metodi tramite IDispatch</span><span class="sxs-lookup"><span data-stu-id="f1c6d-119">Exposing Methods through IDispatch</span></span>](exposing-methods-through-idispatch.md)
-   [<span data-ttu-id="f1c6d-120">Eventi nei controlli</span><span class="sxs-lookup"><span data-stu-id="f1c6d-120">Events in Controls</span></span>](events-in-controls.md)
-   [<span data-ttu-id="f1c6d-121">Pagine delle proprietà</span><span class="sxs-lookup"><span data-stu-id="f1c6d-121">Property Pages</span></span>](property-pages.md)
-   [<span data-ttu-id="f1c6d-122">Proprietà di ambiente per i controlli</span><span class="sxs-lookup"><span data-stu-id="f1c6d-122">Ambient Properties for Controls</span></span>](ambient-properties-for-controls.md)
-   [<span data-ttu-id="f1c6d-123">Uso della funzionalità del contenitore</span><span class="sxs-lookup"><span data-stu-id="f1c6d-123">Using the Container's Functionality</span></span>](using-the-container-s-functionality.md)

## <a name="related-topics"></a><span data-ttu-id="f1c6d-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1c6d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1c6d-125">Linee guida per il controllo ActiveX e il controllo del contenitore</span><span class="sxs-lookup"><span data-stu-id="f1c6d-125">ActiveX Control and Control Container Guidelines</span></span>](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




