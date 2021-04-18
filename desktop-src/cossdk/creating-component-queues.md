---
description: Un'applicazione che contiene almeno un componente accodabile può essere contrassegnata come accodata utilizzando lo strumento di amministrazione Servizi componenti.
ms.assetid: 7d9fec63-0bb7-45f3-9d40-736a60d69185
title: Creazione di code di componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc6f6731144a1744a7648d2d3d2bd5c3c4b217b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304830"
---
# <a name="creating-component-queues"></a><span data-ttu-id="11f54-103">Creazione di code di componenti</span><span class="sxs-lookup"><span data-stu-id="11f54-103">Creating Component Queues</span></span>

<span data-ttu-id="11f54-104">Un'applicazione che contiene almeno un componente accodabile può essere contrassegnata come accodata utilizzando lo strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="11f54-104">An application that contains at least one queuable component can be marked as queued using the component services administrative tool.</span></span>

<span data-ttu-id="11f54-105">Quando un'applicazione è contrassegnata come accodata, COM+ crea automaticamente una coda di Accodamento messaggi.</span><span class="sxs-lookup"><span data-stu-id="11f54-105">When an application is marked as queued, COM+ automatically creates a message queuing queue for it.</span></span> <span data-ttu-id="11f54-106">Il nome della coda è il nome dell'applicazione. Se il nome della coda corrisponde al nome di una coda esistente, COM+ utilizzerà la coda esistente.</span><span class="sxs-lookup"><span data-stu-id="11f54-106">The queue name is the name of the application; if the queue name matches the name of an existing queue, COM+ will use the existing queue.</span></span>

> [!Note]  
> <span data-ttu-id="11f54-107">Il parametro del *percorso* di Accodamento messaggi è una combinazione del nome del server remoto (RSN) e del nome dell'applicazione com+.</span><span class="sxs-lookup"><span data-stu-id="11f54-107">The Message Queuing *PathName* parameter is a combination of the Remote Server Name (RSN) and the COM+ application name.</span></span> <span data-ttu-id="11f54-108">RSN fa riferimento alla destinazione di un'attivazione remota.</span><span class="sxs-lookup"><span data-stu-id="11f54-108">The RSN refers to the target of a remote activation.</span></span> <span data-ttu-id="11f54-109">Si specifica un RSN durante l'installazione di un'applicazione client esportabile in un computer client.</span><span class="sxs-lookup"><span data-stu-id="11f54-109">You specify an RSN during the installation of a client exportable application on a client computer.</span></span> <span data-ttu-id="11f54-110">La procedura di installazione usa RSN per indirizzare l'attivazione a un computer client specifico.</span><span class="sxs-lookup"><span data-stu-id="11f54-110">The installation procedure uses the RSN to direct activation to a specified client computer.</span></span> <span data-ttu-id="11f54-111">Per ulteriori informazioni sui nomi delle code, fare riferimento alla tabella di parametri nella sezione "parametri del moniker della coda" in [utilizzo del moniker della coda](using-the-queue-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="11f54-111">For more information about queue names, refer to the table of parameters in the "Queue Moniker Parameters" section in [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="11f54-112">Strumento di amministrazione Servizi componenti</span><span class="sxs-lookup"><span data-stu-id="11f54-112">Component Services Administrative Tool</span></span>

<span data-ttu-id="11f54-113">Per specificare un'applicazione COM+ come accodata, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="11f54-113">To specify a COM+ application as queued, use the following steps:</span></span>

1.  <span data-ttu-id="11f54-114">Nell'albero della console dello strumento di amministrazione Servizi componenti, in **Servizi componenti**, aprire la cartella **applicazioni com+** associata al computer che si desidera gestire.</span><span class="sxs-lookup"><span data-stu-id="11f54-114">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="11f54-115">Fare clic con il pulsante destro del mouse sull'applicazione per la quale si desidera creare una coda e quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="11f54-115">Right-click the application for which you wish to create a queue, and then click **Properties**.</span></span>

3.  <span data-ttu-id="11f54-116">Selezionare la scheda **Accodamento** nella finestra di dialogo Proprietà.</span><span class="sxs-lookup"><span data-stu-id="11f54-116">Select the **Queuing** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="11f54-117">Attivare la casella **di controllo in coda: questa applicazione può essere raggiunta dalle code MSMQ**.</span><span class="sxs-lookup"><span data-stu-id="11f54-117">Activate the check box labeled **Queued – This application can be reached by MSMQ queues**.</span></span>

    > [!Note]  
    > <span data-ttu-id="11f54-118">Se la casella di controllo in **coda** è disabilitata, l'applicazione non contiene componenti accodabili.</span><span class="sxs-lookup"><span data-stu-id="11f54-118">If the **Queued** check box is grayed out, the application contains no queuable components.</span></span>

     

5.  <span data-ttu-id="11f54-119">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="11f54-119">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="11f54-120">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="11f54-120">Visual Basic</span></span>

<span data-ttu-id="11f54-121">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="11f54-121">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="11f54-122">C/C++</span><span class="sxs-lookup"><span data-stu-id="11f54-122">C/C++</span></span>

<span data-ttu-id="11f54-123">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="11f54-123">Does not apply.</span></span>

## <a name="remarks"></a><span data-ttu-id="11f54-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="11f54-124">Remarks</span></span>

<span data-ttu-id="11f54-125">Le code create dalla libreria di amministrazione COM+ o dallo strumento di amministrazione Servizi componenti sono contrassegnate con l'attributo transazionale di Accodamento messaggi.</span><span class="sxs-lookup"><span data-stu-id="11f54-125">Queues created by the COM+ Administration Library or the Component Services administrative tool are marked with the Message Queuing transactional attribute.</span></span>

<span data-ttu-id="11f54-126">Dopo l'installazione di un'applicazione in coda nel server, è possibile renderla disponibile ai client esportando l'applicazione e quindi importando l'applicazione in ogni client.</span><span class="sxs-lookup"><span data-stu-id="11f54-126">After a queued application is installed at the server, it can be made available to clients by exporting the application and then importing the application at each client.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11f54-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11f54-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11f54-128">Creazione di componenti accodabili</span><span class="sxs-lookup"><span data-stu-id="11f54-128">Creating Queuable Components</span></span>](creating-queuable-components.md)
</dt> <dt>

[<span data-ttu-id="11f54-129">Architettura dei componenti in coda</span><span class="sxs-lookup"><span data-stu-id="11f54-129">Queued Components Architecture</span></span>](queued-components-architecture.md)
</dt> </dl>

 

 



