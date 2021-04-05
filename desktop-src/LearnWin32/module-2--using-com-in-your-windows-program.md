---
title: Uso di COM nell'app di Windows
description: Il modulo 1 di questa serie ha illustrato come creare una finestra e rispondere ai messaggi della finestra, ad esempio WM \_ Paint e WM \_ Close. Nel modulo 2 è stata introdotta la Component Object Model (COM).
ms.assetid: 6e867618-4d02-4c17-b7ea-dc7290507689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c03f16937846c4479a70e16141f1b50bde3efc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726951"
---
# <a name="module-2-using-com-in-your-windows-based-program"></a><span data-ttu-id="65c41-104">Modulo 2.</span><span class="sxs-lookup"><span data-stu-id="65c41-104">Module 2.</span></span> <span data-ttu-id="65c41-105">Uso di COM nel programma Windows-Based</span><span class="sxs-lookup"><span data-stu-id="65c41-105">Using COM in Your Windows-Based Program</span></span>

<span data-ttu-id="65c41-106">Il [modulo 1](your-first-windows-program.md) di questa serie ha illustrato come creare una finestra e rispondere ai messaggi della finestra, ad esempio [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) e [**WM \_ Close**](/windows/desktop/winmsg/wm-close).</span><span class="sxs-lookup"><span data-stu-id="65c41-106">[Module 1](your-first-windows-program.md) of this series showed how to create a window and respond to window messages such as [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) and [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close).</span></span> <span data-ttu-id="65c41-107">Nel modulo 2 è stata introdotta la Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="65c41-107">Module 2 introduces the Component Object Model (COM).</span></span>

<span data-ttu-id="65c41-108">COM è una specifica per la creazione di componenti software riutilizzabili.</span><span class="sxs-lookup"><span data-stu-id="65c41-108">COM is a specification for creating reusable software components.</span></span> <span data-ttu-id="65c41-109">Molte delle funzionalità che si utilizzeranno in un programma moderno basato su Windows si basano su COM, come nel seguente esempio:</span><span class="sxs-lookup"><span data-stu-id="65c41-109">Many of the features that you will use in a modern Windows-based program rely on COM, such as the following:</span></span>

-   <span data-ttu-id="65c41-110">Grafica (Direct2D)</span><span class="sxs-lookup"><span data-stu-id="65c41-110">Graphics (Direct2D)</span></span>
-   <span data-ttu-id="65c41-111">Testo (DirectWrite)</span><span class="sxs-lookup"><span data-stu-id="65c41-111">Text (DirectWrite)</span></span>
-   <span data-ttu-id="65c41-112">Shell di Windows</span><span class="sxs-lookup"><span data-stu-id="65c41-112">The Windows Shell</span></span>
-   <span data-ttu-id="65c41-113">Controllo Ribbon</span><span class="sxs-lookup"><span data-stu-id="65c41-113">The Ribbon control</span></span>
-   <span data-ttu-id="65c41-114">Animazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="65c41-114">UI animation</span></span>

<span data-ttu-id="65c41-115">Alcune tecnologie in questo elenco utilizzano un subset di COM e pertanto non sono "pure" COM.</span><span class="sxs-lookup"><span data-stu-id="65c41-115">(Some technologies on this list use a subset of COM and are therefore not "pure" COM.)</span></span>

<span data-ttu-id="65c41-116">COM ha una reputazione per essere difficile da apprendere.</span><span class="sxs-lookup"><span data-stu-id="65c41-116">COM has a reputation for being difficult to learn.</span></span> <span data-ttu-id="65c41-117">Ed è vero che scrivere un nuovo modulo software per supportare COM può essere difficile.</span><span class="sxs-lookup"><span data-stu-id="65c41-117">And it is true that writing a new software module to support COM can be tricky.</span></span> <span data-ttu-id="65c41-118">Tuttavia, se il programma è esclusivamente un *consumatore* di com, è possibile che com sia più facile da comprendere del previsto.</span><span class="sxs-lookup"><span data-stu-id="65c41-118">But if your program is strictly a *consumer* of COM, you may find that COM is easier to understand than you expect.</span></span>

<span data-ttu-id="65c41-119">Questo modulo illustra come chiamare le API basate su COM nel programma.</span><span class="sxs-lookup"><span data-stu-id="65c41-119">This module shows how to call COM-based APIs in your program.</span></span> <span data-ttu-id="65c41-120">Descrive anche alcuni dei ragionamenti dietro la progettazione di COM.</span><span class="sxs-lookup"><span data-stu-id="65c41-120">It also describes some of the reasoning behind the design of COM.</span></span> <span data-ttu-id="65c41-121">Se si comprende il motivo per cui COM è progettato, è possibile programmare in modo più efficace.</span><span class="sxs-lookup"><span data-stu-id="65c41-121">If you understand why COM is designed as it is, you can program with it more effectively.</span></span> <span data-ttu-id="65c41-122">La seconda parte del modulo descrive alcune procedure di programmazione consigliate per COM.</span><span class="sxs-lookup"><span data-stu-id="65c41-122">The second part of the module describes some recommended programming practices for COM.</span></span>

