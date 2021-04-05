---
title: Indipendenza da altri componenti
description: I dati degli errori estesi sono utili anche quando il server o l'applicazione attraverso cui la catena è passata non riconosce i dati di errore estesi o non ne sfrutta i vantaggi. Alla fine di questa sezione vengono forniti gli approcci consigliati per tali situazioni.
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- Indipendenza da altri componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba20a47a5bb30d8e23c1a90d666bc6b957ebb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955759"
---
# <a name="independence-from-other-components"></a><span data-ttu-id="04e37-105">Indipendenza da altri componenti</span><span class="sxs-lookup"><span data-stu-id="04e37-105">Independence From Other Components</span></span>

<span data-ttu-id="04e37-106">I dati degli errori estesi sono utili anche quando il server o l'applicazione attraverso cui la catena è passata non riconosce i dati di errore estesi o non ne sfrutta i vantaggi.</span><span class="sxs-lookup"><span data-stu-id="04e37-106">Extended error data is useful even when the server or application through which the chain passed does not recognize extended error data, or does not take advantage of it.</span></span> <span data-ttu-id="04e37-107">Alla fine di questa sezione vengono forniti gli approcci consigliati per tali situazioni.</span><span class="sxs-lookup"><span data-stu-id="04e37-107">Recommended approaches for such situations are provided at the end of this section.</span></span>

<span data-ttu-id="04e37-108">I dati degli errori estesi sono particolarmente utili quando le applicazioni o i server che usano RPC sfruttano le informazioni estese sugli errori.</span><span class="sxs-lookup"><span data-stu-id="04e37-108">Extended error data is most useful when applications or servers using RPC take advantage of extended error information.</span></span> <span data-ttu-id="04e37-109">Quando si analizza un codice di errore di RPC \_ \_ \* e i server o le applicazioni in cui si verificano i dati di errore estesi non sono disponibili, considerare gli approcci seguenti:</span><span class="sxs-lookup"><span data-stu-id="04e37-109">When investigating an RPC\_S\_\* error code and the servers or applications involved do not make extended error data available, consider the following approaches:</span></span>

-   <span data-ttu-id="04e37-110">Prendere una sniffata.</span><span class="sxs-lookup"><span data-stu-id="04e37-110">Take a sniff.</span></span>

    <span data-ttu-id="04e37-111">Riprodurre lo scenario durante l'esecuzione dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="04e37-111">Reproduce the scenario while taking the sniff.</span></span> <span data-ttu-id="04e37-112">L'analisi della rete conterrà i dati di errore estesi.</span><span class="sxs-lookup"><span data-stu-id="04e37-112">The sniff of the wire will contain the extended error data.</span></span>

-   <span data-ttu-id="04e37-113">Esaminarlo dal debugger.</span><span class="sxs-lookup"><span data-stu-id="04e37-113">Examine it from the debugger.</span></span>

    <span data-ttu-id="04e37-114">Se l'analisi del problema non funziona perché la chiamata è locale o perché l'errore ha origine localmente, connettere un debugger al processo che restituisce l'errore e inserire un punto di interruzione immediatamente dopo la chiamata RPC che ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="04e37-114">If taking a sniff of the problem does not work, because the call is local or because the error originates locally, attach a debugger to the process returning the error and put a breakpoint immediately after the RPC call generating the error.</span></span> <span data-ttu-id="04e37-115">RPC spesso indica errori generando eccezioni, pertanto se si sta cercando l'errore 1825 ( \_ errore pkg di RPC S \_ sec \_ \_ ), abilitare l'eccezione 1825 e quando il debugger interrompe tale eccezione, esaminare le informazioni estese sull'errore per il thread.</span><span class="sxs-lookup"><span data-stu-id="04e37-115">RPC often indicates errors by throwing exceptions, so if you are looking for error 1825 (RPC\_S\_SEC\_PKG\_ERROR), enable exception 1825 and when the debugger breaks on that exception, examine the extended error information for the thread.</span></span>

 

 




