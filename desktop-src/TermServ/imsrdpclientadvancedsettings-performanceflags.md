---
title: Proprietà PerformanceFlags di IMsRdpClientAdvancedSettings
description: Specifica un set di funzionalità che è possibile impostare nel server per migliorare le prestazioni.
ms.assetid: dbbc7c13-ad8a-461d-9d2e-c454bf4b9dea
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PerformanceFlags
- Servizi Desktop remoto proprietà PerformanceFlags, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà PerformanceFlags
- Servizi Desktop remoto proprietà PerformanceFlags, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà PerformanceFlags
- Servizi Desktop remoto proprietà PerformanceFlags, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà PerformanceFlags
- Servizi Desktop remoto proprietà PerformanceFlags, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà PerformanceFlags
- Servizi Desktop remoto proprietà PerformanceFlags, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà PerformanceFlags
- Servizi Desktop remoto proprietà PerformanceFlags, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà PerformanceFlags
- Servizi Desktop remoto proprietà PerformanceFlags, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà PerformanceFlags
- Servizi Desktop remoto proprietà PerformanceFlags, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà PerformanceFlags
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PerformanceFlags
- IMsRdpClientAdvancedSettings.get_PerformanceFlags
- IMsRdpClientAdvancedSettings.put_PerformanceFlags
- IMsRdpClientAdvancedSettings2.PerformanceFlags
- IMsRdpClientAdvancedSettings2.get_PerformanceFlags
- IMsRdpClientAdvancedSettings2.put_PerformanceFlags
- IMsRdpClientAdvancedSettings3.PerformanceFlags
- IMsRdpClientAdvancedSettings3.get_PerformanceFlags
- IMsRdpClientAdvancedSettings3.put_PerformanceFlags
- IMsRdpClientAdvancedSettings4.PerformanceFlags
- IMsRdpClientAdvancedSettings4.get_PerformanceFlags
- IMsRdpClientAdvancedSettings4.put_PerformanceFlags
- IMsRdpClientAdvancedSettings5.PerformanceFlags
- IMsRdpClientAdvancedSettings5.get_PerformanceFlags
- IMsRdpClientAdvancedSettings5.put_PerformanceFlags
- IMsRdpClientAdvancedSettings6.PerformanceFlags
- IMsRdpClientAdvancedSettings6.get_PerformanceFlags
- IMsRdpClientAdvancedSettings6.put_PerformanceFlags
- IMsRdpClientAdvancedSettings7.PerformanceFlags
- IMsRdpClientAdvancedSettings7.get_PerformanceFlags
- IMsRdpClientAdvancedSettings7.put_PerformanceFlags
- IMsRdpClientAdvancedSettings8.PerformanceFlags
- IMsRdpClientAdvancedSettings8.get_PerformanceFlags
- IMsRdpClientAdvancedSettings8.put_PerformanceFlags
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1731afc6d58cede5da055da8cacaf11c8712d3c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400445"
---
# <a name="imsrdpclientadvancedsettingsperformanceflags-property"></a><span data-ttu-id="3b27a-120">IMsRdpClientAdvancedSettings::P proprietà erformanceFlags</span><span class="sxs-lookup"><span data-stu-id="3b27a-120">IMsRdpClientAdvancedSettings::PerformanceFlags property</span></span>

<span data-ttu-id="3b27a-121">Specifica un set di funzionalità che è possibile impostare nel server per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="3b27a-121">Specifies a set of features that can be set at the server to improve performance.</span></span>

<span data-ttu-id="3b27a-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3b27a-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b27a-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b27a-123">Syntax</span></span>


```C++
HRESULT put_PerformanceFlags(
  [in]  LONG DisableList = TS_PERF_DISABLE_NOTHING
);

HRESULT get_PerformanceFlags(
  [out] LONG *pDisableList
);
```



## <a name="property-value"></a><span data-ttu-id="3b27a-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3b27a-124">Property value</span></span>

<span data-ttu-id="3b27a-125">Nuovi flag.</span><span class="sxs-lookup"><span data-stu-id="3b27a-125">The new flags.</span></span> <span data-ttu-id="3b27a-126">Il valore predefinito è 0 (le **prestazioni di Servizi terminal \_ \_ \_ non sono valide**).</span><span class="sxs-lookup"><span data-stu-id="3b27a-126">The default is 0 (**TS\_PERF\_DISABLE\_NOTHING**.)</span></span>

<dt>

<span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>

