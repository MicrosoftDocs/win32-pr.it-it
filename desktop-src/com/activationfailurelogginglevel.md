---
title: ActivationFailureLoggingLevel
description: Imposta il livello di dettaglio delle voci del registro eventi sulle richieste non riuscite per l'avvio e l'attivazione dei componenti.
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- Valore ActivationFailureLoggingLevel del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdd834be35a59dd5d8e207cd679dae68043d70c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396870"
---
# <a name="activationfailurelogginglevel"></a><span data-ttu-id="27584-104">ActivationFailureLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="27584-104">ActivationFailureLoggingLevel</span></span>

<span data-ttu-id="27584-105">Imposta il livello di dettaglio delle voci del registro eventi sulle richieste non riuscite per l'avvio e l'attivazione dei componenti.</span><span class="sxs-lookup"><span data-stu-id="27584-105">Sets the verbosity of event log entries about failed requests for component launch and activation.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="27584-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="27584-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="27584-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="27584-107">Remarks</span></span>

<span data-ttu-id="27584-108">Si tratta di un valore **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="27584-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="27584-109">Valore</span><span class="sxs-lookup"><span data-stu-id="27584-109">Value</span></span> | <span data-ttu-id="27584-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27584-110">Description</span></span>                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27584-111">0</span><span class="sxs-lookup"><span data-stu-id="27584-111">0</span></span>     | <span data-ttu-id="27584-112">Usare la registrazione discrezionale.</span><span class="sxs-lookup"><span data-stu-id="27584-112">Use discretionary logging.</span></span> <span data-ttu-id="27584-113">Per impostazione predefinita, gli errori di log, ma i client possono eseguire l'override di questo comportamento specificando CLSCTX \_ nessun \_ log degli errori \_ in [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex).</span><span class="sxs-lookup"><span data-stu-id="27584-113">Log failures by default, but clients can override this behavior by specifying CLSCTX\_NO\_FAILURE\_LOG in [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex).</span></span> <span data-ttu-id="27584-114">Rappresenta il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="27584-114">This is the default value.</span></span> |
| <span data-ttu-id="27584-115">1</span><span class="sxs-lookup"><span data-stu-id="27584-115">1</span></span>     | <span data-ttu-id="27584-116">Registrare sempre tutti gli errori indipendentemente dal client specificato.</span><span class="sxs-lookup"><span data-stu-id="27584-116">Always log all failures no matter what the client specified.</span></span>                                                                                                                                                      |
| <span data-ttu-id="27584-117">2</span><span class="sxs-lookup"><span data-stu-id="27584-117">2</span></span>     | <span data-ttu-id="27584-118">Non registrare mai eventuali errori indipendentemente dal client specificato.</span><span class="sxs-lookup"><span data-stu-id="27584-118">Never log any failures no matter what the client specified.</span></span>                                                                                                                                                       |



 

<span data-ttu-id="27584-119">Se è necessaria un'applicazione per controllare la registrazione degli eventi, è consigliabile impostare questo valore su 0 e scrivere il codice client per eseguirne l'override quando necessario.</span><span class="sxs-lookup"><span data-stu-id="27584-119">If you need an application to control event logging, it is recommended that you set this value to 0 and write the client code to override it when needed.</span></span> <span data-ttu-id="27584-120">Si consiglia vivamente di non impostare il valore su 2.</span><span class="sxs-lookup"><span data-stu-id="27584-120">It is strongly recommended that you do not set the value to 2.</span></span> <span data-ttu-id="27584-121">Se la registrazione degli eventi è disabilitata, è più difficile diagnosticare i problemi.</span><span class="sxs-lookup"><span data-stu-id="27584-121">If event logging is disabled, it is more difficult to diagnose problems.</span></span> <span data-ttu-id="27584-122">Per gli errori di autorizzazione per le restrizioni del computer, in cui COM non dispone dei bit CLSCTX, COM considererà un valore pari a 0 come 1.</span><span class="sxs-lookup"><span data-stu-id="27584-122">For machine restrictions permission failures, where COM does not have the CLSCTX bits, COM will treat a value of 0 as 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27584-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27584-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27584-124">Impostazione della sicurezza per le applicazioni COM</span><span class="sxs-lookup"><span data-stu-id="27584-124">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




