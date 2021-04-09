---
description: ICEM05 verifica che il modulo unione sia associato correttamente ai componenti del modulo. Associando erroneamente un componente a un modulo, il componente viene associato erroneamente al database di destinazione.
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ca481ef836c2675c381817fe2242e37384818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049904"
---
# <a name="icem05"></a><span data-ttu-id="ad345-104">ICEM05</span><span class="sxs-lookup"><span data-stu-id="ad345-104">ICEM05</span></span>

<span data-ttu-id="ad345-105">ICEM05 verifica che il modulo unione sia associato correttamente ai componenti del modulo.</span><span class="sxs-lookup"><span data-stu-id="ad345-105">ICEM05 verifies that the merge module is correctly associated with components in the module.</span></span> <span data-ttu-id="ad345-106">Associando erroneamente un componente a un modulo, il componente viene associato erroneamente al database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ad345-106">Incorrectly associating a component with a module causes the component to be incorrectly associated with the target database.</span></span>

<span data-ttu-id="ad345-107">I moduli CIEM di tipo merge vengono archiviati in un file con estensione cub del modulo merge denominato Mergemod. cub e non nel file con estensione cub contenente i ghiacci utilizzati per la convalida del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="ad345-107">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="ad345-108">Risultato</span><span class="sxs-lookup"><span data-stu-id="ad345-108">Result</span></span>

<span data-ttu-id="ad345-109">ICEM05 Invia un errore se il database del modulo associa erroneamente i componenti e il modulo.</span><span class="sxs-lookup"><span data-stu-id="ad345-109">ICEM05 posts an error if the module database incorrectly associates components and the module.</span></span>

## <a name="example"></a><span data-ttu-id="ad345-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="ad345-110">Example</span></span>

