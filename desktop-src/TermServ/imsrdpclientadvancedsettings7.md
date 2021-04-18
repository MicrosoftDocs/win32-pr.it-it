---
title: Interfaccia IMsRdpClientAdvancedSettings7
description: Espone metodi e proprietà che gestiscono le impostazioni avanzate del controllo ActiveX.
ms.assetid: 2d6848b4-2ce6-4624-b46e-65e7daf2d0f1
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed28c5d26ecf280507ce3cce835a6d0a71fc3bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301223"
---
# <a name="imsrdpclientadvancedsettings7-interface"></a><span data-ttu-id="e2a58-105">Interfaccia IMsRdpClientAdvancedSettings7</span><span class="sxs-lookup"><span data-stu-id="e2a58-105">IMsRdpClientAdvancedSettings7 interface</span></span>

<span data-ttu-id="e2a58-106">Espone metodi e proprietà che gestiscono le impostazioni avanzate del controllo ActiveX.</span><span class="sxs-lookup"><span data-stu-id="e2a58-106">Exposes methods and properties that manage advanced settings of the ActiveX control.</span></span>

<span data-ttu-id="e2a58-107">Per ottenere un'istanza di questa interfaccia, usare la proprietà [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) per ottenere un puntatore a interfaccia [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="e2a58-107">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="e2a58-108">Chiamare quindi [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul puntatore **IMsTscAdvancedSettings** e passare **IID \_ IMsRdpClientAdvancedSettings7** a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="e2a58-108">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings7** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="e2a58-109">Membri</span><span class="sxs-lookup"><span data-stu-id="e2a58-109">Members</span></span>

<span data-ttu-id="e2a58-110">L'interfaccia **IMsRdpClientAdvancedSettings7** eredita da **IMsRdpClientAdvancedSettings6**.</span><span class="sxs-lookup"><span data-stu-id="e2a58-110">The **IMsRdpClientAdvancedSettings7** interface inherits from **IMsRdpClientAdvancedSettings6**.</span></span> <span data-ttu-id="e2a58-111">**IMsRdpClientAdvancedSettings7** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e2a58-111">**IMsRdpClientAdvancedSettings7** also has these types of members:</span></span>

