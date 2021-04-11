---
description: È possibile monitorare le statistiche degli oggetti durante l'esecuzione di un'applicazione. In questo modo, è possibile ottimizzare le caratteristiche del pool di oggetti per ottenere il bilanciamento delle prestazioni e delle risorse che si desidera ottenere.
ms.assetid: 57987cc1-8bb5-4bbd-a425-fda2e5a8b597
title: Monitoraggio delle statistiche degli oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f438bc7081546083f1930fe31f16a2198b09b48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342201"
---
# <a name="monitoring-object-statistics"></a><span data-ttu-id="ca7ad-104">Monitoraggio delle statistiche degli oggetti</span><span class="sxs-lookup"><span data-stu-id="ca7ad-104">Monitoring Object Statistics</span></span>

<span data-ttu-id="ca7ad-105">È possibile monitorare le statistiche degli oggetti durante l'esecuzione di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ca7ad-105">You can monitor object statistics as an application runs.</span></span> <span data-ttu-id="ca7ad-106">In questo modo, è possibile ottimizzare le caratteristiche del pool di oggetti per ottenere il bilanciamento delle prestazioni e delle risorse che si desidera ottenere.</span><span class="sxs-lookup"><span data-stu-id="ca7ad-106">By doing so, you can fine-tune the object pool characteristics to achieve the balance in performance and resources that you would like to have.</span></span>

<span data-ttu-id="ca7ad-107">È possibile monitorare lo stato di tutti gli oggetti configurati per supportare le statistiche degli oggetti e la segnalazione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="ca7ad-107">You can monitor status for any objects that are configured to support object statistics and event reporting.</span></span> <span data-ttu-id="ca7ad-108">L'abilitazione delle statistiche degli oggetti presenta un lieve sovraccarico delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="ca7ad-108">Enabling object statistics has a very slight performance overhead.</span></span>

<span data-ttu-id="ca7ad-109">**Per abilitare le statistiche degli oggetti**</span><span class="sxs-lookup"><span data-stu-id="ca7ad-109">**To enable object statistics**</span></span>

1.  <span data-ttu-id="ca7ad-110">Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul componente che si desidera configurare, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="ca7ad-110">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="ca7ad-111">Nella finestra di dialogo Proprietà componente fare clic sulla scheda **attivazione** .</span><span class="sxs-lookup"><span data-stu-id="ca7ad-111">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="ca7ad-112">Per abilitare le statistiche degli oggetti per il componente, in **contesto di attivazione** selezionare la casella di controllo **componente supporta eventi e statistiche** .</span><span class="sxs-lookup"><span data-stu-id="ca7ad-112">To enable object statistics for the component, under **Activation Context**, select the **Component supports events and statistics** check box.</span></span>

<span data-ttu-id="ca7ad-113">**Per monitorare lo stato di un oggetto**</span><span class="sxs-lookup"><span data-stu-id="ca7ad-113">**To monitor object status**</span></span>

1.  <span data-ttu-id="ca7ad-114">Nell'albero della console dello strumento di amministrazione Servizi componenti aprire la cartella per l'applicazione che include i componenti che si desidera monitorare.</span><span class="sxs-lookup"><span data-stu-id="ca7ad-114">In the console tree of the Component Services administrative tool, open the folder for the application that includes the components you want to monitor.</span></span>

