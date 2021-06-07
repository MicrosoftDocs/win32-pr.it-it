---
description: Creare collegamenti simbolici che usano un percorso assoluto o relativo usando la funzione CreateSymbolicLink.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Creazione di collegamenti simbolici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252b999b05004fd7735b16582783ef0c3afb0013
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387707"
---
# <a name="creating-symbolic-links"></a><span data-ttu-id="409d1-103">Creazione di collegamenti simbolici</span><span class="sxs-lookup"><span data-stu-id="409d1-103">Creating Symbolic Links</span></span>

<span data-ttu-id="409d1-104">La funzione [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) consente di creare collegamenti simbolici usando un percorso assoluto o relativo.</span><span class="sxs-lookup"><span data-stu-id="409d1-104">The function [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) allows you to create symbolic links using either an absolute or relative path.</span></span>

<span data-ttu-id="409d1-105">I collegamenti simbolici possono essere collegamenti assoluti o relativi.</span><span class="sxs-lookup"><span data-stu-id="409d1-105">Symbolic links can either be absolute or relative links.</span></span> <span data-ttu-id="409d1-106">I collegamenti assoluti sono collegamenti che specificano ogni parte del nome del percorso. i collegamenti relativi vengono determinati in relazione alla posizione in cui gli identificatori di collegamento relativo si trova in un percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="409d1-106">Absolute links are links that specify each portion of the path name; relative links are determined relative to where relative–link specifiers are in a specified path.</span></span> <span data-ttu-id="409d1-107">I collegamenti relativi vengono specificati usando le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="409d1-107">Relative links are specified using the following conventions:</span></span>

-   <span data-ttu-id="409d1-108">Punto (.</span><span class="sxs-lookup"><span data-stu-id="409d1-108">Dot (.</span></span> <span data-ttu-id="409d1-109">e ..) convenzioni, ad esempio ".. \\ " risolve il percorso relativo alla directory padre.</span><span class="sxs-lookup"><span data-stu-id="409d1-109">and ..) conventions—for example, "..\\" resolves the path relative to the parent directory.</span></span>
-   <span data-ttu-id="409d1-110">Nomi senza barre ( ) : \\ ad esempio, "tmp" risolve il percorso relativo alla directory corrente.</span><span class="sxs-lookup"><span data-stu-id="409d1-110">Names with no slashes (\\)—for example, "tmp" resolves the path relative to the current directory.</span></span>
-   <span data-ttu-id="409d1-111">Relativo alla radice, ad esempio , \\ "Windows \\ System32" viene risolto nell'unità corrente : Windows \\ \\ System32.</span><span class="sxs-lookup"><span data-stu-id="409d1-111">Root relative—for example, "\\Windows\\System32" resolves to the "*current drive*:\\Windows\\System32".</span></span> <span data-ttu-id="409d1-112">directory</span><span class="sxs-lookup"><span data-stu-id="409d1-112">directory</span></span>
-   <span data-ttu-id="409d1-113">Relativo alla directory di lavoro corrente, ad esempio se la directory di lavoro corrente è "C: \\ Windows \\ System32", "C:File.txt" viene risolto in "C: \\ Windows \\ System32 \\File.txt".</span><span class="sxs-lookup"><span data-stu-id="409d1-113">Current working directory-relative—for example, if the current working directory is "C:\\Windows\\System32", "C:File.txt" resolves to "C:\\Windows\\System32\\File.txt".</span></span>

    <span data-ttu-id="409d1-114">**Nota**  Se si specifica un collegamento relativo alla directory di lavoro corrente, viene creato come collegamento assoluto, a causa del modo in cui la directory di lavoro corrente viene elaborata in base all'utente e al thread.</span><span class="sxs-lookup"><span data-stu-id="409d1-114">**Note**  If you specify a current working directory–relative link, it is created as an absolute link, due to the way the current working directory is processed based on the user and the thread.</span></span>

<span data-ttu-id="409d1-115">Un collegamento simbolico può contenere anche punti di giunzione e cartelle montate come parte del nome del percorso.</span><span class="sxs-lookup"><span data-stu-id="409d1-115">A symbolic link can also contain both junction points and mounted folders as a part of the path name.</span></span>

<span data-ttu-id="409d1-116">I collegamenti simbolici possono puntare direttamente a un file o a una directory remota usando il percorso UNC.</span><span class="sxs-lookup"><span data-stu-id="409d1-116">Symbolic links can point directly to a remote file or directory using the UNC path.</span></span>

<span data-ttu-id="409d1-117">I collegamenti simbolici relativi sono limitati a un singolo volume.</span><span class="sxs-lookup"><span data-stu-id="409d1-117">Relative symbolic links are restricted to a single volume.</span></span>

## <a name="example-of-an-absolute-symbolic-link"></a><span data-ttu-id="409d1-118">Esempio di collegamento simbolico assoluto</span><span class="sxs-lookup"><span data-stu-id="409d1-118">Example of an Absolute Symbolic Link</span></span>

