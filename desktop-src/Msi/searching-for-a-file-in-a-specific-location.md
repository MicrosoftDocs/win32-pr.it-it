---
description: Durante un'installazione di Windows Installer, il programma di installazione può cercare un file in un percorso specifico nel sistema dell'utente.
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: Ricerca di un file in un percorso specifico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ad4e456d331119b698d8e6e696e86b953006eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529497"
---
# <a name="searching-for-a-file-in-a-specific-location"></a><span data-ttu-id="b62a9-103">Ricerca di un file in un percorso specifico</span><span class="sxs-lookup"><span data-stu-id="b62a9-103">Searching for a File in a Specific Location</span></span>

<span data-ttu-id="b62a9-104">**Per cercare un file in un percorso specifico in un sistema utente**</span><span class="sxs-lookup"><span data-stu-id="b62a9-104">**To search for a file in a specific location on a user system**</span></span>

1.  <span data-ttu-id="b62a9-105">Elencare la firma e il nome del file nella [tabella della firma](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="b62a9-105">List the file signature and name in the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="b62a9-106">I campi rimanenti di questo record possono essere null per cercare qualsiasi versione di MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="b62a9-106">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    [<span data-ttu-id="b62a9-107">Tabella di firma</span><span class="sxs-lookup"><span data-stu-id="b62a9-107">Signature Table</span></span>](signature-table.md)

    

    | <span data-ttu-id="b62a9-108">Firma</span><span class="sxs-lookup"><span data-stu-id="b62a9-108">Signature</span></span>          | <span data-ttu-id="b62a9-109">Nome file</span><span class="sxs-lookup"><span data-stu-id="b62a9-109">File name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="b62a9-110">AppFile</span><span class="sxs-lookup"><span data-stu-id="b62a9-110">AppFile</span></span><br/> | <span data-ttu-id="b62a9-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="b62a9-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="b62a9-112">Immettere la proprietà che verrà impostata dal programma di installazione se MyApp.exe è installato.</span><span class="sxs-lookup"><span data-stu-id="b62a9-112">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    <span data-ttu-id="b62a9-113">[Tabella AppSearch](appsearch-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="b62a9-113">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="b62a9-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b62a9-114">Property</span></span>         | <span data-ttu-id="b62a9-115">Firma</span><span class="sxs-lookup"><span data-stu-id="b62a9-115">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="b62a9-116">MYAPP</span><span class="sxs-lookup"><span data-stu-id="b62a9-116">MYAPP</span></span><br/> | <span data-ttu-id="b62a9-117">AppFile</span><span class="sxs-lookup"><span data-stu-id="b62a9-117">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="b62a9-118">Usare la [tabella DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="b62a9-118">Use the [DrLocator Table](drlocator-table.md).</span></span> <span data-ttu-id="b62a9-119">Immettere il percorso completo del file nel sistema utente nel campo percorso.</span><span class="sxs-lookup"><span data-stu-id="b62a9-119">Enter the full path to the file on the user system in the Path field.</span></span> <span data-ttu-id="b62a9-120">Immettere il valore 0 nella colonna profondità per eseguire la ricerca nella cartella bin.</span><span class="sxs-lookup"><span data-stu-id="b62a9-120">Enter a value of 0 into the Depth column to search the bin folder.</span></span>

    [<span data-ttu-id="b62a9-121">Tabella DrLocator</span><span class="sxs-lookup"><span data-stu-id="b62a9-121">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="b62a9-122">Firma</span><span class="sxs-lookup"><span data-stu-id="b62a9-122">Signature</span></span>          | <span data-ttu-id="b62a9-123">Padre</span><span class="sxs-lookup"><span data-stu-id="b62a9-123">Parent</span></span> | <span data-ttu-id="b62a9-124">Percorso</span><span class="sxs-lookup"><span data-stu-id="b62a9-124">Path</span></span>                                                    | <span data-ttu-id="b62a9-125">Profondità</span><span class="sxs-lookup"><span data-stu-id="b62a9-125">Depth</span></span>        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | <span data-ttu-id="b62a9-126">AppFile</span><span class="sxs-lookup"><span data-stu-id="b62a9-126">AppFile</span></span><br/> |        | <span data-ttu-id="b62a9-127">C: \\ programmi programmi per \\ prodotti \\ software \\ bin</span><span class="sxs-lookup"><span data-stu-id="b62a9-127">C:\\Program Files\\MyProducts\\Projects\\bin</span></span><br/> | <span data-ttu-id="b62a9-128">0</span><span class="sxs-lookup"><span data-stu-id="b62a9-128">0</span></span><br/> |

    

     

4.  <span data-ttu-id="b62a9-129">Includere l'azione AppSearch nella sequenza di azione.</span><span class="sxs-lookup"><span data-stu-id="b62a9-129">Include the AppSearch action in the action sequence.</span></span> <span data-ttu-id="b62a9-130">Se MyApp.exe è installato in C: \\ Program Files \\ prodotti prodotti \\ \\ bin, il programma di installazione imposta la proprietà MyApp sul percorso del file.</span><span class="sxs-lookup"><span data-stu-id="b62a9-130">If MyApp.exe is installed in C:\\Program Files\\MyProducts\\Projects\\bin, the Installer sets the property MYAPP to the location of file.</span></span>

 

 




