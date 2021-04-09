---
title: Utilizzo di Gestione remota Windows
description: Gestione remota Windows è progettato per migliorare la gestione dell'hardware in un ambiente di rete con vari dispositivi che eseguono un'ampia gamma di sistemi operativi.
ms.assetid: 6ee2b238-5bc2-4274-b7ca-49dbc728d8f1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c2934694de5913b467521510179fffdb220b601
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118110"
---
# <a name="using-windows-remote-management"></a><span data-ttu-id="9b2f4-103">Utilizzo di Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="9b2f4-103">Using Windows Remote Management</span></span>

<span data-ttu-id="9b2f4-104">Gestione remota Windows è progettato per migliorare la gestione dell'hardware in un ambiente di rete con vari dispositivi che eseguono un'ampia gamma di sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="9b2f4-104">Windows Remote Management is intended to improve hardware management in a network environment with various devices running a variety of operating systems.</span></span> <span data-ttu-id="9b2f4-105">L'intera progettazione del servizio ha come obiettivo principale il monitoraggio e la gestione di computer remoti mediante l'implementazione di un protocollo interoperativo standard.</span><span class="sxs-lookup"><span data-stu-id="9b2f4-105">The entire design of the service is focused on monitoring and managing remote computers by implementing an interoperable standard protocol.</span></span>

<span data-ttu-id="9b2f4-106">Poiché l' [API di scripting WinRM](winrm-scripting-api.md) e l' [API C++ WinRM](winrm-c---api.md) implementano e modellano attentamente le operazioni definite per il protocollo WS-Management, gli script e le applicazioni ricevono flussi di XML in risposta alle richieste.</span><span class="sxs-lookup"><span data-stu-id="9b2f4-106">Because the [WinRM Scripting API](winrm-scripting-api.md) and the [WinRM C++ API](winrm-c---api.md) implement and closely model the operations defined for the WS-Management protocol, scripts and applications receive streams of XML in response to requests.</span></span> <span data-ttu-id="9b2f4-107">I parametri di input per le chiamate al metodo devono essere costruiti in XML.</span><span class="sxs-lookup"><span data-stu-id="9b2f4-107">Input parameters to method calls must be constructed in XML.</span></span> <span data-ttu-id="9b2f4-108">È possibile utilizzare i metodi dell'API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) per visualizzare o costruire stringhe XML.</span><span class="sxs-lookup"><span data-stu-id="9b2f4-108">You can use the methods of the [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API to display or construct XML strings.</span></span> <span data-ttu-id="9b2f4-109">Per un esempio, vedere [visualizzazione dell'output XML dagli script WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="9b2f4-109">For an example, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>

<span data-ttu-id="9b2f4-110">Nell'elenco seguente sono inclusi gli argomenti che descrivono come utilizzare lo script WinRM:</span><span class="sxs-lookup"><span data-stu-id="9b2f4-110">The following list includes topics that describe how to use WinRM scripting:</span></span>

-   [<span data-ttu-id="9b2f4-111">Rilevamento dell'eventuale supporto di WS-Management protocollo da un computer remoto</span><span class="sxs-lookup"><span data-stu-id="9b2f4-111">Detecting Whether a Remote Computer Supports WS-Management Protocol</span></span>](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)
-   [<span data-ttu-id="9b2f4-112">Recupero di dati dal computer locale</span><span class="sxs-lookup"><span data-stu-id="9b2f4-112">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
-   [<span data-ttu-id="9b2f4-113">Recupero di dati da un computer remoto</span><span class="sxs-lookup"><span data-stu-id="9b2f4-113">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
-   [<span data-ttu-id="9b2f4-114">Enumerazione o elenco di tutte le istanze di una risorsa</span><span class="sxs-lookup"><span data-stu-id="9b2f4-114">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
-   [<span data-ttu-id="9b2f4-115">Esecuzione di query per istanze specifiche di una risorsa</span><span class="sxs-lookup"><span data-stu-id="9b2f4-115">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
-   [<span data-ttu-id="9b2f4-116">Visualizzazione dell'output XML dagli script WinRM</span><span class="sxs-lookup"><span data-stu-id="9b2f4-116">Displaying XML Output from WinRM Scripts</span></span>](displaying-xml-output-from-winrm-scripts.md)

## <a name="tracing-winrm-activity"></a><span data-ttu-id="9b2f4-117">Traccia dell'attività WinRM</span><span class="sxs-lookup"><span data-stu-id="9b2f4-117">Tracing WinRM Activity</span></span>

<span data-ttu-id="9b2f4-118">Poiché WinRM ottiene i dati tramite [Strumentazione gestione Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page), è possibile tracciare l'attività WMI risultante dai messaggi WinRM.</span><span class="sxs-lookup"><span data-stu-id="9b2f4-118">Because WinRM obtains data through [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page), you can trace WMI activity that results from WinRM messages.</span></span> <span data-ttu-id="9b2f4-119">A partire da Windows Vista, i [file di log WMI](/windows/desktop/WmiSdk/wmi-log-files)non vengono più utilizzati dal servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="9b2f4-119">Starting with Windows Vista, the WMI service no longer uses the [WMI Log Files](/windows/desktop/WmiSdk/wmi-log-files).</span></span> <span data-ttu-id="9b2f4-120">USA invece [traccia eventi](/windows/desktop/ETW/event-tracing-portal) (ETW) ed eventi sono disponibili tramite l'interfaccia utente **Visualizzatore eventi** o lo strumento da riga di comando Evtutil.</span><span class="sxs-lookup"><span data-stu-id="9b2f4-120">Instead it uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events are available through the **Event Viewer** UI or the Evtutil command line tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b2f4-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b2f4-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b2f4-122">Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="9b2f4-122">Windows Remote Management</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="9b2f4-123">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="9b2f4-123">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="9b2f4-124">Riferimento Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="9b2f4-124">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dt>

[<span data-ttu-id="9b2f4-125">Creazione di script in Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="9b2f4-125">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 