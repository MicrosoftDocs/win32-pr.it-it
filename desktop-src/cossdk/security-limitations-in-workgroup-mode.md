---
description: Limitazioni di sicurezza in modalità gruppo di lavoro
ms.assetid: 05c0aba7-b94b-49d4-a0fc-1ff0a23550b3
title: Limitazioni di sicurezza in modalità gruppo di lavoro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eabe38b8d05c49382ae6dd8337b883a6f4a8079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304809"
---
# <a name="security-limitations-in-workgroup-mode"></a><span data-ttu-id="77f07-103">Limitazioni di sicurezza in modalità gruppo di lavoro</span><span class="sxs-lookup"><span data-stu-id="77f07-103">Security Limitations in Workgroup Mode</span></span>

<span data-ttu-id="77f07-104">La configurazione del gruppo di lavoro [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) non consente al servizio componenti in coda com+ di supportare la sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="77f07-104">The [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) workgroup configuration does not permit the COM+ queued components service to support application security.</span></span> <span data-ttu-id="77f07-105">Se è stato installato Accodamento messaggi con la configurazione del gruppo di lavoro, è necessario [disabilitare la sicurezza](specifying-the-authentication-protocol.md) in ogni applicazione in coda a cui si accede in questa configurazione selezionando non **autenticare i messaggi** nella scheda **Accodamento** per la finestra di dialogo **Proprietà** dell'applicazione com+ utilizzando lo strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="77f07-105">If you've installed Message Queuing with the workgroup configuration, you must [disable security](specifying-the-authentication-protocol.md) on each queued application accessed in this configuration by selecting **Do not authenticate messages** on the **Queuing** tab for the COM+ application's **Properties** dialog, using the Component Services administrative tool.</span></span> <span data-ttu-id="77f07-106">Questa operazione deve essere eseguita solo su una rete attendibile e deve essere eseguita sia sul client che sul server, se l'applicazione è già stata esportata.</span><span class="sxs-lookup"><span data-stu-id="77f07-106">This should be done only on a trusted network and must be done at both client and server if the application has already been exported.</span></span>

 

 



