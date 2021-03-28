---
description: L'interfaccia utente di Windows consente agli utenti di accedere a un'ampia gamma di oggetti necessari per l'esecuzione di applicazioni e la gestione del sistema operativo.
title: Shell di Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1d0d4ed7-9b85-4d70-bf1f-82567a1687fb
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 448e1d5265ec34ce1889ca36f234622e2b082553
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979903"
---
# <a name="windows-shell"></a><span data-ttu-id="97147-103">Shell di Windows</span><span class="sxs-lookup"><span data-stu-id="97147-103">Windows Shell</span></span>

<span data-ttu-id="97147-104">L'interfaccia utente di Windows consente agli utenti di accedere a un'ampia gamma di oggetti necessari per l'esecuzione di applicazioni e la gestione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="97147-104">The Windows UI provides users with access to a wide variety of objects necessary for running applications and managing the operating system.</span></span> <span data-ttu-id="97147-105">I più numerosi e familiari di questi oggetti sono le cartelle e i file che risiedono in unità disco del computer.</span><span class="sxs-lookup"><span data-stu-id="97147-105">The most numerous and familiar of these objects are the folders and files that reside on computer disk drives.</span></span> <span data-ttu-id="97147-106">Sono inoltre disponibili numerosi oggetti virtuali che consentono all'utente di eseguire attività quali l'invio di file alle stampanti remote o l'accesso al Cestino.</span><span class="sxs-lookup"><span data-stu-id="97147-106">There are also a number of virtual objects that allow the user to perform tasks such as sending files to remote printers or accessing the Recycle Bin.</span></span> <span data-ttu-id="97147-107">La shell organizza questi oggetti in uno spazio dei nomi gerarchico e fornisce a utenti e applicazioni un modo coerente ed efficiente per accedere e gestire gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="97147-107">The Shell organizes these objects into a hierarchical namespace and provides users and applications with a consistent and efficient way to access and manage objects.</span></span>

## <a name="shell-development-scenarios"></a><span data-ttu-id="97147-108">Scenari di sviluppo della shell</span><span class="sxs-lookup"><span data-stu-id="97147-108">Shell Development Scenarios</span></span>

<span data-ttu-id="97147-109">Gli scenari di sviluppo seguenti sono correlati allo sviluppo di applicazioni:</span><span class="sxs-lookup"><span data-stu-id="97147-109">The following development scenarios relate to application development:</span></span>

-   <span data-ttu-id="97147-110">Estensione della shell, che consiste nella creazione di un'origine dati (rispetto al modello di dati della Shell)</span><span class="sxs-lookup"><span data-stu-id="97147-110">Extending the Shell, which consists of creating a data source (versus consuming the Shell data model)</span></span>
-   <span data-ttu-id="97147-111">Implementazione di un sottoinsieme delle attività dell'origine dati della shell</span><span class="sxs-lookup"><span data-stu-id="97147-111">Implementing a subset of the Shell data source tasks</span></span>
-   <span data-ttu-id="97147-112">Librerie di supporto e visualizzazioni di elementi in Esplora risorse</span><span class="sxs-lookup"><span data-stu-id="97147-112">Supporting libraries and item views in Windows Explorer</span></span>
-   <span data-ttu-id="97147-113">Uso della finestra di dialogo file comune</span><span class="sxs-lookup"><span data-stu-id="97147-113">Using the common file dialog</span></span>
-   <span data-ttu-id="97147-114">Implementazione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="97147-114">Implementing Control Panel items</span></span>
-   <span data-ttu-id="97147-115">Gestione delle notifiche</span><span class="sxs-lookup"><span data-stu-id="97147-115">Managing notifications</span></span>

<span data-ttu-id="97147-116">Gli scenari di sviluppo seguenti si riferiscono alla proprietà del formato di file:</span><span class="sxs-lookup"><span data-stu-id="97147-116">The following development scenarios relate to file format ownership:</span></span>

-   <span data-ttu-id="97147-117">Implementazione di un sottoinsieme delle attività dell'origine dati della shell</span><span class="sxs-lookup"><span data-stu-id="97147-117">Implementing a subset of the Shell data source tasks</span></span>
-   <span data-ttu-id="97147-118">Implementazione di qualsiasi gestore</span><span class="sxs-lookup"><span data-stu-id="97147-118">Implementing any handler</span></span>
-   <span data-ttu-id="97147-119">Supporto della ricerca desktop</span><span class="sxs-lookup"><span data-stu-id="97147-119">Supporting desktop search</span></span>

