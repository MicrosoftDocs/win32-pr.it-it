---
description: Informazioni su come usare lo strumento Standard User Analyzer (SUA) e la procedura guidata di SUA per testare le applicazioni e rilevare potenziali problemi di compatibilità.
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: Strumento Analizzatore utente standard e procedura guidata Analizzatore utente standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a897c603f185db775c059e4b3dd4a040cba9ad
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314584"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a><span data-ttu-id="109c4-103">Strumento Analizzatore utente standard e procedura guidata Analizzatore utente standard</span><span class="sxs-lookup"><span data-stu-id="109c4-103">Standard User Analyzer (SUA) Tool and Standard User Analyzer Wizard (SUA Wizard)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="109c4-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="109c4-104">Affected Platforms</span></span>

<span data-ttu-id="109c4-105">**Client:** Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="109c4-105">**Clients:** Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="109c4-106">**Server:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="109c4-106">**Servers:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  

## <a name="description"></a><span data-ttu-id="109c4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="109c4-107">Description</span></span>

<span data-ttu-id="109c4-108">Application Compatibility Toolkit include lo strumento Standard User Analyzer (SUA) e la procedura guidata dell'Analizzatore utente standard.</span><span class="sxs-lookup"><span data-stu-id="109c4-108">The Application Compatibility Toolkit includes the Standard User Analyzer (SUA) tool and the Standard User Analyzer Wizard (SUA Wizard).</span></span> <span data-ttu-id="109c4-109">Questi strumenti consentono di testare le applicazioni e di monitorare le chiamate API per rilevare potenziali problemi di compatibilità dovuti alla funzionalità controllo dell'account utente (UAC) nel sistema operativo Windows 7.</span><span class="sxs-lookup"><span data-stu-id="109c4-109">These tools enable you to test your applications and to monitor API calls in order to detect potential compatibility issues due to the User Account Control (UAC) feature in the Windows 7 operating system.</span></span>

<span data-ttu-id="109c4-110">UAC, noto in precedenza come account utente limitato (LUA), richiede che tutti gli utenti (inclusi i membri del gruppo Administrator) vengano eseguiti come utenti standard utilizzando la finestra di dialogo richiesta di sicurezza finché l'applicazione non viene deliberatamente elevata.</span><span class="sxs-lookup"><span data-stu-id="109c4-110">UAC, formerly known as Limited User Account (LUA), requires that all users (including members of the Administrator group) run as Standard Users by using the security prompt dialog box until the application is deliberately elevated.</span></span> <span data-ttu-id="109c4-111">Tuttavia, le applicazioni che richiedono l'accesso e i privilegi per percorsi non disponibili per un utente standard non possono essere eseguite correttamente con il ruolo utente standard.</span><span class="sxs-lookup"><span data-stu-id="109c4-111">However, applications that require access and privileges for locations that are unavailable to a Standard User cannot run properly with the Standard User role.</span></span>

## <a name="usage"></a><span data-ttu-id="109c4-112">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="109c4-112">Usage</span></span>

<span data-ttu-id="109c4-113">Nelle sezioni seguenti vengono fornite informazioni dettagliate sull'utilizzo degli strumenti della procedura guidata di SUA e di SUA.</span><span class="sxs-lookup"><span data-stu-id="109c4-113">The following sections provide detailed information about how to use the SUA and SUA Wizard tools.</span></span>

<span data-ttu-id="109c4-114">**Strumento SUA**</span><span class="sxs-lookup"><span data-stu-id="109c4-114">**SUA Tool**</span></span>

<span data-ttu-id="109c4-115">Lo strumento SUA consente di analizzare un'applicazione, esaminare un report dettagliato sui problemi correlati al controllo dell'account utente e quindi applicare le attenuazioni delle applicazioni suggerite e selezionate, come illustrato nel diagramma di flusso seguente.</span><span class="sxs-lookup"><span data-stu-id="109c4-115">The SUA tool enables you to analyze an application, review a detailed report about the UAC-related issues, and then apply the suggested and selected application mitigations, as shown in the following flowchart.</span></span>

![Diagramma che mostra il flusso dello strumento S U A.](images/act-suaflowchart-appcookbook.gif)

<span data-ttu-id="109c4-117">*Strumento e virtualizzazione di SUA*</span><span class="sxs-lookup"><span data-stu-id="109c4-117">*SUA Tool and Virtualization*</span></span>

