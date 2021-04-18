---
description: .
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Heap a tolleranza di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349c8c3d6d066de3d563880c169c8dde2e062370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318884"
---
# <a name="fault-tolerant-heap"></a><span data-ttu-id="e6224-103">Heap a tolleranza di errore</span><span class="sxs-lookup"><span data-stu-id="e6224-103">Fault Tolerant Heap</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="e6224-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="e6224-104">Affected Platforms</span></span>

<span data-ttu-id="e6224-105">**Client-** Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6224-105">**Clients -** Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="e6224-106">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="e6224-106">Feature Impact</span></span>

 <span data-ttu-id="e6224-107">**Gravità-** Media</span><span class="sxs-lookup"><span data-stu-id="e6224-107">**Severity -** Medium</span></span>  
<span data-ttu-id="e6224-108">**Frequenza-** Basso</span><span class="sxs-lookup"><span data-stu-id="e6224-108">**Frequency -** Low</span></span>  


## <a name="description"></a><span data-ttu-id="e6224-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6224-109">Description</span></span>

<span data-ttu-id="e6224-110">L'heap a tolleranza di errore (FTH) è un sottosistema di Windows 7 responsabile del monitoraggio degli arresti anomali dell'applicazione e dell'applicazione autonoma delle mitigazioni per impedire arresti anomali futuri in base alle singole applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e6224-110">The Fault Tolerant Heap (FTH) is a subsystem of Windows 7 responsible for monitoring application crashes and autonomously applying mitigations to prevent future crashes on a per application basis.</span></span> <span data-ttu-id="e6224-111">Per la maggior parte degli utenti, FTH funzionerà senza alcuna necessità di intervento o modifica.</span><span class="sxs-lookup"><span data-stu-id="e6224-111">For the vast majority of users, FTH will function with no need for intervention or change on their part.</span></span> <span data-ttu-id="e6224-112">Tuttavia, in alcuni casi, gli sviluppatori di applicazioni e i tester software potrebbero dover eseguire l'override del comportamento predefinito di questo sistema.</span><span class="sxs-lookup"><span data-stu-id="e6224-112">However, in some cases, application developers and software testers may need to override the default behavior of this system.</span></span>

## <a name="solution"></a><span data-ttu-id="e6224-113">Soluzione</span><span class="sxs-lookup"><span data-stu-id="e6224-113">Solution</span></span>

<span data-ttu-id="e6224-114">**Visualizzazione dell'attività heap a tolleranza di errore**</span><span class="sxs-lookup"><span data-stu-id="e6224-114">**Viewing Fault Tolerant Heap activity**</span></span>

<span data-ttu-id="e6224-115">L'heap a tolleranza di errore registra le informazioni quando il servizio viene avviato, arrestato o inizia a mitigare i problemi per una nuova applicazione.</span><span class="sxs-lookup"><span data-stu-id="e6224-115">Fault Tolerant Heap logs information when the service starts, stops, or starts mitigating problems for a new application.</span></span> <span data-ttu-id="e6224-116">Per vedere le informazioni, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="e6224-116">To view this information, follow these steps:</span></span>

1.  <span data-ttu-id="e6224-117">Fare clic sul menu Start.</span><span class="sxs-lookup"><span data-stu-id="e6224-117">Click the Start menu.</span></span>
2.  <span data-ttu-id="e6224-118">Fare clic con il pulsante destro del mouse su **computer** e scegliere **gestione**.</span><span class="sxs-lookup"><span data-stu-id="e6224-118">Right-click **Computer** and click **Manage**.</span></span>
3.  <span data-ttu-id="e6224-119">Fare clic su **Visualizzatore eventi**  >  **registri applicazioni e servizi**  >  **Microsoft**  >  **Windows > a tolleranza di errore-heap**</span><span class="sxs-lookup"><span data-stu-id="e6224-119">Click **Event Viewer** > **Applications and Services Logs** > **Microsoft** > **Windows > Fault-Tolerant-Heap**</span></span>
4.  <span data-ttu-id="e6224-120">Visualizzare gli eventi FTH.</span><span class="sxs-lookup"><span data-stu-id="e6224-120">View FTH Events.</span></span>