-   [<span data-ttu-id="e2a58-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e2a58-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2a58-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e2a58-113">Properties</span></span>

<span data-ttu-id="e2a58-114">L'interfaccia **IMsRdpClientAdvancedSettings7** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e2a58-114">The **IMsRdpClientAdvancedSettings7** interface has these properties.</span></span>



| <span data-ttu-id="e2a58-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e2a58-115">Property</span></span>                                                                                                    | <span data-ttu-id="e2a58-116">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="e2a58-116">Access type</span></span>           | <span data-ttu-id="e2a58-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2a58-117">Description</span></span>                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2a58-118">**AudioCaptureRedirectionMode**</span><span class="sxs-lookup"><span data-stu-id="e2a58-118">**AudioCaptureRedirectionMode**</span></span>](imsrdpclientadvancedsettings7-audiocaptureredirectionmode.md)<br/> | <span data-ttu-id="e2a58-119">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e2a58-119">Read/write</span></span><br/> | <span data-ttu-id="e2a58-120">Specifica o recupera un valore che indica se il dispositivo di input audio predefinito viene reindirizzato dal client alla sessione remota.</span><span class="sxs-lookup"><span data-stu-id="e2a58-120">Specifies or retrieves a value that indicates whether the default audio input device is redirected from the client to the remote session.</span></span><br/> |
| [<span data-ttu-id="e2a58-121">**AudioQualityMode**</span><span class="sxs-lookup"><span data-stu-id="e2a58-121">**AudioQualityMode**</span></span>](imsrdpclientadvancedsettings7-audioqualitymode.md)<br/>                       | <span data-ttu-id="e2a58-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e2a58-122">Read/write</span></span><br/> | <span data-ttu-id="e2a58-123">Specifica o recupera un valore che indica l'impostazione della modalità di qualità audio per l'audio reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="e2a58-123">Specifies or retrieves a value that indicates the audio quality mode setting for redirected audio.</span></span><br/>                                        |
| [<span data-ttu-id="e2a58-124">**EnableSuperPan**</span><span class="sxs-lookup"><span data-stu-id="e2a58-124">**EnableSuperPan**</span></span>](imsrdpclientadvancedsettings7-enablesuperpan.md)<br/>                           | <span data-ttu-id="e2a58-125">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e2a58-125">Read/write</span></span><br/> | <span data-ttu-id="e2a58-126">Specifica o recupera un valore che indica se SuperPan è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="e2a58-126">Specifies or retrieves a value that indicates whether SuperPan is enabled or disabled.</span></span><br/>                                                    |
| [<span data-ttu-id="e2a58-127">**NetworkConnectionType**</span><span class="sxs-lookup"><span data-stu-id="e2a58-127">**NetworkConnectionType**</span></span>](imsrdpclientadvancedsettings7-networkconnectiontype.md)<br/>             | <span data-ttu-id="e2a58-128">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e2a58-128">Read/write</span></span><br/> | <span data-ttu-id="e2a58-129">Specifica o recupera un valore che indica il tipo di connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="e2a58-129">Specifies or retrieves a value that indicates the network connection type.</span></span><br/>                                                                |
| [<span data-ttu-id="e2a58-130">**RedirectDirectX**</span><span class="sxs-lookup"><span data-stu-id="e2a58-130">**RedirectDirectX**</span></span>](imsrdpclientadvancedsettings7-redirectdirectx.md)<br/>                         | <span data-ttu-id="e2a58-131">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e2a58-131">Read/write</span></span><br/> | <span data-ttu-id="e2a58-132">Questa proprietà non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e2a58-132">This property is not used.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="e2a58-133">**SuperPanAccelerationFactor**</span><span class="sxs-lookup"><span data-stu-id="e2a58-133">**SuperPanAccelerationFactor**</span></span>](imsrdpclientadvancedsettings7-superpanaccelerationfactor.md)<br/>   | <span data-ttu-id="e2a58-134">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e2a58-134">Read/write</span></span><br/> | <span data-ttu-id="e2a58-135">Specifica o recupera un valore che indica il fattore di accelerazione SuperPan.</span><span class="sxs-lookup"><span data-stu-id="e2a58-135">Specifies or retrieves a value that indicates the SuperPan acceleration factor.</span></span><br/>                                                           |
| [<span data-ttu-id="e2a58-136">**VideoPlaybackMode**</span><span class="sxs-lookup"><span data-stu-id="e2a58-136">**VideoPlaybackMode**</span></span>](imsrdpclientadvancedsettings7-videoplaybackmode.md)<br/>                     | <span data-ttu-id="e2a58-137">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e2a58-137">Read/write</span></span><br/> | <span data-ttu-id="e2a58-138">Specifica o recupera un valore che indica la modalità di riproduzione video.</span><span class="sxs-lookup"><span data-stu-id="e2a58-138">Specifies or retrieves a value that indicates the video playback mode.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="e2a58-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2a58-139">Requirements</span></span>



| <span data-ttu-id="e2a58-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2a58-140">Requirement</span></span> | <span data-ttu-id="e2a58-141">Valore</span><span class="sxs-lookup"><span data-stu-id="e2a58-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a58-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2a58-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e2a58-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2a58-143">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="e2a58-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2a58-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e2a58-145">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e2a58-145">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="e2a58-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e2a58-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="e2a58-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2a58-147"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e2a58-148">DLL</span><span class="sxs-lookup"><span data-stu-id="e2a58-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2a58-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2a58-149"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e2a58-150">IID</span><span class="sxs-lookup"><span data-stu-id="e2a58-150">IID</span></span><br/>                      | <span data-ttu-id="e2a58-151">IID \_ IMsRdpClientAdvancedSettings7 è definito come 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="e2a58-151">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2a58-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2a58-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a58-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e2a58-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e2a58-154">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e2a58-154">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e2a58-155">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e2a58-155">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e2a58-156">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e2a58-156">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="e2a58-157">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e2a58-157">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="e2a58-158">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e2a58-158">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e2a58-159">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e2a58-159">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

