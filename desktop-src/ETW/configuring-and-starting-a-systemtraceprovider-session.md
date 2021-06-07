---
description: SystemTraceProvider è un provider di kernel con un set predefinito di eventi del kernel supportati in Windows 7, Windows Server 2008 R2 e versioni successive.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Configurazione e avvio di una sessione SystemTraceProvider
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 66e9d672a7c8e6358c2a92e7661e0d4e2a5878ab
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386741"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a><span data-ttu-id="6af3e-103">Configurazione e avvio di una sessione SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="6af3e-103">Configuring and Starting a SystemTraceProvider Session</span></span>

<span data-ttu-id="6af3e-104">SystemTraceProvider è un provider di kernel con un set predefinito di eventi del kernel supportati in Windows 7, Windows Server 2008 R2 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6af3e-104">The SystemTraceProvider is a kernel provider with a predefined sets of kernel events supported on Windows 7, Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="6af3e-105">In Windows 7 e Windows Server 2008 R2, SystemTraceProvider può essere usato solo per la sessione del logger del kernel NT.</span><span class="sxs-lookup"><span data-stu-id="6af3e-105">On Windows 7 and Windows Server 2008 R2, the SystemTraceProvider could only be used for the NT Kernel Logger session.</span></span>

<span data-ttu-id="6af3e-106">In Windows 8, Windows Server 2012 e versioni successive, è possibile eseguire il multiplexing di SystemTraceProvider per un massimo di 8 sessioni di logger.</span><span class="sxs-lookup"><span data-stu-id="6af3e-106">On Windows 8, Windows Server 2012, and later, the SystemTraceProvider can be multiplexed for up to 8 logger sessions.</span></span> <span data-ttu-id="6af3e-107">I primi due slot per le sessioni del logger sono riservati al logger del kernel NT e al logger di contesto del kernel circolare .</span><span class="sxs-lookup"><span data-stu-id="6af3e-107">The first two slots for logger sessions are reserved for the NT Kernel Logger and the Circular Kernel Context Logger .</span></span>

<span data-ttu-id="6af3e-108">Per altre informazioni sull'uso della sessione del logger del kernel NT come provider di traccia, vedere [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="6af3e-108">For more information on using the NT Kernel Logger session as a trace provider, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="6af3e-109">In Windows 10 SDK 20348 e versioni successive, SystemTraceProvider può essere configurato tramite provider di sistema separati, che possono essere controllati con [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) come i provider di eventi Event Tracing for Windows standard.</span><span class="sxs-lookup"><span data-stu-id="6af3e-109">On Windows 10 SDK build 20348 and later, the SystemTraceProvider can be configured via separate System Providers, which can be controlled with [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) like standard Event Tracing for Windows event providers.</span></span> <span data-ttu-id="6af3e-110">Per un elenco completo dei provider di sistema, delle parole chiave e dei gruppi legacy corrispondenti, vedere [Provider di sistema](system-providers.md)</span><span class="sxs-lookup"><span data-stu-id="6af3e-110">For a full list of system providers, keywords, and corresponding legacy flags and groups, see [System Providers](system-providers.md)</span></span>

## <a name="enable-a-systemtraceprovider-session"></a><span data-ttu-id="6af3e-111">Abilitare una sessione SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="6af3e-111">Enable a SystemTraceProvider session</span></span>

<span data-ttu-id="6af3e-112">Per consentire a SystemTraceProvider di avviare una sessione diversa dal logger del kernel NT, eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="6af3e-112">To enable the SystemTraceProvider to start a session other than the NT Kernel Logger, execute the following command:</span></span>

<span data-ttu-id="6af3e-113">**tracelog -start MySession -f c: \\ Kernel1.etl -eflag PROC \_ THREAD+LOADER+CSWITCH**</span><span class="sxs-lookup"><span data-stu-id="6af3e-113">**tracelog -start MySession -f c:\\Kernel1.etl -eflag PROC\_THREAD+LOADER+CSWITCH**</span></span>

<span data-ttu-id="6af3e-114">Per consentire a livello di codice a SystemTraceProvider di avviare una sessione diversa dal logger del kernel NT, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="6af3e-114">To programmatically enable the SystemTraceProvider to start a session other than the NT Kernel Logger, use the following steps.</span></span>