<span data-ttu-id="97147-120">Gli scenari di sviluppo seguenti si riferiscono alla proprietà dell'archiviazione dei dati:</span><span class="sxs-lookup"><span data-stu-id="97147-120">The following development scenarios relate to data storage ownership:</span></span>

-   <span data-ttu-id="97147-121">Supporto per la ricerca desktop e OpenSearch</span><span class="sxs-lookup"><span data-stu-id="97147-121">Supporting desktop search and OpenSearch</span></span>
-   <span data-ttu-id="97147-122">Implementazione di un sottoinsieme delle attività dell'origine dati della shell (cartelle virtuali)</span><span class="sxs-lookup"><span data-stu-id="97147-122">Implementing a subset of the Shell data source tasks (virtual folders)</span></span>
-   <span data-ttu-id="97147-123">Librerie di supporto in Esplora risorse</span><span class="sxs-lookup"><span data-stu-id="97147-123">Supporting libraries in Windows Explorer</span></span>

<span data-ttu-id="97147-124">Lo scenario di sviluppo seguente si riferisce al supporto dei dispositivi:</span><span class="sxs-lookup"><span data-stu-id="97147-124">The following development scenario relates to device support:</span></span>

-   <span data-ttu-id="97147-125">Esecuzione automatica e riproduzione automatica</span><span class="sxs-lookup"><span data-stu-id="97147-125">Auto run and auto play</span></span>

## <a name="windows-shell-sdk-documentation"></a><span data-ttu-id="97147-126">Documentazione di Windows Shell SDK</span><span class="sxs-lookup"><span data-stu-id="97147-126">Windows Shell SDK Documentation</span></span>

<span data-ttu-id="97147-127">Questa documentazione è suddivisa in tre sezioni principali:</span><span class="sxs-lookup"><span data-stu-id="97147-127">This documentation is broken into three major sections:</span></span>

-   <span data-ttu-id="97147-128">La [Guida](intro.md) per gli sviluppatori della shell fornisce materiale concettuale sul funzionamento della shell e su come usare l'API della shell nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97147-128">The [Shell Developer's Guide](intro.md) provides conceptual material about how the Shell works and how to use the Shell's API in your application.</span></span>
-   <span data-ttu-id="97147-129">La sezione di [riferimento della shell](shell-reference-bumper.md) documenta gli elementi di programmazione che costituiscono le varie API della shell.</span><span class="sxs-lookup"><span data-stu-id="97147-129">The [Shell Reference](shell-reference-bumper.md) section documents programming elements that make up the various Shell APIs.</span></span>
-   <span data-ttu-id="97147-130">[Esempi di Shell](samples-entry.md) fornisce collegamenti ad esempi di codice correlati.</span><span class="sxs-lookup"><span data-stu-id="97147-130">[Shell Samples](samples-entry.md) provides links to related code samples.</span></span>

<span data-ttu-id="97147-131">La tabella seguente fornisce una descrizione della sezione di riferimento della shell.</span><span class="sxs-lookup"><span data-stu-id="97147-131">The following table provides an outline of the Shell Reference section.</span></span> <span data-ttu-id="97147-132">Se non specificato diversamente, tutti gli elementi di programmazione sono documentati in C++ non gestito.</span><span class="sxs-lookup"><span data-stu-id="97147-132">Unless otherwise noted, all programming elements are documented in unmanaged C++.</span></span>



