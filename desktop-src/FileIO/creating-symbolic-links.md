---
description: Creare collegamenti simbolici che usano un percorso assoluto o relativo tramite la funzione CreateSymbolicLink.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Creazione di collegamenti simbolici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c978532ffc11e44615d4de0ea902152438ecc7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347831"
---
# <a name="creating-symbolic-links"></a><span data-ttu-id="6fec5-103">Creazione di collegamenti simbolici</span><span class="sxs-lookup"><span data-stu-id="6fec5-103">Creating Symbolic Links</span></span>

<span data-ttu-id="6fec5-104">La funzione [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) consente di creare collegamenti simbolici usando un percorso assoluto o relativo.</span><span class="sxs-lookup"><span data-stu-id="6fec5-104">The function [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) allows you to create symbolic links using either an absolute or relative path.</span></span>

<span data-ttu-id="6fec5-105">I collegamenti simbolici possono essere collegamenti assoluti o relativi.</span><span class="sxs-lookup"><span data-stu-id="6fec5-105">Symbolic links can either be absolute or relative links.</span></span> <span data-ttu-id="6fec5-106">I collegamenti assoluti sono collegamenti che specificano ogni parte del nome del percorso; i collegamenti relativi vengono determinati in relazione alla posizione in cui gli identificatori di collegamento relativi si trovano in un percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="6fec5-106">Absolute links are links that specify each portion of the path name; relative links are determined relative to where relative–link specifiers are in a specified path.</span></span> <span data-ttu-id="6fec5-107">I collegamenti relativi vengono specificati usando le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6fec5-107">Relative links are specified using the following conventions:</span></span>

-   <span data-ttu-id="6fec5-108">Punto (.</span><span class="sxs-lookup"><span data-stu-id="6fec5-108">Dot (.</span></span> <span data-ttu-id="6fec5-109">e..) convenzioni, ad esempio ".. \\ " risolve il percorso relativo alla directory padre.</span><span class="sxs-lookup"><span data-stu-id="6fec5-109">and ..) conventions—for example, "..\\" resolves the path relative to the parent directory.</span></span>
-   <span data-ttu-id="6fec5-110">Nomi senza barre ( \) ad esempio, "tmp" risolve il percorso relativo alla directory corrente.</span><span class="sxs-lookup"><span data-stu-id="6fec5-110">Names with no slashes (\)—for example, "tmp" resolves the path relative to the current directory.</span></span>
-   <span data-ttu-id="6fec5-111">Relativa radice, ad esempio " \\ Windows \\ system32" viene risolto nell'*unità "Current Drive*: \\ Windows \\ system32".</span><span class="sxs-lookup"><span data-stu-id="6fec5-111">Root relative—for example, "\\Windows\\System32" resolves to the "*current drive*:\\Windows\\System32".</span></span> <span data-ttu-id="6fec5-112">directory</span><span class="sxs-lookup"><span data-stu-id="6fec5-112">directory</span></span>
-   <span data-ttu-id="6fec5-113">Relativa alla directory di lavoro corrente, ad esempio se la directory di lavoro corrente è "C: \\ Windows \\ system32", "C:File.txt" viene risolto in "c: \\ Windows \\ system32 \\File.txt".</span><span class="sxs-lookup"><span data-stu-id="6fec5-113">Current working directory-relative—for example, if the current working directory is "C:\\Windows\\System32", "C:File.txt" resolves to "C:\\Windows\\System32\\File.txt".</span></span>

    <span data-ttu-id="6fec5-114">**Nota**  Se si specifica un collegamento relativo alla directory di lavoro corrente, viene creato come collegamento assoluto, a causa del modo in cui la directory di lavoro corrente viene elaborata in base all'utente e al thread.</span><span class="sxs-lookup"><span data-stu-id="6fec5-114">**Note**  If you specify a current working directory–relative link, it is created as an absolute link, due to the way the current working directory is processed based on the user and the thread.</span></span>

<span data-ttu-id="6fec5-115">Un collegamento simbolico può anche contenere entrambi i punti di giunzione e le cartelle montate come parte del nome del percorso.</span><span class="sxs-lookup"><span data-stu-id="6fec5-115">A symbolic link can also contain both junction points and mounted folders as a part of the path name.</span></span>

<span data-ttu-id="6fec5-116">I collegamenti simbolici possono puntare direttamente a un file o a una directory remota utilizzando il percorso UNC.</span><span class="sxs-lookup"><span data-stu-id="6fec5-116">Symbolic links can point directly to a remote file or directory using the UNC path.</span></span>

<span data-ttu-id="6fec5-117">I collegamenti simbolici relativi sono limitati a un singolo volume.</span><span class="sxs-lookup"><span data-stu-id="6fec5-117">Relative symbolic links are restricted to a single volume.</span></span>

## <a name="example-of-an-absolute-symbolic-link"></a><span data-ttu-id="6fec5-118">Esempio di collegamento simbolico assoluto</span><span class="sxs-lookup"><span data-stu-id="6fec5-118">Example of an Absolute Symbolic Link</span></span>

