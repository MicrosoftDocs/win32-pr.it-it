---
description: .
ms.assetid: 11169540-555A-48A9-A4CD-535D5765C005
title: Internet Explorer Compatibility Test Tool (IECTT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25e39263f448c7e11db1be32463b3801e4a8761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313699"
---
# <a name="internet-explorer-compatibility-test-tool-iectt"></a><span data-ttu-id="c4855-103">Internet Explorer Compatibility Test Tool (IECTT)</span><span class="sxs-lookup"><span data-stu-id="c4855-103">Internet Explorer Compatibility Test Tool (IECTT)</span></span>

<span data-ttu-id="c4855-104">Lo strumento di verifica della compatibilità di Internet Explorer (IECTT) è un componente di [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span><span class="sxs-lookup"><span data-stu-id="c4855-104">The Internet Explorer Compatibility Test Tool (IECTT) is a component of the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span></span> <span data-ttu-id="c4855-105">Questo strumento consente di diagnosticare i problemi nelle applicazioni Web visualizzando i problemi in tempo reale e, facoltativamente, di caricare i risultati in un database ACT.</span><span class="sxs-lookup"><span data-stu-id="c4855-105">This tool can help you diagnose issues in your web applications by displaying issues in real time and optionally uploading the results to an ACT database.</span></span> <span data-ttu-id="c4855-106">I risultati includono informazioni dettagliate sui possibili problemi di compatibilità e sui collegamenti per ulteriori informazioni su ogni problema di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="c4855-106">The results include details about possible compatibility issues and links for more information about each compatibility issue.</span></span> <span data-ttu-id="c4855-107">IECTT consente inoltre di escludere i problemi e modificare gli attributi disponibili.</span><span class="sxs-lookup"><span data-stu-id="c4855-107">IECTT also enables you to exclude issues and modify available attributes.</span></span>

## <a name="to-open-iectt"></a><span data-ttu-id="c4855-108">Per aprire IECTT</span><span class="sxs-lookup"><span data-stu-id="c4855-108">To open IECTT</span></span>

1.  <span data-ttu-id="c4855-109">Installare [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span><span class="sxs-lookup"><span data-stu-id="c4855-109">Install the [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).</span></span>
2.  <span data-ttu-id="c4855-110">Fare clic sul pulsante **Start**, scegliere **programmi**, **Microsoft Application Compatibility Toolkit 5,6**, scegliere **strumenti per sviluppatori e tester**, quindi fare clic su **strumento di test di compatibilità di Internet Explorer**.</span><span class="sxs-lookup"><span data-stu-id="c4855-110">Click **Start**, point to **Programs**, point to **Microsoft Application Compatibility Toolkit 5.6**, point to **Developer and Tester Tools**, and then click **Internet Explorer Compatibility Test Tool**.</span></span>

<span data-ttu-id="c4855-111">Le sezioni seguenti descrivono scenari IECTT comuni.</span><span class="sxs-lookup"><span data-stu-id="c4855-111">The following sections describe common IECTT scenarios.</span></span>

## <a name="view-issues-in-real-time"></a><span data-ttu-id="c4855-112">Visualizza i problemi in tempo reale</span><span class="sxs-lookup"><span data-stu-id="c4855-112">View Issues in Real Time</span></span>

<span data-ttu-id="c4855-113">È possibile individuare e visualizzare i problemi basati sul Web in tempo reale, mentre si esegue il test di siti Web e applicazioni Web in Windows Internet Explorer 7 e Windows Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="c4855-113">You can locate and view your web-based issues in real time, while you are testing your websites and web applications against Windows Internet Explorer 7 and Windows Internet Explorer 8.</span></span> <span data-ttu-id="c4855-114">Dopo aver completato il test, è possibile visualizzare i risultati nella schermata **Live Data** del IECTT.</span><span class="sxs-lookup"><span data-stu-id="c4855-114">After you complete your testing, you can view your results in the **Live Data** screen of the IECTT.</span></span>

## <a name="upload-issues-to-your-act-database"></a><span data-ttu-id="c4855-115">Caricare problemi nel database ACT</span><span class="sxs-lookup"><span data-stu-id="c4855-115">Upload Issues to Your ACT Database</span></span>

<span data-ttu-id="c4855-116">È possibile caricare i problemi basati sul Web nel database ACT, che elabora le informazioni e consente di visualizzare i risultati nella schermata **analizza** di gestione compatibilità applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c4855-116">You can upload your web-based issues to the ACT database, which processes the information and enables you to view your results on the **Analyze** screen of the Application Compatibility Manager.</span></span>

## <a name="collect-your-compatibility-data"></a><span data-ttu-id="c4855-117">Raccogliere i dati di compatibilità</span><span class="sxs-lookup"><span data-stu-id="c4855-117">Collect Your Compatibility Data</span></span>

<span data-ttu-id="c4855-118">È possibile raccogliere i dati di compatibilità del sito Web e dell'applicazione Web utilizzando lo strumento IECTT con Internet Explorer 7 o Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="c4855-118">You can collect your website and web application-related compatibility data by using the IECTT tool with either Internet Explorer 7 or Internet Explorer 7.</span></span>

<span data-ttu-id="c4855-119">**Per raccogliere i dati di compatibilità**</span><span class="sxs-lookup"><span data-stu-id="c4855-119">**To collect your compatibility data**</span></span>

1.  <span data-ttu-id="c4855-120">Chiudere tutte le finestre di Windows Internet Explorer attive.</span><span class="sxs-lookup"><span data-stu-id="c4855-120">Close all of your active Windows Internet Explorer windows.</span></span>
2.  <span data-ttu-id="c4855-121">In IECTT, sulla barra degli strumenti di **test di compatibilità di Internet Explorer** , fare clic su **Abilita**.</span><span class="sxs-lookup"><span data-stu-id="c4855-121">In IECTT, on the **Internet Explorer Compatibility Test Tool** toolbar, click **Enable**.</span></span>
3.  <span data-ttu-id="c4855-122">Aprire una finestra di Internet Explorer 7 o Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="c4855-122">Open an Internet Explorer 7 or Internet Explorer 8 window.</span></span>

    <span data-ttu-id="c4855-123">Viene visualizzato un messaggio che indica che la registrazione della valutazione della compatibilità è attivata.</span><span class="sxs-lookup"><span data-stu-id="c4855-123">A message appears and states that compatibility evaluation logging is turned on.</span></span>

4.  <span data-ttu-id="c4855-124">Visitare i siti Web o le applicazioni Web che sono necessari per l'uso da parte dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="c4855-124">Visit the websites or web applications that are required for use by your organization.</span></span> <span data-ttu-id="c4855-125">Quando si visita ogni sito, lo strumento IECTT Visualizza in tempo reale i potenziali problemi di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="c4855-125">As you visit each site, the IECTT tool displays, in real-time, your potential compatibility issues.</span></span>
5.  <span data-ttu-id="c4855-126">Sulla barra degli strumenti di **test di compatibilità di Internet Explorer** fare clic su **Disabilita** al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c4855-126">On the **Internet Explorer Compatibility Test Tool** toolbar, click **Disable** when you are done.</span></span>

    <span data-ttu-id="c4855-127">Il processo di registrazione della compatibilità termina e si arresta.</span><span class="sxs-lookup"><span data-stu-id="c4855-127">The compatibility logging process finishes and stops.</span></span>

## <a name="filter-your-issue-results"></a><span data-ttu-id="c4855-128">Filtrare i risultati del problema</span><span class="sxs-lookup"><span data-stu-id="c4855-128">Filter Your Issue Results</span></span>

<span data-ttu-id="c4855-129">È possibile filtrare i risultati di IECTT in base al nome dell'oggetto, al tipo di problema o a entrambi.</span><span class="sxs-lookup"><span data-stu-id="c4855-129">You can filter any of your IECTT results by object name, by issue type, or by both.</span></span>

<span data-ttu-id="c4855-130">**Per filtrare i risultati del problema**</span><span class="sxs-lookup"><span data-stu-id="c4855-130">**To filter your issue results**</span></span>

1.  <span data-ttu-id="c4855-131">Nella schermata dello **strumento di test della compatibilità di Internet Explorer** fare clic su **filtro**.</span><span class="sxs-lookup"><span data-stu-id="c4855-131">On the **Internet Explorer Compatibility Test Tool** screen, click **Filter**.</span></span>

    <span data-ttu-id="c4855-132">Verrà visualizzata la finestra di dialogo **filtro problemi** .</span><span class="sxs-lookup"><span data-stu-id="c4855-132">The **Issues Filter** dialog box appears.</span></span>

2.  <span data-ttu-id="c4855-133">Immettere il nome dell'oggetto che si desidera visualizzare nella casella **immettere il nome dell'oggetto per visualizzare i problemi relativi** a.</span><span class="sxs-lookup"><span data-stu-id="c4855-133">Enter the name of the object that you intend to view in the **Enter the name of the object to view issues for** box.</span></span>

<span data-ttu-id="c4855-134">Per ulteriori informazioni su questo strumento e sugli altri strumenti per sviluppatori, vedere la pagina relativa [allo strumento di test della compatibilità di Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) in MSDN Library e il post di Blog relativo alla [registrazione per la compatibilità delle applicazioni in IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) .</span><span class="sxs-lookup"><span data-stu-id="c4855-134">For more information about this tool and other developers tools, see [What is the Internet Explorer Compatibility Test Tool?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) in the MSDN Library and the [Application Compatibility Logging in IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) blog post.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4855-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4855-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4855-136">Strumenti per il debug di applicazioni Web e componenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="c4855-136">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 
