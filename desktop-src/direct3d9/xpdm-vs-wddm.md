---
description: L'API Direct3D 9 opera sul modello di driver video (XPDM) di Windows XP o sul modello di driver di visualizzazione (WDDM) di Windows Vista, a seconda del sistema operativo installato.
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM e WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12c7d811850c953eb53c346b628363a2642dda9
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343536"
---
# <a name="xpdm-vs-wddm"></a><span data-ttu-id="4b611-103">XPDM e WDDM</span><span class="sxs-lookup"><span data-stu-id="4b611-103">XPDM vs. WDDM</span></span>

<span data-ttu-id="4b611-104">L'API Direct3D 9 opera sul modello di driver video (XPDM) di Windows XP o sul modello di driver di visualizzazione (WDDM) di Windows Vista, a seconda del sistema operativo installato.</span><span class="sxs-lookup"><span data-stu-id="4b611-104">The Direct3D 9 API operates on either the Windows XP display driver model (XPDM) or the Windows Vista display driver model (WDDM), depending on the operating system installed.</span></span> <span data-ttu-id="4b611-105">Esistono alcune differenze nel comportamento dell'API Direct3D nei due modelli di driver.</span><span class="sxs-lookup"><span data-stu-id="4b611-105">There are some differences in the way the Direct3D API behaves on the two driver models.</span></span>

-   [<span data-ttu-id="4b611-106">Desktop sicuro</span><span class="sxs-lookup"><span data-stu-id="4b611-106">Secure Desktop</span></span>](#secure-desktop)
-   [<span data-ttu-id="4b611-107">Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="4b611-107">Remote Desktop</span></span>](#remote-desktop)
-   [<span data-ttu-id="4b611-108">Servizio Windows</span><span class="sxs-lookup"><span data-stu-id="4b611-108">Windows Service</span></span>](#windows-service)
-   [<span data-ttu-id="4b611-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4b611-109">Related topics</span></span>](#related-topics)

## <a name="secure-desktop"></a><span data-ttu-id="4b611-110">Desktop sicuro</span><span class="sxs-lookup"><span data-stu-id="4b611-110">Secure Desktop</span></span>

<span data-ttu-id="4b611-111">Il desktop protetto è attivo ogni volta che si verifica una delle operazioni seguenti: l'utente blocca il desktop (Windows+L), il screen saver viene attivato (quando nessun utente è connesso) o per impostazione predefinita quando controllo dell'account utente visualizza una richiesta.</span><span class="sxs-lookup"><span data-stu-id="4b611-111">The secure desktop is active whenever any of the following occur: the user locks their desktop (Windows+L), the screen saver activates (when no user is logged in), or by default when User Account Control presents a prompt.</span></span> <span data-ttu-id="4b611-112">Quando il desktop sicuro è attivo, il dispositivo HAL non è accessibile.</span><span class="sxs-lookup"><span data-stu-id="4b611-112">When the secure desktop is active, the HAL device is not accessible.</span></span>

<span data-ttu-id="4b611-113">Differenze tra XPDM e WDDM:</span><span class="sxs-lookup"><span data-stu-id="4b611-113">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="4b611-114">Il tentativo di creare un dispositivo Direct3D9 HAL avrà esito negativo (con **D3DERR \_ NON \_ DISPONIBILE)** e qualsiasi dispositivo Direct3D 9 esistente indicherà un codice restituito del dispositivo perso in Present.</span><span class="sxs-lookup"><span data-stu-id="4b611-114">Attempting to create a Direct3D9 HAL device will fail (with **D3DERR\_NOT\_AVAILABLE**), and any existing Direct3D 9 device will indicate a lost device return code on Present.</span></span>

- <span data-ttu-id="4b611-115">Le API Direct3D9Ex e Direct3D 10 possono creare correttamente un dispositivo mentre il desktop protetto è attivo e qualsiasi chiamata a Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) o DXGI) restituirà un codice di stato che indica che il desktop non è attualmente disponibile.</span><span class="sxs-lookup"><span data-stu-id="4b611-115">Direct3D9Ex and Direct3D 10 APIs can successfully create a device while the secure desktop is active, and any calls to Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) or DXGI) will return a status code indicating the desktop is currently unavailable.</span></span>



 

## <a name="remote-desktop"></a><span data-ttu-id="4b611-116">Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="4b611-116">Remote Desktop</span></span>

<span data-ttu-id="4b611-117">Quando un desktop remoto è attivo, lo schermo viene gestito dal computer di visualizzazione con il computer di hosting che invia informazioni tramite la rete.</span><span class="sxs-lookup"><span data-stu-id="4b611-117">When a remote desktop is active, the display is handled by the viewing machine with the hosting machine sending information via the network.</span></span>

<span data-ttu-id="4b611-118">Differenze tra XPDM e WDDM:</span><span class="sxs-lookup"><span data-stu-id="4b611-118">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="4b611-119">In XPDM tutti i tentativi di creare un dispositivo Direct3D 9 in un desktop remoto avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4b611-119">On XPDM, all attempts to create a Direct3D 9 device on a remote desktop will fail.</span></span>

