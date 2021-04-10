---
title: Implementazione di IEnumSTATPROPSTG-Compound file
description: L'implementazione del file composto dell'interfaccia IEnumSTATPROPSTG viene utilizzata per enumerare le proprietà, ottenendo le strutture Campo STATPROPSTG, che contengono dati statistici sulle proprietà.
ms.assetid: 8fa536f4-cce6-47e4-a860-2f43e48fa469
keywords:
- IEnumSTATPROPSTG Strctd STG, implementazione del file composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbffce14016efdb4e2a77d60096b6776e6c2189
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963357"
---
# <a name="ienumstatpropstg-compound-file-implementation"></a><span data-ttu-id="4dbf5-104">Implementazione di IEnumSTATPROPSTG-Compound file</span><span class="sxs-lookup"><span data-stu-id="4dbf5-104">IEnumSTATPROPSTG-Compound File Implementation</span></span>

<span data-ttu-id="4dbf5-105">L'implementazione del file composto dell'interfaccia [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) viene utilizzata per enumerare le proprietà, ottenendo le strutture [**Campo STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , che contengono dati statistici sulle proprietà.</span><span class="sxs-lookup"><span data-stu-id="4dbf5-105">The compound file implementation of the [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) interface is used to enumerate properties, resulting in [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures, which contain statistical property data.</span></span> <span data-ttu-id="4dbf5-106">L'implementazione di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) gestisce i dati statistici ed è associata a un oggetto di archiviazione file composto corrente.</span><span class="sxs-lookup"><span data-stu-id="4dbf5-106">The implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) manages the statistical data and is associated with a current compound file storage object.</span></span>

<span data-ttu-id="4dbf5-107">Il costruttore nell'implementazione COM di [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) crea una classe che legge l'intero set di proprietà e crea una matrice statica che può essere condivisa quando viene chiamato **IEnumSTATPROPSTG:: Clone** .</span><span class="sxs-lookup"><span data-stu-id="4dbf5-107">The constructor in the COM implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) creates a class that reads the entire property set, and creates a static array which can be shared when **IEnumSTATPROPSTG::Clone** is called.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="4dbf5-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="4dbf5-108">When to Use</span></span>

<span data-ttu-id="4dbf5-109">Chiamare l'implementazione del file composto di [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) per enumerare le strutture [**Campo STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) che contengono dati sulle proprietà all'interno del set di proprietà corrente.</span><span class="sxs-lookup"><span data-stu-id="4dbf5-109">Call the compound file implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) to enumerate the [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures that contain data about the properties within the current property set.</span></span> <span data-ttu-id="4dbf5-110">Quando si usa l'implementazione del file composto delle interfacce di archiviazione delle proprietà, chiamare [**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) per restituire un puntatore a **IEnumSTATPROPSTG** per gestire l'oggetto di archiviazione della proprietà e gli elementi al suo interno.</span><span class="sxs-lookup"><span data-stu-id="4dbf5-110">When using the compound file implementation of the property storage interfaces, call [**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) to return a pointer to **IEnumSTATPROPSTG** to manage the property storage object and the elements within it.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dbf5-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="4dbf5-111">Remarks</span></span>

<dl> <dt>

<span data-ttu-id="4dbf5-112"><span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="4dbf5-112"><span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="4dbf5-113">Ottiene le successive strutture [**Campo STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) (il numero viene specificato dal parametro *celt* ).</span><span class="sxs-lookup"><span data-stu-id="4dbf5-113">Gets the next one or more [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures (the number is specified by the *celt* parameter).</span></span> <span data-ttu-id="4dbf5-114">Restituisce \_ OK se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4dbf5-114">Returns S\_OK if successful.</span></span>

</dd> <dt>

<span data-ttu-id="4dbf5-115"><span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG:: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="4dbf5-115"><span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG::Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="4dbf5-116">Ignora il numero di elementi specificato in *celt*.</span><span class="sxs-lookup"><span data-stu-id="4dbf5-116">Skips the number of elements specified in *celt*.</span></span> <span data-ttu-id="4dbf5-117">L'elemento successivo da enumerare tramite una chiamata a Next diventa quindi l'elemento dopo gli elementi ignorati.</span><span class="sxs-lookup"><span data-stu-id="4dbf5-117">The next element to be enumerated through a call to Next then becomes the element after the skipped elements.</span></span> <span data-ttu-id="4dbf5-118">Restituisce \_ OK se gli elementi *celt* sono stati ignorati. restituisce \_ false se il numero di elementi *celt* è stato ignorato.</span><span class="sxs-lookup"><span data-stu-id="4dbf5-118">Returns S\_OK if *celt* elements were skipped; returns S\_FALSE if fewer than *celt* elements were skipped.</span></span>

</dd> <dt>

<span data-ttu-id="4dbf5-119"><span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG:: Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="4dbf5-119"><span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG::Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="4dbf5-120">Imposta il cursore all'inizio dell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="4dbf5-120">Sets the cursor to the beginning of the enumeration.</span></span> <span data-ttu-id="4dbf5-121">Se ha esito positivo, restituisce S \_ OK. in caso contrario, restituisce STG \_ E \_ INVALIDHANDLE.</span><span class="sxs-lookup"><span data-stu-id="4dbf5-121">If successful, returns S\_OK, otherwise, returns STG\_E\_INVALIDHANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="4dbf5-122"><span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="4dbf5-122"><span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="4dbf5-123">Usa il costruttore per [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) per creare una copia della matrice.</span><span class="sxs-lookup"><span data-stu-id="4dbf5-123">Uses the constructor for the [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) to create a copy of the array.</span></span> <span data-ttu-id="4dbf5-124">Poiché la classe che costruisce la matrice statica contiene effettivamente l'oggetto, questa funzione aggiunge principalmente al conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="4dbf5-124">Because the class that constructs the static array actually contains the object, this function mainly adds to the reference count.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="4dbf5-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4dbf5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dbf5-126">**Campo STATPROPSTG**</span><span class="sxs-lookup"><span data-stu-id="4dbf5-126">**STATPROPSTG**</span></span>](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dt>

[<span data-ttu-id="4dbf5-127">**IPropertyStorage:: enum**</span><span class="sxs-lookup"><span data-stu-id="4dbf5-127">**IPropertyStorage::Enum**</span></span>](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> </dl>

 

 