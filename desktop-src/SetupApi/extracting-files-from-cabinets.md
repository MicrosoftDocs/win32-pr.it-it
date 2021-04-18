---
description: È possibile estrarre i file da un file CAB in due modi. Il primo e il modo più semplice consiste nel sfruttare l'elaborazione automatica del cabinet incorporata nelle funzioni di installazione.
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: Estrazione di file da file CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94f413b4ad0ee1511dde21af747cd2665a4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308107"
---
# <a name="extracting-files-from-cabinets"></a><span data-ttu-id="00301-104">Estrazione di file da file CAB</span><span class="sxs-lookup"><span data-stu-id="00301-104">Extracting Files from Cabinets</span></span>

<span data-ttu-id="00301-105">È possibile estrarre i file da un file CAB in due modi.</span><span class="sxs-lookup"><span data-stu-id="00301-105">You can extract files from a cabinet in two ways.</span></span> <span data-ttu-id="00301-106">Il primo e il modo più semplice consiste nel sfruttare l'elaborazione automatica del cabinet incorporata nelle funzioni di installazione.</span><span class="sxs-lookup"><span data-stu-id="00301-106">The first and simplest way is to take advantage of the automatic cabinet processing built into the setup functions.</span></span>

<span data-ttu-id="00301-107">Le funzioni di installazione, ad esempio [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)e [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), controllano la compressione in ogni file.</span><span class="sxs-lookup"><span data-stu-id="00301-107">The installation functions, such as [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), and [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), check the compression on each file.</span></span> <span data-ttu-id="00301-108">Se il file si trova in un file CAB, le funzioni cercano innanzitutto un file con tale nome all'esterno del cabinet.</span><span class="sxs-lookup"><span data-stu-id="00301-108">If the file is in a cabinet, the functions first search for a file of that name outside the cabinet.</span></span> <span data-ttu-id="00301-109">Se trovate, le funzioni installano il file esterno, ignorando il file all'interno del cabinet.</span><span class="sxs-lookup"><span data-stu-id="00301-109">If found, the functions install the external file, ignoring the file inside the cabinet.</span></span> <span data-ttu-id="00301-110">In questo modo è possibile aggiornare un singolo file all'interno del cabinet senza ricompilare il file CAB.</span><span class="sxs-lookup"><span data-stu-id="00301-110">This enables you to update a single file inside the cabinet without rebuilding the cabinet.</span></span>

<span data-ttu-id="00301-111">Le funzioni di installazione tengono inoltre traccia dei file di un file CAB che sono stati recuperati, in modo che un file venga estratto una sola volta, anche se viene installato più volte.</span><span class="sxs-lookup"><span data-stu-id="00301-111">The setup functions also track which files in a cabinet have been retrieved, so that a file is extracted only once, even if it is installed several times.</span></span>

<span data-ttu-id="00301-112">Il secondo modo per estrarre i file da un file CAB consiste nell'usare [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="00301-112">The second way to extract files from a cabinet is by using [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="00301-113">Questa funzione esegue l'iterazione di ogni file in un file CAB, inviando una notifica a una routine di callback per ogni file trovato.</span><span class="sxs-lookup"><span data-stu-id="00301-113">This function iterates through each file in a cabinet, sending a notification to a callback routine for each file found.</span></span> <span data-ttu-id="00301-114">La routine di callback restituisce quindi un valore che indica se il file deve essere estratto o ignorato.</span><span class="sxs-lookup"><span data-stu-id="00301-114">The callback routine then returns a value that indicates whether the file should be extracted or skipped.</span></span>

> [!Note]  
> <span data-ttu-id="00301-115">L'API di installazione non fornisce una routine di callback predefinita per la gestione delle notifiche del cabinet.</span><span class="sxs-lookup"><span data-stu-id="00301-115">The Setup API does not supply a default callback routine to handle cabinet notifications.</span></span> <span data-ttu-id="00301-116">Se si chiama [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) in modo esplicito, è necessario fornire una routine di callback per elaborare le notifiche del cabinet restituite dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="00301-116">If you call [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) explicitly, you must supply a callback routine to process the cabinet notifications that the function returns.</span></span>

 

 

 



