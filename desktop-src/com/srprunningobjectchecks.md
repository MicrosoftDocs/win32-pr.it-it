---
title: SRPRunningObjectChecks
description: Determina se i tentativi di connessione agli oggetti in esecuzione vengono selezionati per i livelli di attendibilità dei criteri di restrizione software (SRP) compatibili.
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- Valore SRPRunningObjectChecks del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad307856bcfdd30cfaa6c731551ac6570d2bec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709430"
---
# <a name="srprunningobjectchecks"></a><span data-ttu-id="eb81c-104">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="eb81c-104">SRPRunningObjectChecks</span></span>

<span data-ttu-id="eb81c-105">Determina se i tentativi di connessione agli oggetti in esecuzione vengono selezionati per i livelli di attendibilità dei criteri di restrizione software (SRP) compatibili.</span><span class="sxs-lookup"><span data-stu-id="eb81c-105">Determines whether attempts to connect to running objects are screened for compatible software restriction policy (SRP) trust levels.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="eb81c-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="eb81c-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a><span data-ttu-id="eb81c-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb81c-107">Remarks</span></span>

<span data-ttu-id="eb81c-108">Si tratta di un valore **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="eb81c-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="eb81c-109">I valori stringa di {N, N, NO, no, no} indicano che i tentativi di connessione agli oggetti in esecuzione non vengono selezionati per i livelli di attendibilità SRP compatibili.</span><span class="sxs-lookup"><span data-stu-id="eb81c-109">String values of {N, n, NO, No, no} indicate that attempts to connect to running objects are not screened for compatible SRP trust levels.</span></span> <span data-ttu-id="eb81c-110">Se questo valore del registro di sistema è impostato su qualsiasi altro valore o non esiste, l'oggetto in esecuzione non può disporre di un livello di attendibilità del rollup meno rigoroso rispetto all'oggetto client.</span><span class="sxs-lookup"><span data-stu-id="eb81c-110">If this registry value is set to any other value or does not exist, the running object cannot have a less stringent SRP trust level than the client object.</span></span> <span data-ttu-id="eb81c-111">L'oggetto in esecuzione, ad esempio, non può avere un livello di attendibilità non consentito se l'oggetto client ha un livello di attendibilità senza restrizioni.</span><span class="sxs-lookup"><span data-stu-id="eb81c-111">For example, the running object cannot have a Disallowed trust level if the client object has an Unrestricted trust level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb81c-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb81c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb81c-113">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="eb81c-113">SRPTrustLevel</span></span>](srptrustlevel.md)
</dt> </dl>

 

 