<span data-ttu-id="e6224-121">Gli eventi di arresto e avvio del servizio non contengono dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="e6224-121">The service stop and start events contain no additional data.</span></span> <span data-ttu-id="e6224-122">L'evento FTH Enabled contiene l'ID del processo (PID), il nome dell'immagine del processo e l'ora di inizio dell'istanza del processo.</span><span class="sxs-lookup"><span data-stu-id="e6224-122">The FTH Enabled event contains the Process ID (PID), the process image name, and the process instance start time.</span></span>

<span data-ttu-id="e6224-123">**Disabilitazione dell'heap a tolleranza di errore**</span><span class="sxs-lookup"><span data-stu-id="e6224-123">**Disabling Fault Tolerant Heap**</span></span>

<span data-ttu-id="e6224-124">**Attenzione** Se si modifica il registro di sistema in modo errato utilizzando l'editor del registro di sistema o un altro metodo, possono verificarsi problemi gravi.</span><span class="sxs-lookup"><span data-stu-id="e6224-124">**Caution** Serious problems may occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="e6224-125">Questi problemi potrebbero richiedere la reinstallazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e6224-125">These problems may require you to reinstall the operating system.</span></span> <span data-ttu-id="e6224-126">Microsoft non garantisce la possibilità di risolvere questi problemi.</span><span class="sxs-lookup"><span data-stu-id="e6224-126">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="e6224-127">La modifica del Registro di sistema è a rischio e pericolo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e6224-127">Modify the registry at your own risk.</span></span>  
 <span data-ttu-id="e6224-128">Per disabilitare completamente l'heap a tolleranza di errore in un sistema, impostare il \_ valore reg DWORD **HKLM \\ software \\ Microsoft \\ FTH \\ abilitato** su **0**.</span><span class="sxs-lookup"><span data-stu-id="e6224-128">To disable Fault Tolerant Heap entirely on a system, set the REG\_DWORD value **HKLM\\Software\\Microsoft\\FTH\\Enabled** to **0**.</span></span>

<span data-ttu-id="e6224-129">Dopo avere modificato questo valore, riavviare il sistema.</span><span class="sxs-lookup"><span data-stu-id="e6224-129">After changing this value, restart the system.</span></span> <span data-ttu-id="e6224-130">FTH non si attiverà più per le nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e6224-130">FTH will no longer activate for new applications.</span></span>

<span data-ttu-id="e6224-131">**Reimpostazione dell'elenco di applicazioni registrate da FTH**</span><span class="sxs-lookup"><span data-stu-id="e6224-131">**Resetting the list of applications tracked by FTH**</span></span>

<span data-ttu-id="e6224-132">L'heap a tolleranza di errore è gestito autonomamente e si arresterà in modo autonomo nel caso in cui le mitigazioni non siano valide per una determinata applicazione.</span><span class="sxs-lookup"><span data-stu-id="e6224-132">Fault Tolerant heap is self-managing and will autonomously stop applying in the case that mitigations are not effective for a given application.</span></span> <span data-ttu-id="e6224-133">Tuttavia, se è necessario reimpostare l'elenco delle applicazioni per cui FTH è in grado di attenuare i problemi (ad esempio, se si sta testando un'applicazione ed è necessario riprodurre un arresto anomalo di FTH), è possibile eseguire il comando seguente da un prompt dei comandi con privilegi elevati:  **Rundll32.exe fthsvc.dll, FthSysprepSpecialize**</span><span class="sxs-lookup"><span data-stu-id="e6224-133">However, if you need to reset the list of applications for which FTH is mitigating problems (for example, if you are testing an application and need to reproduce a crash that FTH is mitigating), you can run the following command from an elevated command prompt:  **Rundll32.exe fthsvc.dll,FthSysprepSpecialize**</span></span>  
<span data-ttu-id="e6224-134">**Attenzione** L'esecuzione di questo comando eliminerà tutte le applicazioni FTH, in modo che le applicazioni che funzionano attualmente correttamente potrebbero iniziare a arrestarsi nuovamente dopo l'esecuzione di questo comando.</span><span class="sxs-lookup"><span data-stu-id="e6224-134">**Caution** Running this command will clear all FTH applications, so applications that are currently functioning properly may begin to crash again after running this command.</span></span>  

 

 



