---
title: Completamento e annullamento di un processo
description: Per completare un processo di trasferimento, chiamare il metodo Metodo ibackgroundcopyjob complete.
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- trasferimento BITS processo, annullamento
- annullamento di un bit di processo
- trasferimento BITS processo, completamento
- completamento di un bit di processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb5cd6a33cf8cefa8749a1802c922dc80518722
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470979"
---
# <a name="completing-and-canceling-a-job"></a><span data-ttu-id="56768-107">Completamento e annullamento di un processo</span><span class="sxs-lookup"><span data-stu-id="56768-107">Completing and Canceling a Job</span></span>

<span data-ttu-id="56768-108">Per completare un processo di trasferimento, chiamare il metodo [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="56768-108">To complete a transfer job, call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="56768-109">Per i processi di download, è possibile chiamare il metodo **complete** prima che tutti i file del processo siano stati trasferiti (prima che lo stato del processo sia il \_ processo BG \_ stato \_ trasferito).</span><span class="sxs-lookup"><span data-stu-id="56768-109">For download jobs, you can call the **Complete** method before all files in the job have been transferred (before the job's state is BG\_JOB\_STATE\_TRANSFERRED).</span></span> <span data-ttu-id="56768-110">Solo i file che sono stati trasferiti nel client prima di chiamare il metodo **complete** sono disponibili per l'utente.</span><span class="sxs-lookup"><span data-stu-id="56768-110">Only those files that BITS successfully transferred to the client before you called the **Complete** method are available to the user.</span></span>

<span data-ttu-id="56768-111">Per i processi di caricamento, chiamare il metodo [**complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) solo se lo stato del processo è BG \_ processo \_ stato \_ trasferito.</span><span class="sxs-lookup"><span data-stu-id="56768-111">For upload jobs, call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method only if the job's state is BG\_JOB\_STATE\_TRANSFERRED.</span></span> <span data-ttu-id="56768-112">Per determinare quando lo stato del processo è BG \_ \_ , stato del processo \_ trasferito, eseguire il [polling](polling-for-the-status-of-the-job.md) della proprietà stato del processo o registrarsi per ricevere la \_ notifica degli \_ \_ [eventi](registering-a-com-callback.md)trasferiti al processo BG Notify.</span><span class="sxs-lookup"><span data-stu-id="56768-112">To determine when the job's state is BG\_JOB\_STATE\_TRANSFERRED, [poll](polling-for-the-status-of-the-job.md) the job's state property or register to receive BG\_NOTIFY\_JOB\_TRANSFERRED [event notification](registering-a-com-callback.md).</span></span>

<span data-ttu-id="56768-113">Per annullare un processo di trasferimento, chiamare il metodo [**Metodo ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) .</span><span class="sxs-lookup"><span data-stu-id="56768-113">To cancel a transfer job, call the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method.</span></span> <span data-ttu-id="56768-114">Il metodo **Cancel** rimuove il processo dalla coda di trasferimento e rimuove i file temporanei dal client.</span><span class="sxs-lookup"><span data-stu-id="56768-114">The **Cancel** method removes the job from the transfer queue and removes the temporary files from the client.</span></span> <span data-ttu-id="56768-115">In genere, questo metodo viene chiamato se non si riesce a risolvere un errore associato al processo.</span><span class="sxs-lookup"><span data-stu-id="56768-115">Typically, you call this method if you are unable to resolve an error associated with the job.</span></span>

<span data-ttu-id="56768-116">Il metodo [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) Annulla un caricamento se il caricamento non è completo.</span><span class="sxs-lookup"><span data-stu-id="56768-116">The [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method cancels an upload if the upload is not complete.</span></span> <span data-ttu-id="56768-117">Se il caricamento è completo e il processo è di tipo BG \_ Reply di caricamento del tipo di processo \_ \_ \_ , il metodo annulla la risposta.</span><span class="sxs-lookup"><span data-stu-id="56768-117">If the upload is complete, and the job is of type BG\_JOB\_TYPE\_UPLOAD\_REPLY, the method cancels the reply.</span></span>

<span data-ttu-id="56768-118">Se non si chiama il metodo [**complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o il metodo [**Metodo ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) entro 90 giorni (impostazione predefinita di [JobInactivityTimeout](group-policies.md) criteri di gruppo), il servizio annulla il processo.</span><span class="sxs-lookup"><span data-stu-id="56768-118">If you do not call the [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method or the [**IBackgroundCopyJob::Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) method within 90 days (default [JobInactivityTimeout](group-policies.md) Group Policy), the service cancels the job.</span></span> <span data-ttu-id="56768-119">Se il servizio annulla il processo, i file scaricati e il file di risposta non sono disponibili per il client. l'annullamento del processo non influisce sui file che sono stati caricati correttamente.</span><span class="sxs-lookup"><span data-stu-id="56768-119">If the service cancels the job, the downloaded files and the reply file are not available to the client; job cancellation does not affect files that have been successfully uploaded.</span></span> <span data-ttu-id="56768-120">È sempre necessario chiamare il metodo **complete** o **Cancel** e non basarsi sul criterio JobInactivityTimeout per la pulizia dei processi.</span><span class="sxs-lookup"><span data-stu-id="56768-120">You should always call the **Complete** or the **Cancel** method and not rely on the JobInactivityTimeout policy to cleanup your jobs.</span></span> <span data-ttu-id="56768-121">I processi rimasti nella coda possono impedire agli utenti di creare altri processi se viene raggiunto il limite dei criteri MaxJobsPerUser o MaxJobsPerMachine.</span><span class="sxs-lookup"><span data-stu-id="56768-121">Jobs left in the queue may prevent users from creating other jobs if the MaxJobsPerUser or MaxJobsPerMachine policy limit is reached.</span></span>

 

 




