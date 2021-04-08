---
title: Inerzia
description: Questa sezione illustra l'inerzia per Windows Touch.
ms.assetid: c33dda89-c715-4da0-a7af-aa0010dfd88b
keywords:
- Windows Touch, inerzia
- inerzia, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b69ad31ec4a61f8723c9e52f87883dc4af3772
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044199"
---
# <a name="inertia"></a><span data-ttu-id="ceaa7-105">Inerzia</span><span class="sxs-lookup"><span data-stu-id="ceaa7-105">Inertia</span></span>

<span data-ttu-id="ceaa7-106">Questa sezione illustra l'inerzia per Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="ceaa7-106">This section explains inertia for Windows Touch.</span></span>

<span data-ttu-id="ceaa7-107">L'API di inerzia inclusa in Windows 7 consente un comportamento coerente degli oggetti nelle applicazioni Windows Touch fornendo un semplice modello di fisica.</span><span class="sxs-lookup"><span data-stu-id="ceaa7-107">The inertia API included in Windows 7 enables consistent object behavior in Windows Touch applications by providing a simple physics model.</span></span> <span data-ttu-id="ceaa7-108">L'inerzia è abilitata usando il processore di inerzia, una classe che incapsula la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ceaa7-108">Inertia is enabled by using the inertia processor, a class that encapsulates functionality.</span></span> <span data-ttu-id="ceaa7-109">Il processore di inerzia funziona elaborando gli eventi che vengono passati al termine delle manipolazioni degli oggetti e gestendo le traiettorie degli oggetti in modo coerente con altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ceaa7-109">The inertia processor works by processing events that are passed to it when object manipulations finish and by handling object trajectories in a way that is consistent with other applications.</span></span> <span data-ttu-id="ceaa7-110">Si noti che il processore di inerzia è strettamente associato al processore di manipolazione per semplificare l'aggiunta del supporto dell'inerzia alle applicazioni che usano le manipolazioni.</span><span class="sxs-lookup"><span data-stu-id="ceaa7-110">Note that the inertia processor is tightly coupled to the manipulation processor to simplify adding inertia support to applications that use manipulations.</span></span> <span data-ttu-id="ceaa7-111">Infatti, il processore di inerzia genera gli stessi eventi che il processore di manipolazione esegue.</span><span class="sxs-lookup"><span data-stu-id="ceaa7-111">In fact, the inertia processor raises the same events that the manipulation processor does.</span></span> <span data-ttu-id="ceaa7-112">La sezione seguente illustra come iniziare a usare l'inerzia.</span><span class="sxs-lookup"><span data-stu-id="ceaa7-112">The following section explains how to get started with inertia.</span></span>



| <span data-ttu-id="ceaa7-113">Sezione</span><span class="sxs-lookup"><span data-stu-id="ceaa7-113">Section</span></span>                                                                      | <span data-ttu-id="ceaa7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ceaa7-114">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ceaa7-115">Meccanismi di inerzia</span><span class="sxs-lookup"><span data-stu-id="ceaa7-115">Inertia Mechanics</span></span>](inertia-mechanics.md)                                   | <span data-ttu-id="ceaa7-116">Illustra le nozioni di base sui calcoli di inerzia.</span><span class="sxs-lookup"><span data-stu-id="ceaa7-116">Explains the basics of inertia calculations.</span></span>                                                                             |
| [<span data-ttu-id="ceaa7-117">Gestione dell'inerzia nel codice non gestito</span><span class="sxs-lookup"><span data-stu-id="ceaa7-117">Handling Inertia in Unmanaged Code</span></span>](handling-inertia-in-unmanaged-code.md) | <span data-ttu-id="ceaa7-118">Viene illustrato come utilizzare l'interfaccia [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) per la gestione dell'inerzia nel codice non gestito.</span><span class="sxs-lookup"><span data-stu-id="ceaa7-118">Explains how to use the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface for handling inertia in unmanaged code.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ceaa7-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ceaa7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ceaa7-120">Modifiche e inerzia</span><span class="sxs-lookup"><span data-stu-id="ceaa7-120">Manipulations and Inertia</span></span>](manipulation-and-inertia.md)
</dt> </dl>

 

 




