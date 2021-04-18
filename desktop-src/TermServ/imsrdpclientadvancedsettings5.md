---
title: Interfaccia IMsRdpClientAdvancedSettings5
description: Gestisce le impostazioni client avanzate. Deriva dall'interfaccia IMsRdpClientAdvancedSettings4.
ms.assetid: a927cd4c-7f70-493e-a4f6-056d0352d56e
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14e37eb28c1fb7a272291c44661c52ec3548708b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301632"
---
# <a name="imsrdpclientadvancedsettings5-interface"></a><span data-ttu-id="ba16f-106">Interfaccia IMsRdpClientAdvancedSettings5</span><span class="sxs-lookup"><span data-stu-id="ba16f-106">IMsRdpClientAdvancedSettings5 interface</span></span>

<span data-ttu-id="ba16f-107">Gestisce le impostazioni client avanzate.</span><span class="sxs-lookup"><span data-stu-id="ba16f-107">Manages advanced client settings.</span></span> <span data-ttu-id="ba16f-108">Deriva dall'interfaccia [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="ba16f-108">Derives from the [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span>

<span data-ttu-id="ba16f-109">Per ottenere un'istanza di questa interfaccia, usare la proprietà [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) per ottenere un puntatore a interfaccia [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="ba16f-109">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="ba16f-110">Chiamare quindi [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul puntatore **IMsTscAdvancedSettings** e passare **IID \_ IMsRdpClientAdvancedSettings5** a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="ba16f-110">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings5** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="ba16f-111">Membri</span><span class="sxs-lookup"><span data-stu-id="ba16f-111">Members</span></span>

<span data-ttu-id="ba16f-112">L'interfaccia **IMsRdpClientAdvancedSettings5** eredita da [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md).</span><span class="sxs-lookup"><span data-stu-id="ba16f-112">The **IMsRdpClientAdvancedSettings5** interface inherits from [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md).</span></span> <span data-ttu-id="ba16f-113">**IMsRdpClientAdvancedSettings5** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ba16f-113">**IMsRdpClientAdvancedSettings5** also has these types of members:</span></span>