<span data-ttu-id="65c41-123">COM è stato introdotto in 1993 per supportare il collegamento a oggetti e l'incorporamento (OLE) 2,0.</span><span class="sxs-lookup"><span data-stu-id="65c41-123">COM was introduced in 1993 to support Object Linking and Embedding (OLE) 2.0.</span></span> <span data-ttu-id="65c41-124">A volte le persone pensano che COM e OLE siano uguali.</span><span class="sxs-lookup"><span data-stu-id="65c41-124">People sometimes think that COM and OLE are the same thing.</span></span> <span data-ttu-id="65c41-125">Questo può essere un altro motivo della percezione che COM è difficile da apprendere.</span><span class="sxs-lookup"><span data-stu-id="65c41-125">This may be another reason for the perception that COM is difficult to learn.</span></span> <span data-ttu-id="65c41-126">OLE 2,0 si basa su COM, ma non è necessario conoscere OLE per comprendere COM.</span><span class="sxs-lookup"><span data-stu-id="65c41-126">OLE 2.0 is built on COM, but you do not have to know OLE to understand COM.</span></span>

<span data-ttu-id="65c41-127">COM è uno *standard binario*, non uno standard del linguaggio: definisce l'interfaccia binaria tra un'applicazione e un componente software.</span><span class="sxs-lookup"><span data-stu-id="65c41-127">COM is a *binary standard*, not a language standard: It defines the binary interface between an application and a software component.</span></span> <span data-ttu-id="65c41-128">Come standard binario, COM è indipendente dalla lingua, sebbene venga mappato naturalmente a determinati costrutti C++.</span><span class="sxs-lookup"><span data-stu-id="65c41-128">As a binary standard, COM is language-neutral, although it maps naturally to certain C++ constructs.</span></span> <span data-ttu-id="65c41-129">Questo modulo si concentrerà su tre obiettivi principali di COM:</span><span class="sxs-lookup"><span data-stu-id="65c41-129">This module will focus on three major goals of COM:</span></span>

-   <span data-ttu-id="65c41-130">Separazione dell'implementazione di un oggetto dalla relativa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="65c41-130">Separating the implementation of an object from its interface.</span></span>
-   <span data-ttu-id="65c41-131">Gestione della durata di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="65c41-131">Managing the lifetime of an object.</span></span>
-   <span data-ttu-id="65c41-132">Individuazione delle funzionalità di un oggetto in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="65c41-132">Discovering the capabilities of an object at run time.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="65c41-133">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="65c41-133">In this section</span></span>

-   [<span data-ttu-id="65c41-134">Che cos'è un'interfaccia COM?</span><span class="sxs-lookup"><span data-stu-id="65c41-134">What Is a COM Interface?</span></span>](what-is-a-com-interface-.md)
-   [<span data-ttu-id="65c41-135">Inizializzazione della libreria COM</span><span class="sxs-lookup"><span data-stu-id="65c41-135">Initializing the COM Library</span></span>](initializing-the-com-library.md)
-   [<span data-ttu-id="65c41-136">Codici di errore in COM</span><span class="sxs-lookup"><span data-stu-id="65c41-136">Error Codes in COM</span></span>](error-codes-in-com.md)
-   [<span data-ttu-id="65c41-137">Creazione di un oggetto in COM</span><span class="sxs-lookup"><span data-stu-id="65c41-137">Creating an Object in COM</span></span>](creating-an-object-in-com.md)
-   [<span data-ttu-id="65c41-138">Esempio: finestra di dialogo Apri</span><span class="sxs-lookup"><span data-stu-id="65c41-138">Example: The Open Dialog Box</span></span>](example--the-open-dialog-box.md)
-   [<span data-ttu-id="65c41-139">Gestione della durata di un oggetto</span><span class="sxs-lookup"><span data-stu-id="65c41-139">Managing the Lifetime of an Object</span></span>](managing-the-lifetime-of-an-object.md)
-   [<span data-ttu-id="65c41-140">Richiesta di un oggetto per un'interfaccia</span><span class="sxs-lookup"><span data-stu-id="65c41-140">Asking an Object for an Interface</span></span>](asking-an-object-for-an-interface.md)
-   [<span data-ttu-id="65c41-141">Allocazione di memoria in COM</span><span class="sxs-lookup"><span data-stu-id="65c41-141">Memory Allocation in COM</span></span>](memory-allocation-in-com.md)
-   [<span data-ttu-id="65c41-142">Procedure di codifica COM</span><span class="sxs-lookup"><span data-stu-id="65c41-142">COM Coding Practices</span></span>](com-coding-practices.md)
-   [<span data-ttu-id="65c41-143">Gestione degli errori in COM</span><span class="sxs-lookup"><span data-stu-id="65c41-143">Error Handling in COM</span></span>](error-handling-in-com.md)

## <a name="related-topics"></a><span data-ttu-id="65c41-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65c41-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65c41-145">Impara a programmare per Windows in C++</span><span class="sxs-lookup"><span data-stu-id="65c41-145">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> </dl>

 

 