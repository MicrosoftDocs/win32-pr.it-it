---
title: Modifica delle impostazioni predefinite di sicurezza per un computer
description: Modifica delle impostazioni predefinite di sicurezza per un computer
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e7a17e7db1f8852dff42e62384c730090bbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395266"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a><span data-ttu-id="91d1f-103">Modifica delle impostazioni predefinite di sicurezza per un computer</span><span class="sxs-lookup"><span data-stu-id="91d1f-103">Modifying the Security Defaults for a Computer</span></span>

<span data-ttu-id="91d1f-104">Non è consigliabile modificare le impostazioni di sicurezza a livello di sistema, in quanto questa operazione influirà su tutte le applicazioni server COM che non impostano una sicurezza a livello di processo e potrebbe impedire il corretto funzionamento.</span><span class="sxs-lookup"><span data-stu-id="91d1f-104">It is not recommended that you change the system-wide security settings, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="91d1f-105">Se si modificano le impostazioni di sicurezza a livello di sistema in modo da influire sulle impostazioni di sicurezza per una particolare applicazione COM, è necessario modificare le impostazioni di sicurezza a livello di processo per quella particolare applicazione COM.</span><span class="sxs-lookup"><span data-stu-id="91d1f-105">If you are changing the system-wide security settings to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="91d1f-106">Per ulteriori informazioni sull'impostazione della sicurezza a livello di processo, vedere [impostazione Process-Wide sicurezza](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="91d1f-106">For more information about setting process-wide security, see [Setting Process-Wide Security](setting-processwide-security.md).</span></span>

<span data-ttu-id="91d1f-107">Determinati valori del registro di sistema determinano le impostazioni di sicurezza per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="91d1f-107">Certain values in the registry determine security settings for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="91d1f-108">È possibile modificare queste impostazioni usando Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="91d1f-108">You can modify these settings using Dcomcnfg.exe.</span></span>

<span data-ttu-id="91d1f-109">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="91d1f-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="91d1f-110">Valori del registro di sistema per System-Wide sicurezza</span><span class="sxs-lookup"><span data-stu-id="91d1f-110">Registry Values for System-Wide Security</span></span>](registry-values-for-machine-wide-security.md)
-   [<span data-ttu-id="91d1f-111">Impostazione della sicurezza System-Wide tramite DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="91d1f-111">Setting System-Wide Security Using DCOMCNFG</span></span>](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a><span data-ttu-id="91d1f-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91d1f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91d1f-113">Impostazione della sicurezza a livello di processo</span><span class="sxs-lookup"><span data-stu-id="91d1f-113">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> <dt>

[<span data-ttu-id="91d1f-114">Impostazione della sicurezza per le applicazioni COM</span><span class="sxs-lookup"><span data-stu-id="91d1f-114">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




