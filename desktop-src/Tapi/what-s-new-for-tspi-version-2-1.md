---
description: A partire da TAPI 2,1, è possibile usare le DLL dell'interfaccia utente del provider di servizi di telefonia per gestire e visualizzare le finestre di dialogo. Tramite TAPI la DLL viene caricata nel processo di un'applicazione che richiama una delle funzioni del provider di servizi in grado di visualizzare una finestra di dialogo.
ms.assetid: 0a0320d1-fb75-405e-8074-b37cef956c9f
title: Novità della versione 2,1 di TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51642fb9ac960732f8e4a56805652333d0c32468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314119"
---
# <a name="whats-new-for-tspi-version-21"></a><span data-ttu-id="2b704-104">Novità della versione 2,1 di TSPI</span><span class="sxs-lookup"><span data-stu-id="2b704-104">What's New for TSPI Version 2.1</span></span>

<span data-ttu-id="2b704-105">A partire da TAPI 2,1, è possibile usare le DLL dell'interfaccia utente del provider di servizi di telefonia per gestire e visualizzare le finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="2b704-105">Starting with TAPI 2.1, the telephony service provider user interface DLLs can be used to manage and display dialog boxes.</span></span> <span data-ttu-id="2b704-106">Tramite TAPI la DLL viene caricata nel processo di un'applicazione che richiama una delle funzioni del provider di servizi in grado di visualizzare una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="2b704-106">TAPI loads the DLL into the process of an application that invokes any of the service provider functions that can display a dialog.</span></span>

<span data-ttu-id="2b704-107">A partire da TAPI 2,1, i gestori di richieste proxy possono essere implementati.</span><span class="sxs-lookup"><span data-stu-id="2b704-107">Starting with TAPI 2.1, proxy request handlers can be implemented.</span></span> <span data-ttu-id="2b704-108">Un gestore è un'applicazione di telefonia completa che in genere viene eseguita in un server di telefonia e fornisce servizi implementati in modo più appropriato in un'applicazione rispetto a un driver.</span><span class="sxs-lookup"><span data-stu-id="2b704-108">A handler is a full telephony application that normally executes on a telephony server and provides services that are more appropriately implemented in an application than a driver.</span></span>

<span data-ttu-id="2b704-109">Le funzioni e i messaggi nuovi o modificati per TSPI versione 2,1 sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b704-109">Functions and messages that were new or changed for TSPI version 2.1 are as follows:</span></span>

