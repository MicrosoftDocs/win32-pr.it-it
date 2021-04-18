---
title: Abilitazione della sicurezza COM tramite DCOMCNFG
description: Dcomcnfg.exe fornisce un'interfaccia utente per la modifica di determinate impostazioni del Registro di sistema.
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01139584b715fccdad923bc5eb3d6a863a63ef8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298017"
---
# <a name="enabling-com-security-using-dcomcnfg"></a><span data-ttu-id="487ed-103">Abilitazione della sicurezza COM tramite DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="487ed-103">Enabling COM Security Using DCOMCNFG</span></span>

<span data-ttu-id="487ed-104">Dcomcnfg.exe fornisce un'interfaccia utente per la modifica di determinate impostazioni del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="487ed-104">Dcomcnfg.exe provides a user interface for modifying certain settings in the registry.</span></span> <span data-ttu-id="487ed-105">Con Dcomcnfg.exe è possibile abilitare la sicurezza a livello di computer o a livello di processo.</span><span class="sxs-lookup"><span data-stu-id="487ed-105">By using Dcomcnfg.exe, you can enable security either on a computer-wide or a process-wide basis.</span></span> <span data-ttu-id="487ed-106">È possibile abilitare la sicurezza per un determinato computer in modo che quando un processo non fornisce le proprie impostazioni di sicurezza, a livello di codice o tramite i valori del registro di sistema, verranno utilizzati i valori impostati da Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="487ed-106">You can enable security for a particular computer so that when a process does not provide its own security settings, either programmatically or through registry values, the values set by Dcomcnfg.exe will be used.</span></span> <span data-ttu-id="487ed-107">In alternativa, è possibile usare Dcomcnfg.exe per abilitare la sicurezza solo per una particolare applicazione.</span><span class="sxs-lookup"><span data-stu-id="487ed-107">Or you can use Dcomcnfg.exe to enable security for a particular application only.</span></span>

<span data-ttu-id="487ed-108">Quando si Abilita la sicurezza, è necessario eseguire due attività principali:</span><span class="sxs-lookup"><span data-stu-id="487ed-108">When enabling security, there are two primary tasks to accomplish:</span></span>

-   <span data-ttu-id="487ed-109">Impostare un livello di autenticazione diverso da None.</span><span class="sxs-lookup"><span data-stu-id="487ed-109">Set an authentication level that is not None.</span></span>
-   <span data-ttu-id="487ed-110">Impostare le autorizzazioni, incluse le autorizzazioni di avvio e di accesso.</span><span class="sxs-lookup"><span data-stu-id="487ed-110">Set permissions, including both launch and access permissions.</span></span>

<span data-ttu-id="487ed-111">I passaggi necessari per eseguire queste attività variano a seconda che si stia abilitando la protezione per l'intero computer o solo per una particolare applicazione.</span><span class="sxs-lookup"><span data-stu-id="487ed-111">The steps taken to accomplish these tasks depend on whether you are enabling security for the whole computer or just for a particular application.</span></span> <span data-ttu-id="487ed-112">Inoltre, potrebbe essere necessario impostare altri valori per il computer o l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="487ed-112">Also, you may want to set other values for the computer or application.</span></span>

> [!Note]  
> <span data-ttu-id="487ed-113">Per eseguire Dcomcnfg.exe, è necessario essere un amministratore.</span><span class="sxs-lookup"><span data-stu-id="487ed-113">You must be an administrator to run Dcomcnfg.exe.</span></span>

 

<span data-ttu-id="487ed-114">Negli argomenti seguenti vengono fornite procedure dettagliate su come impostare la sicurezza con Dcomcnfg.exe:</span><span class="sxs-lookup"><span data-stu-id="487ed-114">The following topics provide step-by-step procedures on how to set security with Dcomcnfg.exe:</span></span>

-   [<span data-ttu-id="487ed-115">Impostazione della sicurezza System-Wide tramite DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="487ed-115">Setting System-Wide Security Using DCOMCNFG</span></span>](setting-machine-wide-security-using-dcomcnfg.md)
-   [<span data-ttu-id="487ed-116">Impostazione della sicurezza di Processwide tramite DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="487ed-116">Setting Processwide Security Using DCOMCNFG</span></span>](setting-processwide-security-using-dcomcnfg.md)

## <a name="related-topics"></a><span data-ttu-id="487ed-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="487ed-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="487ed-118">Sicurezza in COM</span><span class="sxs-lookup"><span data-stu-id="487ed-118">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="487ed-119">Disattivazione della sicurezza</span><span class="sxs-lookup"><span data-stu-id="487ed-119">Turning Off Security</span></span>](turning-off-security.md)
</dt> </dl>

 

 




