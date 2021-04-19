---
description: Il provider WMI per Hyper-V consente agli sviluppatori e ai creatori di script di creare rapidamente strumenti, utilità e miglioramenti personalizzati per la piattaforma di virtualizzazione. Le interfacce WMI possono gestire tutti gli aspetti dei servizi Hyper-V.
ms.assetid: 773BB141-7B9C-4015-81A0-BD17B8233CCD
title: Informazioni sul provider WMI Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70c30b329f7e8a3fd3ae65b49f8467a8f712707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312350"
---
# <a name="about-the-hyper-v-wmi-provider"></a><span data-ttu-id="ff490-104">Informazioni sul provider WMI Hyper-V</span><span class="sxs-lookup"><span data-stu-id="ff490-104">About the Hyper-V WMI provider</span></span>

<span data-ttu-id="ff490-105">Il provider WMI per Hyper-V consente agli sviluppatori e ai creatori di script di creare rapidamente strumenti, utilità e miglioramenti personalizzati per la piattaforma di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ff490-105">The WMI provider for Hyper-V enable developers, and scripters, to quickly build custom tools, utilities, and enhancements for the virtualization platform.</span></span> <span data-ttu-id="ff490-106">Le interfacce WMI possono gestire tutti gli aspetti dei servizi Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="ff490-106">The WMI interfaces can manage all aspects of the Hyper-V services.</span></span>

## <a name="about-microsoft-windows-server-2008-r2-hyper-v"></a><span data-ttu-id="ff490-107">Informazioni su Microsoft Windows Server 2008 R2 Hyper-V</span><span class="sxs-lookup"><span data-stu-id="ff490-107">About Microsoft Windows Server 2008 R2 Hyper-V</span></span>

<span data-ttu-id="ff490-108">Microsoft Windows Server 2008 R2 Hyper-V consente agli amministratori di sistema di consolidare server hardware distinti in un singolo server che esegue Microsoft Windows Server 2008 R2 come sistema operativo host.</span><span class="sxs-lookup"><span data-stu-id="ff490-108">Microsoft Windows Server 2008 R2 Hyper-V allows system administrators to consolidate separate hardware servers on to a single server running Microsoft Windows Server 2008 R2 as the host operating system.</span></span>

<span data-ttu-id="ff490-109">Ognuna delle macchine virtuali ospitate viene eseguita in un ambiente virtuale separato e isolato.</span><span class="sxs-lookup"><span data-stu-id="ff490-109">Each of the hosted virtual machines runs in its own separate and isolated virtual environment.</span></span> <span data-ttu-id="ff490-110">Questo consente all'amministratore di gestire, fornire e gestire con facilità un numero elevato di macchine virtuali, riducendo al tempo stesso la necessità di eseguire più soluzioni hardware per l'utilizzo di diversi prodotti e sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="ff490-110">This allows the administrator to easily manage, provide for, and maintain large numbers of virtual machines while reducing the need to run multiple hardware solutions to use various products and operating systems.</span></span>

<span data-ttu-id="ff490-111">Un altro vantaggio dell'ambiente di macchina virtuale è il test e il supporto.</span><span class="sxs-lookup"><span data-stu-id="ff490-111">Another advantage of the virtual machine environment is in test and support.</span></span> <span data-ttu-id="ff490-112">È possibile distribuire e testare le nuove configurazioni del server e del sistema in parallelo con il sistema esistente senza tempi di inattività costosi durante la fase di implementazione.</span><span class="sxs-lookup"><span data-stu-id="ff490-112">New server and system configurations can be deployed and tested in parallel with the existing system without requiring costly downtime during the rollout phase.</span></span> <span data-ttu-id="ff490-113">Ogni macchina virtuale può essere impostata in modo da usare configurazioni variabili mentre è in esecuzione su una piattaforma standard per produrre risultati di test migliori.</span><span class="sxs-lookup"><span data-stu-id="ff490-113">Each virtual machine can be setup to use varying configurations while running on a standard platform to produce better test results.</span></span> <span data-ttu-id="ff490-114">Con il supporto per i sistemi operativi precedenti, è possibile supportare e testare l'hardware, i sistemi e le applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="ff490-114">With support for earlier operating systems, one can support and test legacy hardware, systems and applications.</span></span> <span data-ttu-id="ff490-115">Il supporto di snapshot consente di creare uno snapshot dello stato di una macchina virtuale, in modo da poter tornare a un evento precedente, se necessario.</span><span class="sxs-lookup"><span data-stu-id="ff490-115">Snapshot support allows you to take a snapshot of a virtual machine's state so you can return to a prior event if needed.</span></span>

<span data-ttu-id="ff490-116">Hyper-V espone un'interfaccia avanzata che consente all'utente di monitorare e controllare l'ambiente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ff490-116">Hyper-V exposes a rich interface which permits the user to monitor and control the virtual machine environment.</span></span> <span data-ttu-id="ff490-117">La maggior parte di Hyper-V può essere controllata tramite il provider WMI, che consente una personalizzazione semplice, ma potente delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="ff490-117">Most of Hyper-V can be controlled by using the WMI provider, which allows easy, yet powerful customization of the virtual machines.</span></span> <span data-ttu-id="ff490-118">Per ulteriori informazioni su ciò che è possibile controllare con il provider WMI, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff490-118">For more information about what can be controlled with the WMI provider, see the following topics:</span></span>

-   [<span data-ttu-id="ff490-119">Servizio di gestione del sistema virtuale</span><span class="sxs-lookup"><span data-stu-id="ff490-119">Virtual system management service</span></span>](virtual-system-management-service.md)
-   [<span data-ttu-id="ff490-120">Servizio di rete</span><span class="sxs-lookup"><span data-stu-id="ff490-120">Networking service</span></span>](networking-service.md)
-   [<span data-ttu-id="ff490-121">Servizio Gestione risorse</span><span class="sxs-lookup"><span data-stu-id="ff490-121">Resource management service</span></span>](resource-management-service.md)
-   [<span data-ttu-id="ff490-122">Novità del provider WMI Hyper-V</span><span class="sxs-lookup"><span data-stu-id="ff490-122">What's new in Hyper-V WMI provider</span></span>](what-s-new-in-hyper-v.md)

 

 



