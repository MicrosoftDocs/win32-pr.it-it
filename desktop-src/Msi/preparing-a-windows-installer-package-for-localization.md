---
description: Attenersi a queste linee guida per semplificare la localizzazione dei pacchetti di Windows Installer.
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: Preparazione di un pacchetto di Windows Installer per la localizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa46af5259b880398aa84dc817eb201bd63456eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305631"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a><span data-ttu-id="7c10c-103">Preparazione di un pacchetto di Windows Installer per la localizzazione</span><span class="sxs-lookup"><span data-stu-id="7c10c-103">Preparing a Windows Installer Package for Localization</span></span>

<span data-ttu-id="7c10c-104">La localizzazione di un pacchetto di Windows Installer in più lingue può essere molto semplificata seguendo questa procedura:</span><span class="sxs-lookup"><span data-stu-id="7c10c-104">Localization of a Windows Installer package into multiple languages can be greatly facilitated by doing the following:</span></span>

-   <span data-ttu-id="7c10c-105">Creare un database di installazione di base indipendente dalla tabella codici.</span><span class="sxs-lookup"><span data-stu-id="7c10c-105">Author a base installation database that is code page neutral.</span></span> <span data-ttu-id="7c10c-106">Vedere la [pagina relativa alla creazione di un database con una tabella codici indipendente](creating-a-database-with-a-neutral-code-page.md).</span><span class="sxs-lookup"><span data-stu-id="7c10c-106">See [Creating a database with a neutral code page](creating-a-database-with-a-neutral-code-page.md).</span></span> <span data-ttu-id="7c10c-107">La tabella codici del database localizzato può quindi essere impostata importando una tabella di archiviazione di testo con una tabella codici non neutra nel database di base.</span><span class="sxs-lookup"><span data-stu-id="7c10c-107">The code page of the localized database can then be set by importing a text archive table with a non-neutral code page into the base database.</span></span> <span data-ttu-id="7c10c-108">Vedere [impostazione della tabella codici di un database](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="7c10c-108">See [Setting the code page of a database](setting-the-code-page-of-a-database.md).</span></span>
-   <span data-ttu-id="7c10c-109">Organizzare i file che richiedono la localizzazione in componenti separati e installare questi file in directory separate.</span><span class="sxs-lookup"><span data-stu-id="7c10c-109">Organize files requiring localization into separate components and install these files into separate directories.</span></span> <span data-ttu-id="7c10c-110">In questo modo si garantisce che due pacchetti localizzati non installino mai file con nome identico nella stessa directory.</span><span class="sxs-lookup"><span data-stu-id="7c10c-110">This ensures that two localized packages never install identically named files into the same directory.</span></span>

<span data-ttu-id="7c10c-111">Ad esempio, un'applicazione globale che usa le risorse seguenti può avere tre componenti.</span><span class="sxs-lookup"><span data-stu-id="7c10c-111">For example, a worldwide application using the following resources may have three components.</span></span>



| <span data-ttu-id="7c10c-112">Componente</span><span class="sxs-lookup"><span data-stu-id="7c10c-112">Component</span></span> | <span data-ttu-id="7c10c-113">Risorsa</span><span class="sxs-lookup"><span data-stu-id="7c10c-113">Resource</span></span>                   |
|-----------|----------------------------|
| <span data-ttu-id="7c10c-114">MONDO</span><span class="sxs-lookup"><span data-stu-id="7c10c-114">WORLD</span></span>     | <span data-ttu-id="7c10c-115">worldwide.exe</span><span class="sxs-lookup"><span data-stu-id="7c10c-115">worldwide.exe</span></span>              |
| <span data-ttu-id="7c10c-116">MONDO</span><span class="sxs-lookup"><span data-stu-id="7c10c-116">WORLD</span></span>     | <span data-ttu-id="7c10c-117">voci del registro di sistema nel mondo</span><span class="sxs-lookup"><span data-stu-id="7c10c-117">worldwide registry entries</span></span> |
| <span data-ttu-id="7c10c-118">MONDO</span><span class="sxs-lookup"><span data-stu-id="7c10c-118">WORLD</span></span>     | <span data-ttu-id="7c10c-119">collegamento globale</span><span class="sxs-lookup"><span data-stu-id="7c10c-119">worldwide shortcut</span></span>         |
| <span data-ttu-id="7c10c-120">ENG</span><span class="sxs-lookup"><span data-stu-id="7c10c-120">ENG</span></span>       | <span data-ttu-id="7c10c-121">engui.dll</span><span class="sxs-lookup"><span data-stu-id="7c10c-121">engui.dll</span></span>                  |
| <span data-ttu-id="7c10c-122">ENG</span><span class="sxs-lookup"><span data-stu-id="7c10c-122">ENG</span></span>       | <span data-ttu-id="7c10c-123">readme.txt</span><span class="sxs-lookup"><span data-stu-id="7c10c-123">readme.txt</span></span>                 |
| <span data-ttu-id="7c10c-124">FRA</span><span class="sxs-lookup"><span data-stu-id="7c10c-124">FRA</span></span>       | <span data-ttu-id="7c10c-125">fraui.dll</span><span class="sxs-lookup"><span data-stu-id="7c10c-125">fraui.dll</span></span>                  |
| <span data-ttu-id="7c10c-126">FRA</span><span class="sxs-lookup"><span data-stu-id="7c10c-126">FRA</span></span>       | <span data-ttu-id="7c10c-127">readme.txt</span><span class="sxs-lookup"><span data-stu-id="7c10c-127">readme.txt</span></span>                 |



 

<span data-ttu-id="7c10c-128">I file che devono essere localizzati possono essere installati nei seguenti percorsi di directory:</span><span class="sxs-lookup"><span data-stu-id="7c10c-128">The files that need to be localized may be installed into the following directory locations:</span></span>

-   <span data-ttu-id="7c10c-129">\[ProgramFilesFolder \] \\ World \\worldwide.exe</span><span class="sxs-lookup"><span data-stu-id="7c10c-129">\[ProgramFilesFolder\]\\World\\worldwide.exe</span></span>
-   <span data-ttu-id="7c10c-130">\[\] \\ \\engui.dll inglese del mondo ProgramFilesFolder \\</span><span class="sxs-lookup"><span data-stu-id="7c10c-130">\[ProgramFilesFolder\]\\World\\English\\engui.dll</span></span>
-   <span data-ttu-id="7c10c-131">\[\] \\ \\readme.txt inglese del mondo ProgramFilesFolder \\</span><span class="sxs-lookup"><span data-stu-id="7c10c-131">\[ProgramFilesFolder\]\\World\\English\\readme.txt</span></span>
-   <span data-ttu-id="7c10c-132">\[\] \\ \\fraui.dll francese del mondo ProgramFilesFolder \\</span><span class="sxs-lookup"><span data-stu-id="7c10c-132">\[ProgramFilesFolder\]\\World\\French\\fraui.dll</span></span>
-   <span data-ttu-id="7c10c-133">\[\] \\ \\readme.txt francese del mondo ProgramFilesFolder \\</span><span class="sxs-lookup"><span data-stu-id="7c10c-133">\[ProgramFilesFolder\]\\World\\French\\readme.txt</span></span>

 

 



