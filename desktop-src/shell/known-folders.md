---
description: Windows Vista introduce nuovi scenari di archiviazione e un nuovo spazio dei nomi del profilo utente.
title: Cartelle note
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d0c25eef-53ac-4dad-805a-b9ba4cd86be9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7527b7242c68f0d6c78cd0fae427626c182302f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980242"
---
# <a name="known-folders"></a><span data-ttu-id="b39f9-103">Cartelle note</span><span class="sxs-lookup"><span data-stu-id="b39f9-103">Known Folders</span></span>

<span data-ttu-id="b39f9-104">Windows Vista introduce nuovi scenari di archiviazione e un nuovo spazio dei nomi del profilo utente.</span><span class="sxs-lookup"><span data-stu-id="b39f9-104">Windows Vista introduces new storage scenarios and a new user profile namespace.</span></span> <span data-ttu-id="b39f9-105">Per risolvere questi nuovi fattori, il sistema precedente di riferimento alle cartelle standard da un valore [**CSIDL**](csidl.md) è stato sostituito.</span><span class="sxs-lookup"><span data-stu-id="b39f9-105">To address these new factors, the older system of referring to standard folders by a [**CSIDL**](csidl.md) value has been replaced.</span></span> <span data-ttu-id="b39f9-106">A partire da Windows Vista, a tali cartelle viene fatto riferimento da un nuovo set di valori GUID detti ID cartella noti.</span><span class="sxs-lookup"><span data-stu-id="b39f9-106">As of Windows Vista, those folders are referenced by a new set of GUID values called Known Folder IDs.</span></span>

<span data-ttu-id="b39f9-107">Il sistema di cartelle note offre i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b39f9-107">The Known Folder system provides these advantages:</span></span>

-   <span data-ttu-id="b39f9-108">I fornitori di software indipendenti (ISV) possono estendere il set di ID cartella note con i rispettivi.</span><span class="sxs-lookup"><span data-stu-id="b39f9-108">Independent software vendors (ISVs) can extend the set of Known Folder IDs with their own.</span></span> <span data-ttu-id="b39f9-109">Possono definire cartelle, assegnare loro ID e registrarle nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b39f9-109">They can define folders, give them IDs, and register them with the system.</span></span> <span data-ttu-id="b39f9-110">Non è stato possibile estendere i valori CSIDL.</span><span class="sxs-lookup"><span data-stu-id="b39f9-110">CSIDL values could not be extended.</span></span>
-   <span data-ttu-id="b39f9-111">È possibile enumerare tutte le cartelle note in un sistema.</span><span class="sxs-lookup"><span data-stu-id="b39f9-111">All Known Folders on a system can be enumerated.</span></span> <span data-ttu-id="b39f9-112">Nessuna API ha fornito questa funzionalità per i valori CSIDL.</span><span class="sxs-lookup"><span data-stu-id="b39f9-112">No API provided this functionality for CSIDL values.</span></span> <span data-ttu-id="b39f9-113">Per ulteriori informazioni, vedere [**IKnownFolderManager:: GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) .</span><span class="sxs-lookup"><span data-stu-id="b39f9-113">See [**IKnownFolderManager::GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) for more information.</span></span>
-   <span data-ttu-id="b39f9-114">Una cartella nota aggiunta da un ISV può aggiungere proprietà personalizzate che consentono di spiegarne lo scopo e l'utilizzo previsto.</span><span class="sxs-lookup"><span data-stu-id="b39f9-114">A known folder added by an ISV can add custom properties that allow it to explain its purpose and intended use.</span></span>
-   <span data-ttu-id="b39f9-115">Molte cartelle note possono essere reindirizzate a nuove posizioni, inclusi i percorsi di rete.</span><span class="sxs-lookup"><span data-stu-id="b39f9-115">Many known folders can be redirected to new locations, including network locations.</span></span> <span data-ttu-id="b39f9-116">Nel sistema CSIDL è possibile reindirizzare solo la cartella **documenti** .</span><span class="sxs-lookup"><span data-stu-id="b39f9-116">Under the CSIDL system, only the **My Documents** folder could be redirected.</span></span>
-   <span data-ttu-id="b39f9-117">Le cartelle note possono avere gestori personalizzati da usare durante la creazione o l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="b39f9-117">Known folders can have custom handlers for use during creation or deletion.</span></span>

<span data-ttu-id="b39f9-118">Il sistema CSIDL e le API che usano i valori CSIDL sono ancora supportati per garantire la compatibilità.</span><span class="sxs-lookup"><span data-stu-id="b39f9-118">The CSIDL system and APIs that make use of CSIDL values are still supported for compatibility.</span></span> <span data-ttu-id="b39f9-119">Tuttavia, non è consigliabile usarli in un nuovo sviluppo.</span><span class="sxs-lookup"><span data-stu-id="b39f9-119">However, it is not recommended to use them in any new development.</span></span>


<span data-ttu-id="b39f9-120">Negli argomenti seguenti vengono illustrate le specifiche del sistema di cartelle note.</span><span class="sxs-lookup"><span data-stu-id="b39f9-120">The following topics discuss the specifics of the Known Folders system.</span></span>

