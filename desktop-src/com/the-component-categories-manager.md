---
title: Gestione categorie di componenti
description: Gestione categorie di componenti
ms.assetid: bd43ef98-2299-4c8a-9f35-bf9aceb074ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdf301e1b344bbc2403fd656dd90447ccffc357
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471219"
---
# <a name="the-component-categories-manager"></a><span data-ttu-id="eccc9-103">Gestione categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="eccc9-103">The Component Categories Manager</span></span>

<span data-ttu-id="eccc9-104">Per facilitare la gestione delle categorie di componenti e garantire la coerenza del registro di sistema, il sistema fornisce il componente Gestione categorie di componenti, un oggetto COM con CLSID \_ StdComponentCategoriesMgr.</span><span class="sxs-lookup"><span data-stu-id="eccc9-104">To facilitate the handling of component categories and to guarantee consistency of the registry, the system provides the Component Categories Manager, a COM object with a CLSID of CLSID\_StdComponentCategoriesMgr.</span></span> <span data-ttu-id="eccc9-105">Questo oggetto COM fornisce le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="eccc9-105">This COM object provides the following interfaces:</span></span>

-   [<span data-ttu-id="eccc9-106">**ICatInformation**</span><span class="sxs-lookup"><span data-stu-id="eccc9-106">**ICatInformation**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
-   [<span data-ttu-id="eccc9-107">**ICatRegister**</span><span class="sxs-lookup"><span data-stu-id="eccc9-107">**ICatRegister**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatregister)

<span data-ttu-id="eccc9-108">[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) fornisce metodi per ottenere informazioni sulle categorie implementate o richieste da una determinata classe e fornisce informazioni sulle categorie registrate in un determinato computer.</span><span class="sxs-lookup"><span data-stu-id="eccc9-108">[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) provides methods for obtaining information about the categories implemented or required by a certain class and provides information about the categories registered on a given machine.</span></span>

<span data-ttu-id="eccc9-109">[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) fornisce metodi per la registrazione e l'annullamento della registrazione delle informazioni sulle categorie di componenti nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="eccc9-109">[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) provides methods for registering and unregistering component category information in the registry.</span></span> <span data-ttu-id="eccc9-110">Sono inclusi i nomi leggibili delle categorie e le categorie implementate o richieste da un determinato componente o classe.</span><span class="sxs-lookup"><span data-stu-id="eccc9-110">This includes both the human-readable names of categories and the categories implemented or required by a given component or class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eccc9-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eccc9-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eccc9-112">Associazione di icone a una categoria</span><span class="sxs-lookup"><span data-stu-id="eccc9-112">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="eccc9-113">Categorizzazione in base alle funzionalità del componente</span><span class="sxs-lookup"><span data-stu-id="eccc9-113">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="eccc9-114">Categorizzazione in base alle funzionalità del contenitore</span><span class="sxs-lookup"><span data-stu-id="eccc9-114">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="eccc9-115">Classi e associazioni predefinite</span><span class="sxs-lookup"><span data-stu-id="eccc9-115">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="eccc9-116">Definizione delle categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="eccc9-116">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> </dl>

 

 




