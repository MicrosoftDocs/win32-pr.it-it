---
description: WMI utilizza traccia eventi (ETW) ed è possibile ottenere gli eventi tramite l'interfaccia utente Visualizzatore eventi o lo strumento da riga di comando wevtutil. Per ulteriori informazioni, vedere traccia dell'attività WMI.
ms.assetid: 315b8355-03b9-40f9-a6c1-29a49f5a2cd8
ms.tgt_platform: multiple
title: File di log WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51dfe4efbec32e60812980511676f723fd5aee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309749"
---
# <a name="wmi-log-files"></a><span data-ttu-id="0a26f-104">File di log WMI</span><span class="sxs-lookup"><span data-stu-id="0a26f-104">WMI Log Files</span></span>

<span data-ttu-id="0a26f-105">WMI utilizza [traccia eventi](/windows/desktop/ETW/event-tracing-portal) (ETW) ed è possibile ottenere gli eventi tramite l'interfaccia utente **Visualizzatore eventi** o lo strumento da riga di comando wevtutil.</span><span class="sxs-lookup"><span data-stu-id="0a26f-105">WMI uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events can be obtained through the **Event Viewer** user interface or the Wevtutil command line tool.</span></span> <span data-ttu-id="0a26f-106">Per ulteriori informazioni, vedere [traccia dell'attività WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="0a26f-106">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

-   [<span data-ttu-id="0a26f-107">Traccia eventi anziché log di testo</span><span class="sxs-lookup"><span data-stu-id="0a26f-107">Event Tracing Instead of Text Logs</span></span>](#event-tracing-instead-of-text-logs)
-   [<span data-ttu-id="0a26f-108">File di log WMI</span><span class="sxs-lookup"><span data-stu-id="0a26f-108">WMI Log Files</span></span>](#wmi-log-files)
-   [<span data-ttu-id="0a26f-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a26f-109">Related topics</span></span>](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a><span data-ttu-id="0a26f-110">Traccia eventi anziché log di testo</span><span class="sxs-lookup"><span data-stu-id="0a26f-110">Event Tracing Instead of Text Logs</span></span>

<span data-ttu-id="0a26f-111">L'attività del servizio WMI viene registrata nel file WMITracing. log.</span><span class="sxs-lookup"><span data-stu-id="0a26f-111">WMI service activity is recorded in the WMITracing.log file.</span></span> <span data-ttu-id="0a26f-112">Per ulteriori informazioni sull'abilitazione della traccia eventi WMI e sull'accesso al file WMITracing. log, vedere [traccia dell'attività WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="0a26f-112">For more information about enabling WMI event tracing and accessing the WMITracing.log file, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span> <span data-ttu-id="0a26f-113">I provider Windows Driver Model (WDM) continuano ad accedere al file Wbemprov. log.</span><span class="sxs-lookup"><span data-stu-id="0a26f-113">Windows Driver Model (WDM) providers continue to log in the Wbemprov.log file.</span></span>

## <a name="wmi-log-files"></a><span data-ttu-id="0a26f-114">File di log WMI</span><span class="sxs-lookup"><span data-stu-id="0a26f-114">WMI Log Files</span></span>

<span data-ttu-id="0a26f-115">Il servizio WMI e alcuni provider scrivono file di log di testo per registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="0a26f-115">The WMI service and some providers write text log files to record events.</span></span>

<dl> <dt>

<span data-ttu-id="0a26f-116"><span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[File di log del provider WMI](wmi-provider-log-files.md)</span><span class="sxs-lookup"><span data-stu-id="0a26f-116"><span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[WMI Provider Log Files](wmi-provider-log-files.md)</span></span>
</dt> <dd>

<span data-ttu-id="0a26f-117">Anche i provider WMI possono gestire i log.</span><span class="sxs-lookup"><span data-stu-id="0a26f-117">WMI providers also may maintain logs.</span></span> <span data-ttu-id="0a26f-118">I file di log visualizzati in un sistema dipendono dai provider installati.</span><span class="sxs-lookup"><span data-stu-id="0a26f-118">Which log files appear on a system depends on which providers are installed.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="0a26f-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a26f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a26f-120">Informazioni di riferimento su WMI</span><span class="sxs-lookup"><span data-stu-id="0a26f-120">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="0a26f-121">Traccia dell'attività WMI</span><span class="sxs-lookup"><span data-stu-id="0a26f-121">Tracing WMI Activity</span></span>](tracing-wmi-activity.md)
</dt> <dt>

[<span data-ttu-id="0a26f-122">Registrazione dell'attività WMI</span><span class="sxs-lookup"><span data-stu-id="0a26f-122">Logging WMI Activity</span></span>](logging-wmi-activity.md)
</dt> </dl>

 

 
