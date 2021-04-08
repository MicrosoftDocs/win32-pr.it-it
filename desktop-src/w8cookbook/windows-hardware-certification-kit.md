---
title: Kit di certificazione hardware Windows
description: Kit di certificazione hardware Windows
ms.assetid: 99BD2D7D-8F9D-445E-AE04-6A58FFF3DCE6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dba820d62d6766f74549ed23f7a5abdccbca258b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104047491"
---
# <a name="windows-hardware-certification-kit"></a><span data-ttu-id="7a7b2-103">Kit di certificazione hardware Windows</span><span class="sxs-lookup"><span data-stu-id="7a7b2-103">Windows Hardware Certification Kit</span></span>

## <a name="platforms"></a><span data-ttu-id="7a7b2-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="7a7b2-104">Platforms</span></span>

 <span data-ttu-id="7a7b2-105">**Client** -Windows 7 \| Windows 8</span><span class="sxs-lookup"><span data-stu-id="7a7b2-105">**Clients** - Windows 7 \| Windows 8</span></span>  
<span data-ttu-id="7a7b2-106">**Server** -windows Server 2008 R2 \| Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a7b2-106">**Servers** - Windows Server 2008 R2 \| Windows Server 2012</span></span>  
<span data-ttu-id="7a7b2-107">**Server/controller** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7a7b2-107">**Server/Controller** - Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="7a7b2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a7b2-108">Description</span></span>

<span data-ttu-id="7a7b2-109">Il kit di certificazione hardware di Windows consente a sviluppatori, ISV, IHV e OEM di certificare i dispositivi hardware, i sistemi e i driver dei filtri per i sistemi operativi Windows più recenti.</span><span class="sxs-lookup"><span data-stu-id="7a7b2-109">The Windows Hardware Certification Kit enables developers, ISVs, IHVs, and OEMs to certify their hardware devices, systems, and filter drivers for the latest Windows operating systems.</span></span> <span data-ttu-id="7a7b2-110">Contiene tutti gli strumenti e la documentazione necessari per certificare l'hardware e filtrare i driver per questi sistemi operativi:</span><span class="sxs-lookup"><span data-stu-id="7a7b2-110">It contains all the tools and documentation that you need to certify your hardware and filter drivers for these operating systems:</span></span>

-   <span data-ttu-id="7a7b2-111">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7a7b2-111">Windows 8</span></span>
-   <span data-ttu-id="7a7b2-112">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a7b2-112">Windows Server 2012</span></span>
-   <span data-ttu-id="7a7b2-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7a7b2-113">Windows 7</span></span>
-   <span data-ttu-id="7a7b2-114">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7a7b2-114">Windows Server 2008 R2</span></span>

<span data-ttu-id="7a7b2-115">Il kit di certificazione hardware di Windows sostituisce Windows Logo Kit ed è parte del programma di certificazione Windows.</span><span class="sxs-lookup"><span data-stu-id="7a7b2-115">The Windows Hardware Certification Kit replaces the Windows Logo Kit and is a part of the Windows Certification Program.</span></span>

## <a name="usage-or-best-practices"></a><span data-ttu-id="7a7b2-116">Utilizzo o procedure consigliate</span><span class="sxs-lookup"><span data-stu-id="7a7b2-116">Usage or best practices</span></span>

<span data-ttu-id="7a7b2-117">Prima di poter testare qualsiasi hardware o driver di filtro, è necessario configurare l'ambiente di test appropriato in base all'hardware o al driver del filtro che si sta certificando.</span><span class="sxs-lookup"><span data-stu-id="7a7b2-117">Before you can test any hardware or filter driver, you must set up the proper test environment based on the hardware or filter driver you are certifying.</span></span> <span data-ttu-id="7a7b2-118">Sono inclusi controller, client e hardware potenzialmente aggiuntivi (ad esempio, dispositivi multifunzione) o software.</span><span class="sxs-lookup"><span data-stu-id="7a7b2-118">This includes the controller, client, and potentially additional hardware (for example, multi-function devices) or software.</span></span> <span data-ttu-id="7a7b2-119">Dopo aver configurato l'ambiente, è possibile testare l'hardware usando il nuovo strumento di studio di HCK.</span><span class="sxs-lookup"><span data-stu-id="7a7b2-119">After your environment is set up, you can test your hardware using the new HCK’s Studio tool.</span></span> <span data-ttu-id="7a7b2-120">Questi passaggi descrivono il processo di test di certificazione.</span><span class="sxs-lookup"><span data-stu-id="7a7b2-120">These steps outline the certification test process.</span></span>

1.  <span data-ttu-id="7a7b2-121">Configurare l'ambiente di test.</span><span class="sxs-lookup"><span data-stu-id="7a7b2-121">Set up test environment.</span></span>
2.  <span data-ttu-id="7a7b2-122">Creare un progetto.</span><span class="sxs-lookup"><span data-stu-id="7a7b2-122">Create a project.</span></span>
3.  <span data-ttu-id="7a7b2-123">Creare uno o più pool di computer.</span><span class="sxs-lookup"><span data-stu-id="7a7b2-123">Create one or more machine pools.</span></span>
4.  <span data-ttu-id="7a7b2-124">Selezionare le funzionalità da convalidare.</span><span class="sxs-lookup"><span data-stu-id="7a7b2-124">Select features to validate.</span></span>
5.  <span data-ttu-id="7a7b2-125">Selezionare ed eseguire i test in base a tali funzionalità.</span><span class="sxs-lookup"><span data-stu-id="7a7b2-125">Select and run tests against those features.</span></span>
6.  <span data-ttu-id="7a7b2-126">Visualizzare i risultati dei test.</span><span class="sxs-lookup"><span data-stu-id="7a7b2-126">View test results.</span></span>
7.  <span data-ttu-id="7a7b2-127">Inviare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7a7b2-127">Submit your package.</span></span>

## <a name="resources"></a><span data-ttu-id="7a7b2-128">Risorse</span><span class="sxs-lookup"><span data-stu-id="7a7b2-128">Resources</span></span>

-   [<span data-ttu-id="7a7b2-129">Sviluppo di hardware Windows</span><span class="sxs-lookup"><span data-stu-id="7a7b2-129">Windows Hardware Development</span></span>](https://msdn.microsoft.com/windows/hardware/)
-   <span data-ttu-id="7a7b2-130">[Programma di certificazione hardware di Windows](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7a7b2-130">[Windows Hardware Certification Program](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))</span></span>
-   <span data-ttu-id="7a7b2-131">[Inizia a sviluppare hardware per Windows](/previous-versions/gg507680(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7a7b2-131">[Start Developing Hardware for Windows](/previous-versions/gg507680(v=msdn.10))</span></span>

 

 