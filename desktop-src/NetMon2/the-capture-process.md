---
description: Il processo di acquisizione è lo stesso per ognuna delle quattro interfacce di NPP.
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: Processo di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0ca1987266b7e042713f1d1c292cf63d5e3ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571101"
---
# <a name="the-capture-process"></a><span data-ttu-id="18d9f-103">Processo di acquisizione</span><span class="sxs-lookup"><span data-stu-id="18d9f-103">The Capture Process</span></span>

<span data-ttu-id="18d9f-104">Il processo di acquisizione è lo stesso per ognuna delle quattro interfacce di NPP.</span><span class="sxs-lookup"><span data-stu-id="18d9f-104">The capture process is the same for each of the four NPP interfaces.</span></span> <span data-ttu-id="18d9f-105">In ogni caso, il processo include:</span><span class="sxs-lookup"><span data-stu-id="18d9f-105">In each case, the process includes:</span></span>

-   <span data-ttu-id="18d9f-106">Recupero dell'oggetto dell'interfaccia NPP da usare</span><span class="sxs-lookup"><span data-stu-id="18d9f-106">Obtaining the NPP interface object to use</span></span>
-   <span data-ttu-id="18d9f-107">Connessione alla rete</span><span class="sxs-lookup"><span data-stu-id="18d9f-107">Connecting to the network</span></span>
-   <span data-ttu-id="18d9f-108">Avvio e arresto dell' [ *acquisizione*](c.md)</span><span class="sxs-lookup"><span data-stu-id="18d9f-108">Starting and then stopping the [*capture*](c.md)</span></span>
-   <span data-ttu-id="18d9f-109">Disconnessione dalla rete</span><span class="sxs-lookup"><span data-stu-id="18d9f-109">Disconnecting from the network</span></span>

> [!Note]  
> <span data-ttu-id="18d9f-110">Quando si ottiene l'oggetto interfaccia desiderato, assicurarsi di chiamare solo i metodi inclusi in tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="18d9f-110">When you obtain the interface object that you want, ensure you call only the methods included in that interface.</span></span> <span data-ttu-id="18d9f-111">Nell'illustrazione seguente viene mostrata ogni interfaccia che fornisce metodi simili per l'acquisizione dei dati di rete.</span><span class="sxs-lookup"><span data-stu-id="18d9f-111">The following illustration shows each interface provides similar methods for capturing network data.</span></span> <span data-ttu-id="18d9f-112">Viene restituito un errore se ci si connette alla rete con un'interfaccia e quindi si prova a eseguire un'acquisizione usando i metodi di un'altra interfaccia.</span><span class="sxs-lookup"><span data-stu-id="18d9f-112">An error is returned if you connect to the network with one interface and then try to run a capture using the methods from another interface.</span></span>

 

<span data-ttu-id="18d9f-113">Le illustrazioni seguenti illustrano due modi diversi per eseguire un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="18d9f-113">The following illustrations show two different ways you could run a capture.</span></span> <span data-ttu-id="18d9f-114">Nella prima figura viene illustrato come eseguire una o più acquisizioni sequenziali, consentendo di creare un numero qualsiasi di acquisizioni indipendenti.</span><span class="sxs-lookup"><span data-stu-id="18d9f-114">The first illustration shows how to run one or more sequential captures, allowing you to create any number of independent captures.</span></span>

![acquisizione sequenziale](images/capt1.png)

<span data-ttu-id="18d9f-116">Come illustrato sopra, dopo la connessione alla rete è possibile avviare e arrestare un'acquisizione il numero di volte desiderato, avviando una nuova acquisizione e generando nuove statistiche ogni volta che si riavvia l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="18d9f-116">As shown above, after you connect to the network you can start and stop a capture as many times as you wish, starting a new capture and generating new statistics every time you restart the capture.</span></span> <span data-ttu-id="18d9f-117">Ad esempio, per un'acquisizione ritardata tramite l'interfaccia [**IDelaydC**](idelaydc.md) , viene creato un nuovo [*file di acquisizione*](c.md) ogni volta che viene riavviata l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="18d9f-117">For example, for a delayed capture using the [**IDelaydC**](idelaydc.md) interface, a new [*capture file*](c.md) would be created each time you restarted the capture.</span></span>

<span data-ttu-id="18d9f-118">Tuttavia, tenere presente che ogni volta che si riavvia il processo di acquisizione è necessario chiamare il metodo Configure appropriato per riconfigurare la connessione.</span><span class="sxs-lookup"><span data-stu-id="18d9f-118">However, also be aware that every time you restart the capture process you must call the appropriate configure method to reconfigure the connection.</span></span> <span data-ttu-id="18d9f-119">Per la chiamata iniziale per avviare l'acquisizione, la connessione viene configurata dalla chiamata per connettersi alla rete.</span><span class="sxs-lookup"><span data-stu-id="18d9f-119">For the initial call to start the capture, the connection is configured by the call to connect to the network.</span></span>

<span data-ttu-id="18d9f-120">La seconda illustrazione mostra come eseguire una singola acquisizione sospendendo e riavviando.</span><span class="sxs-lookup"><span data-stu-id="18d9f-120">The second illustration shows how you could run a single capture by pausing and restarting.</span></span>

![acquisizione singola mediante sospensione e riavvio](images/capt2.png)

