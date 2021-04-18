---
description: L'API Direct3D 9 funziona in Windows XP Display Driver Model (XPDM) o in Windows Vista Display Driver Model (WDDM), a seconda del sistema operativo installato.
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: Confronto tra XPDM e WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccdf4bba28b53959d8e86d8928c786db3b1d0c7f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303792"
---
# <a name="xpdm-vs-wddm"></a><span data-ttu-id="0a370-103">Confronto tra XPDM e WDDM</span><span class="sxs-lookup"><span data-stu-id="0a370-103">XPDM vs. WDDM</span></span>

<span data-ttu-id="0a370-104">L'API Direct3D 9 funziona in Windows XP Display Driver Model (XPDM) o in Windows Vista Display Driver Model (WDDM), a seconda del sistema operativo installato.</span><span class="sxs-lookup"><span data-stu-id="0a370-104">The Direct3D 9 API operates on either the Windows XP display driver model (XPDM) or the Windows Vista display driver model (WDDM), depending on the operating system installed.</span></span> <span data-ttu-id="0a370-105">Esistono alcune differenze nel modo in cui l'API Direct3D si comporta sui due modelli di driver.</span><span class="sxs-lookup"><span data-stu-id="0a370-105">There are some differences in the way the Direct3D API behaves on the two driver models.</span></span>