2.  <span data-ttu-id="ca7ad-115">Fare clic con il pulsante destro del mouse sulla cartella **componenti** , scegliere **Visualizza** e quindi fare clic su **visualizzazione stato**.</span><span class="sxs-lookup"><span data-stu-id="ca7ad-115">Right-click the **Components** folder, point to **View**, and then click **Status View**.</span></span> <span data-ttu-id="ca7ad-116">Il riquadro dei dettagli Visualizza ora la visualizzazione stato per tutti i componenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ca7ad-116">The details pane now displays the status view for all components in the application.</span></span> <span data-ttu-id="ca7ad-117">Nella tabella seguente vengono descritte le sei colonne della vista di stato.</span><span class="sxs-lookup"><span data-stu-id="ca7ad-117">The following table describes the six columns in the status view.</span></span>

    

    | <span data-ttu-id="ca7ad-118">Colonna</span><span class="sxs-lookup"><span data-stu-id="ca7ad-118">Column</span></span>                        | <span data-ttu-id="ca7ad-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca7ad-119">Description</span></span>                                                                                                                                                                                                                |
    |-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="ca7ad-120">**ProgID**</span><span class="sxs-lookup"><span data-stu-id="ca7ad-120">**ProgID**</span></span><br/>         | <span data-ttu-id="ca7ad-121">Identifica un componente specifico.</span><span class="sxs-lookup"><span data-stu-id="ca7ad-121">Identifies a specific component.</span></span><br/>                                                                                                                                                                                |
    | <span data-ttu-id="ca7ad-122">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="ca7ad-122">**Objects**</span></span><br/>        | <span data-ttu-id="ca7ad-123">Mostra il numero di oggetti attualmente conservati dai riferimenti client.</span><span class="sxs-lookup"><span data-stu-id="ca7ad-123">Shows the number of objects that are currently held by client references.</span></span><br/>                                                                                                                                       |
    | <span data-ttu-id="ca7ad-124">**Attivato**</span><span class="sxs-lookup"><span data-stu-id="ca7ad-124">**Activated**</span></span><br/>      | <span data-ttu-id="ca7ad-125">Mostra il numero di oggetti attualmente attivati.</span><span class="sxs-lookup"><span data-stu-id="ca7ad-125">Shows the number of objects that are currently activated.</span></span> <br/>                                                                                                                                                      |
    | <span data-ttu-id="ca7ad-126">**In pool**</span><span class="sxs-lookup"><span data-stu-id="ca7ad-126">**Pooled**</span></span><br/>         | <span data-ttu-id="ca7ad-127">Mostra il numero totale di oggetti creati dal pool, inclusi gli oggetti in uso e gli oggetti che sono stati disattivati.</span><span class="sxs-lookup"><span data-stu-id="ca7ad-127">Shows the total number of objects created by the pool, including objects that are in use and objects that are deactivated.</span></span><br/>                                                                                      |
    | <span data-ttu-id="ca7ad-128">**Nella chiamata**</span><span class="sxs-lookup"><span data-stu-id="ca7ad-128">**In Call**</span></span><br/>        | <span data-ttu-id="ca7ad-129">Identifica gli oggetti nella chiamata.</span><span class="sxs-lookup"><span data-stu-id="ca7ad-129">Identifies objects in call.</span></span><br/>                                                                                                                                                                                     |
    | <span data-ttu-id="ca7ad-130">**Tempo di chiamata (MS)**</span><span class="sxs-lookup"><span data-stu-id="ca7ad-130">**Call Time (ms)**</span></span><br/> | <span data-ttu-id="ca7ad-131">Mostra la durata media della chiamata (in millisecondi) di chiamate al metodo effettuate negli ultimi 20 secondi (fino a 20 chiamate).</span><span class="sxs-lookup"><span data-stu-id="ca7ad-131">Shows the average call duration (in milliseconds) of method calls made in the last 20 seconds (up to 20 calls).</span></span> <span data-ttu-id="ca7ad-132">Il tempo di chiamata viene misurato in corrispondenza dell'oggetto e non include il tempo usato per attraversare la rete.</span><span class="sxs-lookup"><span data-stu-id="ca7ad-132">Call time is measured at the object and does not include the time used to traverse the network.</span></span><br/> |

    

     

## <a name="related-topics"></a><span data-ttu-id="ca7ad-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca7ad-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca7ad-134">Configurazione di un componente da raggruppare</span><span class="sxs-lookup"><span data-stu-id="ca7ad-134">Configuring a Component to Be Pooled</span></span>](configuring-a-component-to-be-pooled.md)
</dt> </dl>

 

 