-   [<span data-ttu-id="ba16f-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba16f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba16f-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba16f-115">Properties</span></span>

<span data-ttu-id="ba16f-116">L'interfaccia **IMsRdpClientAdvancedSettings5** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ba16f-116">The **IMsRdpClientAdvancedSettings5** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="ba16f-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba16f-117">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="ba16f-118">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="ba16f-118">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="ba16f-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba16f-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="ba16f-120"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba16f-120"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="ba16f-121">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="ba16f-121">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="ba16f-122">Modalità di reindirizzamento audio.</span><span class="sxs-lookup"><span data-stu-id="ba16f-122">The audio redirection mode.</span></span> <span data-ttu-id="ba16f-123">La proprietà <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a> presenta i valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="ba16f-123">The <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a> property has the following possible values.</span></span><br/><span data-ttu-id="ba16f-124">
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (il reindirizzamento audio è abilitato e l'opzione per il reindirizzamento viene &quot; portata a questo computer &quot; .</span><span class="sxs-lookup"><span data-stu-id="ba16f-124">
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (Audio redirection is enabled and the option for redirection is &quot;Bring to this computer&quot;.</span></span> <span data-ttu-id="ba16f-125">Questa è la modalità predefinita.</span><span class="sxs-lookup"><span data-stu-id="ba16f-125">This is the default mode.)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="ba16f-126"><dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (il reindirizzamento audio è abilitato e l'opzione viene &quot; lasciata nel computer remoto &quot; .</span><span class="sxs-lookup"><span data-stu-id="ba16f-126"><dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (Audio redirection is enabled and the option is &quot;Leave at remote computer&quot;.</span></span> <span data-ttu-id="ba16f-127">L' &quot; opzione Esci da computer remoto &quot; è supportata solo quando ci si connette in remoto a un computer host che esegue Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ba16f-127">The &quot;Leave at remote computer&quot; option is supported only when connecting remotely to a host computer that is running Windows Vista.</span></span> <span data-ttu-id="ba16f-128">Se la connessione è a un computer host che esegue Windows Server 2008, l'opzione &quot; lascia nel computer remoto &quot; è cambiata in non &quot; riprodurre &quot; .</span><span class="sxs-lookup"><span data-stu-id="ba16f-128">If the connection is to a host computer that is running Windows Server 2008, the option &quot;Leave at remote computer&quot; is changed to &quot;Do not play&quot;.)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="ba16f-129"><dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (il reindirizzamento audio è abilitato e la modalità non è disponibile &quot; &quot; ).</span><span class="sxs-lookup"><span data-stu-id="ba16f-129"><dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (Audio redirection is enabled and the mode is &quot;Do not play&quot;.)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="ba16f-130"><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba16f-130"><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="ba16f-131">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="ba16f-131">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="ba16f-132">Specifica le dimensioni del file di cache virtuale per le bitmap di 32 bit per pixel (BPP).</span><span class="sxs-lookup"><span data-stu-id="ba16f-132">Specifies the virtual cache file size for 32 bits per pixel (bpp) bitmaps.</span></span> <span data-ttu-id="ba16f-133">Il valore massimo è 48 megabyte (MB).</span><span class="sxs-lookup"><span data-stu-id="ba16f-133">The maximum value is 48 megabytes (MB).</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="ba16f-134"><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba16f-134"><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="ba16f-135">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="ba16f-135">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="ba16f-136">Specifica se il pulsante di blocco deve essere visualizzato sulla barra di connessione.</span><span class="sxs-lookup"><span data-stu-id="ba16f-136">Specifies whether the pin button should be shown on the connection bar.</span></span> <span data-ttu-id="ba16f-137">Per impostazione predefinita, il valore è <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="ba16f-137">By default, the value is <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="ba16f-138"><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>PublicMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba16f-138"><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>PublicMode</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="ba16f-139">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="ba16f-139">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="ba16f-140">Specifica se la modalità pubblica deve essere abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="ba16f-140">Specifies whether public mode should be enabled or disabled.</span></span> <span data-ttu-id="ba16f-141">Per impostazione predefinita, la modalità pubblica è impostata su <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="ba16f-141">By default, public mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="ba16f-142"><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba16f-142"><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="ba16f-143">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="ba16f-143">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="ba16f-144">Specifica se il reindirizzamento degli Appunti deve essere abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="ba16f-144">Specifies whether clipboard redirection should be enabled or disabled.</span></span> <span data-ttu-id="ba16f-145">Per impostazione predefinita, la modalità di reindirizzamento degli Appunti è impostata su <strong>true</strong> (abilitato).</span><span class="sxs-lookup"><span data-stu-id="ba16f-145">By default, clipboard redirection mode is set to <strong>TRUE</strong> (enabled).</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="ba16f-146"><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba16f-146"><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="ba16f-147">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="ba16f-147">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="ba16f-148">Specifica se i dispositivi reindirizzati devono essere abilitati o disabilitati.</span><span class="sxs-lookup"><span data-stu-id="ba16f-148">Specifies whether redirected devices should be enabled or disabled.</span></span> <span data-ttu-id="ba16f-149">Per impostazione predefinita, la modalità dispositivi reindirizzati è impostata su <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="ba16f-149">By default, redirected devices mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="ba16f-150"><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba16f-150"><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="ba16f-151">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="ba16f-151">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="ba16f-152">Specifica se i dispositivi reindirizzati punto di servizio devono essere abilitati o disabilitati.</span><span class="sxs-lookup"><span data-stu-id="ba16f-152">Specifies whether Point of Service redirected devices should be enabled or disabled.</span></span> <span data-ttu-id="ba16f-153">Per impostazione predefinita, la modalità dispositivi reindirizzati punto di servizio è impostata su <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="ba16f-153">By default, Point of Service redirected devices mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="ba16f-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba16f-154">Remarks</span></span>

<span data-ttu-id="ba16f-155">Questa interfaccia è stata estesa dalle interfacce seguenti, in cui ogni nuova interfaccia eredita tutti i metodi e le proprietà delle interfacce precedenti:</span><span class="sxs-lookup"><span data-stu-id="ba16f-155">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="ba16f-156">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ba16f-156">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="ba16f-157">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ba16f-157">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
-   [<span data-ttu-id="ba16f-158">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ba16f-158">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)

## <a name="requirements"></a><span data-ttu-id="ba16f-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba16f-159">Requirements</span></span>



| <span data-ttu-id="ba16f-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba16f-160">Requirement</span></span> | <span data-ttu-id="ba16f-161">Valore</span><span class="sxs-lookup"><span data-stu-id="ba16f-161">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba16f-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba16f-162">Minimum supported client</span></span><br/> | <span data-ttu-id="ba16f-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba16f-163">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="ba16f-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba16f-164">Minimum supported server</span></span><br/> | <span data-ttu-id="ba16f-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba16f-165">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="ba16f-166">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ba16f-166">Type library</span></span><br/>             | <dl> <span data-ttu-id="ba16f-167"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba16f-167"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ba16f-168">DLL</span><span class="sxs-lookup"><span data-stu-id="ba16f-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba16f-169"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba16f-169"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ba16f-170">IID</span><span class="sxs-lookup"><span data-stu-id="ba16f-170">IID</span></span><br/>                      | <span data-ttu-id="ba16f-171">IID \_ IMsRdpClientAdvancedSettings5 è definito come FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="ba16f-171">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba16f-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba16f-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba16f-173">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ba16f-173">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ba16f-174">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ba16f-174">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="ba16f-175">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ba16f-175">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ba16f-176">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ba16f-176">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ba16f-177">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ba16f-177">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ba16f-178">Riferimento Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="ba16f-178">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

