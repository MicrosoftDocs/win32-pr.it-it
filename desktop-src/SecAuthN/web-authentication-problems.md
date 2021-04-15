---
description: In questo argomento vengono descritti i suggerimenti per la risoluzione dei problemi relativi all'utilizzo delle API del broker di autenticazione Web per le pagine Web.
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Problemi relativi all'autenticazione Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc4611461effd9cbc5546059e71fc8ca3f1f0be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554571"
---
# <a name="web-authentication-problems"></a><span data-ttu-id="59133-103">Problemi relativi all'autenticazione Web</span><span class="sxs-lookup"><span data-stu-id="59133-103">Web authentication problems</span></span>

<span data-ttu-id="59133-104">In questo argomento vengono descritti i suggerimenti per la risoluzione dei problemi relativi all'utilizzo delle API del broker di autenticazione Web per le pagine Web.</span><span class="sxs-lookup"><span data-stu-id="59133-104">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span>

-   [<span data-ttu-id="59133-105">Log operativi</span><span class="sxs-lookup"><span data-stu-id="59133-105">Operational logs</span></span>](#operational-logs)
-   [<span data-ttu-id="59133-106">Uso di Fiddler con il broker di autenticazione Web</span><span class="sxs-lookup"><span data-stu-id="59133-106">Using Fiddler with Web Authentication Broker</span></span>](#using-fiddler-with-web-authentication-broker)
-   [<span data-ttu-id="59133-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59133-107">Related topics</span></span>](#related-topics)

## <a name="operational-logs"></a><span data-ttu-id="59133-108">Log operativi</span><span class="sxs-lookup"><span data-stu-id="59133-108">Operational logs</span></span>

<span data-ttu-id="59133-109">Spesso, per identificare l'elemento problematico puoi usare i log operativi.</span><span class="sxs-lookup"><span data-stu-id="59133-109">Often you can determine what is not working by using the operational logs.</span></span> <span data-ttu-id="59133-110">È disponibile un canale di log eventi dedicato Microsoft-Windows-WebAuth \\ operativo che consente agli sviluppatori di siti Web di comprendere il modo in cui vengono elaborate le pagine Web dal broker di autenticazione Web.</span><span class="sxs-lookup"><span data-stu-id="59133-110">There is a dedicated event log channel Microsoft-Windows-WebAuth\\Operational that allows website developers to understand how their web pages are being processed by the Web Authentication Broker.</span></span> <span data-ttu-id="59133-111">Per abilitarla, avviare eventvwr.exe e abilitare il log operativo sotto l'applicazione e servizi \\ Microsoft \\ Windows \\ WebAuth.</span><span class="sxs-lookup"><span data-stu-id="59133-111">To enable it, launch eventvwr.exe and enable Operational log under the Application and Services\\Microsoft\\Windows\\WebAuth.</span></span> <span data-ttu-id="59133-112">Inoltre, il broker di autenticazione Web Accoda una stringa univoca alla stringa agente utente per identificarsi sul server Web.</span><span class="sxs-lookup"><span data-stu-id="59133-112">Also, the Web Authentication Broker appends a unique string to the user agent string to identify itself on the web server.</span></span> <span data-ttu-id="59133-113">Tale stringa è "MSAuthHost/1.0".</span><span class="sxs-lookup"><span data-stu-id="59133-113">The string is "MSAuthHost/1.0".</span></span> <span data-ttu-id="59133-114">Ricorda che il numero di versione può cambiare in futuro, pertanto il tuo codice non deve dipendere da tale valore.</span><span class="sxs-lookup"><span data-stu-id="59133-114">Note that the version number may change in the future, so you should not to depend on that version number in your code.</span></span> <span data-ttu-id="59133-115">Di seguito è riportato un esempio di stringa agente utente completa:</span><span class="sxs-lookup"><span data-stu-id="59133-115">An example of the full user agent string is as follows:</span></span>

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

<span data-ttu-id="59133-116">Esempio di utilizzo dei log operativi</span><span class="sxs-lookup"><span data-stu-id="59133-116">Example of using operational logs</span></span>

1.  <span data-ttu-id="59133-117">Abilitare i log operativi</span><span class="sxs-lookup"><span data-stu-id="59133-117">Enable operational logs</span></span>
2.  <span data-ttu-id="59133-118">Eseguire contoso Social Application</span><span class="sxs-lookup"><span data-stu-id="59133-118">Run Contoso social application</span></span>![log operativi webauth visualizzati nel visualizzatore eventi](images/wab-figure15.png)
3.  <span data-ttu-id="59133-120">Le voci di log generate possono essere usate per comprendere in modo più dettagliato il comportamento del broker di autenticazione Web.</span><span class="sxs-lookup"><span data-stu-id="59133-120">The generated logs entries can be used to understand the behavior of Web Authentication Broker in greater detail.</span></span> <span data-ttu-id="59133-121">In questo caso, tali voci possono includere:</span><span class="sxs-lookup"><span data-stu-id="59133-121">In this case, these can include:</span></span>
    -   <span data-ttu-id="59133-122">Inizio esplorazione: registra l'avvio di AuthHost e contiene informazioni sugli URL di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="59133-122">Navigation Start: Logs when the AuthHost is started and contains information about the start and termination URLs.</span></span>
    -   ![illustra in dettaglio l'inizio dell'esplorazione](images/wab-figure16.png)
    -   <span data-ttu-id="59133-124">Completamento esplorazione: registra il completamento del caricamento di una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="59133-124">Navigation Complete: Logs the completion of loading a web page.</span></span>
    -   <span data-ttu-id="59133-125">Tag META: registra il momento del rilevamento di un tag META, inclusi i dettagli.</span><span class="sxs-lookup"><span data-stu-id="59133-125">Meta Tag: Logs when a meta-tag is encountered including the details.</span></span>
    -   <span data-ttu-id="59133-126">Termine esplorazione: termine dell'esplorazione da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="59133-126">Navigation Terminate: Navigation terminated by the user.</span></span>
    -   <span data-ttu-id="59133-127">Errore di esplorazione: AuthHost rileva un errore di esplorazione per l'URL che include HttpStatusCode.</span><span class="sxs-lookup"><span data-stu-id="59133-127">Navigation Error: AuthHost encounters a navigation error at a URL including HttpStatusCode.</span></span>
    -   <span data-ttu-id="59133-128">Fine esplorazione: rilevamento dell'URL di fine.</span><span class="sxs-lookup"><span data-stu-id="59133-128">Navigation End: Terminating URL is encountered.</span></span>

## <a name="using-fiddler-with-web-authentication-broker"></a><span data-ttu-id="59133-129">Uso di Fiddler con il broker di autenticazione Web</span><span class="sxs-lookup"><span data-stu-id="59133-129">Using Fiddler with Web Authentication Broker</span></span>

<span data-ttu-id="59133-130">Il debugger Web Fiddler può essere usato con le app di Windows 8.</span><span class="sxs-lookup"><span data-stu-id="59133-130">The Fiddler web debugger can be used with Windows 8 apps.</span></span>

1.  <span data-ttu-id="59133-131">Poiché AuthHost viene eseguito nel proprio contenitore di app per garantire la funzionalità di rete privata, devi impostare una chiave del Registro di sistema: Editor del Registro di sistema di Windows versione 5.00</span><span class="sxs-lookup"><span data-stu-id="59133-131">Since the AuthHost runs in its own app container to give it the private network capability, you must set a registry key: Windows Registry Editor Version 5.00</span></span>

    <span data-ttu-id="59133-132">**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Image File Execution Options** \\ **authhost.exe** \\ **EnablePrivateNetwork** = 00000001</span><span class="sxs-lookup"><span data-stu-id="59133-132">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Image File Execution Options**\\**authhost.exe**\\**EnablePrivateNetwork** = 00000001</span></span><dl> <dt>

                     Data type
</dt> <dd>                     <span data-ttu-id="59133-133">DWORD</span><span class="sxs-lookup"><span data-stu-id="59133-133">DWORD</span></span></dd> </dl>

2.  <span data-ttu-id="59133-134">Aggiungi una regola per AuthHost in quanto esso genera il traffico in uscita.</span><span class="sxs-lookup"><span data-stu-id="59133-134">Add a rule for the AuthHost as this is what is generating the outbound traffic.</span></span>
    ```cmd
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.a.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
    D:\Windows\System32>CheckNetIsolation.exe LoopbackExempt -s
    List Loopback Exempted AppContainers
    [1] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
        SID:  S-1-15-2-1973105767-3975693666-32999980-3747492175-1074076486-3102532000-500629349
    [2] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
        SID:  S-1-15-2-166260-4150837609-3669066492-3071230600-3743290616-3683681078-2492089544
    [3] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.a.p_8wekyb3d8bbwe
        SID:  S-1-15-2-3506084497-1208594716-3384433646-2514033508-1838198150-1980605558-3480344935
    ```

    

3.  <span data-ttu-id="59133-135">Aggiungi una regola firewall per il traffico in entrata in Fiddler.</span><span class="sxs-lookup"><span data-stu-id="59133-135">Add a firewall rule for incoming traffic to Fiddler.</span></span>

<span data-ttu-id="59133-136">Per altre informazioni, vedere [il Blog sull'uso del debugger Web Fiddler con le app di Windows Store](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).</span><span class="sxs-lookup"><span data-stu-id="59133-136">For more information, see [Blog on using Fiddler web debugger with Windows Store apps](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).</span></span>

## <a name="related-topics"></a><span data-ttu-id="59133-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59133-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59133-138">Considerazioni relative allo sviluppo di pagine Web</span><span class="sxs-lookup"><span data-stu-id="59133-138">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="59133-139">Domande frequenti sul broker di autenticazione Web</span><span class="sxs-lookup"><span data-stu-id="59133-139">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)
</dt> <dt>

[<span data-ttu-id="59133-140">App di esempio SDK Web Authentication broker</span><span class="sxs-lookup"><span data-stu-id="59133-140">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="59133-141">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="59133-141">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
