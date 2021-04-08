---
title: Avvio e arresto di Microsoft Locator
description: Quando necessario, le librerie di runtime RPC avviano automaticamente Microsoft Locator. È possibile arrestare e avviare manualmente il localizzatore se, ad esempio, è necessario cancellare il database durante il debug di un'applicazione distribuita.
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433ffdb11e86b06ee53d9b01f7f7755758538f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104043999"
---
# <a name="starting-and-stopping-microsoft-locator"></a><span data-ttu-id="b241a-104">Avvio e arresto di Microsoft Locator</span><span class="sxs-lookup"><span data-stu-id="b241a-104">Starting and Stopping Microsoft Locator</span></span>

<span data-ttu-id="b241a-105">Quando necessario, le librerie di runtime RPC avviano automaticamente Microsoft Locator.</span><span class="sxs-lookup"><span data-stu-id="b241a-105">The RPC run-time libraries automatically start Microsoft Locator when necessary.</span></span> <span data-ttu-id="b241a-106">È possibile arrestare e avviare manualmente il localizzatore se, ad esempio, è necessario cancellare il database durante il debug di un'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="b241a-106">You can manually stop and start the Locator if, for example, you need to clear the database while debugging a distributed application.</span></span>

<span data-ttu-id="b241a-107">**Per arrestare e avviare Microsoft Locator**</span><span class="sxs-lookup"><span data-stu-id="b241a-107">**To stop and start Microsoft Locator**</span></span>

1.  <span data-ttu-id="b241a-108">Nel pannello di controllo fare clic sull'icona servizi.</span><span class="sxs-lookup"><span data-stu-id="b241a-108">From Control Panel, click the Services icon.</span></span>

    <span data-ttu-id="b241a-109">Verrà visualizzata la finestra di dialogo **Servizi** .</span><span class="sxs-lookup"><span data-stu-id="b241a-109">The **Services** dialog box appears.</span></span>

2.  <span data-ttu-id="b241a-110">Nella finestra di dialogo **servizio** selezionare **Microsoft Locator** , quindi fare clic su **Avvia** o **Arresta**.</span><span class="sxs-lookup"><span data-stu-id="b241a-110">In the **Service** dialog box, select **Microsoft Locator** and then click **Start** or **Stop**.</span></span>

<span data-ttu-id="b241a-111">È anche possibile avviare e arrestare Microsoft Locator dalla riga di comando digitando:</span><span class="sxs-lookup"><span data-stu-id="b241a-111">You can also start and stop Microsoft Locator from the command line by typing:</span></span>

<span data-ttu-id="b241a-112">**NET \[ Start/Stop \] RpcLocator**</span><span class="sxs-lookup"><span data-stu-id="b241a-112">**net \[start/stop\] rpclocator**</span></span>

<span data-ttu-id="b241a-113">Solo un amministratore può avviare Microsoft Locator dopo che è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="b241a-113">Only an administrator can start Microsoft Locator once it is stopped.</span></span> <span data-ttu-id="b241a-114">Se arrestata, verrà riavviata in base alle esigenze delle librerie di runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="b241a-114">If stopped, it will be restarted as necessary by the RPC run-time libraries.</span></span>

 

 




