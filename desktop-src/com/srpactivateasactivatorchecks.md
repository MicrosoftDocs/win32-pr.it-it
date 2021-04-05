---
title: SRPActivateAsActivatorChecks
description: Determina se i livelli di attendibilità dei criteri di restrizione software vengono usati durante le attivazioni di ActivateAsActivator.
ms.assetid: b0d616c3-1cb0-4854-a4f9-6635d61b0698
keywords:
- Valore SRPActivateAsActivatorChecks del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b66ae6b1c7f267f48f24441c04e95eea75e4345
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709433"
---
# <a name="srpactivateasactivatorchecks"></a><span data-ttu-id="b8bc0-104">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="b8bc0-104">SRPActivateAsActivatorChecks</span></span>

<span data-ttu-id="b8bc0-105">Determina se i livelli di attendibilità dei criteri di restrizione software vengono usati durante le attivazioni di ActivateAsActivator.</span><span class="sxs-lookup"><span data-stu-id="b8bc0-105">Determines whether software restriction policy (SRP) trust levels are used during ActivateAsActivator activations.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b8bc0-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="b8bc0-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPActivateAsActivatorChecks = value
```

## <a name="remarks"></a><span data-ttu-id="b8bc0-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8bc0-107">Remarks</span></span>

<span data-ttu-id="b8bc0-108">Si tratta di un valore **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="b8bc0-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="b8bc0-109">I valori stringa di {N, N, NO, no, no} indicano che l'oggetto server viene eseguito con il livello di attendibilità SRP dell'oggetto client, indipendentemente dal livello di attendibilità SRP con cui è stato configurato.</span><span class="sxs-lookup"><span data-stu-id="b8bc0-109">String values of {N, n, NO, No, no} indicate that the server object runs with the SRP trust level of the client object, regardless of the SRP trust level with which it was configured.</span></span> <span data-ttu-id="b8bc0-110">Se questo valore del registro di sistema è impostato su qualsiasi altro valore o non esiste, il livello di attendibilità SRP configurato per l'oggetto server viene confrontato con il livello di attendibilità SRP dell'oggetto client e il livello di attendibilità più rigoroso viene utilizzato per eseguire l'oggetto server.</span><span class="sxs-lookup"><span data-stu-id="b8bc0-110">If this registry value is set to any other value or does not exist, the SRP trust level that is configured for the server object is compared with the SRP trust level of the client object and that the more stringent trust level is used to run the server object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8bc0-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b8bc0-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8bc0-112">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="b8bc0-112">SRPTrustLevel</span></span>](srptrustlevel.md)
</dt> </dl>

 

 




