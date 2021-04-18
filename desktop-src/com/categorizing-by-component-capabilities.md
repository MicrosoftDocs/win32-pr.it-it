---
title: Categorizzazione in base alle funzionalità del componente
description: È possibile utilizzare le categorie di componenti per visualizzare un subset di tutti i componenti installati.
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff44e03e9eae0226ac57279c37d4a5dfd32fc6bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297959"
---
# <a name="categorizing-by-component-capabilities"></a><span data-ttu-id="9701e-103">Categorizzazione in base alle funzionalità del componente</span><span class="sxs-lookup"><span data-stu-id="9701e-103">Categorizing by Component Capabilities</span></span>

<span data-ttu-id="9701e-104">È possibile utilizzare le categorie di componenti per visualizzare un subset di tutti i componenti installati.</span><span class="sxs-lookup"><span data-stu-id="9701e-104">Component categories can be used to display a subset of all of the installed components.</span></span> <span data-ttu-id="9701e-105">Ogni categoria di componenti è identificata da un GUID, indicato come ID di categoria (CATId).</span><span class="sxs-lookup"><span data-stu-id="9701e-105">Each component category is identified by a GUID, referred to as a Category ID (CATID).</span></span> <span data-ttu-id="9701e-106">Ogni CATId dispone di un elenco di nomi a cui è stato assegnato un nome leggibile dalle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="9701e-106">Each CATID has a list of locale-tagged, human-readable names associated with it.</span></span> <span data-ttu-id="9701e-107">Un elenco di CATID e i nomi leggibili sono archiviati in una posizione nota nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9701e-107">A listing of the CATIDs and the human-readable names is stored in a well-known location in the registry.</span></span>

<span data-ttu-id="9701e-108">Ad esempio, tutti i componenti che implementano la funzionalità per l'incorporamento di documenti OLE possono essere classificati all'interno di una categoria di componenti.</span><span class="sxs-lookup"><span data-stu-id="9701e-108">For example, all components that implement the functionality for OLE document embedding can be classified within a component category.</span></span> <span data-ttu-id="9701e-109">In passato, questi oggetti venivano identificati dalla chiave "Insertable" nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9701e-109">In the past, these objects would have been identified by the "Insertable" key in the registry.</span></span> <span data-ttu-id="9701e-110">Per usare invece le categorie di componenti, al registro di sistema vengono aggiunte le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9701e-110">To use component categories instead, the following information would be added to the registry:</span></span>

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

<span data-ttu-id="9701e-111">Ogni classe che implementa la funzionalità corrispondente a una categoria di componenti elenca l'ID di categoria per tale categoria all'interno della chiave CLSID nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9701e-111">Each class that implements the functionality corresponding to a component category lists the category ID for that category within the CLSID key in the registry.</span></span> <span data-ttu-id="9701e-112">Poiché un singolo componente può supportare un'ampia gamma di funzionalità, i componenti possono appartenere a più categorie di componenti.</span><span class="sxs-lookup"><span data-stu-id="9701e-112">Because a single component can support a wide range of functionality, components can belong to multiple component categories.</span></span> <span data-ttu-id="9701e-113">Ad esempio, un particolare controllo OLE potrebbe supportare tutte le funzionalità necessarie per partecipare come incorporamento di documenti OLE, Microsoft Visual Basic data binding e funzionalità Internet.</span><span class="sxs-lookup"><span data-stu-id="9701e-113">For example, a particular OLE control might support all of the functionality required to participate as OLE document embedding, Microsoft Visual Basic data binding, and Internet functionality.</span></span> <span data-ttu-id="9701e-114">Un controllo di questo tipo avrebbe memorizzato le informazioni seguenti nella relativa chiave CLSID nel registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="9701e-114">Such a control would have the following information stored in its CLSID key in the registry:</span></span>

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

<span data-ttu-id="9701e-115">Con queste informazioni, un contenitore può enumerare i controlli installati in un sistema e visualizzare solo i controlli che supportano la funzionalità richiesta dal contenitore.</span><span class="sxs-lookup"><span data-stu-id="9701e-115">With this information, a container can enumerate the controls installed on a system and display only those controls that support the functionality required by the container.</span></span> <span data-ttu-id="9701e-116">L'uso delle categorie di componenti consente di categorizzare i componenti in base alla funzionalità implementata del componente.</span><span class="sxs-lookup"><span data-stu-id="9701e-116">The use of component categories provides a way to categorize components by the implemented functionality of the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9701e-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9701e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9701e-118">Associazione di icone a una categoria</span><span class="sxs-lookup"><span data-stu-id="9701e-118">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="9701e-119">Categorizzazione in base alle funzionalità del contenitore</span><span class="sxs-lookup"><span data-stu-id="9701e-119">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="9701e-120">Classi e associazioni predefinite</span><span class="sxs-lookup"><span data-stu-id="9701e-120">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="9701e-121">Definizione delle categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="9701e-121">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="9701e-122">Gestione categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="9701e-122">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




