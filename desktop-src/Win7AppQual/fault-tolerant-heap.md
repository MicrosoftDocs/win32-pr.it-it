---
description: Heap a tolleranza di errore
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Heap a tolleranza di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17ab2630e6dc28cb84604e48be1aa60bf208a97
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088399"
---
# <a name="fault-tolerant-heap"></a><span data-ttu-id="07995-103">Heap a tolleranza di errore</span><span class="sxs-lookup"><span data-stu-id="07995-103">Fault Tolerant Heap</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="07995-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="07995-104">Affected Platforms</span></span>

<span data-ttu-id="07995-105">**Client -** Windows 7</span><span class="sxs-lookup"><span data-stu-id="07995-105">**Clients -** Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="07995-106">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="07995-106">Feature Impact</span></span>

 <span data-ttu-id="07995-107">**Gravità :** Medio</span><span class="sxs-lookup"><span data-stu-id="07995-107">**Severity -** Medium</span></span>  
<span data-ttu-id="07995-108">**Frequenza -** Basso</span><span class="sxs-lookup"><span data-stu-id="07995-108">**Frequency -** Low</span></span>  


## <a name="description"></a><span data-ttu-id="07995-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07995-109">Description</span></span>

<span data-ttu-id="07995-110">L'heap a tolleranza di errore (FTH) è un sottosistema di Windows 7 responsabile del monitoraggio degli arresti anomali delle applicazioni e dell'applicazione autonoma di mitigazioni per evitare arresti anomali futuri per ogni applicazione.</span><span class="sxs-lookup"><span data-stu-id="07995-110">The Fault Tolerant Heap (FTH) is a subsystem of Windows 7 responsible for monitoring application crashes and autonomously applying mitigations to prevent future crashes on a per application basis.</span></span> <span data-ttu-id="07995-111">Per la maggior parte degli utenti, FTH funzionerà senza necessità di intervento o modifica da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="07995-111">For the vast majority of users, FTH will function with no need for intervention or change on their part.</span></span> <span data-ttu-id="07995-112">Tuttavia, in alcuni casi, gli sviluppatori di applicazioni e i tester software potrebbero dover eseguire l'override del comportamento predefinito di questo sistema.</span><span class="sxs-lookup"><span data-stu-id="07995-112">However, in some cases, application developers and software testers may need to override the default behavior of this system.</span></span>

## <a name="solution"></a><span data-ttu-id="07995-113">Soluzione</span><span class="sxs-lookup"><span data-stu-id="07995-113">Solution</span></span>

<span data-ttu-id="07995-114">**Visualizzazione dell'attività heap a tolleranza di errore**</span><span class="sxs-lookup"><span data-stu-id="07995-114">**Viewing Fault Tolerant Heap activity**</span></span>

<span data-ttu-id="07995-115">Heap a tolleranza di errore registra le informazioni all'avvio, all'arresto o all'avvio del servizio per attenuare i problemi relativi a una nuova applicazione.</span><span class="sxs-lookup"><span data-stu-id="07995-115">Fault Tolerant Heap logs information when the service starts, stops, or starts mitigating problems for a new application.</span></span> <span data-ttu-id="07995-116">Per vedere le informazioni, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="07995-116">To view this information, follow these steps:</span></span>

1.  <span data-ttu-id="07995-117">Fare clic sul menu Start.</span><span class="sxs-lookup"><span data-stu-id="07995-117">Click the Start menu.</span></span>
2.  <span data-ttu-id="07995-118">Fare clic con il pulsante **destro del mouse** su Computer e scegliere **Gestisci**.</span><span class="sxs-lookup"><span data-stu-id="07995-118">Right-click **Computer** and click **Manage**.</span></span>
3.  <span data-ttu-id="07995-119">Fare **clic Visualizzatore eventi** registri applicazioni e  >  **servizi** di  >  **Microsoft** Windows > heap a tolleranza di  >  **errore**</span><span class="sxs-lookup"><span data-stu-id="07995-119">Click **Event Viewer** > **Applications and Services Logs** > **Microsoft** > **Windows > Fault-Tolerant-Heap**</span></span>
4.  <span data-ttu-id="07995-120">Visualizzare gli eventi FTH.</span><span class="sxs-lookup"><span data-stu-id="07995-120">View FTH Events.</span></span>

