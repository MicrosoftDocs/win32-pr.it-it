---
title: Microsoft Platform Ready Test Tool
description: Microsoft Platform Ready Test Tool
ms.assetid: C41FBE70-E392-4FD0-954B-6C24168CB93E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6286e7ed64f013a8ea002ea392ba0d3bcac67296
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730727"
---
# <a name="microsoft-platform-ready-test-tool"></a><span data-ttu-id="994f2-103">Microsoft Platform Ready Test Tool</span><span class="sxs-lookup"><span data-stu-id="994f2-103">Microsoft Platform Ready Test Tool</span></span>

## <a name="platform"></a><span data-ttu-id="994f2-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="994f2-104">Platform</span></span>

 <span data-ttu-id="994f2-105">**Server** : windows Server 2012 \| Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="994f2-105">**Servers** – Windows Server 2012 \| Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="994f2-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="994f2-106">Description</span></span>

<span data-ttu-id="994f2-107">Lo strumento di test Microsoft Platform Ready (MPR) viene usato per la preparazione delle applicazioni per la piattaforma e per convalidare la conformità ai requisiti di certificazione per le applicazioni Windows Server 2012 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="994f2-107">The Microsoft Platform Ready (MPR) Test Tool is used for platform application readiness and to validate compliance with certification requirements for Windows Server 2012 and Windows Server 2012 R2 applications.</span></span>

<span data-ttu-id="994f2-108">Microsoft consiglia vivamente di incorporare lo strumento di test di MPR nei processi di compilazione e test del software, garantendo in tal modo la preparazione della piattaforma prima che le applicazioni vengano rilasciate sul mercato.</span><span class="sxs-lookup"><span data-stu-id="994f2-108">Microsoft strongly encourages incorporating the MPR Test Tool into the software build and test processes, thereby ensuring platform readiness before applications are released to market.</span></span> <span data-ttu-id="994f2-109">Lo strumento di test di MPR è inoltre uno strumento consigliato per testare le applicazioni line-of-business e per valutare i prodotti server per la compatibilità della piattaforma prima di prendere decisioni di acquisto.</span><span class="sxs-lookup"><span data-stu-id="994f2-109">The MPR Test Tool is also a recommended tool to test line of business applications and for evaluating server products for their platform compatibility before making purchasing decisions.</span></span>

## <a name="requirements"></a><span data-ttu-id="994f2-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="994f2-110">Requirements</span></span>

<span data-ttu-id="994f2-111">Lo strumento di test di MPR include test automatizzati per:</span><span class="sxs-lookup"><span data-stu-id="994f2-111">The MPR Test Tool includes automated tests for:</span></span>

-   <span data-ttu-id="994f2-112">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="994f2-112">Windows Installer</span></span>
-   <span data-ttu-id="994f2-113">Installazione e funzionalità primarie</span><span class="sxs-lookup"><span data-stu-id="994f2-113">Setup and Primary Functionality</span></span>
-   <span data-ttu-id="994f2-114">Driver e sicurezza</span><span class="sxs-lookup"><span data-stu-id="994f2-114">Drivers and Security</span></span>
-   <span data-ttu-id="994f2-115">Procedure consigliate</span><span class="sxs-lookup"><span data-stu-id="994f2-115">Best Practices</span></span>

<span data-ttu-id="994f2-116">Il test automatico e l'invio di risultati per la maggior parte delle app Server dovrebbero richiedere almeno due ore; app più complesse possono richiedere circa 4 ore.</span><span class="sxs-lookup"><span data-stu-id="994f2-116">Self-testing and submission of results for most Server apps should take 2 hours or less; more complex apps can take around 4 hours.</span></span>

<span data-ttu-id="994f2-117">Tutti i driver devono passare separatamente i test di certificazione hardware Windows ed essere firmati da Microsoft per Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="994f2-117">All drivers must separately pass Windows Hardware Certification testing and be signed by Microsoft for Windows Server 2012.</span></span>

## <a name="usage"></a><span data-ttu-id="994f2-118">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="994f2-118">Usage</span></span>

<span data-ttu-id="994f2-119">Per testare le app:</span><span class="sxs-lookup"><span data-stu-id="994f2-119">To test your apps:</span></span>

1.  <span data-ttu-id="994f2-120">Installare la versione più recente di Windows Server 2012 Configuration (GUI completa, interfaccia server minima o Server Core) in base alle esigenze dell'app.</span><span class="sxs-lookup"><span data-stu-id="994f2-120">Install the latest Windows Server 2012 minimum configuration (Full Server GUI, Minimal Server Interface, or Server Core) as required for your app.</span></span>
2.  <span data-ttu-id="994f2-121">Esaminare i requisiti di certificazione.</span><span class="sxs-lookup"><span data-stu-id="994f2-121">Review the certification requirements.</span></span>
3.  <span data-ttu-id="994f2-122">In un sistema pulito eseguire lo strumento di test di MPR in modalità interfaccia utente completa o in modalità riga di comando.</span><span class="sxs-lookup"><span data-stu-id="994f2-122">On a clean system, run the MPR Test Tool in either full UI mode or command line mode.</span></span>
4.  <span data-ttu-id="994f2-123">Completare il processo di test guidato autonomamente.</span><span class="sxs-lookup"><span data-stu-id="994f2-123">Complete the self-guided testing process.</span></span>
5.  <span data-ttu-id="994f2-124">Esaminare i risultati e correggere l'app secondo le esigenze.</span><span class="sxs-lookup"><span data-stu-id="994f2-124">Review results and fix your app as required.</span></span>
6.  <span data-ttu-id="994f2-125">Eseguire l'accesso e caricare i risultati nel portale di Microsoft Platform Ready per l'elenco nel catalogo di Windows Server e l'utilizzo del logo.</span><span class="sxs-lookup"><span data-stu-id="994f2-125">Sign-in and upload successful results to Microsoft Platform Ready portal for listing in Windows Server Catalog and usage of the logo.</span></span>

## <a name="resources"></a><span data-ttu-id="994f2-126">Risorse</span><span class="sxs-lookup"><span data-stu-id="994f2-126">Resources</span></span>

-   [<span data-ttu-id="994f2-127">Requisiti per il programma di certificazione delle app di Windows Server</span><span class="sxs-lookup"><span data-stu-id="994f2-127">Requirements for Windows Server App Certification Program</span></span>](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [<span data-ttu-id="994f2-128">Microsoft Platform Ready (MPR) Test Tool</span><span class="sxs-lookup"><span data-stu-id="994f2-128">Microsoft Platform Ready (MPR) Test Tool</span></span>](https://www.microsoft.com/download/details.aspx?id=37143)
-   [<span data-ttu-id="994f2-129">Programma di certificazione applicazioni Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="994f2-129">Windows Server 2012 Application Certification Program</span></span>](https://azure.microsoft.com/overview/commercial-marketplace/)
-   [<span data-ttu-id="994f2-130">Commenti sul logo di Windows Server</span><span class="sxs-lookup"><span data-stu-id="994f2-130">Windows Server Logo Feedback</span></span>](mailto:WSLogoFB@microsoft.com)

 

 