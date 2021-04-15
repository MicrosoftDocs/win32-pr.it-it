---
title: Classi e associazioni predefinite
description: Per alcune categorie, una singola classe può essere associata come classe predefinita.
ms.assetid: 9c48615b-ab10-44e4-a032-49d5ee0c9b01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871c537535c57da0809effbe3ee8ec086a88fd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395327"
---
# <a name="default-classes-and-associations"></a><span data-ttu-id="7ae41-103">Classi e associazioni predefinite</span><span class="sxs-lookup"><span data-stu-id="7ae41-103">Default Classes and Associations</span></span>

<span data-ttu-id="7ae41-104">Per alcune categorie, una singola classe può essere associata come classe predefinita.</span><span class="sxs-lookup"><span data-stu-id="7ae41-104">For certain categories, a single class can be associated as the default class.</span></span> <span data-ttu-id="7ae41-105">La classe predefinita viene selezionata ogni volta che è richiesta una particolare categoria di oggetti.</span><span class="sxs-lookup"><span data-stu-id="7ae41-105">The default class is selected whenever that particular category of object is required.</span></span> <span data-ttu-id="7ae41-106">Sebbene questo potrebbe non essere utile per tutte le categorie di componenti, la definizione di una classe predefinita può essere utile quando è necessario caricare una determinata classe da un elenco di classi possibili senza l'intervento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7ae41-106">While this may not be useful for all component categories, establishing a default class can be helpful when a particular class must be loaded from a list of possible classes without user intervention.</span></span> <span data-ttu-id="7ae41-107">Gli amministratori definiscono la classe che può essere utilizzata modificando il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7ae41-107">Administrators define which class can be used by manipulating the registry.</span></span>

<span data-ttu-id="7ae41-108">Per associare una classe predefinita a una categoria, introdurre una chiave CLSID con lo stesso CLSID del CATId della categoria del componente scelto come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="7ae41-108">To associate a default class with a category, introduce a CLSID key with the same CLSID as the CATID of the component category chosen as the default.</span></span> <span data-ttu-id="7ae41-109">Quindi aggiungere una chiave Treats a questa chiave, usando il valore per il CLSID della classe predefinita per la categoria.</span><span class="sxs-lookup"><span data-stu-id="7ae41-109">Then add a TreatAs key to this key, using the value for the CLSID of the default class for the category.</span></span> <span data-ttu-id="7ae41-110">Per usare la classe predefinita per una categoria di componenti, usare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), specificando il CATID per il parametro CLSID.</span><span class="sxs-lookup"><span data-stu-id="7ae41-110">To use the default class for a component category, use [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), specifying the CATID for the CLSID parameter.</span></span> <span data-ttu-id="7ae41-111">Viene automaticamente reindirizzato al CLSID definito come valore predefinito per questa categoria.</span><span class="sxs-lookup"><span data-stu-id="7ae41-111">This automatically redirects to the CLSID established as the default for this category.</span></span> <span data-ttu-id="7ae41-112">La voce del registro di sistema è la seguente:</span><span class="sxs-lookup"><span data-stu-id="7ae41-112">The registry entry is as follows:</span></span>

```
HKEY_CLASSES_ROOT\CLSID
   {catid}
      TreatAs
          = default clsid
```

<span data-ttu-id="7ae41-113">Durante l'installazione, un componente può verificare l'esistenza di eventuali chiavi di classe predefinite per le relative categorie e presentare all'utente le opzioni per l'override delle impostazioni correnti.</span><span class="sxs-lookup"><span data-stu-id="7ae41-113">During installation, a component can check for the existence of any default class keys for its categories and present the user with options for overriding the current settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ae41-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ae41-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ae41-115">Associazione di icone a una categoria</span><span class="sxs-lookup"><span data-stu-id="7ae41-115">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="7ae41-116">Categorizzazione in base alle funzionalità del componente</span><span class="sxs-lookup"><span data-stu-id="7ae41-116">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="7ae41-117">Categorizzazione in base alle funzionalità del contenitore</span><span class="sxs-lookup"><span data-stu-id="7ae41-117">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="7ae41-118">Definizione delle categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="7ae41-118">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="7ae41-119">Gestione categorie di componenti</span><span class="sxs-lookup"><span data-stu-id="7ae41-119">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




