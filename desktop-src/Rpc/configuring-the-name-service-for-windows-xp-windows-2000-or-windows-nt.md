---
title: Configurazione del servizio nome
description: A partire da Windows 2000, quando si installa il Windows SDK, il programma di installazione seleziona automaticamente Microsoft Locator come provider di servizi nome. È possibile modificare il nome del provider di servizi tramite il pannello di controllo.
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c1c895aecb3bdf74189461cd6aa9ee814b2d68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471230"
---
# <a name="configuring-the-name-service"></a><span data-ttu-id="d6747-104">Configurazione del servizio nome</span><span class="sxs-lookup"><span data-stu-id="d6747-104">Configuring the Name Service</span></span>

<span data-ttu-id="d6747-105">A partire da Windows 2000, quando si installa il Windows SDK, il programma di installazione seleziona automaticamente Microsoft Locator come provider di servizi nome.</span><span class="sxs-lookup"><span data-stu-id="d6747-105">Starting with Windows 2000, when you install the Windows SDK, the setup program automatically selects Microsoft Locator as the name service provider.</span></span> <span data-ttu-id="d6747-106">È possibile modificare il nome del provider di servizi tramite il pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="d6747-106">You can change the name service provider through Control Panel.</span></span>

<span data-ttu-id="d6747-107">Il computer host che esegue NSID funge da gateway per il servizio directory di celle DCE, passando le chiamate di funzione NSI tra computer che eseguono sistemi operativi Microsoft e computer DCE.</span><span class="sxs-lookup"><span data-stu-id="d6747-107">The host computer that runs the nsid acts as a gateway to the DCE Cell Directory Service, passing NSI function calls between computers that run Microsoft operating systems and DCE computers.</span></span> <span data-ttu-id="d6747-108">Un indirizzo di rete può essere composto da un massimo di 80 caratteri, ad esempio 11.1.9.169 è un indirizzo valido.</span><span class="sxs-lookup"><span data-stu-id="d6747-108">A network address can be up to 80 characters—for example, 11.1.9.169 is a valid address.</span></span>

> [!Note]  
> <span data-ttu-id="d6747-109">Per configurare i CD DCE come provider di servizi di nome, è necessario disporre del prodotto CDS digitale Digital Equipment Corporation.</span><span class="sxs-lookup"><span data-stu-id="d6747-109">You must have the Digital Equipment Corporation DCE CDS product to configure the DCE CDS as your name service provider.</span></span> <span data-ttu-id="d6747-110">Per informazioni sui CD DCE, vedere la documentazione fornita da Digital Equipment Corporation.</span><span class="sxs-lookup"><span data-stu-id="d6747-110">See the documentation provided by Digital Equipment Corporation for information about DCE CDS.</span></span>

 

<span data-ttu-id="d6747-111">**Per riconfigurare il provider di servizi dei nomi**</span><span class="sxs-lookup"><span data-stu-id="d6747-111">**To reconfigure the name service provider**</span></span>

