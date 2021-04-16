---
title: InprocServer32
description: Registra un server in-process a 32 bit e specifica il modello di threading dell'Apartment in cui è possibile eseguire il server.
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- InprocServer32 chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daae9d495ad588e0dc710b63fe7d7ae9f48c11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515961"
---
# <a name="inprocserver32"></a><span data-ttu-id="a04af-104">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="a04af-104">InprocServer32</span></span>

<span data-ttu-id="a04af-105">Registra un server in-process a 32 bit e specifica il modello di threading dell'Apartment in cui è possibile eseguire il server.</span><span class="sxs-lookup"><span data-stu-id="a04af-105">Registers a 32-bit in-process server and specifies the threading model of the apartment the server can run in.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a04af-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="a04af-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         (Default) = path
         ThreadingModel = value
```

## <a name="remarks"></a><span data-ttu-id="a04af-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="a04af-107">Remarks</span></span>

<span data-ttu-id="a04af-108">**ThreadingModel** è un valore **reg \_ SZ** che specifica il modello di Threading.</span><span class="sxs-lookup"><span data-stu-id="a04af-108">**ThreadingModel** is a **REG\_SZ** value the specifies the threading model.</span></span> <span data-ttu-id="a04af-109">I valori possibili sono illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a04af-109">The possible values are shown in the following table.</span></span>



| <span data-ttu-id="a04af-110">Valore</span><span class="sxs-lookup"><span data-stu-id="a04af-110">Value</span></span>     | <span data-ttu-id="a04af-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a04af-111">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="a04af-112">Apartment</span><span class="sxs-lookup"><span data-stu-id="a04af-112">Apartment</span></span> | <span data-ttu-id="a04af-113">Apartment a thread singolo</span><span class="sxs-lookup"><span data-stu-id="a04af-113">Single-threaded apartment</span></span>                  |
| <span data-ttu-id="a04af-114">Entrambi</span><span class="sxs-lookup"><span data-stu-id="a04af-114">Both</span></span>      | <span data-ttu-id="a04af-115">Apartment a thread singolo o a thread multipli</span><span class="sxs-lookup"><span data-stu-id="a04af-115">Single-threaded or multithreaded apartment</span></span> |
| <span data-ttu-id="a04af-116">Gratuito</span><span class="sxs-lookup"><span data-stu-id="a04af-116">Free</span></span>      | <span data-ttu-id="a04af-117">Apartment a thread multipli</span><span class="sxs-lookup"><span data-stu-id="a04af-117">Multithreaded apartment</span></span>                    |
| <span data-ttu-id="a04af-118">Neutralità</span><span class="sxs-lookup"><span data-stu-id="a04af-118">Neutral</span></span>   | <span data-ttu-id="a04af-119">Apartment neutro</span><span class="sxs-lookup"><span data-stu-id="a04af-119">Neutral apartment</span></span>                          |



 

<span data-ttu-id="a04af-120">È necessario utilizzare lo stesso valore per ogni oggetto fornito dal server in-process.</span><span class="sxs-lookup"><span data-stu-id="a04af-120">You must use the same value for every object provided by the in-process server.</span></span>

<span data-ttu-id="a04af-121">Se **ThreadingModel** non è presente o non è impostato su un valore, il server viene caricato nel primo Apartment inizializzato nel processo.</span><span class="sxs-lookup"><span data-stu-id="a04af-121">If **ThreadingModel** is not present or is not set to a value, the server is loaded into the first apartment that was initialized in the process.</span></span> <span data-ttu-id="a04af-122">Questo Apartment viene talvolta definito Apartment a thread singolo principale (STA).</span><span class="sxs-lookup"><span data-stu-id="a04af-122">This apartment is sometimes referred to as the main single-threaded apartment (STA).</span></span> <span data-ttu-id="a04af-123">Se il primo STA in un processo inizializzato da COM, anziché da una chiamata esplicita a [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), viene chiamato sta per essere host.</span><span class="sxs-lookup"><span data-stu-id="a04af-123">If the first STA in a process is initialized by COM, rather than by an explicit call to [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), it is called the host STA.</span></span> <span data-ttu-id="a04af-124">Ad esempio, COM crea un'host STA se un server in-process da caricare richiede un STA ma attualmente non è presente alcun STA nel processo.</span><span class="sxs-lookup"><span data-stu-id="a04af-124">For example, COM creates a host STA if an in-process server to be loaded requires an STA but there is currently no STA in the process.</span></span>

<span data-ttu-id="a04af-125">Laddove possibile, il server in-process viene caricato nello stesso apartment del client che lo carica.</span><span class="sxs-lookup"><span data-stu-id="a04af-125">Whenever possible, the in-process server is loaded in the same apartment as the client that loads it.</span></span> <span data-ttu-id="a04af-126">Se il modello di threading dell'Apartment client non è compatibile con il modello specificato, il server viene caricato come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a04af-126">If the threading model of the client apartment is not compatible with the model specified, the server is loaded as indicated in the following table.</span></span>



| <span data-ttu-id="a04af-127">Modello di threading del server</span><span class="sxs-lookup"><span data-stu-id="a04af-127">Threading model of server</span></span> | <span data-ttu-id="a04af-128">Il server Apartment viene eseguito in</span><span class="sxs-lookup"><span data-stu-id="a04af-128">Apartment server is run in</span></span> |
|---------------------------|----------------------------|
| <not specified>     | <span data-ttu-id="a04af-129">STA principale</span><span class="sxs-lookup"><span data-stu-id="a04af-129">Main STA</span></span>                   |
| <span data-ttu-id="a04af-130">Entrambi</span><span class="sxs-lookup"><span data-stu-id="a04af-130">Both</span></span>                      | <span data-ttu-id="a04af-131">Stesso apartment del client</span><span class="sxs-lookup"><span data-stu-id="a04af-131">Same apartment as client</span></span>   |
| <span data-ttu-id="a04af-132">Gratuito</span><span class="sxs-lookup"><span data-stu-id="a04af-132">Free</span></span>                      | <span data-ttu-id="a04af-133">Apartment a thread multipli</span><span class="sxs-lookup"><span data-stu-id="a04af-133">Multithreaded apartment</span></span>    |
| <span data-ttu-id="a04af-134">Neutralità</span><span class="sxs-lookup"><span data-stu-id="a04af-134">Neutral</span></span>                   | <span data-ttu-id="a04af-135">Apartment neutro</span><span class="sxs-lookup"><span data-stu-id="a04af-135">Neutral apartment</span></span>          |



 

<span data-ttu-id="a04af-136">Se il modello di threading del server è Apartment, l'Apartment in cui viene caricato il server dipende dall'Apartment in cui è in esecuzione il client, come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a04af-136">If the threading model of the server is Apartment, the apartment the server is loaded in depends on the apartment the client is running in, as indicated in the following table.</span></span>



| <span data-ttu-id="a04af-137">Il client Apartment viene eseguito in</span><span class="sxs-lookup"><span data-stu-id="a04af-137">Apartment client is run in</span></span> | <span data-ttu-id="a04af-138">Il server Apartment viene eseguito in</span><span class="sxs-lookup"><span data-stu-id="a04af-138">Apartment server is run in</span></span> |
|----------------------------|----------------------------|
| <span data-ttu-id="a04af-139">Multithreading</span><span class="sxs-lookup"><span data-stu-id="a04af-139">Multithreaded</span></span>              | <span data-ttu-id="a04af-140">Host STA</span><span class="sxs-lookup"><span data-stu-id="a04af-140">Host STA</span></span>                   |
| <span data-ttu-id="a04af-141">Neutro (sul thread STA)</span><span class="sxs-lookup"><span data-stu-id="a04af-141">Neutral (on STA thread)</span></span>    | <span data-ttu-id="a04af-142">Stesso apartment del client</span><span class="sxs-lookup"><span data-stu-id="a04af-142">Same apartment as client</span></span>   |
| <span data-ttu-id="a04af-143">Neutro (su thread MTA)</span><span class="sxs-lookup"><span data-stu-id="a04af-143">Neutral (on MTA thread)</span></span>    | <span data-ttu-id="a04af-144">Host STA</span><span class="sxs-lookup"><span data-stu-id="a04af-144">Host STA</span></span>                   |



 

<span data-ttu-id="a04af-145">COM è inoltre in grado di creare un Apartment a thread multipli (MTA) host.</span><span class="sxs-lookup"><span data-stu-id="a04af-145">COM can also create a host multithreaded apartment (MTA).</span></span> <span data-ttu-id="a04af-146">Se un client in un Apartment a thread singolo richiede un server in-process il cui modello di threading è gratuito quando non è presente alcun MTA nel processo, COM crea un MTA host e lo carica nel server.</span><span class="sxs-lookup"><span data-stu-id="a04af-146">If a client in a single-threaded apartment requests an in-process server whose threading model is Free when there is no MTA in the process, COM creates a host MTA and loads the server into it.</span></span>

<span data-ttu-id="a04af-147">Per un server in-process a 32 bit, è necessario registrare le chiavi [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InprocServer32** e [**Insertable**](insertable.md) .</span><span class="sxs-lookup"><span data-stu-id="a04af-147">For a 32-bit in-process server, the [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InprocServer32**, and [**Insertable**](insertable.md) keys must be registered.</span></span> <span data-ttu-id="a04af-148">La voce **InprocServer** è necessaria solo per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="a04af-148">The **InprocServer** entry is needed only for backward compatibility.</span></span> <span data-ttu-id="a04af-149">Se non è presente, la classe funziona ancora, ma non può essere caricata in applicazioni a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="a04af-149">If it is missing, the class still works but it cannot be loaded in 16-bit applications.</span></span>

<span data-ttu-id="a04af-150">Se un contenitore esegue una ricerca nel registro di sistema per un server in-process, la versione a 16 bit ha la priorità con un contenitore a 16 bit e la versione a 32 bit ha la priorità con un contenitore a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a04af-150">If a container is searching the registry for an in-process server, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a04af-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a04af-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a04af-152">**InprocServer**</span><span class="sxs-lookup"><span data-stu-id="a04af-152">**InprocServer**</span></span>](inprocserver.md)
</dt> </dl>

 

 