- <span data-ttu-id="4b611-120">In WDDM Desktop remoto supporta la creazione di un dispositivo HAL in una sessione desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="4b611-120">On WDDM, remote desktop does support creating a HAL device over a remote desktop session.</span></span>



 

## <a name="windows-service"></a><span data-ttu-id="4b611-121">Servizio Windows</span><span class="sxs-lookup"><span data-stu-id="4b611-121">Windows Service</span></span>

<span data-ttu-id="4b611-122">Un servizio Windows è un processo eseguito in background, controllato da Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="4b611-122">A Windows service is a process that runs in the background, controlled by the service-control manager (SCM).</span></span> <span data-ttu-id="4b611-123">Un servizio viene eseguito indipendentemente dal desktop attivo e pertanto ha una capacità limitata di interagire con gli utenti.</span><span class="sxs-lookup"><span data-stu-id="4b611-123">A service runs independent of the active desktop and therefore has limited ability to interact with users.</span></span>

<span data-ttu-id="4b611-124">Differenze tra XPDM e WDDM:</span><span class="sxs-lookup"><span data-stu-id="4b611-124">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="4b611-125">In WDDM, sessione 0 Isolation garantisce che un servizio non abbia accesso ad alcun desktop utente come misura di sicurezza, pertanto un dispositivo Direct3D 9 HAL non è mai disponibile da un servizio Windows.</span><span class="sxs-lookup"><span data-stu-id="4b611-125">On WDDM, Session 0 Isolation ensures that a service does not have access to any user desktop as a security measure, therefore, a Direct3D 9 HAL device is never available from a Windows service.</span></span>



 