-   [<span data-ttu-id="0a370-106">Desktop protetto</span><span class="sxs-lookup"><span data-stu-id="0a370-106">Secure Desktop</span></span>](#secure-desktop)
-   [<span data-ttu-id="0a370-107">Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="0a370-107">Remote Desktop</span></span>](#remote-desktop)
-   [<span data-ttu-id="0a370-108">Servizio Windows</span><span class="sxs-lookup"><span data-stu-id="0a370-108">Windows Service</span></span>](#windows-service)
-   [<span data-ttu-id="0a370-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a370-109">Related topics</span></span>](#related-topics)

## <a name="secure-desktop"></a><span data-ttu-id="0a370-110">Desktop protetto</span><span class="sxs-lookup"><span data-stu-id="0a370-110">Secure Desktop</span></span>

<span data-ttu-id="0a370-111">Il desktop protetto è attivo ogni volta che si verifica una delle condizioni seguenti: l'utente blocca il desktop (Windows + L), il screen saver viene attivato (quando nessun utente è connesso) o per impostazione predefinita quando il controllo dell'account utente visualizza un messaggio di richiesta.</span><span class="sxs-lookup"><span data-stu-id="0a370-111">The secure desktop is active whenever any of the following occur: the user locks their desktop (Windows+L), the screen saver activates (when no user is logged in), or by default when User Account Control presents a prompt.</span></span> <span data-ttu-id="0a370-112">Quando il desktop protetto è attivo, il dispositivo HAL non è accessibile.</span><span class="sxs-lookup"><span data-stu-id="0a370-112">When the secure desktop is active, the HAL device is not accessible.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a370-113">Differenze tra XPDM e WDDM:</span><span class="sxs-lookup"><span data-stu-id="0a370-113">Differences between XPDM and WDDM:</span></span><br/> <span data-ttu-id="0a370-114">Il tentativo di creare un dispositivo HAL Direct3D9 avrà esito negativo (con **D3DERR \_ non \_ disponibile**) e qualsiasi dispositivo Direct3D 9 esistente indicherà che è presente un codice di ritorno del dispositivo perso.</span><span class="sxs-lookup"><span data-stu-id="0a370-114">Attempting to create a Direct3D9 HAL device will fail (with **D3DERR\_NOT\_AVAILABLE**), and any existing Direct3D 9 device will indicate a lost device return code on Present.</span></span><br/> <span data-ttu-id="0a370-115">Le API Direct3D9Ex e Direct3D 10 possono creare correttamente un dispositivo mentre il desktop protetto è attivo e tutte le chiamate a presenti ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) o DXGI) restituiranno un codice di stato che indica che il desktop non è al momento disponibile.</span><span class="sxs-lookup"><span data-stu-id="0a370-115">Direct3D9Ex and Direct3D 10 APIs can successfully create a device while the secure desktop is active, and any calls to Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) or DXGI) will return a status code indicating the desktop is currently unavailable.</span></span><br/> |



 

## <a name="remote-desktop"></a><span data-ttu-id="0a370-116">Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="0a370-116">Remote Desktop</span></span>

<span data-ttu-id="0a370-117">Quando un desktop remoto è attivo, la visualizzazione viene gestita dal computer di visualizzazione con il computer di hosting che invia le informazioni tramite la rete.</span><span class="sxs-lookup"><span data-stu-id="0a370-117">When a remote desktop is active, the display is handled by the viewing machine with the hosting machine sending information via the network.</span></span>



|                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a370-118">Differenze tra XPDM e WDDM:</span><span class="sxs-lookup"><span data-stu-id="0a370-118">Differences between XPDM and WDDM:</span></span><br/> <span data-ttu-id="0a370-119">In XPDM tutti i tentativi di creare un dispositivo Direct3D 9 in un desktop remoto avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0a370-119">On XPDM, all attempts to create a Direct3D 9 device on a remote desktop will fail.</span></span><br/> <span data-ttu-id="0a370-120">In WDDM, desktop remoto supporta la creazione di un dispositivo HAL su una sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0a370-120">On WDDM, remote desktop does support creating a HAL device over a remote desktop session.</span></span><br/> |



 

## <a name="windows-service"></a><span data-ttu-id="0a370-121">Servizio Windows</span><span class="sxs-lookup"><span data-stu-id="0a370-121">Windows Service</span></span>

<span data-ttu-id="0a370-122">Un servizio Windows è un processo eseguito in background, controllato da Gestione controllo servizi (SCM).</span><span class="sxs-lookup"><span data-stu-id="0a370-122">A Windows service is a process that runs in the background, controlled by the service-control manager (SCM).</span></span> <span data-ttu-id="0a370-123">Un servizio viene eseguito indipendentemente dal desktop attivo e pertanto ha una capacità limitata di interagire con gli utenti.</span><span class="sxs-lookup"><span data-stu-id="0a370-123">A service runs independent of the active desktop and therefore has limited ability to interact with users.</span></span>



|                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a370-124">Differenze tra XPDM e WDDM:</span><span class="sxs-lookup"><span data-stu-id="0a370-124">Differences between XPDM and WDDM:</span></span><br/> <span data-ttu-id="0a370-125">In WDDM l'isolamento della sessione 0 garantisce che un servizio non disponga dell'accesso a un desktop utente come misura di sicurezza, pertanto un dispositivo Direct3D 9 HAL non sarà mai disponibile da un servizio Windows.</span><span class="sxs-lookup"><span data-stu-id="0a370-125">On WDDM, Session 0 Isolation ensures that a service does not have access to any user desktop as a security measure, therefore, a Direct3D 9 HAL device is never available from a Windows service.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="0a370-126">Non è possibile usare Direct3D 9 in un servizio Windows.</span><span class="sxs-lookup"><span data-stu-id="0a370-126">You cannot use Direct3D 9 in a Windows service.</span></span> <span data-ttu-id="0a370-127">Per ulteriori informazioni, vedere l' [articolo 978635 del supporto tecnico Microsoft](https://support.microsoft.com/kb/978635).</span><span class="sxs-lookup"><span data-stu-id="0a370-127">For more information, see [Microsoft support article 978635](https://support.microsoft.com/kb/978635).</span></span>

 


<span data-ttu-id="0a370-128">Nella tabella seguente sono riepilogate le differenze elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="0a370-128">The following table summarizes the differences listed here.</span></span>



|                 | <span data-ttu-id="0a370-129">XPDM</span><span class="sxs-lookup"><span data-stu-id="0a370-129">XPDM</span></span> | <span data-ttu-id="0a370-130">WDDM (Direct3D9)</span><span class="sxs-lookup"><span data-stu-id="0a370-130">WDDM (Direct3D9)</span></span> | <span data-ttu-id="0a370-131">WDDM (Direct3D9Ex/Direct3D10)</span><span class="sxs-lookup"><span data-stu-id="0a370-131">WDDM(Direct3D9Ex/Direct3D10)</span></span> |
|-----------------|------|------------------|------------------------------|
| <span data-ttu-id="0a370-132">Desktop protetto</span><span class="sxs-lookup"><span data-stu-id="0a370-132">Secure Desktop</span></span>  |      |                  |                              |
| <span data-ttu-id="0a370-133">NULLREF</span><span class="sxs-lookup"><span data-stu-id="0a370-133">NULLREF</span></span>         | <span data-ttu-id="0a370-134">Sì</span><span class="sxs-lookup"><span data-stu-id="0a370-134">Yes</span></span>  | <span data-ttu-id="0a370-135">Sì</span><span class="sxs-lookup"><span data-stu-id="0a370-135">Yes</span></span>              | <span data-ttu-id="0a370-136">Sì</span><span class="sxs-lookup"><span data-stu-id="0a370-136">Yes</span></span>                          |
| <span data-ttu-id="0a370-137">HAL</span><span class="sxs-lookup"><span data-stu-id="0a370-137">HAL</span></span>             | <span data-ttu-id="0a370-138">No</span><span class="sxs-lookup"><span data-stu-id="0a370-138">No</span></span>   | <span data-ttu-id="0a370-139">No</span><span class="sxs-lookup"><span data-stu-id="0a370-139">No</span></span>               | <span data-ttu-id="0a370-140">Sì</span><span class="sxs-lookup"><span data-stu-id="0a370-140">Yes</span></span>                          |
| <span data-ttu-id="0a370-141">REF</span><span class="sxs-lookup"><span data-stu-id="0a370-141">REF</span></span>             | <span data-ttu-id="0a370-142">Sì</span><span class="sxs-lookup"><span data-stu-id="0a370-142">Yes</span></span>  | <span data-ttu-id="0a370-143">Sì</span><span class="sxs-lookup"><span data-stu-id="0a370-143">Yes</span></span>              | <span data-ttu-id="0a370-144">Sì</span><span class="sxs-lookup"><span data-stu-id="0a370-144">Yes</span></span>                          |
| <span data-ttu-id="0a370-145">Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="0a370-145">Remote Desktop</span></span>  |      |                  |                              |
| <span data-ttu-id="0a370-146">NULLREF</span><span class="sxs-lookup"><span data-stu-id="0a370-146">NULLREF</span></span>         | <span data-ttu-id="0a370-147">No</span><span class="sxs-lookup"><span data-stu-id="0a370-147">No</span></span>   | <span data-ttu-id="0a370-148">Sì</span><span class="sxs-lookup"><span data-stu-id="0a370-148">Yes</span></span>              | <span data-ttu-id="0a370-149">Sì</span><span class="sxs-lookup"><span data-stu-id="0a370-149">Yes</span></span>                          |
| <span data-ttu-id="0a370-150">HAL</span><span class="sxs-lookup"><span data-stu-id="0a370-150">HAL</span></span>             | <span data-ttu-id="0a370-151">No</span><span class="sxs-lookup"><span data-stu-id="0a370-151">No</span></span>   | <span data-ttu-id="0a370-152">Sì</span><span class="sxs-lookup"><span data-stu-id="0a370-152">Yes</span></span>              | <span data-ttu-id="0a370-153">Sì</span><span class="sxs-lookup"><span data-stu-id="0a370-153">Yes</span></span>                          |
| <span data-ttu-id="0a370-154">REF</span><span class="sxs-lookup"><span data-stu-id="0a370-154">REF</span></span>             | <span data-ttu-id="0a370-155">Sì</span><span class="sxs-lookup"><span data-stu-id="0a370-155">Yes</span></span>  | <span data-ttu-id="0a370-156">Sì</span><span class="sxs-lookup"><span data-stu-id="0a370-156">Yes</span></span>              | <span data-ttu-id="0a370-157">Sì</span><span class="sxs-lookup"><span data-stu-id="0a370-157">Yes</span></span>                          |
| <span data-ttu-id="0a370-158">Servizio Windows</span><span class="sxs-lookup"><span data-stu-id="0a370-158">Windows Service</span></span> |      |                  |                              |
| <span data-ttu-id="0a370-159">NULLREF</span><span class="sxs-lookup"><span data-stu-id="0a370-159">NULLREF</span></span>         | <span data-ttu-id="0a370-160">No</span><span class="sxs-lookup"><span data-stu-id="0a370-160">No</span></span>   | <span data-ttu-id="0a370-161">No</span><span class="sxs-lookup"><span data-stu-id="0a370-161">No</span></span>               | <span data-ttu-id="0a370-162">No</span><span class="sxs-lookup"><span data-stu-id="0a370-162">No</span></span>                           |
| <span data-ttu-id="0a370-163">HAL</span><span class="sxs-lookup"><span data-stu-id="0a370-163">HAL</span></span>             | <span data-ttu-id="0a370-164">No</span><span class="sxs-lookup"><span data-stu-id="0a370-164">No</span></span>   | <span data-ttu-id="0a370-165">No</span><span class="sxs-lookup"><span data-stu-id="0a370-165">No</span></span>               | <span data-ttu-id="0a370-166">No</span><span class="sxs-lookup"><span data-stu-id="0a370-166">No</span></span>                           |
| <span data-ttu-id="0a370-167">REF</span><span class="sxs-lookup"><span data-stu-id="0a370-167">REF</span></span>             | <span data-ttu-id="0a370-168">No</span><span class="sxs-lookup"><span data-stu-id="0a370-168">No</span></span>   | <span data-ttu-id="0a370-169">No</span><span class="sxs-lookup"><span data-stu-id="0a370-169">No</span></span>               | <span data-ttu-id="0a370-170">No</span><span class="sxs-lookup"><span data-stu-id="0a370-170">No</span></span>                           |
| <span data-ttu-id="0a370-171">WARP10</span><span class="sxs-lookup"><span data-stu-id="0a370-171">WARP10</span></span>          | <span data-ttu-id="0a370-172">N/D</span><span class="sxs-lookup"><span data-stu-id="0a370-172">N/A</span></span>  | <span data-ttu-id="0a370-173">N/D</span><span class="sxs-lookup"><span data-stu-id="0a370-173">N/A</span></span>              | <span data-ttu-id="0a370-174">Sì</span><span class="sxs-lookup"><span data-stu-id="0a370-174">Yes</span></span>                          |



 

<span data-ttu-id="0a370-175">Per altre informazioni su XPDM, WDDM, Direct3D9Ex e Direct3D 10, vedere [API grafiche in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="0a370-175">For more information about XPDM, WDDM, Direct3D9Ex, and Direct3D 10, see [Graphics APIs in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a370-176">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0a370-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a370-177">Dispositivi Direct3D</span><span class="sxs-lookup"><span data-stu-id="0a370-177">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
