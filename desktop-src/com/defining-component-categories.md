---
title: Definizione delle categorie di componenti
description: Definizione delle categorie di componenti
ms.assetid: 2d67a998-5200-4285-bd99-48cf59683569
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4609654827789949705a2f32803c154152d3f9c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104222109"
---
# <a name="defining-component-categories"></a><span data-ttu-id="efab9-103">Definizione delle categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="efab9-103">Defining Component Categories</span></span>

<span data-ttu-id="efab9-104">L'autore della definizione di una categoria di componenti crea un GUID univoco (CATId) che viene pubblicato insieme alla definizione.</span><span class="sxs-lookup"><span data-stu-id="efab9-104">The author of a component category definition creates a unique GUID (the CATID) that is published along with the definition.</span></span> <span data-ttu-id="efab9-105">Altre parti conoscono la definizione di questo tipo e possono utilizzare di conseguenza le classi supportate.</span><span class="sxs-lookup"><span data-stu-id="efab9-105">Other parties know the definition of this type and can make use of its supported classes accordingly.</span></span> <span data-ttu-id="efab9-106">Analogamente alla firma del metodo di un'interfaccia, la semantica di una categoria non deve essere modificata dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="efab9-106">Like the method signature of an interface, a category's semantics should not be modified after being installed.</span></span> <span data-ttu-id="efab9-107">È preferibile mantenere la compatibilità con le versioni precedenti della categoria introducendo un nuovo identificatore di categoria con la semantica modificata.</span><span class="sxs-lookup"><span data-stu-id="efab9-107">It is better to maintain backward compatibility of the category by introducing a new category identifier with revised semantics.</span></span>

<span data-ttu-id="efab9-108">Poiché gli identificatori di interfaccia (IID) e gli identificatori di categoria di componenti (CATId) si trovano in spazi dei nomi diversi, sembra che sia possibile usare lo stesso GUID sia per un IID che per un CATId.</span><span class="sxs-lookup"><span data-stu-id="efab9-108">Because interface identifiers (IID) and component category identifiers (CATID) exist in different namespaces, it seems as if it would be possible to use the same GUID for both an IID and a CATID.</span></span> <span data-ttu-id="efab9-109">Tuttavia, poiché IID vengono spesso utilizzati per il CLSID del server proxy/stub dell'interfaccia, è possibile che si verifichi un conflitto.</span><span class="sxs-lookup"><span data-stu-id="efab9-109">However, since IIDs are often used for the CLSID of the interface's proxy/stub server, there is the potential for conflict.</span></span> <span data-ttu-id="efab9-110">Pertanto, non utilizzare lo stesso GUID per un IID e un CATId.</span><span class="sxs-lookup"><span data-stu-id="efab9-110">Therefore, do not use the same GUID for an IID and CATID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="efab9-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="efab9-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efab9-112">Associazione di icone a una categoria</span><span class="sxs-lookup"><span data-stu-id="efab9-112">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="efab9-113">Categorizzazione in base alle funzionalità del componente</span><span class="sxs-lookup"><span data-stu-id="efab9-113">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="efab9-114">Categorizzazione in base alle funzionalità del contenitore</span><span class="sxs-lookup"><span data-stu-id="efab9-114">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="efab9-115">Classi e associazioni predefinite</span><span class="sxs-lookup"><span data-stu-id="efab9-115">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="efab9-116">Gestione categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="efab9-116">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