> [!Note]  
> <span data-ttu-id="4b611-126">Non è possibile usare Direct3D 9 in un servizio Windows.</span><span class="sxs-lookup"><span data-stu-id="4b611-126">You cannot use Direct3D 9 in a Windows service.</span></span> <span data-ttu-id="4b611-127">Per altre informazioni, vedere [l'articolo del supporto tecnico Microsoft 978635.](https://support.microsoft.com/kb/978635)</span><span class="sxs-lookup"><span data-stu-id="4b611-127">For more information, see [Microsoft support article 978635](https://support.microsoft.com/kb/978635).</span></span>

 


<span data-ttu-id="4b611-128">La tabella seguente riepiloga le differenze elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="4b611-128">The following table summarizes the differences listed here.</span></span>



| <span data-ttu-id="4b611-129">Desktop sicuro</span><span class="sxs-lookup"><span data-stu-id="4b611-129">Secure Desktop</span></span> | <span data-ttu-id="4b611-130">XPDM</span><span class="sxs-lookup"><span data-stu-id="4b611-130">XPDM</span></span> | <span data-ttu-id="4b611-131">WDDM (Direct3D9)</span><span class="sxs-lookup"><span data-stu-id="4b611-131">WDDM (Direct3D9)</span></span> | <span data-ttu-id="4b611-132">WDDM(Direct3D9Ex/Direct3D10)</span><span class="sxs-lookup"><span data-stu-id="4b611-132">WDDM(Direct3D9Ex/Direct3D10)</span></span> |
|-----------------|------|------------------|------------------------------|
| <span data-ttu-id="4b611-133">NULLREF</span><span class="sxs-lookup"><span data-stu-id="4b611-133">NULLREF</span></span>         | <span data-ttu-id="4b611-134">Sì</span><span class="sxs-lookup"><span data-stu-id="4b611-134">Yes</span></span>  | <span data-ttu-id="4b611-135">Sì</span><span class="sxs-lookup"><span data-stu-id="4b611-135">Yes</span></span>              | <span data-ttu-id="4b611-136">Sì</span><span class="sxs-lookup"><span data-stu-id="4b611-136">Yes</span></span>                          |
| <span data-ttu-id="4b611-137">Hal</span><span class="sxs-lookup"><span data-stu-id="4b611-137">HAL</span></span>             | <span data-ttu-id="4b611-138">No</span><span class="sxs-lookup"><span data-stu-id="4b611-138">No</span></span>   | <span data-ttu-id="4b611-139">No</span><span class="sxs-lookup"><span data-stu-id="4b611-139">No</span></span>               | <span data-ttu-id="4b611-140">Sì</span><span class="sxs-lookup"><span data-stu-id="4b611-140">Yes</span></span>                          |
| <span data-ttu-id="4b611-141">REF</span><span class="sxs-lookup"><span data-stu-id="4b611-141">REF</span></span>             | <span data-ttu-id="4b611-142">Sì</span><span class="sxs-lookup"><span data-stu-id="4b611-142">Yes</span></span>  | <span data-ttu-id="4b611-143">Sì</span><span class="sxs-lookup"><span data-stu-id="4b611-143">Yes</span></span>              | <span data-ttu-id="4b611-144">Sì</span><span class="sxs-lookup"><span data-stu-id="4b611-144">Yes</span></span>                          |
| <span data-ttu-id="4b611-145">Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="4b611-145">Remote Desktop</span></span>  |      |                  |                              |
| <span data-ttu-id="4b611-146">NULLREF</span><span class="sxs-lookup"><span data-stu-id="4b611-146">NULLREF</span></span>         | <span data-ttu-id="4b611-147">No</span><span class="sxs-lookup"><span data-stu-id="4b611-147">No</span></span>   | <span data-ttu-id="4b611-148">Sì</span><span class="sxs-lookup"><span data-stu-id="4b611-148">Yes</span></span>              | <span data-ttu-id="4b611-149">Sì</span><span class="sxs-lookup"><span data-stu-id="4b611-149">Yes</span></span>                          |
| <span data-ttu-id="4b611-150">Hal</span><span class="sxs-lookup"><span data-stu-id="4b611-150">HAL</span></span>             | <span data-ttu-id="4b611-151">No</span><span class="sxs-lookup"><span data-stu-id="4b611-151">No</span></span>   | <span data-ttu-id="4b611-152">Sì</span><span class="sxs-lookup"><span data-stu-id="4b611-152">Yes</span></span>              | <span data-ttu-id="4b611-153">Sì</span><span class="sxs-lookup"><span data-stu-id="4b611-153">Yes</span></span>                          |
| <span data-ttu-id="4b611-154">REF</span><span class="sxs-lookup"><span data-stu-id="4b611-154">REF</span></span>             | <span data-ttu-id="4b611-155">Sì</span><span class="sxs-lookup"><span data-stu-id="4b611-155">Yes</span></span>  | <span data-ttu-id="4b611-156">Sì</span><span class="sxs-lookup"><span data-stu-id="4b611-156">Yes</span></span>              | <span data-ttu-id="4b611-157">Sì</span><span class="sxs-lookup"><span data-stu-id="4b611-157">Yes</span></span>                          |
| <span data-ttu-id="4b611-158">Servizio Windows</span><span class="sxs-lookup"><span data-stu-id="4b611-158">Windows Service</span></span> |      |                  |                              |
| <span data-ttu-id="4b611-159">NULLREF</span><span class="sxs-lookup"><span data-stu-id="4b611-159">NULLREF</span></span>         | <span data-ttu-id="4b611-160">No</span><span class="sxs-lookup"><span data-stu-id="4b611-160">No</span></span>   | <span data-ttu-id="4b611-161">No</span><span class="sxs-lookup"><span data-stu-id="4b611-161">No</span></span>               | <span data-ttu-id="4b611-162">No</span><span class="sxs-lookup"><span data-stu-id="4b611-162">No</span></span>                           |
| <span data-ttu-id="4b611-163">Hal</span><span class="sxs-lookup"><span data-stu-id="4b611-163">HAL</span></span>             | <span data-ttu-id="4b611-164">No</span><span class="sxs-lookup"><span data-stu-id="4b611-164">No</span></span>   | <span data-ttu-id="4b611-165">No</span><span class="sxs-lookup"><span data-stu-id="4b611-165">No</span></span>               | <span data-ttu-id="4b611-166">No</span><span class="sxs-lookup"><span data-stu-id="4b611-166">No</span></span>                           |
| <span data-ttu-id="4b611-167">REF</span><span class="sxs-lookup"><span data-stu-id="4b611-167">REF</span></span>             | <span data-ttu-id="4b611-168">No</span><span class="sxs-lookup"><span data-stu-id="4b611-168">No</span></span>   | <span data-ttu-id="4b611-169">No</span><span class="sxs-lookup"><span data-stu-id="4b611-169">No</span></span>               | <span data-ttu-id="4b611-170">No</span><span class="sxs-lookup"><span data-stu-id="4b611-170">No</span></span>                           |
| <span data-ttu-id="4b611-171">WARP10</span><span class="sxs-lookup"><span data-stu-id="4b611-171">WARP10</span></span>          | <span data-ttu-id="4b611-172">N/D</span><span class="sxs-lookup"><span data-stu-id="4b611-172">N/A</span></span>  | <span data-ttu-id="4b611-173">N/D</span><span class="sxs-lookup"><span data-stu-id="4b611-173">N/A</span></span>              | <span data-ttu-id="4b611-174">Sì</span><span class="sxs-lookup"><span data-stu-id="4b611-174">Yes</span></span>                          |



 

<span data-ttu-id="4b611-175">Per altre informazioni su XPDM, WDDM, Direct3D9Ex e Direct3D 10, vedere API [di grafica in Windows.](../direct3darticles/graphics-apis-in-windows-vista.md)</span><span class="sxs-lookup"><span data-stu-id="4b611-175">For more information about XPDM, WDDM, Direct3D9Ex, and Direct3D 10, see [Graphics APIs in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b611-176">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4b611-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b611-177">Dispositivi Direct3D</span><span class="sxs-lookup"><span data-stu-id="4b611-177">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
