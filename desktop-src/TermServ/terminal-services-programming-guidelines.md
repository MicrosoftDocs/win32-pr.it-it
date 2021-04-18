---
title: Linee guida per la programmazione Servizi Desktop remoto
description: Argomenti che forniscono linee guida per lo sviluppo di applicazioni in un ambiente Servizi Desktop remoto.
ms.assetid: e0cd52c5-40d7-4a48-9d10-fdbcea46a5a0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto, linee guida per la programmazione
- linee guida per la programmazione Servizi Desktop remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e767740a2f279c90ce4f0eb37c49919749465ad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299959"
---
# <a name="remote-desktop-services-programming-guidelines"></a><span data-ttu-id="22b2e-105">Linee guida per la programmazione Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="22b2e-105">Remote Desktop Services programming guidelines</span></span>

<span data-ttu-id="22b2e-106">La maggior parte delle applicazioni basate su Windows a 32 bit o a 64 bit vengono eseguite "così come sono" in un ambiente Servizi Desktop remoto (noto in precedenza come servizi Terminal).</span><span class="sxs-lookup"><span data-stu-id="22b2e-106">Most existing 32-bit or 64-bit Windows-based applications run "as is" in a Remote Desktop Services (formerly known as Terminal Services) environment.</span></span> <span data-ttu-id="22b2e-107">Tuttavia, alcune applicazioni funzionano correttamente ed eseguono buone attività in un ambiente di Servizi Desktop remoto, mentre altre no.</span><span class="sxs-lookup"><span data-stu-id="22b2e-107">However, some applications function correctly and perform well in a Remote Desktop Services environment, while others do not.</span></span> <span data-ttu-id="22b2e-108">Negli argomenti seguenti vengono fornite le linee guida per lo sviluppo di applicazioni in un ambiente Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="22b2e-108">The following topics provide guidelines for developing applications in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="22b2e-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="22b2e-109">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="22b2e-110">Linee guida per più utenti</span><span class="sxs-lookup"><span data-stu-id="22b2e-110">Multiple-user guidelines</span></span>](multiple-user-guidelines.md)
</dt> <dd>

<span data-ttu-id="22b2e-111">Linee guida per lo sviluppo di applicazioni per più utenti in un ambiente Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="22b2e-111">Guidelines for developing applications for multiple users in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="22b2e-112">Linee guida sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="22b2e-112">Performance guidelines</span></span>](performance-guidelines.md)
</dt> <dd>

<span data-ttu-id="22b2e-113">Linee guida per lo sviluppo di applicazioni che offrono prestazioni ottimali in un ambiente Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="22b2e-113">Guidelines for developing applications that perform well in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="22b2e-114">Linee guida generali per la programmazione</span><span class="sxs-lookup"><span data-stu-id="22b2e-114">General programming guidelines</span></span>](general-programming-guidelines.md)
</dt> <dd>

<span data-ttu-id="22b2e-115">Linee guida per lo sviluppo di applicazioni in un ambiente Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="22b2e-115">Guidelines for developing applications in a Remote Desktop Services environment.</span></span>

</dd> </dl>

<span data-ttu-id="22b2e-116">Molte di queste linee guida sono buone procedure di programmazione che trarranno vantaggio dalle applicazioni in esecuzione in qualsiasi ambiente Windows.</span><span class="sxs-lookup"><span data-stu-id="22b2e-116">Many of these guidelines are good programming practices that will benefit applications running in any Windows environment.</span></span> <span data-ttu-id="22b2e-117">Tuttavia, alcune ottimizzazioni consigliate, ad esempio la limitazione degli effetti grafici, sono ottimizzazioni che si desiderano solo quando l'applicazione è in esecuzione in Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="22b2e-117">However, some recommended optimizations, such as limiting graphic effects, are optimizations that you would want only when your application is running under Remote Desktop Services.</span></span> <span data-ttu-id="22b2e-118">Per un esempio di codice che illustra come rilevare un ambiente di Servizi Desktop remoto, vedere [rilevamento dell'ambiente Servizi Desktop remoto](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="22b2e-118">For a code example that shows how to detect a Remote Desktop Services environment, see [Detecting the Remote Desktop Services Environment](detecting-the-terminal-services-environment.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="22b2e-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22b2e-119">Related topics</span></span>

<dl> <span data-ttu-id="22b2e-120"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="22b2e-120"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="22b2e-121">Servizi terminal è ora Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="22b2e-121">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[<span data-ttu-id="22b2e-122">Formato file modello amministrativo</span><span class="sxs-lookup"><span data-stu-id="22b2e-122">Administrative Template File Format</span></span>](/previous-versions/windows/desktop/Policy/administrative-template-file-format)
</dt> <dt>

[<span data-ttu-id="22b2e-123">Diritti di accesso e sicurezza della chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="22b2e-123">Registry Key Security and Access Rights</span></span>](/windows/desktop/SysInfo/registry-key-security-and-access-rights)
</dt> <dt>

[<span data-ttu-id="22b2e-124">Hive del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="22b2e-124">Registry Hives</span></span>](/windows/desktop/SysInfo/registry-hives)
</dt> <dt>

[<span data-ttu-id="22b2e-125">Descrittori di sicurezza</span><span class="sxs-lookup"><span data-stu-id="22b2e-125">Security Descriptors</span></span>](/windows/desktop/SecAuthZ/security-descriptors)
</dt> <dt>

[<span data-ttu-id="22b2e-126">Diritti di accesso standard</span><span class="sxs-lookup"><span data-stu-id="22b2e-126">Standard Access Rights</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[<span data-ttu-id="22b2e-127">Modello di controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="22b2e-127">Access Control Model</span></span>](/windows/desktop/SecAuthZ/access-control-model)
</dt> </dl>

 

 