-   <span data-ttu-id="6af3e-115">Definire un nome di logger privato.</span><span class="sxs-lookup"><span data-stu-id="6af3e-115">Define a private logger name.</span></span>

    <span data-ttu-id="6af3e-116">**\#define PRIVATE \_ LOGGER \_ NAME L"Some Private Trace Session"**</span><span class="sxs-lookup"><span data-stu-id="6af3e-116">**\#define PRIVATE\_LOGGER\_NAME L”Some Private Trace Session”**</span></span>

-   <span data-ttu-id="6af3e-117">Nel controller impostare i membri seguenti della struttura [**EVENT \_ TRACE \_ PROPERTIES.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)</span><span class="sxs-lookup"><span data-stu-id="6af3e-117">At the controller, set the following members of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

    <span data-ttu-id="6af3e-118">Impostare **LogFileMode su** **EVENT TRACE SYSTEM \_ \_ \_ LOGGER \_ MODE**.</span><span class="sxs-lookup"><span data-stu-id="6af3e-118">Set **LogFileMode** to **EVENT\_TRACE\_SYSTEM\_LOGGER\_MODE**.</span></span>

    <span data-ttu-id="6af3e-119">Impostare **LoggerName** su logger privato, invece di **KERNEL \_ LOGGER \_ NAME**.</span><span class="sxs-lookup"><span data-stu-id="6af3e-119">Set **LoggerName** to private logger, instead of **KERNEL\_LOGGER\_NAME**.</span></span>

    <span data-ttu-id="6af3e-120">Assicurarsi che il **membro Wnode.Guid** della struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) non sia impostato su **SystemTraceControlGuid**.</span><span class="sxs-lookup"><span data-stu-id="6af3e-120">Make sure the **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is not set to **SystemTraceControlGuid**.</span></span> <span data-ttu-id="6af3e-121">È necessario assegnare un **nuovo GUID** a questo membro.</span><span class="sxs-lookup"><span data-stu-id="6af3e-121">You must assign a new **GUID** to this member.</span></span>

-   <span data-ttu-id="6af3e-122">Nel consumer impostare il membro **LoggerName** della struttura [**EVENT TRACE \_ \_ LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) su questo logger privato.</span><span class="sxs-lookup"><span data-stu-id="6af3e-122">At the consumer, set the **LoggerName** member of the [**EVENT\_TRACE\_LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) structure to this private logger.</span></span>

> [!Note]  
> <span data-ttu-id="6af3e-123">Se si vuole che un processo non amministratore o non TCB sia in grado di avviare una sessione di traccia di profilatura usando SystemTraceProvider per conto di applicazioni di terze parti, è necessario concedere il privilegio del profilo utente e quindi aggiungere questo utente sia al **GUID** della sessione (creato per la sessione del logger) che al **GUID** del provider di traccia di sistema per abilitare il provider di traccia di sistema.</span><span class="sxs-lookup"><span data-stu-id="6af3e-123">If you want a non-administrators or a non-TCB process to be able to start a profiling trace session using the SystemTraceProvider on behalf of third party applications, then you need to grant the user profile privilege and then add this user to both the session **GUID** (created for the logger session) and the system trace provider **GUID** to enable the system trace provider.</span></span> <span data-ttu-id="6af3e-124">Per altre informazioni, vedere la [**funzione EventAccessControl.**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol)</span><span class="sxs-lookup"><span data-stu-id="6af3e-124">For more information, see the [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6af3e-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6af3e-125">Related topics</span></span>

[<span data-ttu-id="6af3e-126">Configurazione e avvio di una sessione privata del logger</span><span class="sxs-lookup"><span data-stu-id="6af3e-126">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)

[<span data-ttu-id="6af3e-127">Configurazione e avvio di una sessione di autologger</span><span class="sxs-lookup"><span data-stu-id="6af3e-127">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)

[<span data-ttu-id="6af3e-128">Configurazione e avvio di una sessione di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="6af3e-128">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)

[<span data-ttu-id="6af3e-129">Configurazione e avvio della sessione del logger del kernel NT</span><span class="sxs-lookup"><span data-stu-id="6af3e-129">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)

[<span data-ttu-id="6af3e-130">Provider di sistema</span><span class="sxs-lookup"><span data-stu-id="6af3e-130">System Providers</span></span>](system-providers.md)

[<span data-ttu-id="6af3e-131">Aggiornamento di una sessione di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="6af3e-131">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)

 

 