<span data-ttu-id="07995-121">Gli eventi di arresto e avvio del servizio non contengono dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="07995-121">The service stop and start events contain no additional data.</span></span> <span data-ttu-id="07995-122">L'evento FTH Enabled contiene l'ID processo (PID), il nome dell'immagine del processo e l'ora di inizio dell'istanza del processo.</span><span class="sxs-lookup"><span data-stu-id="07995-122">The FTH Enabled event contains the Process ID (PID), the process image name, and the process instance start time.</span></span>

<span data-ttu-id="07995-123">**Disabilitazione dell'heap a tolleranza di errore**</span><span class="sxs-lookup"><span data-stu-id="07995-123">**Disabling Fault Tolerant Heap**</span></span>

<span data-ttu-id="07995-124">**Attenzione** Possono verificarsi problemi gravi se si modifica il Registro di sistema in modo non corretto usando l'editor del Registro di sistema o un altro metodo.</span><span class="sxs-lookup"><span data-stu-id="07995-124">**Caution** Serious problems may occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="07995-125">Questi problemi possono richiedere la reinstallazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="07995-125">These problems may require you to reinstall the operating system.</span></span> <span data-ttu-id="07995-126">Microsoft non garantisce la possibilità di risolvere questi problemi.</span><span class="sxs-lookup"><span data-stu-id="07995-126">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="07995-127">La modifica del Registro di sistema è a rischio e pericolo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="07995-127">Modify the registry at your own risk.</span></span>  
 <span data-ttu-id="07995-128">Per disabilitare l'heap a tolleranza di errore interamente in un sistema, impostare il valore \_ DWORD **REG HKLM \\ Software Microsoft \\ \\ FTH \\ Enabled** su **0.**</span><span class="sxs-lookup"><span data-stu-id="07995-128">To disable Fault Tolerant Heap entirely on a system, set the REG\_DWORD value **HKLM\\Software\\Microsoft\\FTH\\Enabled** to **0**.</span></span>

<span data-ttu-id="07995-129">Dopo aver modificato questo valore, riavviare il sistema.</span><span class="sxs-lookup"><span data-stu-id="07995-129">After changing this value, restart the system.</span></span> <span data-ttu-id="07995-130">FTH non verrà più attivato per le nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="07995-130">FTH will no longer activate for new applications.</span></span>

<span data-ttu-id="07995-131">**Reimpostazione dell'elenco di applicazioni rilevate da FTH**</span><span class="sxs-lookup"><span data-stu-id="07995-131">**Resetting the list of applications tracked by FTH**</span></span>

<span data-ttu-id="07995-132">L'heap a tolleranza di errore è a gestione autonoma e interromperà autonomamente l'applicazione nel caso in cui le mitigazioni non siano effettive per una determinata applicazione.</span><span class="sxs-lookup"><span data-stu-id="07995-132">Fault Tolerant heap is self-managing and will autonomously stop applying in the case that mitigations are not effective for a given application.</span></span> <span data-ttu-id="07995-133">Tuttavia, se è necessario reimpostare l'elenco di applicazioni per cui FTH sta attenuando i problemi (ad esempio, se si sta testando un'applicazione ed è necessario riprodurre un arresto anomalo che FTH sta mitigando), è possibile eseguire il comando seguente da un prompt dei comandi con privilegi elevati:  **Rundll32.exe fthsvc.dll,FthSysprepSpecialize**</span><span class="sxs-lookup"><span data-stu-id="07995-133">However, if you need to reset the list of applications for which FTH is mitigating problems (for example, if you are testing an application and need to reproduce a crash that FTH is mitigating), you can run the following command from an elevated command prompt:  **Rundll32.exe fthsvc.dll,FthSysprepSpecialize**</span></span>  
<span data-ttu-id="07995-134">**Attenzione** L'esecuzione di questo comando cancella tutte le applicazioni FTH, pertanto le applicazioni che funzionano correttamente potrebbero iniziare di nuovo a bloccarsi dopo l'esecuzione di questo comando.</span><span class="sxs-lookup"><span data-stu-id="07995-134">**Caution** Running this command will clear all FTH applications, so applications that are currently functioning properly may begin to crash again after running this command.</span></span>  

 

 



