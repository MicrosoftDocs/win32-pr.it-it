---
title: Impostazione della sicurezza Process-Wide
description: Esistono diversi modi per impostare la sicurezza a livello di processo.
ms.assetid: 596ba257-cbde-4243-aa29-78749304867a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc483bc6f52963eadc12891e657db1cbe51fb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298983"
---
# <a name="setting-process-wide-security"></a><span data-ttu-id="f5746-103">Impostazione della sicurezza Process-Wide</span><span class="sxs-lookup"><span data-stu-id="f5746-103">Setting Process-Wide Security</span></span>

<span data-ttu-id="f5746-104">Esistono diversi modi per impostare la sicurezza a livello di processo.</span><span class="sxs-lookup"><span data-stu-id="f5746-104">There are several ways to set process-wide security.</span></span> <span data-ttu-id="f5746-105">Il primo modo, usando lo strumento Dcomcnfg.exe, è più semplice perché non richiede alcuna programmazione.</span><span class="sxs-lookup"><span data-stu-id="f5746-105">The first way, using the Dcomcnfg.exe tool, is easiest because it requires no programming.</span></span> <span data-ttu-id="f5746-106">La seconda tecnica offre al programmatore maggiore controllo e richiede una chiamata a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="f5746-106">The second technique offers the programmer more control, and it requires a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="f5746-107">Un'altra tecnica consiste nell'impostare la sicurezza a livello di processo nel registro di sistema tramite la chiave [AppID](appid-key.md) .</span><span class="sxs-lookup"><span data-stu-id="f5746-107">Another technique is to set process-wide security in the registry by using the [AppID](appid-key.md) key.</span></span>

<span data-ttu-id="f5746-108">Per ulteriori informazioni su queste tecniche, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="f5746-108">For more information about these techniques, see the following topics:</span></span>

-   [<span data-ttu-id="f5746-109">Impostazione della sicurezza Process-Wide tramite DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="f5746-109">Setting Process-Wide Security Using DCOMCNFG</span></span>](setting-processwide-security-using-dcomcnfg.md)
-   [<span data-ttu-id="f5746-110">Impostazione Process-Wide sicurezza con CoInitializeSecurity</span><span class="sxs-lookup"><span data-stu-id="f5746-110">Setting Process-Wide Security with CoInitializeSecurity</span></span>](setting-processwide-security-with-coinitializesecurity.md)
-   [<span data-ttu-id="f5746-111">Impostazione della sicurezza Process-Wide tramite il registro di sistema</span><span class="sxs-lookup"><span data-stu-id="f5746-111">Setting Process-Wide Security Through the Registry</span></span>](setting-processwide-security-through-the-registry.md)

## <a name="related-topics"></a><span data-ttu-id="f5746-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5746-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5746-113">Impostazione della sicurezza a livello di proxy di interfaccia</span><span class="sxs-lookup"><span data-stu-id="f5746-113">Setting Security at the Interface Proxy Level</span></span>](setting-security-at-the-interface-proxy-level.md)
</dt> <dt>

[<span data-ttu-id="f5746-114">Impostazione della sicurezza per le applicazioni COM</span><span class="sxs-lookup"><span data-stu-id="f5746-114">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