1.  <span data-ttu-id="d6747-112">Nel pannello di controllo fare clic sull'icona **connessioni di rete** .</span><span class="sxs-lookup"><span data-stu-id="d6747-112">In Control Panel, click the **Network Connections** icon.</span></span> <span data-ttu-id="d6747-113">Verrà visualizzata la finestra **connessioni di rete** .</span><span class="sxs-lookup"><span data-stu-id="d6747-113">The **Network Connections** window appears.</span></span>
2.  <span data-ttu-id="d6747-114">Selezionare la connessione di rete da configurare, fare clic con il pulsante destro del mouse e scegliere **Proprietà** dal menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="d6747-114">Select the network connection to configure, right-click, and select **Properties** from the context menu.</span></span> <span data-ttu-id="d6747-115">Verrà visualizzata la finestra di dialogo **Proprietà connessione** .</span><span class="sxs-lookup"><span data-stu-id="d6747-115">The **Connection Properties** dialog appears.</span></span>
3.  <span data-ttu-id="d6747-116">Nella finestra di dialogo **Proprietà connessione** selezionare **client per reti Microsoft** e quindi fare clic sul pulsante **proprietà** .</span><span class="sxs-lookup"><span data-stu-id="d6747-116">In the **Connection Properties** dialog, select **Client for Microsoft Networks** and click the **Properties** button.</span></span> <span data-ttu-id="d6747-117">Verrà visualizzata la finestra **di dialogo client per proprietà rete Microsoft** .</span><span class="sxs-lookup"><span data-stu-id="d6747-117">The **Client for Microsoft Network Properties** dialog appears.</span></span>
4.  <span data-ttu-id="d6747-118">Nella finestra di dialogo **client for Microsoft Network Properties** aprire l'elenco a discesa **Nome provider di servizi** e selezionare un provider di nomi nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="d6747-118">In the **Client for Microsoft Network Properties** dialog, open the **Name service provider** drop-down and select a name provider from the list.</span></span>
    1.  <span data-ttu-id="d6747-119">Quando si seleziona Microsoft Locator, fare clic su OK.</span><span class="sxs-lookup"><span data-stu-id="d6747-119">When you select Microsoft Locator, click OK.</span></span> <span data-ttu-id="d6747-120">Il processo di configurazione viene quindi completato.</span><span class="sxs-lookup"><span data-stu-id="d6747-120">The configuration process is then complete.</span></span>
    2.  <span data-ttu-id="d6747-121">Quando si seleziona il servizio directory celle DCE, nella casella **indirizzo di rete** Digitare il nome del computer host che esegue il daemon NSI (NSID), quindi fare clic su OK.</span><span class="sxs-lookup"><span data-stu-id="d6747-121">When you select the DCE Cell Directory Service, in the **Network Address** box, type the name of the host computer that runs the NSI daemon (nsid), and then click OK.</span></span>

<span data-ttu-id="d6747-122">**Per riconfigurare il provider di servizi dei nomi per Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="d6747-122">**To reconfigure the name service provider for Windows 2000**</span></span>

1.  <span data-ttu-id="d6747-123">Nel pannello di controllo fare clic sull'icona della **rete** .</span><span class="sxs-lookup"><span data-stu-id="d6747-123">In Control Panel, click the **Network** icon.</span></span>

    <span data-ttu-id="d6747-124">Verrà visualizzata la finestra di dialogo **rete** .</span><span class="sxs-lookup"><span data-stu-id="d6747-124">The **Network** dialog box appears.</span></span>

2.  <span data-ttu-id="d6747-125">Nella finestra di dialogo **rete** fare clic su **Configura**.</span><span class="sxs-lookup"><span data-stu-id="d6747-125">In the **Network** dialog box, click **Configure**.</span></span>
3.  <span data-ttu-id="d6747-126">Nell'elenco **NetworkSoftware** selezionare **configurazione RPC**.</span><span class="sxs-lookup"><span data-stu-id="d6747-126">In the **NetworkSoftware** list, select **RPC Configuration**.</span></span>

    <span data-ttu-id="d6747-127">Verrà visualizzata la finestra di dialogo **Configurazione provider di servizi nome RPC** .</span><span class="sxs-lookup"><span data-stu-id="d6747-127">The **RPC Name Service Provider Configuration** dialog box appears.</span></span>

4.  <span data-ttu-id="d6747-128">Nella finestra di dialogo **Configurazione provider di servizi nome RPC** selezionare un provider di servizi di nome dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="d6747-128">In the **RPC Name Service Provider Configuration** dialog box, select a name service provider from the list.</span></span>
    1.  <span data-ttu-id="d6747-129">Quando si seleziona Microsoft Locator, fare clic su OK.</span><span class="sxs-lookup"><span data-stu-id="d6747-129">When you select Microsoft Locator, click OK.</span></span> <span data-ttu-id="d6747-130">Il processo di configurazione viene quindi completato.</span><span class="sxs-lookup"><span data-stu-id="d6747-130">The configuration process is then complete.</span></span>
    2.  <span data-ttu-id="d6747-131">Quando si seleziona il servizio directory celle DCE, nella casella **indirizzo di rete** Digitare il nome del computer host che esegue il daemon NSI (NSID), quindi fare clic su OK.</span><span class="sxs-lookup"><span data-stu-id="d6747-131">When you select the DCE Cell Directory Service, in the **Network Address** box, type the name of the host computer that runs the NSI daemon (nsid), and then click OK.</span></span>

 

 




