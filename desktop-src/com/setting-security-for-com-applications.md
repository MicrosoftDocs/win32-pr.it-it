---
title: Impostazione della sicurezza per le applicazioni COM
description: Impostazione della sicurezza per le applicazioni COM
ms.assetid: 5b615007-e04b-41be-872c-20e0ea818ff1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8dd705015aaa2ca1965d07c556ff3d55aada00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103857018"
---
# <a name="setting-security-for-com-applications"></a><span data-ttu-id="407f6-103">Impostazione della sicurezza per le applicazioni COM</span><span class="sxs-lookup"><span data-stu-id="407f6-103">Setting Security for COM Applications</span></span>

<span data-ttu-id="407f6-104">Esistono diversi modi per controllare la sicurezza per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="407f6-104">There are several ways you can help control security for your applications.</span></span> <span data-ttu-id="407f6-105">È possibile modificare le impostazioni di sicurezza predefinite di un computer, che vengono utilizzate da tutte le applicazioni del computer che non forniscono i propri valori di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="407f6-105">You can change a computer's default security settings, which are used by all applications on the computer that do not supply their own security values.</span></span> <span data-ttu-id="407f6-106">È possibile impostare la sicurezza per un determinato processo usando Dcomcnfg.exe o chiamando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="407f6-106">You can set security for a particular process, either by using Dcomcnfg.exe or by calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="407f6-107">È anche possibile controllare a livello di codice le impostazioni di sicurezza a livello di proxy di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="407f6-107">You can also programmatically control security settings at the interface proxy level.</span></span>

<span data-ttu-id="407f6-108">Negli argomenti seguenti vengono descritte le procedure per l'impostazione della sicurezza:</span><span class="sxs-lookup"><span data-stu-id="407f6-108">The following topics provide procedures that explain how to set security:</span></span>

-   [<span data-ttu-id="407f6-109">Modifica delle impostazioni predefinite di sicurezza per un computer</span><span class="sxs-lookup"><span data-stu-id="407f6-109">Modifying the Security Defaults for a Computer</span></span>](modifying-the-security-defaults-for-a-computer.md)
-   [<span data-ttu-id="407f6-110">Impostazione della sicurezza Process-Wide</span><span class="sxs-lookup"><span data-stu-id="407f6-110">Setting Process-Wide Security</span></span>](setting-processwide-security.md)
-   [<span data-ttu-id="407f6-111">Impostazione della sicurezza a livello di proxy di interfaccia</span><span class="sxs-lookup"><span data-stu-id="407f6-111">Setting Security at the Interface Proxy Level</span></span>](setting-security-at-the-interface-proxy-level.md)

## <a name="related-topics"></a><span data-ttu-id="407f6-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="407f6-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="407f6-113">Sicurezza in COM</span><span class="sxs-lookup"><span data-stu-id="407f6-113">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