-   [<span data-ttu-id="2b704-110">**TSPI_lineConditionalMediaDetection**</span><span class="sxs-lookup"><span data-stu-id="2b704-110">**TSPI_lineConditionalMediaDetection**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   <span data-ttu-id="2b704-111">**TSPI_lineDropNoOwner**:**obsoleto**</span><span class="sxs-lookup"><span data-stu-id="2b704-111">**TSPI_lineDropNoOwner**—**obsolete**</span></span>
-   <span data-ttu-id="2b704-112">**TSPI_lineDropOnClose**:**obsoleto**</span><span class="sxs-lookup"><span data-stu-id="2b704-112">**TSPI_lineDropOnClose**—**obsolete**</span></span>
-   [<span data-ttu-id="2b704-113">**TSPI_lineGetID**</span><span class="sxs-lookup"><span data-stu-id="2b704-113">**TSPI_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [<span data-ttu-id="2b704-114">**TSPI_lineSetCallData**</span><span class="sxs-lookup"><span data-stu-id="2b704-114">**TSPI_lineSetCallData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [<span data-ttu-id="2b704-115">**TSPI_lineSetCallQualityOfService**</span><span class="sxs-lookup"><span data-stu-id="2b704-115">**TSPI_lineSetCallQualityOfService**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [<span data-ttu-id="2b704-116">**TSPI_lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="2b704-116">**TSPI_lineSetCallTreatment**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [<span data-ttu-id="2b704-117">**TSPI_lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="2b704-117">**TSPI_lineSetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [<span data-ttu-id="2b704-118">**TSPI_phoneGetID**</span><span class="sxs-lookup"><span data-stu-id="2b704-118">**TSPI_phoneGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_phonegetid)
-   [<span data-ttu-id="2b704-119">**TSPI_providerInit**</span><span class="sxs-lookup"><span data-stu-id="2b704-119">**TSPI_providerInit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)
-   [<span data-ttu-id="2b704-120">**TSPI_providerShutdown**</span><span class="sxs-lookup"><span data-stu-id="2b704-120">**TSPI_providerShutdown**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)
-   <span data-ttu-id="2b704-121">[**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b704-121">[**LINE_GATHERDIGITS**](/previous-versions/windows/desktop/legacy/ms725229(v=vs.85))</span></span>
-   <span data-ttu-id="2b704-122">[**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b704-122">[**LINE_GENERATE**](/previous-versions/windows/desktop/legacy/ms725230(v=vs.85))</span></span>
-   <span data-ttu-id="2b704-123">[**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b704-123">[**LINE_MONITORDIGITS**](/previous-versions/windows/desktop/legacy/ms725232(v=vs.85))</span></span>
-   <span data-ttu-id="2b704-124">[**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b704-124">[**LINE_MONITORMEDIA**](/previous-versions/windows/desktop/legacy/ms725233(v=vs.85))</span></span>
-   <span data-ttu-id="2b704-125">[**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b704-125">[**LINE_MONITORTONE**](/previous-versions/windows/desktop/legacy/ms725234(v=vs.85))</span></span>
-   <span data-ttu-id="2b704-126">[**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b704-126">[**LINE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725237(v=vs.85))</span></span>
-   <span data-ttu-id="2b704-127">[**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b704-127">[**PHONE_REMOVE**](/previous-versions/windows/desktop/legacy/ms725260(v=vs.85))</span></span>

<span data-ttu-id="2b704-128">La DLL dell'interfaccia utente del provider di servizi di telefonia fornisce un mezzo per consentire l'interazione dell'utente all'interno del contesto dell'applicazione invece che del provider di servizi stesso.</span><span class="sxs-lookup"><span data-stu-id="2b704-128">The Telephony service provider user interface DLL provides a means of allowing user interaction within the context of the application rather than the service provider itself.</span></span> <span data-ttu-id="2b704-129">TSPI versione 2,1 ha fornito le nuove funzioni, i messaggi e le strutture seguenti per l'implementazione:</span><span class="sxs-lookup"><span data-stu-id="2b704-129">TSPI version 2.1 delivered the following new functions, messages, and structures for implementation:</span></span>

-   [<span data-ttu-id="2b704-130">**TSPI_providerFreeDialogInstance**</span><span class="sxs-lookup"><span data-stu-id="2b704-130">**TSPI_providerFreeDialogInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance)
-   [<span data-ttu-id="2b704-131">**TSPI_providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="2b704-131">**TSPI_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata)
-   [<span data-ttu-id="2b704-132">**TSPI_providerUIIdentify**</span><span class="sxs-lookup"><span data-stu-id="2b704-132">**TSPI_providerUIIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify)
-   [<span data-ttu-id="2b704-133">**TUISPI_lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="2b704-133">**TUISPI_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)
-   [<span data-ttu-id="2b704-134">**TUISPI_lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="2b704-134">**TUISPI_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit)
-   [<span data-ttu-id="2b704-135">**TUISPI_phoneConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="2b704-135">**TUISPI_phoneConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog)
-   [<span data-ttu-id="2b704-136">**TUISPI_providerConfig**</span><span class="sxs-lookup"><span data-stu-id="2b704-136">**TUISPI_providerConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig)
-   [<span data-ttu-id="2b704-137">**TUISPI_providerGenericDialog**</span><span class="sxs-lookup"><span data-stu-id="2b704-137">**TUISPI_providerGenericDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog)
-   [<span data-ttu-id="2b704-138">**TUISPI_providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="2b704-138">**TUISPI_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
-   [<span data-ttu-id="2b704-139">**TUISPI_providerInstall**</span><span class="sxs-lookup"><span data-stu-id="2b704-139">**TUISPI_providerInstall**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)
-   [<span data-ttu-id="2b704-140">**TUISPI_providerRemove**</span><span class="sxs-lookup"><span data-stu-id="2b704-140">**TUISPI_providerRemove**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)
-   [<span data-ttu-id="2b704-141">**TUISPICREATEDIALOGINSTANCEPARAMS**</span><span class="sxs-lookup"><span data-stu-id="2b704-141">**TUISPICREATEDIALOGINSTANCEPARAMS**</span></span>](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
-   [<span data-ttu-id="2b704-142">**TUISPIDLLCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="2b704-142">**TUISPIDLLCALLBACK**</span></span>](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
-   [<span data-ttu-id="2b704-143">**LINE_CREATEDIALOGINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="2b704-143">**LINE_CREATEDIALOGINSTANCE**</span></span>](line-createdialoginstance.md)
-   [<span data-ttu-id="2b704-144">**LINE_SENDDIALOGINSTANCEDATA**</span><span class="sxs-lookup"><span data-stu-id="2b704-144">**LINE_SENDDIALOGINSTANCEDATA**</span></span>](line-senddialoginstancedata.md)

 

 
