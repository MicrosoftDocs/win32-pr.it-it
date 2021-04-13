---
description: Attivazione di code di componenti
ms.assetid: cfbf7c73-2521-40cf-8c6e-436f64c07e31
title: Attivazione di code di componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13dadad287facd5555b4e1ed84fee9f764b1c32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401425"
---
# <a name="activating-component-queues"></a><span data-ttu-id="bc64b-103">Attivazione di code di componenti</span><span class="sxs-lookup"><span data-stu-id="bc64b-103">Activating Component Queues</span></span>

<span data-ttu-id="bc64b-104">La creazione di chiamate al metodo su un componente in coda non comporta l'esecuzione diretta del metodo.</span><span class="sxs-lookup"><span data-stu-id="bc64b-104">Making method calls on a queued component does not directly execute the method.</span></span> <span data-ttu-id="bc64b-105">Il metodo di [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) esegue il marshalling e archivia le chiamate al metodo e i parametri in una coda in cui vengono recuperati ed eseguiti successivamente dal componente in coda.</span><span class="sxs-lookup"><span data-stu-id="bc64b-105">Rather, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) marshals and stores method calls and parameters in a queue where they are later retrieved and executed by the queued component.</span></span> <span data-ttu-id="bc64b-106">Diversamente dall'attivazione di un oggetto DCOM remoto, non viene creata un'istanza del componente in coda quando viene chiamato un metodo.</span><span class="sxs-lookup"><span data-stu-id="bc64b-106">Unlike activating a remote DCOM object, the queued component is not instantiated when a method is called.</span></span> <span data-ttu-id="bc64b-107">Si tratta dell'idea di base per l'uso dei componenti in coda: non è necessario creare istanze dei componenti in coda contemporaneamente all'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="bc64b-107">This is the basic idea behind using queued components—queued components need not be instantiated at the same time as the calling application.</span></span>

> [!Note]  
> <span data-ttu-id="bc64b-108">Le descrizioni per l'attivazione di un'applicazione in coda presuppongono che l'applicazione sia contrassegnata come accodata e che la casella di controllo listener sia abilitata.</span><span class="sxs-lookup"><span data-stu-id="bc64b-108">The descriptions for activating a queued application assume that the application is marked as queued and that the listener check box is enabled.</span></span>

 

<span data-ttu-id="bc64b-109">È possibile utilizzare lo scripting per avviare e arrestare un'applicazione in coda.</span><span class="sxs-lookup"><span data-stu-id="bc64b-109">You can use scripting to start and stop a queued application.</span></span> <span data-ttu-id="bc64b-110">È possibile inserire lo script sotto il controllo dell'utilità di pianificazione per eseguirlo come richiesto.</span><span class="sxs-lookup"><span data-stu-id="bc64b-110">You can put the script under the control of the task scheduler to run it as required.</span></span> <span data-ttu-id="bc64b-111">Ad esempio, lo script può essere eseguito al riavvio del sistema se le applicazioni sono permanentemente disponibili.</span><span class="sxs-lookup"><span data-stu-id="bc64b-111">For example, the script can be run on system reboot if the applications are to be permanently available.</span></span> <span data-ttu-id="bc64b-112">Se l'applicazione deve elaborare le transazioni in modalità batch, è possibile eseguire lo script in un determinato momento ogni giorno insieme a uno script di arresto per assicurarsi che l'elaborazione batch si arresti in un momento specifico.</span><span class="sxs-lookup"><span data-stu-id="bc64b-112">If the application is to process transactions in batch mode, the script can be run at a certain time each day in conjunction with a shutdown script to be sure the batch processing stops at a specific time.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="bc64b-113">Strumento di amministrazione Servizi componenti</span><span class="sxs-lookup"><span data-stu-id="bc64b-113">Component Services Administrative Tool</span></span>

<span data-ttu-id="bc64b-114">Per avviare un'applicazione in coda, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="bc64b-114">To start a queued application, use the following steps:</span></span>

1.  <span data-ttu-id="bc64b-115">Nell'albero della console dello strumento di amministrazione Servizi componenti, in **Servizi componenti**, aprire la cartella **applicazioni com+** associata al computer che si desidera gestire.</span><span class="sxs-lookup"><span data-stu-id="bc64b-115">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="bc64b-116">Fare clic con il pulsante destro del mouse sull'applicazione di cui si desidera attivare la coda.</span><span class="sxs-lookup"><span data-stu-id="bc64b-116">Right-click the application whose queue you want to activate.</span></span>

3.  <span data-ttu-id="bc64b-117">Fare clic su **Start** (Avvia).</span><span class="sxs-lookup"><span data-stu-id="bc64b-117">Click **Start**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="bc64b-118">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="bc64b-118">Visual Basic</span></span>

<span data-ttu-id="bc64b-119">Vedere l'esempio COMAdminCatalog. StartApplication.</span><span class="sxs-lookup"><span data-stu-id="bc64b-119">See the COMAdminCatalog.StartApplication example.</span></span>

## <a name="cc"></a><span data-ttu-id="bc64b-120">C/C++</span><span class="sxs-lookup"><span data-stu-id="bc64b-120">C/C++</span></span>

<span data-ttu-id="bc64b-121">Vedere l'esempio [**ICOMAdminCatalog:: StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) .</span><span class="sxs-lookup"><span data-stu-id="bc64b-121">See the [**ICOMAdminCatalog::StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc64b-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc64b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc64b-123">Utilizzo del moniker della coda</span><span class="sxs-lookup"><span data-stu-id="bc64b-123">Using the Queue Moniker</span></span>](using-the-queue-moniker.md)
</dt> </dl>

 

 



