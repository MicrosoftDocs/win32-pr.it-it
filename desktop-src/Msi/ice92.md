---
description: ICE92 verifica che un componente senza un GUID ID componente non sia specificato anche come componente permanente.
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c9cffdfd7ac30313ed24182d8b4cc94f25900f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882733"
---
# <a name="ice92"></a><span data-ttu-id="06ab2-103">ICE92</span><span class="sxs-lookup"><span data-stu-id="06ab2-103">ICE92</span></span>

<span data-ttu-id="06ab2-104">ICE92 verifica che un componente senza un GUID ID componente non sia specificato anche come componente permanente.</span><span class="sxs-lookup"><span data-stu-id="06ab2-104">ICE92 verifies that a component without a Component Id GUID is not also specified as a permanent component.</span></span> <span data-ttu-id="06ab2-105">Questa azione personalizzata ICE controlla la [tabella](component-table.md) dei componenti senza un [GUID](guid.md) specificato nel campo ComponentID e verifica che il flag **msidbComponentAttributesPermanent** non sia stato impostato nel campo attributi.</span><span class="sxs-lookup"><span data-stu-id="06ab2-105">This ICE custom action checks the [Component Table](component-table.md) for components without a [GUID](guid.md) specified in the ComponentId field and verifies that the **msidbComponentAttributesPermanent** flag has not been set in the Attributes field.</span></span> <span data-ttu-id="06ab2-106">ICE92 verifica anche che nessun componente abbia entrambi gli attributi **msidbComponentAttributesPermanent** e **msidbComponentAttributesUninstallOnSupersedence** .</span><span class="sxs-lookup"><span data-stu-id="06ab2-106">ICE92 also verifies that no component has both the **msidbComponentAttributesPermanent** and **msidbComponentAttributesUninstallOnSupersedence** attributes.</span></span>

<span data-ttu-id="06ab2-107">Se la colonna ComponentId è null, il programma di installazione non registra il componente e il componente non può essere rimosso o ripristinato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="06ab2-107">If the ComponentId column is null, the installer does not register the component and the component cannot be removed or repaired by the installer.</span></span>

## <a name="result"></a><span data-ttu-id="06ab2-108">Risultato</span><span class="sxs-lookup"><span data-stu-id="06ab2-108">Result</span></span>

<span data-ttu-id="06ab2-109">ICE92 invia il seguente errore.</span><span class="sxs-lookup"><span data-stu-id="06ab2-109">ICE92 posts the following error.</span></span>



| <span data-ttu-id="06ab2-110">Errore ICE92</span><span class="sxs-lookup"><span data-stu-id="06ab2-110">ICE92 error</span></span>                                                          | <span data-ttu-id="06ab2-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06ab2-111">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06ab2-112">Il componente ' \[ 1 \] ' non contiene ComponentID ed è contrassegnato come permanente.</span><span class="sxs-lookup"><span data-stu-id="06ab2-112">The Component '\[1\]' has no ComponentId and is marked as permanent.</span></span> | <span data-ttu-id="06ab2-113">La voce per questo componente nella tabella dei componenti presenta un valore null nella colonna ComponentId e include **msidbComponentAttributesPermanent** nella colonna Attributes.</span><span class="sxs-lookup"><span data-stu-id="06ab2-113">The entry for this component in the Component table has null in the ComponentId column and has **msidbComponentAttributesPermanent** in the Attributes column.</span></span> |



 

<span data-ttu-id="06ab2-114">ICE92 invia il seguente avviso.</span><span class="sxs-lookup"><span data-stu-id="06ab2-114">ICE92 posts the following warning.</span></span>



| <span data-ttu-id="06ab2-115">Avviso di ICE92</span><span class="sxs-lookup"><span data-stu-id="06ab2-115">ICE92 warning</span></span>                                                                                                                                                           | <span data-ttu-id="06ab2-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06ab2-116">Description</span></span>                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06ab2-117">Il componente ' \[ 1 \] ' è contrassegnato come Permanent e Uninstall-on-sostituzione.</span><span class="sxs-lookup"><span data-stu-id="06ab2-117">The Component '\[1\]' is marked as permanent and uninstall-on-supersedence.</span></span> <span data-ttu-id="06ab2-118">L'attributo Uninstall-on-sostituzione verrà ignorato perché il componente è permanente.</span><span class="sxs-lookup"><span data-stu-id="06ab2-118">The uninstall-on-supersedence attribute will be ignored because the component is permanent.</span></span> | <span data-ttu-id="06ab2-119">Per la voce per questo componente nella [tabella dei componenti](component-table.md) sono specificati entrambi gli attributi **msidbComponentAttributesPermanent** e **msidbComponentAttributesUninstallOnSupersedence** .</span><span class="sxs-lookup"><span data-stu-id="06ab2-119">The entry for this component in the [Component table](component-table.md) has both the **msidbComponentAttributesPermanent** and **msidbComponentAttributesUninstallOnSupersedence** attributes specified.</span></span> |



 

## <a name="example"></a><span data-ttu-id="06ab2-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="06ab2-120">Example</span></span>

<span data-ttu-id="06ab2-121">ICE92 segnala l'errore seguente per l'esempio:</span><span class="sxs-lookup"><span data-stu-id="06ab2-121">ICE92 reports the following error for the example:</span></span>

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

<span data-ttu-id="06ab2-122">[Tabella componenti](component-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="06ab2-122">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="06ab2-123">Componente</span><span class="sxs-lookup"><span data-stu-id="06ab2-123">Component</span></span>  | <span data-ttu-id="06ab2-124">ComponentId</span><span class="sxs-lookup"><span data-stu-id="06ab2-124">ComponentId</span></span> | <span data-ttu-id="06ab2-125">Directory\_</span><span class="sxs-lookup"><span data-stu-id="06ab2-125">Directory\_</span></span> | <span data-ttu-id="06ab2-126">Attributi</span><span class="sxs-lookup"><span data-stu-id="06ab2-126">Attributes</span></span> | <span data-ttu-id="06ab2-127">KeyPath</span><span class="sxs-lookup"><span data-stu-id="06ab2-127">KeyPath</span></span> |
|------------|-------------|-------------|------------|---------|
| <span data-ttu-id="06ab2-128">Component1</span><span class="sxs-lookup"><span data-stu-id="06ab2-128">Component1</span></span> |             | <span data-ttu-id="06ab2-129">Directory</span><span class="sxs-lookup"><span data-stu-id="06ab2-129">DirectoryA</span></span>  | <span data-ttu-id="06ab2-130">16</span><span class="sxs-lookup"><span data-stu-id="06ab2-130">16</span></span>         | <span data-ttu-id="06ab2-131">FileA</span><span class="sxs-lookup"><span data-stu-id="06ab2-131">FileA</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="06ab2-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06ab2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06ab2-133">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="06ab2-133">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



