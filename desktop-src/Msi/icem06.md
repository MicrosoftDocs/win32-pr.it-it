---
description: ICEM06 verifica la presenza di riferimenti diretti non validi alle funzionalità da parte del modulo.
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945d45471ec86605e0fa509fc1855aa1cfd5d698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882406"
---
# <a name="icem06"></a><span data-ttu-id="a191b-103">ICEM06</span><span class="sxs-lookup"><span data-stu-id="a191b-103">ICEM06</span></span>

<span data-ttu-id="a191b-104">ICEM06 verifica la presenza di riferimenti diretti non validi alle funzionalità da parte del modulo.</span><span class="sxs-lookup"><span data-stu-id="a191b-104">ICEM06 checks for invalid direct references to features by the module.</span></span>

<span data-ttu-id="a191b-105">I moduli CIEM di tipo merge vengono archiviati in un file con estensione cub del modulo merge denominato Mergemod. cub e non nel file con estensione cub contenente i ghiacci utilizzati per la convalida del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a191b-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="a191b-106">Risultato</span><span class="sxs-lookup"><span data-stu-id="a191b-106">Result</span></span>

<span data-ttu-id="a191b-107">ICEM06 Invia un errore quando il database del modulo contiene riferimenti diretti a una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a191b-107">ICEM06 posts an error when the module database contains direct references to a feature.</span></span> <span data-ttu-id="a191b-108">Le informazioni sulle funzionalità devono essere fornite dall'utente del modulo.</span><span class="sxs-lookup"><span data-stu-id="a191b-108">Feature information must be provided by the user of the module.</span></span>

## <a name="example"></a><span data-ttu-id="a191b-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="a191b-109">Example</span></span>

<span data-ttu-id="a191b-110">ICEM06 invia i messaggi di errore seguenti per un modulo contenente le voci di database indicate di seguito.</span><span class="sxs-lookup"><span data-stu-id="a191b-110">ICEM06 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The target of shortcut Shortcut1.GUID1 is not a property and not a null GUID. 
Modules may not directly reference features.
The row GUID2.LocalServer32.Component2 in the Class table has a feature reference 
that is not a null GUID. Modules may not directly reference features.
```

<span data-ttu-id="a191b-111">[Tabella collegamenti](shortcut-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="a191b-111">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="a191b-112">Tasto di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="a191b-112">Shortcut</span></span>          | <span data-ttu-id="a191b-113">Destinazione</span><span class="sxs-lookup"><span data-stu-id="a191b-113">Target</span></span>                                 |
|-------------------|----------------------------------------|
| <span data-ttu-id="a191b-114">Shortcut1. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="a191b-114">Shortcut1.*GUID1*</span></span> | <span data-ttu-id="a191b-115">cmd.exe</span><span class="sxs-lookup"><span data-stu-id="a191b-115">cmd.exe</span></span>                                |
| <span data-ttu-id="a191b-116">Shortcut2. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="a191b-116">Shortcut2.*GUID1*</span></span> | <span data-ttu-id="a191b-117">\[Prop\]</span><span class="sxs-lookup"><span data-stu-id="a191b-117">\[MyProp\]</span></span>                             |
| <span data-ttu-id="a191b-118">Shortcut3. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="a191b-118">Shortcut3.*GUID1*</span></span> | {00000000-0000-0000-0000-000000000000} |



 

<span data-ttu-id="a191b-119">[Tabella classi](class-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="a191b-119">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="a191b-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="a191b-120">CLSID</span></span>   | <span data-ttu-id="a191b-121">Context</span><span class="sxs-lookup"><span data-stu-id="a191b-121">Context</span></span>       | <span data-ttu-id="a191b-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="a191b-122">Component\_</span></span> | <span data-ttu-id="a191b-123">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="a191b-123">Feature\_</span></span>                              |
|---------|---------------|-------------|----------------------------------------|
| <span data-ttu-id="a191b-124">*GUID1*</span><span class="sxs-lookup"><span data-stu-id="a191b-124">*GUID1*</span></span> | <span data-ttu-id="a191b-125">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="a191b-125">LocalServer32</span></span> | <span data-ttu-id="a191b-126">Component1</span><span class="sxs-lookup"><span data-stu-id="a191b-126">Component1</span></span>  | {00000000-0000-0000-0000-000000000000} |
| <span data-ttu-id="a191b-127">*GUID2*</span><span class="sxs-lookup"><span data-stu-id="a191b-127">*GUID2*</span></span> | <span data-ttu-id="a191b-128">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="a191b-128">LocalServer32</span></span> | <span data-ttu-id="a191b-129">Component2</span><span class="sxs-lookup"><span data-stu-id="a191b-129">Component2</span></span>  | <span data-ttu-id="a191b-130">Funzionalità di</span><span class="sxs-lookup"><span data-stu-id="a191b-130">MyFeature</span></span>                              |



 

<span data-ttu-id="a191b-131">ICEM06 segnala il primo errore perché il primo record nella tabella dei collegamenti include una voce nel campo di destinazione che non è una proprietà o un GUID null.</span><span class="sxs-lookup"><span data-stu-id="a191b-131">ICEM06 reports the first error because the first record in the Shortcut table has an entry in the Target field that is not a property or a null GUID.</span></span> <span data-ttu-id="a191b-132">Un modulo non può fare riferimento direttamente a una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a191b-132">A module cannot reference a feature directly.</span></span> <span data-ttu-id="a191b-133">Le informazioni sulle funzionalità devono essere fornite dall'utente del modulo.</span><span class="sxs-lookup"><span data-stu-id="a191b-133">Feature information must be provided by the user of the module.</span></span> <span data-ttu-id="a191b-134">Per correggere l'errore, i riferimenti a una funzionalità devono essere sostituiti da un GUID null.</span><span class="sxs-lookup"><span data-stu-id="a191b-134">To fix this error, references to a feature should be replaced by a null GUID.</span></span>

<span data-ttu-id="a191b-135">ICEM06 segnala il secondo errore perché il secondo record nella tabella della classe include una voce nel campo della funzionalità che non è un GUID null.</span><span class="sxs-lookup"><span data-stu-id="a191b-135">ICEM06 reports the second error because the second record in the Class table has an entry in the Feature field that is not a null GUID.</span></span> <span data-ttu-id="a191b-136">Un modulo non può fare riferimento direttamente a una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a191b-136">A module cannot reference a feature directly.</span></span> <span data-ttu-id="a191b-137">Le informazioni sulle funzionalità devono essere fornite dall'utente del modulo.</span><span class="sxs-lookup"><span data-stu-id="a191b-137">Feature information must be provided by the user of the module.</span></span> <span data-ttu-id="a191b-138">Per correggere l'errore, i riferimenti a una funzionalità devono essere sostituiti da un GUID null.</span><span class="sxs-lookup"><span data-stu-id="a191b-138">To fix this error, references to a feature should be replaced by a null GUID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a191b-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a191b-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a191b-140">Riferimento ghiaccio del modulo merge</span><span class="sxs-lookup"><span data-stu-id="a191b-140">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



