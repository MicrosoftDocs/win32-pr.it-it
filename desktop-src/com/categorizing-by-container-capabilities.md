---
title: Categorizzazione in base alle funzionalità del contenitore
description: I componenti richiedono spesso determinate funzionalità dal contenitore e non funzionano con un contenitore che non fornisce il supporto.
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987546c20ff77a40666bb74689466a15fab989a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045282"
---
# <a name="categorizing-by-container-capabilities"></a><span data-ttu-id="81c94-103">Categorizzazione in base alle funzionalità del contenitore</span><span class="sxs-lookup"><span data-stu-id="81c94-103">Categorizing by Container Capabilities</span></span>

<span data-ttu-id="81c94-104">I componenti richiedono spesso determinate funzionalità dal contenitore e non funzionano con un contenitore che non fornisce il supporto.</span><span class="sxs-lookup"><span data-stu-id="81c94-104">Components often require certain functionality from the container and will not work with a container that does not provide the support.</span></span> <span data-ttu-id="81c94-105">L'interfaccia utente deve filtrare i componenti che richiedono funzionalità non supportate dal contenitore.</span><span class="sxs-lookup"><span data-stu-id="81c94-105">The user interface should filter out components that require functionality the container does not support.</span></span> <span data-ttu-id="81c94-106">A tale scopo, i componenti possono essere classificati in base alla funzionalità del contenitore richiesta.</span><span class="sxs-lookup"><span data-stu-id="81c94-106">To accomplish this, components can be categorized by the required container functionality.</span></span>

<span data-ttu-id="81c94-107">Un esempio di componenti che richiedono funzionalità dal contenitore e che non funzionano in contenitori che non supportano tale funzionalità sono semplici controlli OLE frame.</span><span class="sxs-lookup"><span data-stu-id="81c94-107">An example of components that require functionality from the container and do not work in containers that do not support that functionality are simple frame OLE controls.</span></span> <span data-ttu-id="81c94-108">La categorizzazione in base alle funzionalità del contenitore viene eseguita da un'altra chiave del registro di sistema all'interno della chiave CLSID del componente:</span><span class="sxs-lookup"><span data-stu-id="81c94-108">Categorizing by container capabilities is accomplished by an additional registry key within the component's CLSID key:</span></span>

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

<span data-ttu-id="81c94-109">Come illustrato in questo esempio, un componente può appartenere a categorie di componenti che indicano le funzionalità supportate, oltre alle categorie di componenti che indicano la funzionalità richiesta.</span><span class="sxs-lookup"><span data-stu-id="81c94-109">As shown in this example, a component can belong to component categories that indicate supported functionality as well as to component categories that indicate required functionality.</span></span>

<span data-ttu-id="81c94-110">Nell'esempio seguente il controllo Button è un controllo OLE generico che non supporta alcuna funzionalità aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="81c94-110">In the following example, the button control is a generic OLE control that supports no additional functionality.</span></span> <span data-ttu-id="81c94-111">Funzionerà in qualsiasi contenitore di controlli OLE.</span><span class="sxs-lookup"><span data-stu-id="81c94-111">It will work in any OLE control container.</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

<span data-ttu-id="81c94-112">Confrontare l'esempio precedente con l'esempio successivo in cui MyDBControl può usare Visual Basic data binding se il contenitore lo supporta.</span><span class="sxs-lookup"><span data-stu-id="81c94-112">Compare the preceding example with the next example in which the MyDBControl can use Visual Basic data binding if the container supports it.</span></span> <span data-ttu-id="81c94-113">Tuttavia, è stato definito in modo che funzioni in contenitori che non supportano Visual Basic data binding (probabilmente da un'API di database diversa):</span><span class="sxs-lookup"><span data-stu-id="81c94-113">However, it has been defined so that it will work in containers that do not support Visual Basic data binding (perhaps by a different database API):</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

<span data-ttu-id="81c94-114">Il controllo GroupBox è un semplice controllo frame.</span><span class="sxs-lookup"><span data-stu-id="81c94-114">The GroupBox control is a simple frame control.</span></span> <span data-ttu-id="81c94-115">Si basa sul contenitore che implementa l'interfaccia [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) e funzionerà correttamente solo in questi contenitori:</span><span class="sxs-lookup"><span data-stu-id="81c94-115">It relies on the container implementing the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface and will work correctly only in such containers:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

<span data-ttu-id="81c94-116">Un contenitore che supporta Visual Basic controlli associati a dati ma non supporta i controlli frame semplici specifica \_ il controllo CATID e il VBDATABOUND CATID nell' \_ interfaccia utente del controllo Insert.</span><span class="sxs-lookup"><span data-stu-id="81c94-116">A container that supports Visual Basic data bound controls but does not support simple frame controls would specify CATID\_Control and CATID\_VBDatabound to the insert control user interface.</span></span> <span data-ttu-id="81c94-117">L'elenco dei controlli visualizzati per l'utente conterrebbe il pulsante CLSID \_ e CLSID \_ MyDBControl.</span><span class="sxs-lookup"><span data-stu-id="81c94-117">The list of controls displayed to the user would contain the CLSID\_Button and CLSID\_MyDBControl.</span></span> <span data-ttu-id="81c94-118">Il \_ GroupBox del CLSID non verrà visualizzato.</span><span class="sxs-lookup"><span data-stu-id="81c94-118">CLSID\_GroupBox would not be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81c94-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81c94-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81c94-120">Associazione di icone a una categoria</span><span class="sxs-lookup"><span data-stu-id="81c94-120">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="81c94-121">Categorizzazione in base alle funzionalità del componente</span><span class="sxs-lookup"><span data-stu-id="81c94-121">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="81c94-122">Classi e associazioni predefinite</span><span class="sxs-lookup"><span data-stu-id="81c94-122">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="81c94-123">Definizione delle categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="81c94-123">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="81c94-124">Gestione categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="81c94-124">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




