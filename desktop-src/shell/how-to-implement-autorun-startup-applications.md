---
description: Non esistono essenzialmente vincoli per la scrittura di un'applicazione di avvio automatico.
ms.assetid: 6D95E5F0-8D93-47A8-9D8C-49CBDCA150A7
title: Come implementare le applicazioni di avvio AutoRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b553e102f574835103898b17558541000633412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967445"
---
# <a name="how-to-implement-autorun-startup-applications"></a><span data-ttu-id="7e825-103">Come implementare le applicazioni di avvio AutoRun</span><span class="sxs-lookup"><span data-stu-id="7e825-103">How to Implement AutoRun Startup Applications</span></span>

<span data-ttu-id="7e825-104">Non esistono essenzialmente vincoli per la scrittura di un'applicazione di avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="7e825-104">There are essentially no constraints on how to write an AutoRun startup application.</span></span> <span data-ttu-id="7e825-105">È possibile implementare l'applicazione di avvio per eseguire tutte le operazioni necessarie per installare, disinstallare, configurare o eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e825-105">You can implement the startup application to do whatever you find necessary to install, uninstall, configure, or run your application.</span></span> <span data-ttu-id="7e825-106">Tuttavia, i suggerimenti seguenti forniscono alcune linee guida per l'implementazione di un'applicazione di avvio AutoRun efficace.</span><span class="sxs-lookup"><span data-stu-id="7e825-106">However, the following tips provide some guidelines to implementing an effective AutoRun startup application.</span></span>

## <a name="instructions"></a><span data-ttu-id="7e825-107">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="7e825-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="7e825-108">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="7e825-108">Step 1:</span></span>

<span data-ttu-id="7e825-109">Assicurarsi che gli utenti ricevano il feedback appena possibile dopo aver inserito un disco di AutoRun nell'unità.</span><span class="sxs-lookup"><span data-stu-id="7e825-109">Make sure that users receive feedback as soon as possible after they insert an AutoRun disc into the drive.</span></span> <span data-ttu-id="7e825-110">Le applicazioni di avvio devono essere piccoli programmi che si caricano rapidamente.</span><span class="sxs-lookup"><span data-stu-id="7e825-110">Startup applications should be small programs that load quickly.</span></span> <span data-ttu-id="7e825-111">Devono identificare chiaramente l'applicazione e fornire un modo semplice per annullare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7e825-111">They should clearly identify the application and provide an easy way to cancel the operation.</span></span>

### <a name="step-2"></a><span data-ttu-id="7e825-112">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="7e825-112">Step 2:</span></span>

<span data-ttu-id="7e825-113">Verificare se il programma è già installato.</span><span class="sxs-lookup"><span data-stu-id="7e825-113">Check to see if the program is already installed.</span></span> <span data-ttu-id="7e825-114">In caso contrario, il passaggio successivo sarà probabilmente la procedura di installazione.</span><span class="sxs-lookup"><span data-stu-id="7e825-114">If not, the next step will probably be the setup procedure.</span></span> <span data-ttu-id="7e825-115">L'applicazione di avvio può trarre vantaggio dal tempo impiegato dall'utente per leggere la finestra di dialogo avviando un altro thread per iniziare a caricare il codice di installazione.</span><span class="sxs-lookup"><span data-stu-id="7e825-115">The startup application can take advantage of the time the user spends reading the dialog box by starting another thread to begin loading the setup code.</span></span> <span data-ttu-id="7e825-116">Quando l'utente fa clic su **OK**, il programma di installazione sarà già in parte se non è completamente caricato.</span><span class="sxs-lookup"><span data-stu-id="7e825-116">By the time the user clicks **OK**, your setup program will already be partly if not fully loaded.</span></span> <span data-ttu-id="7e825-117">Questo approccio riduce significativamente la percezione dell'utente della quantità di tempo necessaria per caricare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e825-117">This approach significantly reduces the user's perception of the amount of time it takes to load your application.</span></span>

> [!Note]  
> <span data-ttu-id="7e825-118">In genere, la parte iniziale dell'applicazione di avvio presenta agli utenti un'interfaccia utente, ad esempio una finestra di dialogo, in cui viene chiesto come procedere.</span><span class="sxs-lookup"><span data-stu-id="7e825-118">Typically, the initial part of the startup application presents users with a user interface, such as a dialog box, asking them how they would like to proceed.</span></span>

 

