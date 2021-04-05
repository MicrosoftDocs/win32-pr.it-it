---
title: Requisiti di IIS per i caricamenti BITS
description: Per i caricamenti, BITS richiede IIS 6,0 in Windows Server 2003 e IIS 7,0 su Windows Server 2008; BITS non supporta IIS 5,1 in Windows XP.
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc1eb9bae86e7bb2635b3a250e8a9efe1bc630
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708119"
---
# <a name="iis-requirements-for-bits-uploads"></a><span data-ttu-id="2e69e-103">Requisiti di IIS per i caricamenti BITS</span><span class="sxs-lookup"><span data-stu-id="2e69e-103">IIS Requirements for BITS Uploads</span></span>

<span data-ttu-id="2e69e-104">Per i caricamenti, BITS richiede IIS 6,0 in Windows Server 2003 e IIS 7,0 su Windows Server 2008; BITS non supporta IIS 5,1 in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2e69e-104">For uploads, BITS requires IIS 6.0 on Windows Server 2003, and IIS 7.0 on Windows Server 2008; BITS does not support IIS 5.1 on Windows XP.</span></span> <span data-ttu-id="2e69e-105">È necessario abilitare la directory virtuale IIS per i caricamenti e configurare le estensioni IIS BITS.</span><span class="sxs-lookup"><span data-stu-id="2e69e-105">The IIS virtual directory must be enabled for uploads and have the BITS IIS extensions configured.</span></span>

<span data-ttu-id="2e69e-106">**Installazioni di base di Windows Server:** Le estensioni IIS BITS non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="2e69e-106">**Core installations of Windows Server:** BITS IIS extensions are not supported.</span></span>

<span data-ttu-id="2e69e-107">In Windows Server 2008, utilizzare il **Server Manager** per installare la funzionalità estensioni server BITS.</span><span class="sxs-lookup"><span data-stu-id="2e69e-107">On Windows Server 2008, use the **Server Manager** to install the BITS Server Extensions feature.</span></span> <span data-ttu-id="2e69e-108">Dal **Server Manager** fare clic su **funzionalità** nel riquadro sinistro.</span><span class="sxs-lookup"><span data-stu-id="2e69e-108">From **Server Manager**, click **Features** in the left pane.</span></span> <span data-ttu-id="2e69e-109">Nell' **Aggiunta guidata funzionalità**, controllare le estensioni del server BITS.</span><span class="sxs-lookup"><span data-stu-id="2e69e-109">In the **Add Features Wizard**, check BITS Server Extensions.</span></span> <span data-ttu-id="2e69e-110">Si noti che è necessario installare i ruoli di compatibilità di gestione con IIS 6.</span><span class="sxs-lookup"><span data-stu-id="2e69e-110">Note that the IIS 6 Management Compatibility roles must be installed.</span></span>

<span data-ttu-id="2e69e-111">In Windows Server 2003, utilizzare la **procedura guidata componenti di Windows** per installare l'estensione del server BITS.</span><span class="sxs-lookup"><span data-stu-id="2e69e-111">On Windows Server 2003, use the **Windows Components Wizard** to install the BITS server extension.</span></span> <span data-ttu-id="2e69e-112">Nel **Pannello di controllo** selezionare **Installazione applicazioni**.</span><span class="sxs-lookup"><span data-stu-id="2e69e-112">From **Control Panel**, select **Add or Remove Programs**.</span></span> <span data-ttu-id="2e69e-113">Selezionare quindi **Aggiungi/Rimuovi componenti di Windows** per visualizzare la **procedura guidata componenti di Windows**.</span><span class="sxs-lookup"><span data-stu-id="2e69e-113">Then, select **Add/Remove Windows Components** to display the **Windows Components Wizard**.</span></span> <span data-ttu-id="2e69e-114">L'estensione del server BITS è un sottocomponente di Internet Information Services (IIS), che è un componente secondario del server applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="2e69e-114">The BITS server extension is a subcomponent of Internet Information Services (IIS) which is a sub-component of Web Application Server.</span></span>

> [!Note]  
> <span data-ttu-id="2e69e-115">Se il servizio IISAdmin viene riavviato, il processo di lavoro IIS deve essere riciclato prima che il servizio BITS possa riprendere i caricamenti.</span><span class="sxs-lookup"><span data-stu-id="2e69e-115">If the IISAdmin service is restarted, the IIS worker process must be recycled before the BITS service can resume uploads.</span></span> <span data-ttu-id="2e69e-116">È possibile riciclare manualmente il processo di lavoro IIS utilizzando l'utilità della riga di comando **IISReset.exe** .</span><span class="sxs-lookup"><span data-stu-id="2e69e-116">The IIS worker process can be manually recycled by using the **IISReset.exe** command line utility.</span></span>

 

<span data-ttu-id="2e69e-117">Per informazioni sulla configurazione di IIS per il caricamento, vedere [configurazione del server per il caricamento](setting-up-the-server-for-uploads.md).</span><span class="sxs-lookup"><span data-stu-id="2e69e-117">For information on configuring IIS for uploads, see [Setting Up the Server for Uploads](setting-up-the-server-for-uploads.md).</span></span>

<span data-ttu-id="2e69e-118">Per informazioni dettagliate sulle proprietà aggiunte da BITS a IIS, vedere [BITS Server Settings for upload Jobs](bits-server-settings-for-upload-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="2e69e-118">For details on the properties that BITS adds to IIS, see [BITS Server Settings for Upload Jobs](bits-server-settings-for-upload-jobs.md).</span></span>

 

 




