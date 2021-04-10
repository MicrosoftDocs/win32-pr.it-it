---
description: .
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8-Protezione esecuzione dati/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bf23ba40be518e3d4c1421012e6b46fdb7b5e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882618"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a><span data-ttu-id="46cf8-103">Internet Explorer 8-Protezione esecuzione dati/NX</span><span class="sxs-lookup"><span data-stu-id="46cf8-103">Internet Explorer 8 - Data Execution Protection/NX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="46cf8-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="46cf8-104">Affected Platforms</span></span>

 <span data-ttu-id="46cf8-105">**Client** -Windows XP Windows \| Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="46cf8-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="46cf8-106">**Server** -windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46cf8-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  










> [!Note]  
> <span data-ttu-id="46cf8-107">Internet Explorer 8 Abilita la protezione DEP/NX quando viene eseguita in un sistema operativo con la Service Pack più recente.</span><span class="sxs-lookup"><span data-stu-id="46cf8-107">Internet Explorer 8 will enable DEP/NX protection when run on an operating system with the latest service pack.</span></span> <span data-ttu-id="46cf8-108">Per Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1 e Windows Server 2008 tutti i programmi DEP/NX sono abilitati per impostazione predefinita in Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="46cf8-108">Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1, and Windows Server 2008 all have DEP/NX enabled by default in Internet Explorer 8.</span></span>

 

## <a name="feature-impact"></a><span data-ttu-id="46cf8-109">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="46cf8-109">Feature Impact</span></span>

<span data-ttu-id="46cf8-110">**Gravità** -medio</span><span class="sxs-lookup"><span data-stu-id="46cf8-110">**Severity** - Medium</span></span>  
<span data-ttu-id="46cf8-111">**Frequenza** -bassa</span><span class="sxs-lookup"><span data-stu-id="46cf8-111">**Frequency** - Low</span></span>  

> [!Note]  
> <span data-ttu-id="46cf8-112">In genere, qualsiasi applicazione eseguita in Internet Explorer e non è compatibile con DEP/NX si arresterà in modo anomalo all'avvio e non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="46cf8-112">Typically, any application that runs in Internet Explorer and is not compatible with DEP/NX will crash on startup and will not function.</span></span> <span data-ttu-id="46cf8-113">Internet Explorer potrebbe arrestarsi in modo anomalo all'avvio se sono installati componenti aggiuntivi che non sono compatibili con DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="46cf8-113">Internet Explorer may crash on startup if add-ons that are not compatible with DEP/NX are installed.</span></span>

 

## <a name="description"></a><span data-ttu-id="46cf8-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46cf8-114">Description</span></span>

<span data-ttu-id="46cf8-115">DEP/NX è una funzionalità di sicurezza che consente di ridurre le vulnerabilità correlate alla memoria.</span><span class="sxs-lookup"><span data-stu-id="46cf8-115">DEP/NX is a security feature that helps mitigate memory-related vulnerabilities.</span></span> <span data-ttu-id="46cf8-116">A partire da Internet Explorer 8, tutti i processi di Internet Explorer abilitano la funzionalità DEP/NX per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="46cf8-116">As of Internet Explorer 8, all Internet Explorer processes enable the DEP/NX feature by default.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="46cf8-117">Manifesto di effetto</span><span class="sxs-lookup"><span data-stu-id="46cf8-117">Manifestation of Impact</span></span>

<span data-ttu-id="46cf8-118">Il kernel di Windows monitora l'esecuzione di un programma.</span><span class="sxs-lookup"><span data-stu-id="46cf8-118">The Windows Kernel monitors a program's execution.</span></span> <span data-ttu-id="46cf8-119">Se il kernel rileva un tentativo di eseguire codice da una pagina di memoria non contrassegnata come eseguibile, il kernel interrompe l'esecuzione del programma, causando un "arresto anomalo".</span><span class="sxs-lookup"><span data-stu-id="46cf8-119">If the Kernel detects an attempt to run code from a memory page that is not marked executable, the Kernel halts execution of the program, resulting in a "crash."</span></span> <span data-ttu-id="46cf8-120">Si tratta di una misura di sicurezza che consente di garantire che le vulnerabilità correlate alla memoria (ad esempio, gli overflow del buffer) nell'applicazione non possano essere sfruttate per poter eseguire codice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="46cf8-120">This is a security measure to help ensure that memory-related vulnerabilities (for example, buffer overflows) in the application cannot be exploited in order to execute arbitrary code.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="46cf8-121">Attenuazione End-User</span><span class="sxs-lookup"><span data-stu-id="46cf8-121">End-User Mitigation</span></span>