<span data-ttu-id="ad345-111">ICEM05 invia i messaggi di errore seguenti per un modulo contenente le voci di database indicate di seguito.</span><span class="sxs-lookup"><span data-stu-id="ad345-111">ICEM05 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The component Component2.OtherModule.GUID2.1033 in the 
ModuleComponents table does not belong to this Merge Module.
The component Component1.MyModule.GUID1.1033 in the ModuleComponents 
table is not listed in the Component table.
The component 'Component3' in the Component table is not listed in the 
ModuleComponents table.
```

[<span data-ttu-id="ad345-112">Tabella ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="ad345-112">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="ad345-113">ModuleID</span><span class="sxs-lookup"><span data-stu-id="ad345-113">ModuleID</span></span>         | <span data-ttu-id="ad345-114">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="ad345-114">Language</span></span> | <span data-ttu-id="ad345-115">Versione</span><span class="sxs-lookup"><span data-stu-id="ad345-115">Version</span></span> |
|------------------|----------|---------|
| <span data-ttu-id="ad345-116">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="ad345-116">MyModule.*GUID1*</span></span> | <span data-ttu-id="ad345-117">1033</span><span class="sxs-lookup"><span data-stu-id="ad345-117">1033</span></span>     | <span data-ttu-id="ad345-118">1.0</span><span class="sxs-lookup"><span data-stu-id="ad345-118">1.0</span></span>     |



 

[<span data-ttu-id="ad345-119">**Tabella ModuleComponents**</span><span class="sxs-lookup"><span data-stu-id="ad345-119">**ModuleComponents Table**</span></span>](modulecomponents-table.md)



| <span data-ttu-id="ad345-120">Componente</span><span class="sxs-lookup"><span data-stu-id="ad345-120">Component</span></span>  | <span data-ttu-id="ad345-121">ModuleID</span><span class="sxs-lookup"><span data-stu-id="ad345-121">ModuleID</span></span>            | <span data-ttu-id="ad345-122">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="ad345-122">Language</span></span> |
|------------|---------------------|----------|
| <span data-ttu-id="ad345-123">Component1</span><span class="sxs-lookup"><span data-stu-id="ad345-123">Component1</span></span> | <span data-ttu-id="ad345-124">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="ad345-124">MyModule.*GUID1*</span></span>    | <span data-ttu-id="ad345-125">1033</span><span class="sxs-lookup"><span data-stu-id="ad345-125">1033</span></span>     |
| <span data-ttu-id="ad345-126">Component2</span><span class="sxs-lookup"><span data-stu-id="ad345-126">Component2</span></span> | <span data-ttu-id="ad345-127">OtherModule. *Guid2*</span><span class="sxs-lookup"><span data-stu-id="ad345-127">OtherModule.*GUID2*</span></span> | <span data-ttu-id="ad345-128">1033</span><span class="sxs-lookup"><span data-stu-id="ad345-128">1033</span></span>     |



 

<span data-ttu-id="ad345-129">[Tabella componenti](component-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="ad345-129">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="ad345-130">Componente</span><span class="sxs-lookup"><span data-stu-id="ad345-130">Component</span></span>  | <span data-ttu-id="ad345-131">ComponentID</span><span class="sxs-lookup"><span data-stu-id="ad345-131">ComponentID</span></span> |
|------------|-------------|
| <span data-ttu-id="ad345-132">Component3</span><span class="sxs-lookup"><span data-stu-id="ad345-132">Component3</span></span> | <span data-ttu-id="ad345-133">*GUID4*</span><span class="sxs-lookup"><span data-stu-id="ad345-133">*GUID4*</span></span>     |
| <span data-ttu-id="ad345-134">Component2</span><span class="sxs-lookup"><span data-stu-id="ad345-134">Component2</span></span> | <span data-ttu-id="ad345-135">*GUID5*</span><span class="sxs-lookup"><span data-stu-id="ad345-135">*GUID5*</span></span>     |



 

<span data-ttu-id="ad345-136">Il modulo merge ICE segnala il primo errore perché la tabella ModuleComponents tenta di associare un componente a un altro modulo che non è il modulo corrente specificato nella tabella ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="ad345-136">The merge module ICE reports the first error because the ModuleComponents table attempts to associate a component with another module that is not the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="ad345-137">Per risolvere questo problema, modificare le colonne ModuleID e Language del record ModuleComponents per Component2 in quello per il modulo corrente, modulo. *Guid1*.</span><span class="sxs-lookup"><span data-stu-id="ad345-137">To fix this, change the ModuleID and Language columns of the ModuleComponents record for Component2 to that for the current module, MyModule.*GUID1*.</span></span>

<span data-ttu-id="ad345-138">Il modulo merge ICE segnala il secondo errore perché il primo record nella tabella ModuleComponents tenta di associare Component1 al modulo.</span><span class="sxs-lookup"><span data-stu-id="ad345-138">The merge module ICE reports the second error because the first record in the ModuleComponents table attempts to associate Component1 with the module.</span></span> <span data-ttu-id="ad345-139">Questo componente non esiste nella tabella dei componenti del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="ad345-139">This component does not exist in the Component Table of the merge module.</span></span> <span data-ttu-id="ad345-140">Un modulo può essere associato solo a un componente esistente nel modulo.</span><span class="sxs-lookup"><span data-stu-id="ad345-140">A module can only be associated with a component that exists in the module.</span></span> <span data-ttu-id="ad345-141">Per risolvere il problema, rimuovere il record per il componente non esistente.</span><span class="sxs-lookup"><span data-stu-id="ad345-141">To fix this, remove the record for the non-existent component.</span></span>

<span data-ttu-id="ad345-142">Il modulo merge ICE segnala il terzo errore perché il modulo tenta di aggiungere Component3 al database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ad345-142">The merge module ICE reports the third error because the module attempts to add Component3 to the target database.</span></span> <span data-ttu-id="ad345-143">Questo componente non è stato associato al modulo nella tabella ModuleComponents.</span><span class="sxs-lookup"><span data-stu-id="ad345-143">This component has not been associated with the module in the ModuleComponents table.</span></span> <span data-ttu-id="ad345-144">Per correggere l'errore, aggiungere un record per Component3 alla tabella ModuleComponents.</span><span class="sxs-lookup"><span data-stu-id="ad345-144">To fix this error, add a record for Component3 to the ModuleComponents table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad345-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad345-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad345-146">Riferimento ghiaccio del modulo merge</span><span class="sxs-lookup"><span data-stu-id="ad345-146">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



