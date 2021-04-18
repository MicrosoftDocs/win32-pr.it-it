---
title: Uso di BITS
description: Uso di BITS
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- Servizio trasferimento intelligente in background
- Servizio trasferimento intelligente in background, attività
- BIT di trasferimento di file
- Uso di bit BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5158e183ef7e7c142a481f1d89e329a9b04f422b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300346"
---
# <a name="using-bits"></a><span data-ttu-id="6faac-107">Uso di BITS</span><span class="sxs-lookup"><span data-stu-id="6faac-107">Using BITS</span></span>

<span data-ttu-id="6faac-108">Nei passaggi seguenti viene illustrato come eseguire un trasferimento di file utilizzando le  [interfacce](bits-interfaces.md)servizio trasferimento intelligente in background (BITS).</span><span class="sxs-lookup"><span data-stu-id="6faac-108">The following steps show how to perform a file transfer using the Background Intelligent Transfer Service (BITS)  [interfaces](bits-interfaces.md).</span></span>

<span data-ttu-id="6faac-109">**Per eseguire un trasferimento di file**</span><span class="sxs-lookup"><span data-stu-id="6faac-109">**To perform a file transfer**</span></span>

1.  [<span data-ttu-id="6faac-110">Connettersi al servizio BITS</span><span class="sxs-lookup"><span data-stu-id="6faac-110">Connect to the BITS service</span></span>](connecting-to-the-bits-service.md)
2.  [<span data-ttu-id="6faac-111">Creazione di un processo di trasferimento</span><span class="sxs-lookup"><span data-stu-id="6faac-111">Create a transfer job</span></span>](creating-a-job.md)
3.  [<span data-ttu-id="6faac-112">Aggiungere file al processo</span><span class="sxs-lookup"><span data-stu-id="6faac-112">Add files to the job</span></span>](adding-files-to-a-job.md)
4.  [<span data-ttu-id="6faac-113">Avviare il processo</span><span class="sxs-lookup"><span data-stu-id="6faac-113">Start the job</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [<span data-ttu-id="6faac-114">Determinare se i BITS hanno trasferito correttamente i file</span><span class="sxs-lookup"><span data-stu-id="6faac-114">Determine if BITS successfully transferred the files</span></span>](determining-the-status-of-a-job.md)
6.  [<span data-ttu-id="6faac-115">Completare il processo</span><span class="sxs-lookup"><span data-stu-id="6faac-115">Complete the job</span></span>](completing-and-canceling-a-job.md)

<span data-ttu-id="6faac-116">I passaggi precedenti illustrano come trasferire file usando i valori di proprietà predefiniti per un processo.</span><span class="sxs-lookup"><span data-stu-id="6faac-116">The previous steps show how to transfer files using the default property values for a job.</span></span> <span data-ttu-id="6faac-117">È possibile modificare il comportamento predefinito modificando uno o più valori di proprietà del processo.</span><span class="sxs-lookup"><span data-stu-id="6faac-117">You can change the default behavior by changing one or more of the job's property values.</span></span> <span data-ttu-id="6faac-118">È ad esempio possibile modificare la priorità in base alla quale il processo viene elaborato rispetto ad altri processi nella coda, specificare l'impostazione del proxy e registrarsi per ricevere la notifica degli eventi quando i file vengono trasferiti da BITS.</span><span class="sxs-lookup"><span data-stu-id="6faac-118">For example, you can change the priority that the job is processed relative to other jobs in the queue, specify your own proxy setting, and register to receive event notification when BITS has transferred the files.</span></span> <span data-ttu-id="6faac-119">Per ulteriori informazioni, vedere [impostazione e recupero delle proprietà di un processo](setting-and-retrieving-the-properties-of-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="6faac-119">For more information, see [Setting and Retrieving the Properties of a Job](setting-and-retrieving-the-properties-of-a-job.md).</span></span>

<span data-ttu-id="6faac-120">Windows PowerShell fornisce un meccanismo semplice per gestire molte attività BITS.</span><span class="sxs-lookup"><span data-stu-id="6faac-120">Windows PowerShell provides a simple mechanism to manage many BITS tasks.</span></span> <span data-ttu-id="6faac-121">Questa sezione contiene gli argomenti seguenti che illustrano come usare i cmdlet di Windows PowerShell con BITS:</span><span class="sxs-lookup"><span data-stu-id="6faac-121">This section contains the following topics that show how to use Windows PowerShell cmdlets with BITS:</span></span>

-   [<span data-ttu-id="6faac-122">Uso di Windows PowerShell per creare processi di trasferimento di BITS</span><span class="sxs-lookup"><span data-stu-id="6faac-122">Using Windows PowerShell to Create BITS Transfer Jobs</span></span>](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [<span data-ttu-id="6faac-123">Utilizzo dei cmdlet di Windows PowerShell per WinRM per gestire i processi di trasferimento BITS</span><span class="sxs-lookup"><span data-stu-id="6faac-123">Using WinRM Windows PowerShell Cmdlets to Manage BITS Transfer Jobs</span></span>](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [<span data-ttu-id="6faac-124">Uso dei cmdlet di Windows PowerShell per WMI per gestire BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="6faac-124">Using WMI Windows PowerShell Cmdlets to Manage the BITS Compact Server</span></span>](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> <span data-ttu-id="6faac-125">A partire da Windows 10, versione 1607, è anche possibile eseguire i cmdlet di PowerShell e usare BITSAdmin o altre applicazioni che usano le [interfacce](bits-interfaces.md) BITS da una riga di comando remota di PowerShell connessa a un altro computer (fisico o virtuale).</span><span class="sxs-lookup"><span data-stu-id="6faac-125">Starting with Windows 10, version 1607, you can also run PowerShell Cmdlets and use BITSAdmin or other applications that use the BITS [interfaces](bits-interfaces.md) from a PowerShell Remote command line connected to another machine (physical or virtual).</span></span> <span data-ttu-id="6faac-126">Questa funzionalità non è disponibile quando si usa una riga di comando di [PowerShell diretta](/virtualization/hyper-v-on-windows/user_guide/vmsession) in una macchina virtuale nello stesso computer fisico e non è disponibile quando si usano i cmdlet WinRM.</span><span class="sxs-lookup"><span data-stu-id="6faac-126">This capability is not available when using a [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) command line to a virtual machine on the same physical machine, and it is not available when using WinRM cmdlets.</span></span>
>
> <span data-ttu-id="6faac-127">Un processo BITS creato da una sessione remota di PowerShell verrà eseguito nel contesto dell'account utente della sessione e verrà eseguito solo quando esiste almeno una sessione di accesso locale attiva o una sessione remota di PowerShell associata a tale account utente.</span><span class="sxs-lookup"><span data-stu-id="6faac-127">A BITS Job created from a Remote PowerShell session will run under that session’s user account context and will only make progress when there is at least one active local logon session or Remote PowerShell session associated with that user account.</span></span> <span data-ttu-id="6faac-128">Per altre informazioni, vedere [per gestire le sessioni remote di PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="6faac-128">For more information, see [To manage PowerShell Remote sessions](using-windows-powershell-to-create-bits-transfer-jobs.md).</span></span>

 

<span data-ttu-id="6faac-129">Questa sezione contiene anche gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="6faac-129">This section also contains the following topics:</span></span>

-   [<span data-ttu-id="6faac-130">Procedure consigliate per l'uso di BITS</span><span class="sxs-lookup"><span data-stu-id="6faac-130">Best Practices When Using BITS</span></span>](best-practices-when-using-bits.md)
-   [<span data-ttu-id="6faac-131">Enumerazione dei processi nella coda di trasferimento</span><span class="sxs-lookup"><span data-stu-id="6faac-131">Enumerating jobs in the transfer queue</span></span>](enumerating-jobs-in-the-transfer-queue.md)
-   [<span data-ttu-id="6faac-132">Enumerazione dei file in un processo</span><span class="sxs-lookup"><span data-stu-id="6faac-132">Enumerating files in a job</span></span>](enumerating-files-in-a-job.md)
-   [<span data-ttu-id="6faac-133">Gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="6faac-133">Handling errors</span></span>](handling-errors.md)
-   [<span data-ttu-id="6faac-134">Recuperare la risposta da un processo di caricamento-risposta</span><span class="sxs-lookup"><span data-stu-id="6faac-134">Retrieve the reply from an upload-reply job</span></span>](retrieving-the-reply-from-an-upload-reply-job.md)

<span data-ttu-id="6faac-135">Per il codice di esempio che usa le interfacce BITS, vedere [esempi e strumenti bits](bits-samples-and-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6faac-135">For sample code that uses the BITS interfaces, see [BITS Samples and Tools](bits-samples-and-tools.md).</span></span>

 

 