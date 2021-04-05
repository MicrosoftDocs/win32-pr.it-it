---
description: Durante un'installazione di Windows Installer, il programma di installazione può cercare un file e creare una proprietà contenente il percorso del file.
ms.assetid: 6587b349-852d-4d4e-a8d4-76dfb0ef0f0b
title: Ricerca di un file e creazione di una proprietà che contiene il percorso del file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed742ee874c2e4b76137e9f17e90fbf54e9729f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882709"
---
# <a name="searching-for-a-file-and-creating-a-property-holding-the-files-path"></a><span data-ttu-id="41ac2-103">Ricerca di un file e creazione di una proprietà che contiene il percorso del file</span><span class="sxs-lookup"><span data-stu-id="41ac2-103">Searching for a File and Creating a Property Holding the File's Path</span></span>

<span data-ttu-id="41ac2-104">**Per cercare un file e creare una proprietà contenente il percorso del file**</span><span class="sxs-lookup"><span data-stu-id="41ac2-104">**To search for a file and create a property holding the path of that file**</span></span>

1.  <span data-ttu-id="41ac2-105">Eseguire innanzitutto una ricerca del file elencando la firma e il nome del file nella [tabella della firma](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="41ac2-105">First do a search for the file by listing the file signature and name in the [Signature Table](signature-table.md).</span></span>

    <span data-ttu-id="41ac2-106">I campi rimanenti di questo record possono essere lasciati vuoti per specificare la ricerca di qualsiasi versione di MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="41ac2-106">The remaining fields of this record can be left empty to specify a search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="41ac2-107">[Tabella delle firme](signature-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="41ac2-107">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="41ac2-108">Firma</span><span class="sxs-lookup"><span data-stu-id="41ac2-108">Signature</span></span>          | <span data-ttu-id="41ac2-109">Nome file</span><span class="sxs-lookup"><span data-stu-id="41ac2-109">File name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="41ac2-110">AppFile</span><span class="sxs-lookup"><span data-stu-id="41ac2-110">AppFile</span></span><br/> | <span data-ttu-id="41ac2-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="41ac2-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="41ac2-112">Specificare quindi il percorso del file in cui viene eseguita la ricerca nella [tabella DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="41ac2-112">Next, specify the path of the file that is being searched for in the [DrLocator Table](drlocator-table.md).</span></span>

    <span data-ttu-id="41ac2-113">Poiché AppFolder non è elencato nella [tabella Signature](signature-table.md), il programma di installazione determina che appfolder è una cartella anziché un file.</span><span class="sxs-lookup"><span data-stu-id="41ac2-113">Because AppFolder is not listed in the [Signature Table](signature-table.md), the Installer determines that AppFolder is a folder rather than a file.</span></span>

    [<span data-ttu-id="41ac2-114">Tabella DrLocator</span><span class="sxs-lookup"><span data-stu-id="41ac2-114">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="41ac2-115">Firma</span><span class="sxs-lookup"><span data-stu-id="41ac2-115">Signature</span></span>            | <span data-ttu-id="41ac2-116">Padre</span><span class="sxs-lookup"><span data-stu-id="41ac2-116">Parent</span></span>             | <span data-ttu-id="41ac2-117">Percorso</span><span class="sxs-lookup"><span data-stu-id="41ac2-117">Path</span></span> | <span data-ttu-id="41ac2-118">Profondità</span><span class="sxs-lookup"><span data-stu-id="41ac2-118">Depth</span></span> |
    |----------------------|--------------------|------|-------|
    | <span data-ttu-id="41ac2-119">AppFile</span><span class="sxs-lookup"><span data-stu-id="41ac2-119">AppFile</span></span><br/>   |                    |      |       |
    | <span data-ttu-id="41ac2-120">AppFolder</span><span class="sxs-lookup"><span data-stu-id="41ac2-120">AppFolder</span></span><br/> | <span data-ttu-id="41ac2-121">AppFile</span><span class="sxs-lookup"><span data-stu-id="41ac2-121">AppFile</span></span><br/> |      |       |

    

     

3.  <span data-ttu-id="41ac2-122">Infine, popolare la [tabella AppSearch](appsearch-table.md) in modo che l' [azione AppSearch](appsearch-action.md) restituisca il percorso di AppFolder.</span><span class="sxs-lookup"><span data-stu-id="41ac2-122">Finally, populate the [AppSearch Table](appsearch-table.md) so that the [AppSearch Action](appsearch-action.md) returns the path of AppFolder.</span></span>

    <span data-ttu-id="41ac2-123">Dopo che il programma di installazione ha eseguito l'azione AppSearch, il valore di fileFolder è il percorso completo di AppFolder.</span><span class="sxs-lookup"><span data-stu-id="41ac2-123">After the Installer executes the AppSearch action, the value of MYFOLDER is the full path of AppFolder.</span></span>

    <span data-ttu-id="41ac2-124">[Tabella AppSearch](appsearch-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="41ac2-124">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="41ac2-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="41ac2-125">Property</span></span>            | <span data-ttu-id="41ac2-126">Firma</span><span class="sxs-lookup"><span data-stu-id="41ac2-126">Signature</span></span>            |
    |---------------------|----------------------|
    | <span data-ttu-id="41ac2-127">MYFOLDER</span><span class="sxs-lookup"><span data-stu-id="41ac2-127">MYFOLDER</span></span><br/> | <span data-ttu-id="41ac2-128">AppFolder</span><span class="sxs-lookup"><span data-stu-id="41ac2-128">AppFolder</span></span><br/> |

    

     

 

 