<span data-ttu-id="3b27a-127"><span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>**Servizi terminal \_ \_ \_ Non disabilitare le prestazioni** (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="3b27a-127"><span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>**TS\_PERF\_DISABLE\_NOTHING** (0x00000000)</span></span>


</dt> <dd>

<span data-ttu-id="3b27a-128">Nessuna funzionalità è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="3b27a-128">No features are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>

<span data-ttu-id="3b27a-129"><span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>**Servizi terminal \_ \_ \_ Sfondo prestazioni disabilitato** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="3b27a-129"><span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>**TS\_PERF\_DISABLE\_WALLPAPER** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="3b27a-130">Lo sfondo sul desktop non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="3b27a-130">Wallpaper on the desktop is not displayed.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>

<span data-ttu-id="3b27a-131"><span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>**Servizi terminal \_ PERF \_ Disable \_ FULLWINDOWDRAG** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="3b27a-131"><span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>**TS\_PERF\_DISABLE\_FULLWINDOWDRAG** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="3b27a-132">Il trascinamento della finestra completa è disabilitato; Quando la finestra viene spostata, viene visualizzata solo la struttura della finestra.</span><span class="sxs-lookup"><span data-stu-id="3b27a-132">Full-window drag is disabled; only the window outline is displayed when the window is moved.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>

<span data-ttu-id="3b27a-133"><span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>**Servizi terminal \_ PERF \_ Disable \_ MENUANIMATIONS** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="3b27a-133"><span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>**TS\_PERF\_DISABLE\_MENUANIMATIONS** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="3b27a-134">Le animazioni dei menu sono disabilitate.</span><span class="sxs-lookup"><span data-stu-id="3b27a-134">Menu animations are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>

<span data-ttu-id="3b27a-135"><span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>**Servizi terminal \_ PERF \_ Disable \_** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="3b27a-135"><span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>**TS\_PERF\_DISABLE\_THEMING** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="3b27a-136">I temi sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="3b27a-136">Themes are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>

<span data-ttu-id="3b27a-137"><span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>**Servizi terminal \_ \_Abilitazione della \_ funzionalità grafica migliorata** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="3b27a-137"><span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>**TS\_PERF\_ENABLE\_ENHANCED GRAPHICS** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="3b27a-138">Abilita la grafica migliorata.</span><span class="sxs-lookup"><span data-stu-id="3b27a-138">Enable enhanced graphics.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>

<span data-ttu-id="3b27a-139"><span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>**Servizi terminal \_ \_Disattiva \_ \_ ombreggiatura cursore** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="3b27a-139"><span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>**TS\_PERF\_DISABLE\_CURSOR\_SHADOW** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="3b27a-140">Per il cursore non viene visualizzata alcuna ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="3b27a-140">No shadow is displayed for the cursor.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>

<span data-ttu-id="3b27a-141"><span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>**Servizi terminal \_ PERF \_ Disable \_ CURSORSETTINGS** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="3b27a-141"><span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>**TS\_PERF\_DISABLE\_CURSORSETTINGS** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="3b27a-142">Il cursore lampeggiante è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="3b27a-142">Cursor blinking is disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>

<span data-ttu-id="3b27a-143"><span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>**Servizi terminal \_ PRESTAZIONI \_ Abilita \_ \_ smussatura carattere** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="3b27a-143"><span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>**TS\_PERF\_ENABLE\_FONT\_SMOOTHING** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="3b27a-144">Abilitare la smussatura dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="3b27a-144">Enable font smoothing.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>

<span data-ttu-id="3b27a-145"><span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>**Servizi terminal \_ PERF \_ enable \_ Desktop \_ Composition** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="3b27a-145"><span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>**TS\_PERF\_ENABLE\_DESKTOP\_COMPOSITION** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="3b27a-146">Abilitare composizione desktop.</span><span class="sxs-lookup"><span data-stu-id="3b27a-146">Enable desktop composition.</span></span>

</dd> <dt>

<span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>

<span data-ttu-id="3b27a-147"><span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>**Servizi terminal \_ \_Impostazione di \_ NONPERFCLIENT \_ default Perf** (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="3b27a-147"><span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>**TS\_PERF\_DEFAULT\_NONPERFCLIENT\_SETTING** (0x40000000)</span></span>


</dt> <dd>

<span data-ttu-id="3b27a-148">Impostare internamente per i client che non sono in grado di riconoscere questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="3b27a-148">Set internally for clients not aware of this setting.</span></span>

</dd> <dt>

<span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>

<span data-ttu-id="3b27a-149"><span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>**Servizi terminal \_ PRESTAZIONI \_ RESERVED1** (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="3b27a-149"><span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>**TS\_PERF\_RESERVED1** (0x80000000)</span></span>


</dt> <dd>

<span data-ttu-id="3b27a-150">Riservato e usato internamente dal client.</span><span class="sxs-lookup"><span data-stu-id="3b27a-150">Reserved and used internally by the client.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="3b27a-151">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="3b27a-151">Error codes</span></span>

<span data-ttu-id="3b27a-152">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3b27a-152">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b27a-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b27a-153">Remarks</span></span>

<span data-ttu-id="3b27a-154">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3b27a-154">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b27a-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b27a-155">Requirements</span></span>



| <span data-ttu-id="3b27a-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b27a-156">Requirement</span></span> | <span data-ttu-id="3b27a-157">Valore</span><span class="sxs-lookup"><span data-stu-id="3b27a-157">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b27a-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b27a-158">Minimum supported client</span></span><br/> | <span data-ttu-id="3b27a-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b27a-159">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="3b27a-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b27a-160">Minimum supported server</span></span><br/> | <span data-ttu-id="3b27a-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b27a-161">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="3b27a-162">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3b27a-162">Type library</span></span><br/>             | <dl> <span data-ttu-id="3b27a-163"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b27a-163"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="3b27a-164">DLL</span><span class="sxs-lookup"><span data-stu-id="3b27a-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b27a-165"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b27a-165"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="3b27a-166">IID</span><span class="sxs-lookup"><span data-stu-id="3b27a-166">IID</span></span><br/>                      | <span data-ttu-id="3b27a-167">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="3b27a-167">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b27a-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b27a-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b27a-169">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="3b27a-169">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="3b27a-170">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="3b27a-170">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="3b27a-171">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="3b27a-171">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="3b27a-172">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="3b27a-172">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="3b27a-173">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="3b27a-173">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="3b27a-174">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="3b27a-174">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="3b27a-175">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="3b27a-175">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="3b27a-176">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="3b27a-176">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