<span data-ttu-id="6fec5-119">In questo esempio, il percorso originale contiene un componente,'*x*', che è un collegamento simbolico assoluto.</span><span class="sxs-lookup"><span data-stu-id="6fec5-119">In this example, the original path contains a component, '*x*', which is an absolute symbolic link.</span></span> <span data-ttu-id="6fec5-120">Quando viene rilevato '*x*', il frammento del percorso originale fino *a' x*' viene sostituito completamente dal percorso a cui punta '*x*'.</span><span class="sxs-lookup"><span data-stu-id="6fec5-120">When '*x*' is encountered, the fragment of the original path up to and including '*x*' is completely replaced by the path that is pointed to by '*x*'.</span></span> <span data-ttu-id="6fec5-121">Il resto del percorso dopo '*x*' viene aggiunto al nuovo percorso.</span><span class="sxs-lookup"><span data-stu-id="6fec5-121">The remainder of the path after '*x*' is appended to this new path.</span></span> <span data-ttu-id="6fec5-122">Ora diventa il percorso modificato.</span><span class="sxs-lookup"><span data-stu-id="6fec5-122">This now becomes the modified path.</span></span>

<span data-ttu-id="6fec5-123">X: "C: \\ Alpha \\ beta \\ absLink \\ gamma \\ file"</span><span class="sxs-lookup"><span data-stu-id="6fec5-123">X: "C:\\alpha\\beta\\absLink\\gamma\\file"</span></span>

<span data-ttu-id="6fec5-124">Link: "absLink" viene mappato a " \\ \\ machineB \\ share"</span><span class="sxs-lookup"><span data-stu-id="6fec5-124">Link: "absLink" maps to "\\\\machineB\\share"</span></span>

<span data-ttu-id="6fec5-125">Percorso modificato: " \\ \\ machineB \\ condivisione \\ \\ file gamma"</span><span class="sxs-lookup"><span data-stu-id="6fec5-125">Modified Path: "\\\\machineB\\share\\gamma\\file"</span></span>

## <a name="example-of-a-relative-symbolic-links"></a><span data-ttu-id="6fec5-126">Esempio di collegamenti simbolici relativi</span><span class="sxs-lookup"><span data-stu-id="6fec5-126">Example of a Relative Symbolic Links</span></span>

<span data-ttu-id="6fec5-127">In questo esempio, il percorso originale contiene un componente "*x*", che è un collegamento simbolico relativo.</span><span class="sxs-lookup"><span data-stu-id="6fec5-127">In this example, the original path contains a component '*x*', which is a relative symbolic link.</span></span> <span data-ttu-id="6fec5-128">Quando viene rilevato '*x*','*x*' viene sostituito completamente dal nuovo frammento a cui punta '*x*'.</span><span class="sxs-lookup"><span data-stu-id="6fec5-128">When '*x*' is encountered, '*x*' is completely replaced by the new fragment pointed to by '*x*'.</span></span> <span data-ttu-id="6fec5-129">Il resto del percorso dopo '*x*' viene aggiunto al nuovo percorso.</span><span class="sxs-lookup"><span data-stu-id="6fec5-129">The remainder of the path after '*x*', is appended to the new path.</span></span> <span data-ttu-id="6fec5-130">Tutti i punti (..) in questo nuovo percorso sostituiscono i componenti visualizzati prima dei punti (..).</span><span class="sxs-lookup"><span data-stu-id="6fec5-130">Any dots (..) in this new path replace components that appear before the dots (..).</span></span> <span data-ttu-id="6fec5-131">Ogni set di punti sostituisce il componente precedente.</span><span class="sxs-lookup"><span data-stu-id="6fec5-131">Each set of dots replace the component preceding.</span></span> <span data-ttu-id="6fec5-132">Se il numero di punti (..) supera il numero di componenti, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="6fec5-132">If the number of dots (..) exceed the number of components, an error is returned.</span></span> <span data-ttu-id="6fec5-133">In caso contrario, al termine della sostituzione di tutti i componenti, rimane il percorso finale modificato.</span><span class="sxs-lookup"><span data-stu-id="6fec5-133">Otherwise, when all component replacement has finished, the final, modified path remains.</span></span>

<span data-ttu-id="6fec5-134">X: C: \\ \\ \\ file gamma di collegamento alfa beta \\ \\</span><span class="sxs-lookup"><span data-stu-id="6fec5-134">X: C:\\alpha\\beta\\link\\gamma\\file</span></span>

<span data-ttu-id="6fec5-135">Collegamento: "link" esegue il mapping a ".. \\ .. \\ Theta</span><span class="sxs-lookup"><span data-stu-id="6fec5-135">Link: "link" maps to "..\\..\\theta"</span></span>

<span data-ttu-id="6fec5-136">Percorso modificato: "C: \\ Alpha \\ beta \\ .. \\ .. \\ \\file gamma Theta \\ "</span><span class="sxs-lookup"><span data-stu-id="6fec5-136">Modified Path: "C:\\alpha\\beta\\..\\..\\theta\\gamma\\file"</span></span>

<span data-ttu-id="6fec5-137">Percorso finale: "C: \\ theta \\ gamma \\ file"</span><span class="sxs-lookup"><span data-stu-id="6fec5-137">Final Path: "C:\\theta\\gamma\\file"</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fec5-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6fec5-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fec5-139">Collegamenti simbolici</span><span class="sxs-lookup"><span data-stu-id="6fec5-139">Symbolic Links</span></span>](symbolic-links.md)
</dt> <dt>

[<span data-ttu-id="6fec5-140">Collegamenti reali e giunzioni</span><span class="sxs-lookup"><span data-stu-id="6fec5-140">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)
</dt> <dt>

[<span data-ttu-id="6fec5-141">Denominazione di file, percorsi e spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="6fec5-141">Naming Files, Paths, and Namespaces</span></span>](naming-a-file.md)
</dt> </dl>

 

 