| <span data-ttu-id="97147-133">Sezione</span><span class="sxs-lookup"><span data-stu-id="97147-133">Section</span></span>                                                               | <span data-ttu-id="97147-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97147-134">Description</span></span>                                                                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97147-135">Classi shell</span><span class="sxs-lookup"><span data-stu-id="97147-135">Shell Classes</span></span>](classes.md)                                          | <span data-ttu-id="97147-136">In questa sezione vengono descritte le classi della shell di Windows Select.</span><span class="sxs-lookup"><span data-stu-id="97147-136">This section describes select Windows Shell classes.</span></span>                                                                 |
| [<span data-ttu-id="97147-137">Interfacce della shell</span><span class="sxs-lookup"><span data-stu-id="97147-137">Shell Interfaces</span></span>](interfaces.md)                                    | <span data-ttu-id="97147-138">In questa sezione vengono descritte le interfacce di Windows Shell Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="97147-138">This section describes the Windows Shell Component Object Model (COM) interfaces.</span></span>                                    |
| [<span data-ttu-id="97147-139">Funzioni della shell</span><span class="sxs-lookup"><span data-stu-id="97147-139">Shell Functions</span></span>](functions.md)                                      | <span data-ttu-id="97147-140">In questa sezione vengono descritte le funzioni della shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="97147-140">This section describes the Windows Shell functions.</span></span>                                                                  |
| [<span data-ttu-id="97147-141">Funzioni di callback della shell</span><span class="sxs-lookup"><span data-stu-id="97147-141">Shell Callback Functions</span></span>](callbacks.md)                             | <span data-ttu-id="97147-142">In questa sezione vengono descritti i modelli di funzioni di callback della shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="97147-142">This section describes the Windows Shell callback functions templates.</span></span>                                               |
| [<span data-ttu-id="97147-143">Costanti, enumerazioni e flag della shell</span><span class="sxs-lookup"><span data-stu-id="97147-143">Shell Constants, Enumerations, and Flags</span></span>](consts-enums-flags.md)    | <span data-ttu-id="97147-144">In questa sezione vengono descritte le costanti, le enumerazioni e i flag della shell di Windows utilizzati nelle API della shell.</span><span class="sxs-lookup"><span data-stu-id="97147-144">This section describes the Windows Shell constants, enumerations, and flags used in the Shell APIs.</span></span>                  |
| [<span data-ttu-id="97147-145">Funzioni di utilità Lightweight Shell</span><span class="sxs-lookup"><span data-stu-id="97147-145">Shell Lightweight Utility Functions</span></span>](shlwapi.md)                    | <span data-ttu-id="97147-146">In questa sezione vengono descritte le funzioni di utilità Lightweight per la shell di Windows fornite in Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="97147-146">This section describes the Windows Shell lightweight utility functions provided in Shlwapi.dll.</span></span>                      |
| [<span data-ttu-id="97147-147">Macro della shell</span><span class="sxs-lookup"><span data-stu-id="97147-147">Shell Macros</span></span>](macros.md)                                            | <span data-ttu-id="97147-148">In questa sezione vengono descritte le macro di utilità della shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="97147-148">This section describes the Windows Shell utility macros.</span></span>                                                             |
| [<span data-ttu-id="97147-149">Messaggi e notifiche della shell</span><span class="sxs-lookup"><span data-stu-id="97147-149">Shell Messages and Notifications</span></span>](messages.md)                      | <span data-ttu-id="97147-150">In questa sezione vengono descritti i messaggi e le notifiche inviati dagli elementi della shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="97147-150">This section describes the messages and notifications sent by elements of the Windows Shell.</span></span>                         |
| [<span data-ttu-id="97147-151">Oggetti Shell per gli script e Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="97147-151">Shell Objects for Scripting and Microsoft Visual Basic</span></span>](objects.md) | <span data-ttu-id="97147-152">In questa sezione vengono descritti gli oggetti di Windows implementati dalla Shell per l'utilizzo nello scripting e in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="97147-152">This section describes the Windows objects implemented by the Shell for use in scripting and Microsoft Visual Basic.</span></span> |
| [<span data-ttu-id="97147-153">Oggetti Shell per C++</span><span class="sxs-lookup"><span data-stu-id="97147-153">Shell Objects for C++</span></span>](objects-cpp.md)                              | <span data-ttu-id="97147-154">In questa sezione vengono descritti gli oggetti Windows C++ implementati dalla Shell.</span><span class="sxs-lookup"><span data-stu-id="97147-154">This section describes the C++ Windows objects implemented by the Shell.</span></span>                                             |
| [<span data-ttu-id="97147-155">Schemi della shell</span><span class="sxs-lookup"><span data-stu-id="97147-155">Shell Schemas</span></span>](schemas.md)                                          | <span data-ttu-id="97147-156">In questa sezione vengono descritti gli schemi del manifesto della libreria, della proprietà e del trasferimento utilizzati dalla shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="97147-156">This section describes library, property, and transfer manifest schemas used by the Windows Shell.</span></span>                   |
| [<span data-ttu-id="97147-157">Strutture della shell</span><span class="sxs-lookup"><span data-stu-id="97147-157">Shell Structures</span></span>](structures.md)                                    | <span data-ttu-id="97147-158">In questa sezione vengono descritte le strutture della shell di Windows utilizzate nelle API della shell.</span><span class="sxs-lookup"><span data-stu-id="97147-158">This section describes the Windows Shell structures used in the Shell APIs.</span></span>                                          |



 

 

 



