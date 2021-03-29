---
description: SystemTraceProvider è un provider di kernel con set predefiniti di eventi kernel supportati in Windows 7, Windows Server 2008 R2 e versioni successive.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Configurazione e avvio di una sessione SystemTraceProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b718269801a7677572e7bb5b74cd8b89d3711e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977711"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a><span data-ttu-id="928ae-103">Configurazione e avvio di una sessione SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="928ae-103">Configuring and Starting a SystemTraceProvider Session</span></span>

<span data-ttu-id="928ae-104">SystemTraceProvider è un provider di kernel con set predefiniti di eventi kernel supportati in Windows 7, Windows Server 2008 R2 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="928ae-104">The SystemTraceProvider is a kernel provider with a predefined sets of kernel events supported on Windows 7, Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="928ae-105">In Windows 7 e Windows Server 2008 R2, SystemTraceProvider può essere usato solo per la sessione del logger di kernel NT.</span><span class="sxs-lookup"><span data-stu-id="928ae-105">On Windows 7 and Windows Server 2008 R2, the SystemTraceProvider could only be used for the NT Kernel Logger session.</span></span>

<span data-ttu-id="928ae-106">In Windows 8, Windows Server 2012 e versioni successive, il SystemTraceProvider può essere multiplexato per un massimo di 8 sessioni di logger.</span><span class="sxs-lookup"><span data-stu-id="928ae-106">On Windows 8, Windows Server 2012, and later, the SystemTraceProvider can be multiplexed for up to 8 logger sessions.</span></span> <span data-ttu-id="928ae-107">I primi due slot per le sessioni del logger sono riservati per il logger di kernel NT e il logger di contesto del kernel circolare.</span><span class="sxs-lookup"><span data-stu-id="928ae-107">The first two slots for logger sessions are reserved for the NT Kernel Logger and the Circular Kernel Context Logger .</span></span>

<span data-ttu-id="928ae-108">Per ulteriori informazioni sull'utilizzo della sessione del logger del kernel NT come provider di traccia, vedere [configurazione e avvio della sessione del logger del kernel NT](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="928ae-108">For more information on using the NT Kernel Logger session as a trace provider, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="928ae-109">Per abilitare SystemTraceProvider per l'avvio di una sessione diversa da NT kernel logger, eseguire il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="928ae-109">To enable the SystemTraceProvider to start a session other than the NT Kernel Logger, execute the following command.</span></span>

<span data-ttu-id="928ae-110">**tracelog-avviare la sessione-f c: \\ Kernel1. etl-EFLAG proc \_ thread + Loader + CSWITCH**</span><span class="sxs-lookup"><span data-stu-id="928ae-110">**tracelog -start MySession -f c:\\Kernel1.etl -eflag PROC\_THREAD+LOADER+CSWITCH**</span></span>

<span data-ttu-id="928ae-111">Per abilitare a livello di codice il SystemTraceProvider per l'avvio di una sessione diversa dal logger di kernel NT, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="928ae-111">To programmatically enable the SystemTraceProvider to start a session other than the NT Kernel Logger, use the following steps.</span></span>

-   <span data-ttu-id="928ae-112">Definire un nome di logger privato.</span><span class="sxs-lookup"><span data-stu-id="928ae-112">Define a private logger name.</span></span>

    <span data-ttu-id="928ae-113">**\#definire il \_ nome del registratore privato \_ L "sessione di traccia privata"**</span><span class="sxs-lookup"><span data-stu-id="928ae-113">**\#define PRIVATE\_LOGGER\_NAME L”Some Private Trace Session”**</span></span>

-   <span data-ttu-id="928ae-114">Nel controller impostare i membri seguenti della struttura delle [**proprietà della \_ traccia \_ eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .</span><span class="sxs-lookup"><span data-stu-id="928ae-114">At the controller, set the following members of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

    <span data-ttu-id="928ae-115">Impostare **LogFileMode** sulla **\_ \_ \_ \_ modalità logger di sistema di traccia eventi**.</span><span class="sxs-lookup"><span data-stu-id="928ae-115">Set **LogFileMode** to **EVENT\_TRACE\_SYSTEM\_LOGGER\_MODE**.</span></span>

    <span data-ttu-id="928ae-116">Impostare **loggername** sul logger privato anziché il **nome del \_ logger \_ del kernel**.</span><span class="sxs-lookup"><span data-stu-id="928ae-116">Set **LoggerName** to private logger, instead of **KERNEL\_LOGGER\_NAME**.</span></span>

    <span data-ttu-id="928ae-117">Verificare che il membro **WNODE. Guid** della struttura [**di \_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) non sia impostato su **SystemTraceControlGuid**.</span><span class="sxs-lookup"><span data-stu-id="928ae-117">Make sure the **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is not set to **SystemTraceControlGuid**.</span></span> <span data-ttu-id="928ae-118">È necessario assegnare un nuovo **GUID** a questo membro.</span><span class="sxs-lookup"><span data-stu-id="928ae-118">You must assign a new **GUID** to this member.</span></span>

-   <span data-ttu-id="928ae-119">Al consumer, impostare il membro **loggername** della struttura [**di \_ \_ log di traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) su questo logger privato.</span><span class="sxs-lookup"><span data-stu-id="928ae-119">At the consumer, set the **LoggerName** member of the [**EVENT\_TRACE\_LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) structure to this private logger.</span></span>

> [!Note]  
> <span data-ttu-id="928ae-120">Se si desidera che un processo non amministratori o non TCB sia in grado di avviare una sessione di traccia di profilatura utilizzando SystemTraceProvider per conto di applicazioni di terze parti, è necessario concedere il privilegio profilo utente e quindi aggiungere l'utente sia al **GUID** della sessione (creato per la sessione logger) che al **GUID** del provider di traccia di sistema per abilitare il provider di traccia del sistema.</span><span class="sxs-lookup"><span data-stu-id="928ae-120">If you want a non-administrators or a non-TCB process to be able to start a profiling trace session using the SystemTraceProvider on behalf of third party applications, then you need to grant the user profile privilege and then add this user to both the session **GUID** (created for the logger session) and the system trace provider **GUID** to enable the system trace provider.</span></span> <span data-ttu-id="928ae-121">Per ulteriori informazioni, vedere la funzione [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="928ae-121">For more information, see the [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="928ae-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="928ae-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="928ae-123">Configurazione e avvio di una sessione di logger privata</span><span class="sxs-lookup"><span data-stu-id="928ae-123">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="928ae-124">Configurazione e avvio di una sessione di autologger</span><span class="sxs-lookup"><span data-stu-id="928ae-124">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="928ae-125">Configurazione e avvio di una sessione di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="928ae-125">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="928ae-126">Configurazione e avvio della sessione del logger del kernel NT</span><span class="sxs-lookup"><span data-stu-id="928ae-126">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="928ae-127">Aggiornamento di una sessione di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="928ae-127">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
