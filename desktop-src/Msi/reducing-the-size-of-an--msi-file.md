---
description: Gli sviluppatori di Windows Installer pacchetti possono notare che i file con estensione msi hanno dimensioni maggiori del previsto dopo modifiche e salvataggi ripetuti.
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: Riduzione delle dimensioni di un file con estensione msi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5a19c92f0567fc6081d772279ec2cc0b6cafef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967411"
---
# <a name="reducing-the-size-of-an-msi-file"></a><span data-ttu-id="9ac1d-103">Riduzione delle dimensioni di un file con estensione msi</span><span class="sxs-lookup"><span data-stu-id="9ac1d-103">Reducing the Size of an .msi File</span></span>

<span data-ttu-id="9ac1d-104">Gli sviluppatori di Windows Installer pacchetti possono notare che i file con estensione msi hanno dimensioni maggiori del previsto dopo modifiche e salvataggi ripetuti.</span><span class="sxs-lookup"><span data-stu-id="9ac1d-104">Developers of Windows Installer packages may notice their .msi files getting larger than expected after repeated edits and saves.</span></span> <span data-ttu-id="9ac1d-105">Windows Installer file con estensione msi sono file composti che contengono archivi e flussi e presentano alcune delle stesse limitazioni di archiviazione dei file di documento OLE.</span><span class="sxs-lookup"><span data-stu-id="9ac1d-105">Windows Installer .msi files are compound files that contain storages and streams, and have some of the same storage limitations as OLE document files.</span></span> <span data-ttu-id="9ac1d-106">Se si modifica e si salva lo stesso file con estensione MSI più volte, viene creato uno spazio di archiviazione sprecato nel file.</span><span class="sxs-lookup"><span data-stu-id="9ac1d-106">If you edit and save the same .msi file over and over, it creates wasted storage space in the file.</span></span> <span data-ttu-id="9ac1d-107">Questa operazione interessa solo gli autori dei file con estensione msi e non ha alcun effetto sugli utenti Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9ac1d-107">This only affects authors of .msi files and has no effect on Windows Installer users.</span></span> <span data-ttu-id="9ac1d-108">Gli sviluppatori potrebbero voler rimuovere lo spazio di archiviazione sprecato prima di spedire il file con estensione msi finale.</span><span class="sxs-lookup"><span data-stu-id="9ac1d-108">Developers may want to remove this wasted storage space before shipping their final .msi file.</span></span>

<span data-ttu-id="9ac1d-109">Per rimuovere lo spazio di archiviazione sprecato e ridurre la dimensione finale dei file con estensione msi, sono disponibili le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="9ac1d-109">To remove wasted storage space and reduce the final size of .msi files, you have the following options.</span></span>

-   <span data-ttu-id="9ac1d-110">Esportare tutte le tabelle del database nei file con estensione IDT e quindi importarli in un nuovo database.</span><span class="sxs-lookup"><span data-stu-id="9ac1d-110">Export all of the tables in the database to .idt files, and then import those into a new database.</span></span> <span data-ttu-id="9ac1d-111">Questo consente di ottenere l'archiviazione più compatta possibile.</span><span class="sxs-lookup"><span data-stu-id="9ac1d-111">This produces the most compact storage possible.</span></span>
-   <span data-ttu-id="9ac1d-112">Utilizzare un'utilità software per compattare lo spazio di archiviazione dei file di documento OLE.</span><span class="sxs-lookup"><span data-stu-id="9ac1d-112">Use a software utility for compacting the storage space of OLE document files.</span></span>

 

 