-   <span data-ttu-id="46cf8-122">Installare una versione più recente del componente aggiuntivo o del Framework compatibile con DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="46cf8-122">Install a later version of the add-on or framework that is DEP/NX compatible.</span></span>
-   <span data-ttu-id="46cf8-123">Eseguire Internet Explorer con privilegi elevati come amministratore e quindi disabilitare DEP/NX usando la casella **di controllo Abilita protezione della memoria per attenuare gli attacchi online** nella scheda **Opzioni Internet**  /  **Avanzate** .</span><span class="sxs-lookup"><span data-stu-id="46cf8-123">Run Internet Explorer elevated as Administrator, and then disable DEP/NX using the **Enable memory protection to help mitigate online attacks** check box on the **Internet Options** / **Advanced** tab.</span></span>

## <a name="developer-solution"></a><span data-ttu-id="46cf8-124">Soluzione per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="46cf8-124">Developer Solution</span></span>

<span data-ttu-id="46cf8-125">Compilare applicazioni usando le versioni più recenti dei Framework compatibili con DEP.</span><span class="sxs-lookup"><span data-stu-id="46cf8-125">Compile applications by using the latest versions of frameworks that are DEP compatible.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="46cf8-126">Sfruttando le funzionalità</span><span class="sxs-lookup"><span data-stu-id="46cf8-126">Leveraging Feature Capabilities</span></span>

-   <span data-ttu-id="46cf8-127">Usare l'opzione del linker/NXCOMPAT per indicare la compatibilità DEP/NX</span><span class="sxs-lookup"><span data-stu-id="46cf8-127">Use the /NXCOMPAT linker option to indicate DEP/NX compatibility</span></span>
-   <span data-ttu-id="46cf8-128">Scegli il codice in altre difese disponibili, ad esempio/GS (stack Defense), gestione eccezioni sicure (/SafeSEH) e ASLR (/DynamicBase)</span><span class="sxs-lookup"><span data-stu-id="46cf8-128">Opt your code into other available defenses like stack defense (/GS), safe exception handling (/SafeSEH), and ASLR (/DynamicBase)</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="46cf8-129">Compatibilità, prestazioni, affidabilità e test di usabilità</span><span class="sxs-lookup"><span data-stu-id="46cf8-129">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="46cf8-130">Testare il codice con DEP/NX abilitato utilizzando la versione più recente di Internet Explorer rilasciata in Windows Vista SP1 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="46cf8-130">Test your code with DEP/NX enabled by using latest released Internet Explorer version on Windows Vista SP1 or later.</span></span>
-   <span data-ttu-id="46cf8-131">Eseguire un test con Internet Explorer 7 in Windows Vista dopo aver abilitato l'opzione DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="46cf8-131">Test with Internet Explorer 7 on Windows Vista after enabling the DEP/NX option.</span></span> <span data-ttu-id="46cf8-132">Per abilitare DEP/NX per Internet Explorer 7, eseguire Internet Explorer come amministratore, quindi impostare la casella di controllo appropriata nella scheda strumenti > Internet opzioni > avanzate.</span><span class="sxs-lookup"><span data-stu-id="46cf8-132">To enable DEP/NX for Internet Explorer 7, run Internet Explorer as an administrator, then set the appropriate check box in the Tools > Internet Options > Advanced tab.</span></span>
-   <span data-ttu-id="46cf8-133">Eseguire lo strumento di test di compatibilità di Internet Explorer (IECTT), fornito con Application Compatibility Toolkit (ACT) per individuare eventuali problemi causati dalle modifiche DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="46cf8-133">Run the Internet Explorer Compatibility Test Tool (IECTT), provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to the DEP/NX changes.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="46cf8-134">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="46cf8-134">Links to Other Resources</span></span>

-   [<span data-ttu-id="46cf8-135">Sicurezza di Internet Explorer 8 parte I: protezione della memoria DEP/NX</span><span class="sxs-lookup"><span data-stu-id="46cf8-135">Internet Explorer 8 Security Part I: DEP/NX Memory Protection</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="46cf8-136">Protezione esecuzione programmi</span><span class="sxs-lookup"><span data-stu-id="46cf8-136">Data Execution Prevention</span></span>](../memory/data-execution-prevention.md)
-   [<span data-ttu-id="46cf8-137">Nuove API NX aggiunte a Windows Vista SP1, Windows XP SP3 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46cf8-137">New NX APIs added to Windows Vista SP1, Windows XP SP3 and Windows Server 2008 R2</span></span>](/archive/blogs/michael_howard/)
-   [<span data-ttu-id="46cf8-138">Download di Application Compatibility Toolkit</span><span class="sxs-lookup"><span data-stu-id="46cf8-138">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="46cf8-139">[Problemi noti relativi alle funzionalità di sicurezza di Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="46cf8-139">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