<span data-ttu-id="109c4-118">Solo lo strumento SUA consente di attivare e disattivare la funzionalità di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="109c4-118">Only the SUA tool enables you to turn on and off the virtualization feature.</span></span> <span data-ttu-id="109c4-119">Con la disattivazione della funzionalità di virtualizzazione, l'applicazione testata si comporterà in modo più simile quando funziona nel sistema operativo Windows XP.</span><span class="sxs-lookup"><span data-stu-id="109c4-119">By turning off the virtualization feature, the tested application will behave more like when it is functioning on the Windows XP operating system.</span></span>

<span data-ttu-id="109c4-120">*Strumento SUA e privilegi elevati*</span><span class="sxs-lookup"><span data-stu-id="109c4-120">*SUA Tool and Elevated Privileges*</span></span>

<span data-ttu-id="109c4-121">Solo lo strumento SUA consente di attivare e disattivare la funzionalità di **avvio con privilegi elevati** .</span><span class="sxs-lookup"><span data-stu-id="109c4-121">Only the SUA tool enables you to turn on and off the **Launch Elevated** feature.</span></span> <span data-ttu-id="109c4-122">La funzionalità di avvio con privilegi elevati consente di eseguire l'applicazione selezionata come amministratore o come utente standard.</span><span class="sxs-lookup"><span data-stu-id="109c4-122">The Launch Elevated feature enables the selected application to run as an Administrator or as a Standard User.</span></span> <span data-ttu-id="109c4-123">A seconda della selezione effettuata, si troveranno tipi diversi di problemi correlati a UAC.</span><span class="sxs-lookup"><span data-stu-id="109c4-123">Depending on your selection, you will locate different types of UAC-related issues.</span></span> <span data-ttu-id="109c4-124">Se si deseleziona la casella di controllo avvia con privilegi **elevati** , l'applicazione viene eseguita con privilegi di amministratore completi, consentendo a sua di prevedere i problemi che potrebbero verificarsi per un utente standard.</span><span class="sxs-lookup"><span data-stu-id="109c4-124">If you clear the **Launch Elevated** check box, your application will run with full Administrator privileges, which enables SUA to predict the issues that might occur for a Standard User.</span></span> <span data-ttu-id="109c4-125">Se si seleziona la casella di controllo avvia con privilegi elevati, vengono visualizzati gli errori che risultano dall'applicazione in esecuzione e generano errori.</span><span class="sxs-lookup"><span data-stu-id="109c4-125">If you select the Launch Elevated check box, you will see errors that result from the application actually running and generating errors.</span></span>

<span data-ttu-id="109c4-126">**Procedura guidata di SUA**</span><span class="sxs-lookup"><span data-stu-id="109c4-126">**SUA Wizard**</span></span>

<span data-ttu-id="109c4-127">La procedura guidata di SUA guida consente di seguire un processo dettagliato che consente di analizzare un'applicazione e quindi di applicare le attenuazioni delle applicazioni suggerite e selezionate, come illustrato nel diagramma di flusso seguente.</span><span class="sxs-lookup"><span data-stu-id="109c4-127">The SUA Wizard enables you to follow a guided, step-by-step process by which you can analyze an application and then apply the suggested and selected application mitigations, as shown in the following flowchart.</span></span> <span data-ttu-id="109c4-128">A differenza dello strumento SUA, la procedura guidata non consente di esaminare i problemi dettagliati relativi all'UAC.</span><span class="sxs-lookup"><span data-stu-id="109c4-128">Unlike the SUA tool, the wizard does not enable a review of the detailed UAC-related issues.</span></span>

![Diagramma che mostra il flusso della procedura guidata S U A.](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a><span data-ttu-id="109c4-130">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="109c4-130">Links to Other Resources</span></span>

-   [<span data-ttu-id="109c4-131">Download di Application Compatibility Toolkit</span><span class="sxs-lookup"><span data-stu-id="109c4-131">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="109c4-132">[Informazioni sugli strumenti dell'Analizzatore utente standard](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="109c4-132">[Understanding the Standard User Analyzer Tools](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))</span></span>
-   <span data-ttu-id="109c4-133">[Riferimento tecnico per l'Analizzatore utente standard](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="109c4-133">[Standard User Analyzer Technical Reference](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))</span></span>
-   <span data-ttu-id="109c4-134">[Test e attenuazione dei problemi tramite gli strumenti di sviluppo](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="109c4-134">[Testing and Mitigating Issues by Using the Development Tools](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))</span></span>
-   [<span data-ttu-id="109c4-135">Compatibilità delle applicazioni e controllo dell'account utente</span><span class="sxs-lookup"><span data-stu-id="109c4-135">Application Compatibility and User Account Control</span></span>](/previous-versions/windows/)

> [!Note]  
> <span data-ttu-id="109c4-136">Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="109c4-136">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
