---
description: COM+ introduce appartamenti neutri per semplificare la programmazione in ambienti multithread. L'Apartment neutro è il modello preferito per COM+ per i componenti senza interfaccia utente.
ms.assetid: 679742af-7c04-4b0e-822a-a43e1aafa936
title: Appartamenti neutri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac3bdff2670e4f99ad94af20278eaca6a38861e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401433"
---
# <a name="neutral-apartments"></a><span data-ttu-id="f4c22-104">Appartamenti neutri</span><span class="sxs-lookup"><span data-stu-id="f4c22-104">Neutral Apartments</span></span>

<span data-ttu-id="f4c22-105">COM+ introduce appartamenti neutri per semplificare la programmazione in ambienti multithread.</span><span class="sxs-lookup"><span data-stu-id="f4c22-105">COM+ introduces neutral apartments to simplify programming in multithreaded environments.</span></span> <span data-ttu-id="f4c22-106">L'Apartment neutro è il modello preferito per COM+ per i componenti senza interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="f4c22-106">The neutral apartment is the preferred model for COM+ for components with no user interface.</span></span>

<span data-ttu-id="f4c22-107">In passato, per evitare colli di bottiglia, gli sviluppatori COM+ che richiedevano la scalabilità del server dovevano implementare i componenti a thread libero. Tuttavia, i modelli di threading libero sono complicati da implementare perché devono gestire l'accesso con Interlocking.</span><span class="sxs-lookup"><span data-stu-id="f4c22-107">In the past, to prevent bottlenecks, COM+ developers requiring server scalability had to implement free-threaded components; however, free-threading models are complicated to implement because they must deal with interlocking access.</span></span> <span data-ttu-id="f4c22-108">Negli appartamenti neutri gli oggetti seguono le linee guida per gli Apartment a thread multipli ma possono essere eseguiti su qualsiasi tipo di thread.</span><span class="sxs-lookup"><span data-stu-id="f4c22-108">In neutral apartments, objects follow the guidelines for multithreaded apartments but can execute on any kind of thread.</span></span> <span data-ttu-id="f4c22-109">Quando un thread è in esecuzione in un Apartment neutro, il contesto dell'oggetto viene ricevuto senza causare un cambio di thread.</span><span class="sxs-lookup"><span data-stu-id="f4c22-109">When a thread is running in a neutral apartment, the object's context is received without causing a thread switch.</span></span>

<span data-ttu-id="f4c22-110">Ogni processo può avere un solo Apartment neutro.</span><span class="sxs-lookup"><span data-stu-id="f4c22-110">Each process can have only one neutral apartment.</span></span> <span data-ttu-id="f4c22-111">Per selezionare un Apartment neutro, usare l'impostazione del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="f4c22-111">To select a neutral apartment, use the following registry setting:</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         ThreadingModel = Neutral
```

<span data-ttu-id="f4c22-112">I componenti che dispongono di interfacce utente devono continuare a usare Apartment a thread singolo come modello preferito.</span><span class="sxs-lookup"><span data-stu-id="f4c22-112">Components that have user interfaces should continue to use single-threaded apartments as the preferred model.</span></span> <span data-ttu-id="f4c22-113">Per selezionare un Apartment a thread singolo, usare l'impostazione del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="f4c22-113">To select a single-threaded apartment, use the following registry setting:</span></span>

<span data-ttu-id="f4c22-114">**ThreadingModel** = Apartment</span><span class="sxs-lookup"><span data-stu-id="f4c22-114">**ThreadingModel** = Apartment</span></span>

 

 



