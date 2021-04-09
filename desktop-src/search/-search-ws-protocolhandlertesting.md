---
description: Per eseguire il test e il debug delle implementazioni del gestore di protocollo è fondamentale comprendere come vengono avviati i gestori di protocollo.
ms.assetid: 33c99620-7381-4719-9fc6-4c8284481411
title: Debug di gestori di protocollo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d59c0c7915f9bbf84a80091408ba88a9a75ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128515"
---
# <a name="debugging-protocol-handlers"></a><span data-ttu-id="004cf-103">Debug di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="004cf-103">Debugging Protocol Handlers</span></span>

<span data-ttu-id="004cf-104">Per eseguire il test e il debug delle implementazioni del gestore di protocollo è fondamentale comprendere come vengono avviati i gestori di protocollo.</span><span class="sxs-lookup"><span data-stu-id="004cf-104">Integral to testing and debugging your protocol handler implementations is understanding how protocol handlers are launched.</span></span>

<span data-ttu-id="004cf-105">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="004cf-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="004cf-106">Informazioni sui gestori di protocollo di debug</span><span class="sxs-lookup"><span data-stu-id="004cf-106">About Debugging Protocol Handlers</span></span>](#about-debugging-protocol-handlers)
-   [<span data-ttu-id="004cf-107">Impostazione del debug</span><span class="sxs-lookup"><span data-stu-id="004cf-107">Setting Up Debugging</span></span>](#setting-up-debugging)
-   [<span data-ttu-id="004cf-108">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="004cf-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="004cf-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="004cf-109">Related topics</span></span>](#related-topics)

## <a name="about-debugging-protocol-handlers"></a><span data-ttu-id="004cf-110">Informazioni sui gestori di protocollo di debug</span><span class="sxs-lookup"><span data-stu-id="004cf-110">About Debugging Protocol Handlers</span></span>

<span data-ttu-id="004cf-111">Il processo SearchIndexer (searchindexer.exe) avvia una copia del processo SearchProtocolHost (SearchProtocolHost.exe) nel contesto di sistema e in un'altra copia nel contesto utente.</span><span class="sxs-lookup"><span data-stu-id="004cf-111">The SearchIndexer process (searchindexer.exe) launches one copy of the SearchProtocolHost process (SearchProtocolHost.exe) in the system context and another copy in the user context.</span></span> <span data-ttu-id="004cf-112">Quindi, i gestori del protocollo vengono caricati nel processo SearchProtocolHost in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="004cf-112">Then, the protocol handlers are loaded in the SearchProtocolHost process as needed.</span></span> <span data-ttu-id="004cf-113">Non vengono scaricati finché il servizio di ricerca non viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="004cf-113">They are not unloaded until the search service is stopped.</span></span> <span data-ttu-id="004cf-114">La stessa istanza di un gestore di protocollo viene riutilizzata un numero qualsiasi di volte mentre il servizio è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="004cf-114">The same instance of a protocol handler is reused any number of times while the service is running.</span></span>

<span data-ttu-id="004cf-115">I processi SearchIndexer e SearchProtocolHost comunicano spesso durante l'indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="004cf-115">The SearchIndexer and SearchProtocolHost processes communicate frequently during indexing.</span></span> <span data-ttu-id="004cf-116">Se si sospende o si arresta il processo SearchProtocolHost per eseguire il debug, il SearchIndexer avvierà un nuovo processo SearchProtocolHost, invalidando la sessione di debug.</span><span class="sxs-lookup"><span data-stu-id="004cf-116">If you pause or stop the SearchProtocolHost process to debug, the SearchIndexer will launch a new SearchProtocolHost process, invalidating your debugging session.</span></span> <span data-ttu-id="004cf-117">Inoltre, se si connette il debugger direttamente al processo SearchProtocolHost, è possibile interrompere l'ereditarietà del handle da searchindexer.exe a searchprotocolhost.exe e i due processi non saranno in grado di comunicare.</span><span class="sxs-lookup"><span data-stu-id="004cf-117">Also, if you attach your debugger directly to the SearchProtocolHost process, you can break handle-inheritance from searchindexer.exe to searchprotocolhost.exe, and the two processes will be unable to communicate.</span></span>

<span data-ttu-id="004cf-118">Per evitare questi problemi, è necessario inviare una notifica al servizio di ricerca di cui si sta eseguendo il debug ed è necessario associare il debugger al processo SearchIndexer con le istruzioni per eseguire il debug dei processi figlio, come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="004cf-118">To avoid these problems, you need to notify the search service that you are debugging, and you need to attach the debugger to the SearchIndexer process with instructions to debug child processes, as described next.</span></span>

## <a name="setting-up-debugging"></a><span data-ttu-id="004cf-119">Impostazione del debug</span><span class="sxs-lookup"><span data-stu-id="004cf-119">Setting Up Debugging</span></span>

<span data-ttu-id="004cf-120">Per configurare il debug per il gestore di protocollo, attenersi alla procedura riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="004cf-120">Follow these steps to set up debugging for your protocol handler.</span></span>

1.  <span data-ttu-id="004cf-121">Inviare una notifica al servizio di ricerca di cui si sta eseguendo il debug impostando il valore DebugFilters su 1 nel registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="004cf-121">Notify the search service that you are debugging by setting the DebugFilters value to 1 in the registry:</span></span>

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft
       Windows Search
          Gathering Manager
             DebugFilters = 1
    ```

2.  <span data-ttu-id="004cf-122">Connetti un debugger usando la chiave del registro di sistema opzioni di esecuzione file di immagine:</span><span class="sxs-lookup"><span data-stu-id="004cf-122">Attach a debugger using the Image File Execution Options registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion
       Image File Execution Options
          SearchIndexer.exe
             Debugger = <path to debugger> <debugger options> 
    ```

    <span data-ttu-id="004cf-123">Nella tabella seguente sono descritte le opzioni per un debugger di esempio.</span><span class="sxs-lookup"><span data-stu-id="004cf-123">The options for a sample debugger are described in the following table.</span></span>

    

    <span data-ttu-id="004cf-124">**Esempio di uso del debugger NTSD** debugger *= C: \\ Debuggers \\ntsd.exe-odGx-c: "sxe ld mydll.dll; g"*   </span><span class="sxs-lookup"><span data-stu-id="004cf-124">**Example using the ntsd debugger**   *Debugger = C:\\debuggers\\ntsd.exe -odGx -c: "sxe ld mydll.dll;g"*</span></span><br/>

3.  <span data-ttu-id="004cf-125">Riavviare searchindexer.exe nel debugger usando compmgmt. msc, Services. msc o una finestra di comando con comandi simili ai seguenti:</span><span class="sxs-lookup"><span data-stu-id="004cf-125">Restart searchindexer.exe under the debugger using compmgmt.msc, services.msc, or a command window with commands similar to the following:</span></span>
    ```
    net stop wsearch
    <copy new DLLs for debugging>
    net start wsearch
            
    ```

    

<span data-ttu-id="004cf-126">Per distinguere tra un processo SearchProtocolHost in esecuzione nel contesto di sistema e uno in esecuzione nel contesto utente, è possibile esaminare le stringhe di ambiente.</span><span class="sxs-lookup"><span data-stu-id="004cf-126">To distinguish between a SearchProtocolHost process running in the system context and one running in the user context, you can review the environment strings.</span></span> <span data-ttu-id="004cf-127">Con ntsd.exe, ad esempio, è possibile usare il comando Extension **! PEB** per visualizzare una visualizzazione formattata delle informazioni nel blocco dell'ambiente di elaborazione (PEB).</span><span class="sxs-lookup"><span data-stu-id="004cf-127">With ntsd.exe, for example, you can use extension command **!peb** to display a formatted view of the information in the process environment block (PEB).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="004cf-128">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="004cf-128">Additional Resources</span></span>

-   <span data-ttu-id="004cf-129">Per informazioni sulla creazione di gestori, vedere la pagina relativa alla [registrazione delle estensioni della shell](../shell/reg-shell-exts.md).</span><span class="sxs-lookup"><span data-stu-id="004cf-129">For information on creating handlers, see [Registering Shell Extensions](../shell/reg-shell-exts.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="004cf-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="004cf-130">Related topics</span></span>

<dl> <span data-ttu-id="004cf-131"><dt>**Concetti concettuali**</dt> <dt><a href="-search-3x-wds-phaddins.md">sullo sviluppo</a></dt> di gestori di protocollo <dt><a href="-search-3x-wds-extidx-prot-implementing.md">informazioni sui gestori di protocollo</a></dt> che <dt><a href="-search-3x-wds-notifyingofchanges.md">inviano notifiche all'indice delle modifiche aggiunta di</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">icone e menu di scelta rapida</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">esempio di codice: estensioni shell per gestori di protocollo</a></dt> <dt><a href="-search-3x-wds-ph-search-connector.md">creazione di un connettore di ricerca per un gestore di protocollo</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">installazione e registrazione dei gestori di protocollo</a></dt> </span><span class="sxs-lookup"><span data-stu-id="004cf-131"><dt>**Conceptual**</dt> <dt><a href="-search-3x-wds-phaddins.md">Developing Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-extidx-prot-implementing.md">Understanding Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">Notifying the Index of Changes</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">Adding Icons and Context Menus</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">Code Sample: Shell Extensions for Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-ph-search-connector.md">Creating a Search Connector for a Protocol Handler</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">Installing and Registering Protocol Handlers</a></dt> </span></span></dl>

 

 