<span data-ttu-id="18d9f-122">In questo caso, è possibile sospendere e riavviare un'acquisizione tutte le volte che si desidera.</span><span class="sxs-lookup"><span data-stu-id="18d9f-122">In this case, you can pause and restart a capture as many times as you want.</span></span> <span data-ttu-id="18d9f-123">Con questo approccio, è possibile eseguire un'acquisizione i cui dati (e le relative statistiche) vengono registrati come una singola acquisizione.</span><span class="sxs-lookup"><span data-stu-id="18d9f-123">With this approach, you can run a capture whose data (and its related statistics) are recorded as a single capture.</span></span> <span data-ttu-id="18d9f-124">Per eseguire un'acquisizione ritardata tramite l'interfaccia [**IDelaydC**](idelaydc.md) , ad esempio, tutte le informazioni di rete acquisite vengono salvate in un unico [*file di acquisizione*](c.md).</span><span class="sxs-lookup"><span data-stu-id="18d9f-124">For example, to perform a delayed capture using the [**IDelaydC**](idelaydc.md) interface, all the captured network information would be saved in a single [*capture file*](c.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="18d9f-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="18d9f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18d9f-126">**CreateNPPInterface**</span><span class="sxs-lookup"><span data-stu-id="18d9f-126">**CreateNPPInterface**</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="18d9f-127">**IDelaydC:: Configure**</span><span class="sxs-lookup"><span data-stu-id="18d9f-127">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="18d9f-128">**IDelaydC:: Connect**</span><span class="sxs-lookup"><span data-stu-id="18d9f-128">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="18d9f-129">**IDelaydC::D la connessione**</span><span class="sxs-lookup"><span data-stu-id="18d9f-129">**IDelaydC::Disconnect**</span></span>](idelaydc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="18d9f-130">**IDelaydC::P ause**</span><span class="sxs-lookup"><span data-stu-id="18d9f-130">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="18d9f-131">**IDelaydC:: Resume**</span><span class="sxs-lookup"><span data-stu-id="18d9f-131">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="18d9f-132">**IDelaydC:: Start**</span><span class="sxs-lookup"><span data-stu-id="18d9f-132">**IDelaydC::Start**</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="18d9f-133">**IDelaydC:: Stop**</span><span class="sxs-lookup"><span data-stu-id="18d9f-133">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> <dt>

[<span data-ttu-id="18d9f-134">**IESP:: Configure**</span><span class="sxs-lookup"><span data-stu-id="18d9f-134">**IESP::Configure**</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="18d9f-135">**IESP:: Connect**</span><span class="sxs-lookup"><span data-stu-id="18d9f-135">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="18d9f-136">**IESP::D la connessione**</span><span class="sxs-lookup"><span data-stu-id="18d9f-136">**IESP::Disconnect**</span></span>](iesp-disconnect.md)
</dt> <dt>

[<span data-ttu-id="18d9f-137">**IESP::P ause**</span><span class="sxs-lookup"><span data-stu-id="18d9f-137">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="18d9f-138">**IESP:: Resume**</span><span class="sxs-lookup"><span data-stu-id="18d9f-138">**IESP::Resume**</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="18d9f-139">**IESP:: Start**</span><span class="sxs-lookup"><span data-stu-id="18d9f-139">**IESP::Start**</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="18d9f-140">**IESP:: Stop**</span><span class="sxs-lookup"><span data-stu-id="18d9f-140">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> <dt>

[<span data-ttu-id="18d9f-141">**IRTC:: Configure**</span><span class="sxs-lookup"><span data-stu-id="18d9f-141">**IRTC::Configure**</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="18d9f-142">**IRTC:: Connect**</span><span class="sxs-lookup"><span data-stu-id="18d9f-142">**IRTC::Connect**</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="18d9f-143">**IRTC::D la connessione**</span><span class="sxs-lookup"><span data-stu-id="18d9f-143">**IRTC::Disconnect**</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="18d9f-144">**IRTC::P ause**</span><span class="sxs-lookup"><span data-stu-id="18d9f-144">**IRTC::Pause**</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="18d9f-145">**IRTC:: Resume**</span><span class="sxs-lookup"><span data-stu-id="18d9f-145">**IRTC::Resume**</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="18d9f-146">**IRTC:: Start**</span><span class="sxs-lookup"><span data-stu-id="18d9f-146">**IRTC::Start**</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="18d9f-147">**IRTC:: Stop**</span><span class="sxs-lookup"><span data-stu-id="18d9f-147">**IRTC::Stop**</span></span>](irtc-stop.md)
</dt> <dt>

[<span data-ttu-id="18d9f-148">**IStats:: Configure**</span><span class="sxs-lookup"><span data-stu-id="18d9f-148">**IStats::Configure**</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="18d9f-149">**IStats:: Connect**</span><span class="sxs-lookup"><span data-stu-id="18d9f-149">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="18d9f-150">**IStats::D la connessione**</span><span class="sxs-lookup"><span data-stu-id="18d9f-150">**IStats::Disconnect**</span></span>](istats-disconnect.md)
</dt> <dt>

[<span data-ttu-id="18d9f-151">**IStats::P ause**</span><span class="sxs-lookup"><span data-stu-id="18d9f-151">**IStats::Pause**</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="18d9f-152">**IStats:: Resume**</span><span class="sxs-lookup"><span data-stu-id="18d9f-152">**IStats::Resume**</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="18d9f-153">**IStats:: Start**</span><span class="sxs-lookup"><span data-stu-id="18d9f-153">**IStats::Start**</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="18d9f-154">**IStats:: Stop**</span><span class="sxs-lookup"><span data-stu-id="18d9f-154">**IStats::Stop**</span></span>](istats-stop.md)
</dt> </dl>

 

 



