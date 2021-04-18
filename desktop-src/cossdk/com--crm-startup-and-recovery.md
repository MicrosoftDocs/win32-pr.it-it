---
description: Avvio e ripristino di COM+ CRM
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: Avvio e ripristino di COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a0e631e2e5ecef1621705c9af74aa48898d733b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305232"
---
# <a name="com-crm-startup-and-recovery"></a><span data-ttu-id="c6a14-103">Avvio e ripristino di COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="c6a14-103">COM+ CRM Startup and Recovery</span></span>

<span data-ttu-id="c6a14-104">Se per un'applicazione server è selezionata la casella di controllo **Abilita gestori delle risorse di compensazione** (utilizzando lo strumento di amministrazione Servizi componenti, nella scheda **Avanzate** della pagina delle proprietà dell'applicazione com+), alla prima avvio viene creato un file di log CRM che verrà utilizzato da tutti dispongono nel processo dell'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="c6a14-104">If a server application has the **Enable compensating resource managers** checkbox selected (using the Component Services administrative tool, on the **Advanced** tab of the COM+ application's property page), the first time it starts up it creates a CRM log file to be used by all CRMs in that server application process.</span></span> <span data-ttu-id="c6a14-105">Per istruzioni dettagliate sulla configurazione del CRM, vedere [Configuring com+ CRM Components](configuring-com--crm-components.md).</span><span class="sxs-lookup"><span data-stu-id="c6a14-105">(For detailed instructions about configuring the CRM, see [Configuring COM+ CRM Components](configuring-com--crm-components.md).)</span></span>

<span data-ttu-id="c6a14-106">Il nome del file di log CRM creato per l'applicazione server è basato sull'AppId (un GUID) dell'applicazione server e il file di log CRM si trova nella stessa directory del file di log DTC (in genere la directory% SystemRoot% \\ WinNT \\ system32 \\ DtcLog).</span><span class="sxs-lookup"><span data-stu-id="c6a14-106">The name of the CRM log file created for the server application is based on the AppId (a GUID) of the server application, and the CRM log file is placed in the same directory as the DTC log file (normally your %SystemRoot%\\winnt\\system32\\DtcLog directory).</span></span> <span data-ttu-id="c6a14-107">I file di log CRM hanno estensione. crmlog.</span><span class="sxs-lookup"><span data-stu-id="c6a14-107">CRM log files have the extension .crmlog.</span></span>

> [!Note]  
> <span data-ttu-id="c6a14-108">Potrebbe essere necessario modificare il percorso predefinito di un file di log CRM a causa delle prestazioni (in modo che il file di log DTC si trovi in un disco diverso rispetto al file di log CRM) o forse a causa dell'uso del CRM in un ambiente cluster.</span><span class="sxs-lookup"><span data-stu-id="c6a14-108">It may be necessary to change the default location of a CRM log file due to performance reasons (to have the DTC log file on a different disk than the CRM log file) or perhaps due to use of the CRM in a cluster environment.</span></span> <span data-ttu-id="c6a14-109">Il percorso dei file di log CRM può essere modificato utilizzando COM+ Administration SDK.</span><span class="sxs-lookup"><span data-stu-id="c6a14-109">The location of the CRM log files can be changed using the COM+ administration SDK.</span></span> <span data-ttu-id="c6a14-110">Il nome della proprietà è CRMLogFile e esiste nell'oggetto raccolta [**Applications**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="c6a14-110">The property name is CRMLogFile, and it exists on the [**Applications**](applications.md) collection object.</span></span>

 

<span data-ttu-id="c6a14-111">Quando un'applicazione server (abilitata per CRM) viene avviata e rileva che un file di log CRM esiste già per quell'applicazione server, esegue il ripristino sul file di log CRM.</span><span class="sxs-lookup"><span data-stu-id="c6a14-111">When a server application (that is CRM-enabled) starts up and finds that a CRM log file already exists for that server application, it performs recovery on that CRM log file.</span></span> <span data-ttu-id="c6a14-112">Il *ripristino* è il processo di completamento di tutte le transazioni interrotte da un errore e prevede che l'infrastruttura CRM legga il file di log CRM per tutte le transazioni che non sono state completate correttamente.</span><span class="sxs-lookup"><span data-stu-id="c6a14-112">*Recovery* is the process of completing any transactions that were interrupted by a failure and involves the CRM infrastructure reading the CRM log file for any transactions that were not fully completed.</span></span> <span data-ttu-id="c6a14-113">Se trova, contatta il DTC per determinare il risultato della transazione.</span><span class="sxs-lookup"><span data-stu-id="c6a14-113">If it finds any, it contacts the DTC to determine the transaction outcome.</span></span> <span data-ttu-id="c6a14-114">Crea quindi il compensatore CRM e passa le notifiche commit o Interrompi come richiesto, insieme ai record di log associati.</span><span class="sxs-lookup"><span data-stu-id="c6a14-114">It then creates the CRM Compensator and passes on the commit or abort notifications as required, together with the associated log records.</span></span>

<span data-ttu-id="c6a14-115">Le notifiche di preparazione non vengono ricevute dal compensatore CRM durante il ripristino.</span><span class="sxs-lookup"><span data-stu-id="c6a14-115">Prepare notifications are not received by the CRM Compensator during recovery.</span></span> <span data-ttu-id="c6a14-116">Il compensatore CRM dispone di un flag per distinguere se viene chiamato durante il normale funzionamento o durante il ripristino.</span><span class="sxs-lookup"><span data-stu-id="c6a14-116">The CRM Compensator has a flag to distinguish whether it is being called during normal operation or during recovery.</span></span>

<span data-ttu-id="c6a14-117">Il ripristino rileverà normalmente le transazioni non completate solo se l'applicazione server è stata arrestata in modo anomalo a causa di un arresto anomalo del processo dell'applicazione server o di un arresto anomalo del computer.</span><span class="sxs-lookup"><span data-stu-id="c6a14-117">Recovery will normally find uncompleted transactions only if the server application has been shutdown abnormally, due to either a server application process crash or a computer crash.</span></span> <span data-ttu-id="c6a14-118">Se l'applicazione server può essere arrestata normalmente, a causa del timeout di inattività o dell'arresto manuale tramite lo strumento di amministrazione Servizi componenti, il file di log verrà pulito.</span><span class="sxs-lookup"><span data-stu-id="c6a14-118">If the server application is allowed to shut down normally, due either to the idle time-out or to manual shutdown via the Component Services administrative tool, the log file will be clean.</span></span>

<span data-ttu-id="c6a14-119">L'avvio di un'applicazione server CRM per il ripristino non viene avviato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c6a14-119">Starting of a CRM server application for recovery is not automatically initiated.</span></span> <span data-ttu-id="c6a14-120">È necessario intraprendere un'azione esterna per avviare l'applicazione server CRM in cui è necessario il ripristino.</span><span class="sxs-lookup"><span data-stu-id="c6a14-120">Some external action must be taken to start the CRM server application where recovery is required.</span></span> <span data-ttu-id="c6a14-121">In genere si creerebbe un componente in tale applicazione server.</span><span class="sxs-lookup"><span data-stu-id="c6a14-121">Typically this would be creating a component in that server application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6a14-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6a14-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6a14-123">Concetti Gestione risorse di compensazione COM+</span><span class="sxs-lookup"><span data-stu-id="c6a14-123">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[<span data-ttu-id="c6a14-124">Processo operativo COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="c6a14-124">COM+ CRM Operating Process</span></span>](com--crm-operating-process.md)
</dt> </dl>

 

 