-   [<span data-ttu-id="b39f9-121">Utilizzo di cartelle note nelle applicazioni</span><span class="sxs-lookup"><span data-stu-id="b39f9-121">Working with Known Folders in Applications</span></span>](working-with-known-folders.md)
-   [<span data-ttu-id="b39f9-122">Come estendere le cartelle note con cartelle personalizzate</span><span class="sxs-lookup"><span data-stu-id="b39f9-122">How to Extend Known Folders with Custom Folders</span></span>](how-to-extend-known-folders-with-custom-folders.md)
-   [<span data-ttu-id="b39f9-123">**KNOWNFOLDERID**</span><span class="sxs-lookup"><span data-stu-id="b39f9-123">**KNOWNFOLDERID**</span></span>](knownfolderid.md)

<span data-ttu-id="b39f9-124">Le pagine di riferimento seguenti illustrano le funzioni delle cartelle note Win32, che possono essere usate per recuperare il percorso delle cartelle note o reindirizzarle a una nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="b39f9-124">The following reference pages explain the Win32 Known Folders functions, which can be used to retrieve the location of Known Folders or redirect them to a new location.</span></span> <span data-ttu-id="b39f9-125">Queste funzioni sostituiscono le funzioni Win32 precedenti.</span><span class="sxs-lookup"><span data-stu-id="b39f9-125">These functions replace older Win32 functions.</span></span> <span data-ttu-id="b39f9-126">Le nuove funzioni vengono fornite per fornire un comportamento equivalente alle funzioni precedenti, ma ogni nuova funzione viene duplicata anche da un'API Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="b39f9-126">The new functions are provided to give equivalent behavior to the old functions, but each new function is also duplicated by a Component Object Model (COM) API.</span></span>



| <span data-ttu-id="b39f9-127">Nuova funzione</span><span class="sxs-lookup"><span data-stu-id="b39f9-127">New Function</span></span>                                             | <span data-ttu-id="b39f9-128">Sostituisce</span><span class="sxs-lookup"><span data-stu-id="b39f9-128">Replaces</span></span>                                           | <span data-ttu-id="b39f9-129">Equivalente COM</span><span class="sxs-lookup"><span data-stu-id="b39f9-129">COM Equivalent</span></span>                                            |
|----------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="b39f9-130">**SHGetKnownFolderPath**</span><span class="sxs-lookup"><span data-stu-id="b39f9-130">**SHGetKnownFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)     | [<span data-ttu-id="b39f9-131">**SHGetFolderPath**</span><span class="sxs-lookup"><span data-stu-id="b39f9-131">**SHGetFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)         | [<span data-ttu-id="b39f9-132">**IKnownFolder:: GetPath**</span><span class="sxs-lookup"><span data-stu-id="b39f9-132">**IKnownFolder::GetPath**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)     |
| [<span data-ttu-id="b39f9-133">**SHGetKnownFolderIDList**</span><span class="sxs-lookup"><span data-stu-id="b39f9-133">**SHGetKnownFolderIDList**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) | [<span data-ttu-id="b39f9-134">**SHGetFolderLocation**</span><span class="sxs-lookup"><span data-stu-id="b39f9-134">**SHGetFolderLocation**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) | [<span data-ttu-id="b39f9-135">**IKnownFolder::GetIDList**</span><span class="sxs-lookup"><span data-stu-id="b39f9-135">**IKnownFolder::GetIDList**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist) |
| [<span data-ttu-id="b39f9-136">**SHSetKnownFolderPath**</span><span class="sxs-lookup"><span data-stu-id="b39f9-136">**SHSetKnownFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)     | [<span data-ttu-id="b39f9-137">**SHSetFolderPath**</span><span class="sxs-lookup"><span data-stu-id="b39f9-137">**SHSetFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha)         | [<span data-ttu-id="b39f9-138">**IKnownFolder:: SEPATH**</span><span class="sxs-lookup"><span data-stu-id="b39f9-138">**IKnownFolder::SetPath**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath)     |



 

<span data-ttu-id="b39f9-139">Le pagine di riferimento seguenti illustrano le API di cartelle note di COM, che forniscono tutte le funzionalità delle API Win32 elencate in precedenza, oltre ad aggiungere la possibilità di enumerare tutte le cartelle note, accedere alle proprietà della cartella note ed estendere il set standard di cartelle note.</span><span class="sxs-lookup"><span data-stu-id="b39f9-139">The following reference pages explain the COM Known Folders APIs, which provide all of the functionality of the Win32 APIs listed above, plus add the ability to enumerate all Known Folders, access Known Folder properties, and extend the standard set of Known Folders.</span></span>

-   [<span data-ttu-id="b39f9-140">**IKnownFolder**</span><span class="sxs-lookup"><span data-stu-id="b39f9-140">**IKnownFolder**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder)
-   [<span data-ttu-id="b39f9-141">**IKnownFolderManager**</span><span class="sxs-lookup"><span data-stu-id="b39f9-141">**IKnownFolderManager**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

<span data-ttu-id="b39f9-142">Un esempio di C++ che illustra le API delle cartelle note è incluso in Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="b39f9-142">A C++ sample that demonstrates the Known Folder APIs is included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b39f9-143">Una volta installato il Windows SDK nel computer, l'esempio si trova in% ProgramFiles% \\ Microsoft SDK \\ Windows \\ v 6.0 \\ Samples \\ WinUI \\ Shell \\ AppPlatform \\ KnownFolders.</span><span class="sxs-lookup"><span data-stu-id="b39f9-143">Once you have installed the Windows SDK on your computer, the sample can be found under %ProgramFiles%\\Microsoft SDKs\\Windows\\v6.0\\Samples\\WinUI\\Shell\\AppPlatform\\KnownFolders.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b39f9-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b39f9-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b39f9-145">[Esempio di cartelle note](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b39f9-145">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