<span data-ttu-id="409d1-119">In questo esempio il percorso originale contiene un componente, '*x*', che è un collegamento simbolico assoluto.</span><span class="sxs-lookup"><span data-stu-id="409d1-119">In this example, the original path contains a component, '*x*', which is an absolute symbolic link.</span></span> <span data-ttu-id="409d1-120">Quando viene rilevato '*x*', il frammento del percorso originale fino a e incluso '*x*' viene completamente sostituito dal percorso a cui punta '*x*'.</span><span class="sxs-lookup"><span data-stu-id="409d1-120">When '*x*' is encountered, the fragment of the original path up to and including '*x*' is completely replaced by the path that is pointed to by '*x*'.</span></span> <span data-ttu-id="409d1-121">Il resto del percorso dopo '*x*' viene aggiunto a questo nuovo percorso.</span><span class="sxs-lookup"><span data-stu-id="409d1-121">The remainder of the path after '*x*' is appended to this new path.</span></span> <span data-ttu-id="409d1-122">Questo diventa ora il percorso modificato.</span><span class="sxs-lookup"><span data-stu-id="409d1-122">This now becomes the modified path.</span></span>

<span data-ttu-id="409d1-123">X: "C: \\ alpha \\ beta \\ absLink \\ gamma \\ file"</span><span class="sxs-lookup"><span data-stu-id="409d1-123">X: "C:\\alpha\\beta\\absLink\\gamma\\file"</span></span>

<span data-ttu-id="409d1-124">Collegamento: "absLink" esegue il mapping a \\ \\ "machineB \\ share"</span><span class="sxs-lookup"><span data-stu-id="409d1-124">Link: "absLink" maps to "\\\\machineB\\share"</span></span>

<span data-ttu-id="409d1-125">Percorso modificato: " \\ \\ machineB \\ share \\ gamma \\ file"</span><span class="sxs-lookup"><span data-stu-id="409d1-125">Modified Path: "\\\\machineB\\share\\gamma\\file"</span></span>

## <a name="example-of-a-relative-symbolic-links"></a><span data-ttu-id="409d1-126">Esempio di collegamenti simbolici relativi</span><span class="sxs-lookup"><span data-stu-id="409d1-126">Example of a Relative Symbolic Links</span></span>

<span data-ttu-id="409d1-127">In questo esempio il percorso originale contiene un componente '*x*', che è un collegamento simbolico relativo.</span><span class="sxs-lookup"><span data-stu-id="409d1-127">In this example, the original path contains a component '*x*', which is a relative symbolic link.</span></span> <span data-ttu-id="409d1-128">Quando viene rilevato '*x*', '*x*' viene completamente sostituito dal nuovo frammento a cui punta '*x*'.</span><span class="sxs-lookup"><span data-stu-id="409d1-128">When '*x*' is encountered, '*x*' is completely replaced by the new fragment pointed to by '*x*'.</span></span> <span data-ttu-id="409d1-129">Il resto del percorso dopo '*x*', viene aggiunto al nuovo percorso.</span><span class="sxs-lookup"><span data-stu-id="409d1-129">The remainder of the path after '*x*', is appended to the new path.</span></span> <span data-ttu-id="409d1-130">Tutti i punti (..) in questo nuovo percorso sostituiscono i componenti visualizzati prima dei punti (..).</span><span class="sxs-lookup"><span data-stu-id="409d1-130">Any dots (..) in this new path replace components that appear before the dots (..).</span></span> <span data-ttu-id="409d1-131">Ogni set di punti sostituisce il componente precedente.</span><span class="sxs-lookup"><span data-stu-id="409d1-131">Each set of dots replace the component preceding.</span></span> <span data-ttu-id="409d1-132">Se il numero di punti (..) supera il numero di componenti, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="409d1-132">If the number of dots (..) exceed the number of components, an error is returned.</span></span> <span data-ttu-id="409d1-133">In caso contrario, al termine della sostituzione di tutti i componenti, rimane il percorso finale modificato.</span><span class="sxs-lookup"><span data-stu-id="409d1-133">Otherwise, when all component replacement has finished, the final, modified path remains.</span></span>

<span data-ttu-id="409d1-134">X: C: \\ alpha beta link gamma \\ \\ \\ \\ file</span><span class="sxs-lookup"><span data-stu-id="409d1-134">X: C:\\alpha\\beta\\link\\gamma\\file</span></span>

<span data-ttu-id="409d1-135">Collegamento: "link" esegue il mapping a ".. \\ .. \\ theta"</span><span class="sxs-lookup"><span data-stu-id="409d1-135">Link: "link" maps to "..\\..\\theta"</span></span>

<span data-ttu-id="409d1-136">Percorso modificato: "C: \\ alpha \\ beta \\ .. \\ .. \\ theta \\ gamma \\ file"</span><span class="sxs-lookup"><span data-stu-id="409d1-136">Modified Path: "C:\\alpha\\beta\\..\\..\\theta\\gamma\\file"</span></span>

<span data-ttu-id="409d1-137">Percorso finale: "C: \\ theta \\ gamma \\ file"</span><span class="sxs-lookup"><span data-stu-id="409d1-137">Final Path: "C:\\theta\\gamma\\file"</span></span>

## <a name="related-topics"></a><span data-ttu-id="409d1-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="409d1-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="409d1-139">Collegamenti simbolici</span><span class="sxs-lookup"><span data-stu-id="409d1-139">Symbolic Links</span></span>](symbolic-links.md)
</dt> <dt>

[<span data-ttu-id="409d1-140">Collegamenti e giunzioni rigidi</span><span class="sxs-lookup"><span data-stu-id="409d1-140">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)
</dt> <dt>

[<span data-ttu-id="409d1-141">Denominazione di file, percorsi e spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="409d1-141">Naming Files, Paths, and Namespaces</span></span>](naming-a-file.md)
</dt> </dl>

 

 



