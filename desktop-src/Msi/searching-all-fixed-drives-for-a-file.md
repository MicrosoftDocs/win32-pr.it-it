---
description: Durante un'installazione di Windows Installer, il programma di installazione può eseguire ricerche in tutte le unità fisse per un file.
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: Ricerca in tutte le unità fisse per un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b79c7f2999d4ee7937790dc68470210f1d4b2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313793"
---
# <a name="searching-all-fixed-drives-for-a-file"></a><span data-ttu-id="6fc9c-103">Ricerca in tutte le unità fisse per un file</span><span class="sxs-lookup"><span data-stu-id="6fc9c-103">Searching All Fixed Drives for a File</span></span>

<span data-ttu-id="6fc9c-104">**Per eseguire la ricerca in tutte le unità fisse di un file**</span><span class="sxs-lookup"><span data-stu-id="6fc9c-104">**To search all fixed drives for a file**</span></span>

1.  <span data-ttu-id="6fc9c-105">Immettere la firma e il nome del file nella [tabella della firma](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="6fc9c-105">Enter the file signature and name in the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="6fc9c-106">I campi rimanenti di questo record possono essere null per cercare qualsiasi versione di MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-106">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="6fc9c-107">[Tabella delle firme](signature-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="6fc9c-107">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="6fc9c-108">Firma</span><span class="sxs-lookup"><span data-stu-id="6fc9c-108">Signature</span></span>          | <span data-ttu-id="6fc9c-109">File Name</span><span class="sxs-lookup"><span data-stu-id="6fc9c-109">File Name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="6fc9c-110">AppFile</span><span class="sxs-lookup"><span data-stu-id="6fc9c-110">AppFile</span></span><br/> | <span data-ttu-id="6fc9c-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="6fc9c-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="6fc9c-112">Immettere la proprietà che verrà impostata dal programma di installazione se MyApp.exe è installato.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-112">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    [<span data-ttu-id="6fc9c-113">Tabella AppSearch</span><span class="sxs-lookup"><span data-stu-id="6fc9c-113">AppSearch Table</span></span>](appsearch-table.md)

    

    | <span data-ttu-id="6fc9c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6fc9c-114">Property</span></span>         | <span data-ttu-id="6fc9c-115">Firma</span><span class="sxs-lookup"><span data-stu-id="6fc9c-115">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="6fc9c-116">MYAPP</span><span class="sxs-lookup"><span data-stu-id="6fc9c-116">MYAPP</span></span><br/> | <span data-ttu-id="6fc9c-117">AppFile</span><span class="sxs-lookup"><span data-stu-id="6fc9c-117">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="6fc9c-118">Usare la [tabella DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="6fc9c-118">Use the [DrLocator Table](drlocator-table.md).</span></span> <span data-ttu-id="6fc9c-119">Lasciare vuoti i campi padre e percorso per eseguire la ricerca in tutte le unità fisse del sistema utente.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-119">Leave the Parent and Path fields empty to search all fixed drives of the user system.</span></span> <span data-ttu-id="6fc9c-120">Specificare nella colonna profondità il numero di livelli di sottodirectory in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-120">Specify in the Depth column the number of subdirectory levels to search.</span></span> <span data-ttu-id="6fc9c-121">Se ad esempio si imposta depth su 0, viene rilevato c: \\MyApp.exe, ma il file non viene rilevato con una profondità di 2, ad esempio: c: \\ Program Files \\ app \\MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-121">For example, setting Depth to 0 detects c:\\MyApp.exe, but does not detect the file at a depth of 2, for example: c:\\Program Files\\MyApps\\MyApp.exe.</span></span>

    [<span data-ttu-id="6fc9c-122">Tabella DrLocator</span><span class="sxs-lookup"><span data-stu-id="6fc9c-122">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="6fc9c-123">Firma</span><span class="sxs-lookup"><span data-stu-id="6fc9c-123">Signature</span></span>          | <span data-ttu-id="6fc9c-124">Padre</span><span class="sxs-lookup"><span data-stu-id="6fc9c-124">Parent</span></span> | <span data-ttu-id="6fc9c-125">Percorso</span><span class="sxs-lookup"><span data-stu-id="6fc9c-125">Path</span></span> | <span data-ttu-id="6fc9c-126">Profondità</span><span class="sxs-lookup"><span data-stu-id="6fc9c-126">Depth</span></span>        |
    |--------------------|--------|------|--------------|
    | <span data-ttu-id="6fc9c-127">AppFile</span><span class="sxs-lookup"><span data-stu-id="6fc9c-127">AppFile</span></span><br/> |        |      | <span data-ttu-id="6fc9c-128">3</span><span class="sxs-lookup"><span data-stu-id="6fc9c-128">3</span></span><br/> |

    

     

4.  <span data-ttu-id="6fc9c-129">Includere l'azione AppSearch nella sequenza di azione.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-129">Include the AppSearch action in the action sequence.</span></span> <span data-ttu-id="6fc9c-130">Se MyApp.exe è installato, il programma di installazione imposta la proprietà MYAPP sul percorso del file.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-130">If MyApp.exe is installed, the Installer sets the property MYAPP to the location of the file.</span></span> <span data-ttu-id="6fc9c-131">Se il file è installato, MYAPP restituisce true in un'espressione condizionale.</span><span class="sxs-lookup"><span data-stu-id="6fc9c-131">If the file is installed, MYAPP evaluates as True in a conditional expression.</span></span>

 

 




