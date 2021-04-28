---
description: Internet Explorer 8 - Protezione esecuzione dati/NX
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8 - Protezione esecuzione dati/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb0208cc20e78c30f42b09af78460990be20b002
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088249"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a><span data-ttu-id="4c340-103">Internet Explorer 8 - Protezione esecuzione dati/NX</span><span class="sxs-lookup"><span data-stu-id="4c340-103">Internet Explorer 8 - Data Execution Protection/NX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="4c340-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="4c340-104">Affected Platforms</span></span>

 <span data-ttu-id="4c340-105">**Client** - Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="4c340-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="4c340-106">**Server** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4c340-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










> [!Note]  
> <span data-ttu-id="4c340-107">Internet Explorer 8 abiliterà la protezione DEP/NX quando viene eseguita in un sistema operativo con il Service Pack più recente.</span><span class="sxs-lookup"><span data-stu-id="4c340-107">Internet Explorer 8 will enable DEP/NX protection when run on an operating system with the latest service pack.</span></span> <span data-ttu-id="4c340-108">Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1 e Windows Server 2008 dispongono di DEP/NX abilitati per impostazione predefinita in Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="4c340-108">Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1, and Windows Server 2008 all have DEP/NX enabled by default in Internet Explorer 8.</span></span>

 

## <a name="feature-impact"></a><span data-ttu-id="4c340-109">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="4c340-109">Feature Impact</span></span>

<span data-ttu-id="4c340-110">**Gravità** - Media</span><span class="sxs-lookup"><span data-stu-id="4c340-110">**Severity** - Medium</span></span>  
<span data-ttu-id="4c340-111">**Frequenza** - Bassa</span><span class="sxs-lookup"><span data-stu-id="4c340-111">**Frequency** - Low</span></span>  

> [!Note]  
> <span data-ttu-id="4c340-112">In genere, tutte le applicazioni che vengono Internet Explorer e non sono compatibili con DEP/NX si arresteranno in modo anomalo all'avvio e non funzioneranno.</span><span class="sxs-lookup"><span data-stu-id="4c340-112">Typically, any application that runs in Internet Explorer and is not compatible with DEP/NX will crash on startup and will not function.</span></span> <span data-ttu-id="4c340-113">Internet Explorer arresto anomalo all'avvio se sono installati componenti aggiuntivi non compatibili con DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="4c340-113">Internet Explorer may crash on startup if add-ons that are not compatible with DEP/NX are installed.</span></span>

 

## <a name="description"></a><span data-ttu-id="4c340-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c340-114">Description</span></span>

<span data-ttu-id="4c340-115">DEP/NX è una funzionalità di sicurezza che consente di attenuare le vulnerabilità correlate alla memoria.</span><span class="sxs-lookup"><span data-stu-id="4c340-115">DEP/NX is a security feature that helps mitigate memory-related vulnerabilities.</span></span> <span data-ttu-id="4c340-116">A Internet Explorer 8, tutti Internet Explorer processi abilitano la funzionalità DEP/NX per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4c340-116">As of Internet Explorer 8, all Internet Explorer processes enable the DEP/NX feature by default.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="4c340-117">Manifestazione di impatto</span><span class="sxs-lookup"><span data-stu-id="4c340-117">Manifestation of Impact</span></span>

<span data-ttu-id="4c340-118">Il kernel di Windows monitora l'esecuzione di un programma.</span><span class="sxs-lookup"><span data-stu-id="4c340-118">The Windows Kernel monitors a program's execution.</span></span> <span data-ttu-id="4c340-119">Se il kernel rileva un tentativo di eseguire codice da una pagina di memoria non contrassegnata come eseguibile, il kernel arresta l'esecuzione del programma, causando un "arresto anomalo".</span><span class="sxs-lookup"><span data-stu-id="4c340-119">If the Kernel detects an attempt to run code from a memory page that is not marked executable, the Kernel halts execution of the program, resulting in a "crash."</span></span> <span data-ttu-id="4c340-120">Si tratta di una misura di sicurezza per garantire che non sia possibile sfruttare le vulnerabilità correlate alla memoria ,ad esempio gli overflow del buffer, nell'applicazione per eseguire codice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="4c340-120">This is a security measure to help ensure that memory-related vulnerabilities (for example, buffer overflows) in the application cannot be exploited in order to execute arbitrary code.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="4c340-121">End-User mitigazione</span><span class="sxs-lookup"><span data-stu-id="4c340-121">End-User Mitigation</span></span>

