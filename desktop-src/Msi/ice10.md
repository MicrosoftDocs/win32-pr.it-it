---
description: ICE10 verifica che lo stato di annuncio delle funzionalità figlio corrisponda a quello della relativa funzionalità padre.
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac8f1304f4444a0f087d747328cdea4b3d714ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314241"
---
# <a name="ice10"></a><span data-ttu-id="e5a99-103">ICE10</span><span class="sxs-lookup"><span data-stu-id="e5a99-103">ICE10</span></span>

<span data-ttu-id="e5a99-104">ICE10 verifica che lo stato di annuncio delle funzionalità figlio corrisponda a quello della relativa funzionalità padre.</span><span class="sxs-lookup"><span data-stu-id="e5a99-104">ICE10 validates that the advertise state of child features matches that of its parent feature.</span></span>

<span data-ttu-id="e5a99-105">Una funzionalità figlio potrebbe non impedire l'annuncio quando la funzionalità padre consente l'annuncio.</span><span class="sxs-lookup"><span data-stu-id="e5a99-105">A child feature may not disallow advertisement while its parent feature allows advertisement.</span></span> <span data-ttu-id="e5a99-106">La seguente combinazione di attributi padre e figlio non è quindi valida.</span><span class="sxs-lookup"><span data-stu-id="e5a99-106">The following combination of parent and child attributes is therefore invalid.</span></span>

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

<span data-ttu-id="e5a99-107">Questa combinazione non è valida perché potrebbe disattivare l'elemento padre ogni volta che l'elemento padre doveva essere pubblicizzato.</span><span class="sxs-lookup"><span data-stu-id="e5a99-107">This combination is invalid because it would turn off the parent whenever the parent was supposed to be advertised.</span></span> <span data-ttu-id="e5a99-108">È tuttavia consentito il contrario.</span><span class="sxs-lookup"><span data-stu-id="e5a99-108">However, the reverse is allowed.</span></span> <span data-ttu-id="e5a99-109">Un elemento figlio può essere contrassegnato per favorire l'annuncio mentre l'elemento padre è contrassegnato per non consentire l'annuncio.</span><span class="sxs-lookup"><span data-stu-id="e5a99-109">A child can be marked to favor advertisement while the parent is marked to disallow advertisement.</span></span>

<span data-ttu-id="e5a99-110">L'azione personalizzata ICE10 determina lo stato delle funzionalità padre e figlio dalla colonna attributi della tabella delle [funzionalità](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a99-110">The ICE10 custom action determines the state of parent and child features from the Attributes column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="e5a99-111">Si noti che è possibile impostare lo stato di una funzionalità su 0 e che l'elemento padre o figlio impostato su predilige o non consenta l'annuncio.</span><span class="sxs-lookup"><span data-stu-id="e5a99-111">Note that it is valid to set the state of a feature to 0 and have its parent or child set to favor or disallow advertisement.</span></span>

## <a name="result"></a><span data-ttu-id="e5a99-112">Risultato</span><span class="sxs-lookup"><span data-stu-id="e5a99-112">Result</span></span>

<span data-ttu-id="e5a99-113">ICE10 Invia un errore se la colonna Attributes della tabella [feature](feature-table.md) contiene una mancata corrispondenza nello stato advertise.</span><span class="sxs-lookup"><span data-stu-id="e5a99-113">ICE10 posts an error if the Attributes column of the [Feature](feature-table.md) table contains a mismatch in the advertise state.</span></span>

## <a name="example"></a><span data-ttu-id="e5a99-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="e5a99-114">Example</span></span>

<span data-ttu-id="e5a99-115">ICE10 invia il messaggio di errore seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="e5a99-115">ICE10 posts the following error message for the example shown.</span></span>

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

<span data-ttu-id="e5a99-116">Si noti che per questo esempio Microsoft Excel e Microsoft Word sono funzionalità figlio di Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="e5a99-116">Note for this example that Microsoft Excel and Microsoft Word are child features of Microsoft Office.</span></span>

<span data-ttu-id="e5a99-117">Tabella delle [funzionalità](feature-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="e5a99-117">[Feature](feature-table.md) table (partial)</span></span>



| <span data-ttu-id="e5a99-118">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="e5a99-118">Feature</span></span> | <span data-ttu-id="e5a99-119">\_Elemento padre della funzionalità</span><span class="sxs-lookup"><span data-stu-id="e5a99-119">Feature\_Parent</span></span> | <span data-ttu-id="e5a99-120">Attributi</span><span class="sxs-lookup"><span data-stu-id="e5a99-120">Attributes</span></span> |
|---------|-----------------|------------|
| <span data-ttu-id="e5a99-121">Office</span><span class="sxs-lookup"><span data-stu-id="e5a99-121">Office</span></span>  | <span data-ttu-id="e5a99-122">Null</span><span class="sxs-lookup"><span data-stu-id="e5a99-122">Null</span></span>            | <span data-ttu-id="e5a99-123">4</span><span class="sxs-lookup"><span data-stu-id="e5a99-123">4</span></span>          |
| <span data-ttu-id="e5a99-124">Excel</span><span class="sxs-lookup"><span data-stu-id="e5a99-124">Excel</span></span>   | <span data-ttu-id="e5a99-125">Office</span><span class="sxs-lookup"><span data-stu-id="e5a99-125">Office</span></span>          | <span data-ttu-id="e5a99-126">4</span><span class="sxs-lookup"><span data-stu-id="e5a99-126">4</span></span>          |
| <span data-ttu-id="e5a99-127">Word</span><span class="sxs-lookup"><span data-stu-id="e5a99-127">Word</span></span>    | <span data-ttu-id="e5a99-128">Office</span><span class="sxs-lookup"><span data-stu-id="e5a99-128">Office</span></span>          | <span data-ttu-id="e5a99-129">8</span><span class="sxs-lookup"><span data-stu-id="e5a99-129">8</span></span>          |



 

<span data-ttu-id="e5a99-130">Nell'esempio, Word è impostato su non consentire l'annuncio pubblicitario, che è in conflitto con lo stato Consenti annuncio del padre, Office.</span><span class="sxs-lookup"><span data-stu-id="e5a99-130">In the example, Word is set to disallow advertisement, which conflicts with the allow advertisement state of its parent, Office.</span></span>

<span data-ttu-id="e5a99-131">In alcuni casi ICE10 invia l'errore seguente:</span><span class="sxs-lookup"><span data-stu-id="e5a99-131">In some cases ICE10 posts the following error:</span></span>

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

<span data-ttu-id="e5a99-132">Si riferisce a un riferimento di chiave esterna non valido.</span><span class="sxs-lookup"><span data-stu-id="e5a99-132">This refers to an invalid foreign key reference.</span></span> <span data-ttu-id="e5a99-133">Per risolvere il problema, è necessario che "Child" punti alla relativa funzionalità padre corretta oppure aggiungere una voce per la funzionalità padre ' Parent ' alla tabella [feature](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a99-133">The fix is to have 'Child' point to its correct parent feature, or add an entry for the parent feature 'Parent' to the [Feature](feature-table.md) table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5a99-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5a99-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5a99-135">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="e5a99-135">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



