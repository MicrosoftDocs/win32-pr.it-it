---
title: BITS
description: BITS
ms.assetid: 67159ad9-e11b-4fea-bff2-468d5a7447be
keywords:
- Windows Media Player Online Stores, Servizio trasferimento intelligente in background (BITS)
- archivi online, Servizio trasferimento intelligente in background (BITS)
- digitare 2 archivi online, Servizio trasferimento intelligente in background (BITS)
- Servizio trasferimento intelligente in background (BITS)
- BITS (Servizio trasferimento intelligente in background)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527edf56e7505c64657d167e0210190e00d697d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337926"
---
# <a name="bits"></a><span data-ttu-id="8de5d-108">BITS</span><span class="sxs-lookup"><span data-stu-id="8de5d-108">BITS</span></span>

<span data-ttu-id="8de5d-109">Il [servizio trasferimento intelligente in background](/windows/desktop/Bits/background-intelligent-transfer-service-portal) è una funzionalità del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="8de5d-109">The [Background Intelligent Transfer Service](/windows/desktop/Bits/background-intelligent-transfer-service-portal) is a feature of the Windows operating system.</span></span> <span data-ttu-id="8de5d-110">BITS trasferisce i file (download o caricamenti) tra un client e un server e fornisce informazioni sullo stato di avanzamento correlate ai trasferimenti.</span><span class="sxs-lookup"><span data-stu-id="8de5d-110">BITS transfers files (downloads or uploads) between a client and server, and provides progress information related to the transfers.</span></span> <span data-ttu-id="8de5d-111">Se si desidera trasferire file usando il codice C++, BITS è la tecnologia corretta da usare.</span><span class="sxs-lookup"><span data-stu-id="8de5d-111">If you want to transfer files using C++ code, BITS is the correct technology to use.</span></span> <span data-ttu-id="8de5d-112">Se si desidera trasferire i file utilizzando il codice JScript nella pagina Web del negozio online, utilizzare invece gestione download.</span><span class="sxs-lookup"><span data-stu-id="8de5d-112">If you want to transfer files using JScript code in your online store webpage, use the Download Manager instead.</span></span>

<span data-ttu-id="8de5d-113">Poiché Windows Media Player Download Manager USA BITS, è possibile eseguire le operazioni necessarie per configurare i processi di copia BITS in modo che Windows Media Player gestisca i processi.</span><span class="sxs-lookup"><span data-stu-id="8de5d-113">Because the Windows Media Player Download Manager uses BITS, you can take steps to configure your BITS copy jobs in such a way that Windows Media Player manages the jobs for you.</span></span> <span data-ttu-id="8de5d-114">A tale scopo, è necessario seguire la convenzione descritta nella sezione relativa alla [convenzione dei processi BITS di Windows Media Player](windows-media-player-bits-job-convention.md) durante l'aggiunta dei processi alla coda di trasferimento BITS.</span><span class="sxs-lookup"><span data-stu-id="8de5d-114">To do this, you must follow the convention described in the [Windows Media Player BITS Job Convention](windows-media-player-bits-job-convention.md) section when adding your jobs to the BITS transfer queue.</span></span> <span data-ttu-id="8de5d-115">Questa sezione descrive anche un meccanismo per il recupero di informazioni sui processi BITS dalla pagina Web dei negozi online.</span><span class="sxs-lookup"><span data-stu-id="8de5d-115">This section also describes a mechanism for retrieving information about your BITS jobs from your online stores webpage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8de5d-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8de5d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8de5d-117">**Uso di Download Manager**</span><span class="sxs-lookup"><span data-stu-id="8de5d-117">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> <dt>

[<span data-ttu-id="8de5d-118">**Informazioni sui negozi online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="8de5d-118">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> </dl>

 

 