-   <span data-ttu-id="4c340-122">Installare una versione successiva del componente aggiuntivo o del framework compatibile con DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="4c340-122">Install a later version of the add-on or framework that is DEP/NX compatible.</span></span>
-   <span data-ttu-id="4c340-123">Eseguire Internet Explorer con privilegi elevati come amministratore e quindi disabilitare DEP/NX usando la casella di controllo Abilita protezione della memoria per attenuare gli attacchi **online** nella scheda **Opzioni Internet**  /   avanzate .</span><span class="sxs-lookup"><span data-stu-id="4c340-123">Run Internet Explorer elevated as Administrator, and then disable DEP/NX using the **Enable memory protection to help mitigate online attacks** check box on the **Internet Options** / **Advanced** tab.</span></span>

## <a name="developer-solution"></a><span data-ttu-id="4c340-124">Soluzione per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="4c340-124">Developer Solution</span></span>

<span data-ttu-id="4c340-125">Compilare applicazioni usando le versioni più recenti dei framework compatibili con DEP.</span><span class="sxs-lookup"><span data-stu-id="4c340-125">Compile applications by using the latest versions of frameworks that are DEP compatible.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="4c340-126">Sfruttare le funzionalità delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="4c340-126">Leveraging Feature Capabilities</span></span>

-   <span data-ttu-id="4c340-127">Usare l'opzione del linker /NXCOMPAT per indicare la compatibilità DEP/NX</span><span class="sxs-lookup"><span data-stu-id="4c340-127">Use the /NXCOMPAT linker option to indicate DEP/NX compatibility</span></span>
-   <span data-ttu-id="4c340-128">Optare per il codice in altre difese disponibili, ad esempio la difesa dello stack (/GS), la gestione sicura delle eccezioni (/SafeSEH) e ASLR (/DynamicBase)</span><span class="sxs-lookup"><span data-stu-id="4c340-128">Opt your code into other available defenses like stack defense (/GS), safe exception handling (/SafeSEH), and ASLR (/DynamicBase)</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="4c340-129">Test di compatibilità, prestazioni, affidabilità e usabilità</span><span class="sxs-lookup"><span data-stu-id="4c340-129">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="4c340-130">Testare il codice con DEP/NX abilitato usando la versione Internet Explorer versione più recente in Windows Vista SP1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="4c340-130">Test your code with DEP/NX enabled by using latest released Internet Explorer version on Windows Vista SP1 or later.</span></span>
-   <span data-ttu-id="4c340-131">Testare con Internet Explorer 7 in Windows Vista dopo aver abilitato l'opzione DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="4c340-131">Test with Internet Explorer 7 on Windows Vista after enabling the DEP/NX option.</span></span> <span data-ttu-id="4c340-132">Per abilitare DEP/NX per Internet Explorer 7, eseguire Internet Explorer come amministratore, quindi impostare la casella di controllo appropriata nella scheda Strumenti > Opzioni Internet > Avanzate.</span><span class="sxs-lookup"><span data-stu-id="4c340-132">To enable DEP/NX for Internet Explorer 7, run Internet Explorer as an administrator, then set the appropriate check box in the Tools > Internet Options > Advanced tab.</span></span>
-   <span data-ttu-id="4c340-133">Eseguire lo Internet Explorer Compatibility Test Tool (IECTT), fornito con Application Compatibility Toolkit (ACT) per individuare eventuali problemi potenziali dovuti alle modifiche DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="4c340-133">Run the Internet Explorer Compatibility Test Tool (IECTT), provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to the DEP/NX changes.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="4c340-134">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="4c340-134">Links to Other Resources</span></span>

-   [<span data-ttu-id="4c340-135">Internet Explorer 8 Security Part I: DEP/NX Memory Protection</span><span class="sxs-lookup"><span data-stu-id="4c340-135">Internet Explorer 8 Security Part I: DEP/NX Memory Protection</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="4c340-136">Protezione esecuzione programmi</span><span class="sxs-lookup"><span data-stu-id="4c340-136">Data Execution Prevention</span></span>](../memory/data-execution-prevention.md)
-   [<span data-ttu-id="4c340-137">Nuove API NX aggiunte a Windows Vista SP1, Windows XP SP3 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4c340-137">New NX APIs added to Windows Vista SP1, Windows XP SP3 and Windows Server 2008 R2</span></span>](/archive/blogs/michael_howard/)
-   [<span data-ttu-id="4c340-138">Application Compatibility Toolkit Download</span><span class="sxs-lookup"><span data-stu-id="4c340-138">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="4c340-139">[Problemi noti Internet Explorer funzionalità di sicurezza](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="4c340-139">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