### <a name="step-3"></a><span data-ttu-id="7e825-119">Passaggio 3:</span><span class="sxs-lookup"><span data-stu-id="7e825-119">Step 3:</span></span>

<span data-ttu-id="7e825-120">Avviare un altro thread per iniziare a caricare il codice dell'applicazione per ridurre il tempo di attesa per l'utente.</span><span class="sxs-lookup"><span data-stu-id="7e825-120">Start another thread to begin loading application code to shorten the waiting time for the user.</span></span> <span data-ttu-id="7e825-121">Se l'applicazione è già stata installata, è probabile che l'utente abbia inserito il disco per l'esecuzione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e825-121">If the application has already been installed, the user probably inserted the disk to run the application.</span></span>

### <a name="step-4"></a><span data-ttu-id="7e825-122">Passaggio 4:</span><span class="sxs-lookup"><span data-stu-id="7e825-122">Step 4:</span></span>

<span data-ttu-id="7e825-123">Utilizzare gli hint seguenti per ridurre al minimo l'utilizzo del disco rigido:</span><span class="sxs-lookup"><span data-stu-id="7e825-123">Use the following hints to minimize hard disk usage:</span></span>

-   <span data-ttu-id="7e825-124">Tenere al minimo il numero di file che devono essere presenti sul disco rigido.</span><span class="sxs-lookup"><span data-stu-id="7e825-124">Keep the number of files that must be on the hard disk to a minimum.</span></span> <span data-ttu-id="7e825-125">Devono essere limitate a file essenziali per l'esecuzione del programma o che richiederebbe una quantità di tempo inaccettabile per la lettura da parte dei supporti.</span><span class="sxs-lookup"><span data-stu-id="7e825-125">They should be restricted to files that are essential to running the program or that would take an unacceptably large amount of time to read from the media.</span></span>
-   <span data-ttu-id="7e825-126">In molti casi, l'installazione di file non essenziali sul disco rigido non è necessaria, ma potrebbe offrire vantaggi come un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="7e825-126">In many cases, installing nonessential files on the hard disk is not necessary, but might provide benefits such as increased performance.</span></span> <span data-ttu-id="7e825-127">Fornire all'utente la possibilità di decidere come fare il compromesso tra i costi e i vantaggi dell'archiviazione su disco rigido.</span><span class="sxs-lookup"><span data-stu-id="7e825-127">Give the user the option of deciding how to make the trade-off between the costs and benefits of hard disk storage.</span></span>
-   <span data-ttu-id="7e825-128">Fornire un modo per disinstallare tutti i componenti che sono stati posizionati sul disco rigido.</span><span class="sxs-lookup"><span data-stu-id="7e825-128">Provide a way to uninstall any components that were placed on the hard disk.</span></span>
-   <span data-ttu-id="7e825-129">Se l'applicazione memorizza nella cache i dati, fornire all'utente un controllo su di essa.</span><span class="sxs-lookup"><span data-stu-id="7e825-129">If your application caches data, give the user some control over it.</span></span> <span data-ttu-id="7e825-130">Includere le opzioni nell'applicazione di avvio, ad esempio l'impostazione di un limite per la quantità massima di dati memorizzati nella cache che verranno archiviati nel disco rigido o l'eliminazione di tutti i dati memorizzati nella cache al termine dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e825-130">Include options in the startup application such as setting a limit on the maximum amount of cached data that will be stored on the hard disk, or having the application discard any cached data when it terminates.</span></span>

### <a name="step-5"></a><span data-ttu-id="7e825-131">Passaggio 5:</span><span class="sxs-lookup"><span data-stu-id="7e825-131">Step 5:</span></span>

<span data-ttu-id="7e825-132">Se necessario, disabilitare autorun.</span><span class="sxs-lookup"><span data-stu-id="7e825-132">Disable Autorun if needed.</span></span> <span data-ttu-id="7e825-133">L'esecuzione automatica può essere evitata a livello di codice o disabilitata interamente con il registro di sistema, anche quando un supporto include un file Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="7e825-133">AutoRun can be suppressed programmatically or disabled entirely with the registry, even when a medium has an Autorun.inf file.</span></span> <span data-ttu-id="7e825-134">Per ulteriori informazioni, vedere [Abilitazione e disabilitazione dell'esecuzione automatica](autoplay-reg.md) .</span><span class="sxs-lookup"><span data-stu-id="7e825-134">See [Enabling and Disabling AutoRun](autoplay-reg.md) for more information.</span></span>

 

 



