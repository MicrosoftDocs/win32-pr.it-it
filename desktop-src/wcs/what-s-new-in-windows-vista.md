---
title: Novità di Windows Vista
description: La versione 1,0 di gestione colori immagine (ICM) è stata distribuita in Microsoft Windows 95 e fornisce funzionalità di base per la gestione dei colori nei contesti di dispositivi Windows.
ms.assetid: 3079f84c-0d6c-4f87-a041-de86f5f7d99b
keywords:
- Windows Color System (WCS), Windows Vista
- WCS (Windows Color System), Windows Vista
- Gestione colori immagine, Windows Vista
- gestione dei colori, Windows Vista
- colori, Windows Vista
- Sistema di colori Windows (WCS), sistemi operativi
- WCS (sistema di colori Windows), sistemi operativi
- Gestione colori immagine, sistemi operativi
- gestione dei colori, sistemi operativi
- colori, sistemi operativi
- Gestione colori immagine (ICM)
- ICM (gestione colori immagine)
- Gestione dei colori di Windows Vista
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b889dd0ba3b044f0d0f158bd2364f5c3216ec39
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "106320205"
---
# <a name="whats-new-in-windows-vista"></a><span data-ttu-id="26e17-116">Novità di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26e17-116">What's New in Windows Vista</span></span>

<span data-ttu-id="26e17-117">La versione 1,0 di gestione colori immagine (ICM) è stata distribuita in Microsoft Windows 95 e fornisce funzionalità di base per la gestione dei colori nei contesti di dispositivi Windows.</span><span class="sxs-lookup"><span data-stu-id="26e17-117">Version 1.0 of Image Color Management (ICM) was delivered in Microsoft Windows 95, and provides basic color management capabilities within Windows device contexts.</span></span>

<span data-ttu-id="26e17-118">ICM versione 2,0 è stato fornito in Windows 98, Windows Millennium Edition, Windows 2000 e WindowsXP ed è stata inclusa un'ampia gamma di nuove funzioni che implementavano la gestione dei colori all'esterno dei contesti di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="26e17-118">ICM version 2.0 was delivered in Windows 98, Windows Millennium Edition, Windows 2000, and WindowsXP and included a variety of new functions that implemented color management outside of device contexts.</span></span> <span data-ttu-id="26e17-119">Queste nuove funzioni erano adatte per requisiti di gestione dei colori più complessi e davano alle applicazioni un maggiore controllo sul processo di gestione dei colori.</span><span class="sxs-lookup"><span data-stu-id="26e17-119">These new functions were suitable for more demanding color management requirements, and gave applications greater control over the color-management process.</span></span>

<span data-ttu-id="26e17-120">Con il rilascio di Windows Vista, ICM 2,0 è ora incluso in Windows Color System (WCS) 1,0, che aggiunge altre funzionalità.</span><span class="sxs-lookup"><span data-stu-id="26e17-120">With the release of Windows Vista, ICM 2.0 is now included in Windows Color System (WCS) 1.0, which adds more functionality.</span></span> <span data-ttu-id="26e17-121">Nella tabella seguente sono elencate le nuove API (Application Programming Interface) fornite in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="26e17-121">The following table lists new application programming interfaces (API) that ship in Windows Vista.</span></span>

## <a name="new-api-shipping-in-windows-vista"></a><span data-ttu-id="26e17-122">Nuove API per la distribuzione in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26e17-122">New API Shipping in Windows Vista</span></span>



<span data-ttu-id="26e17-123">Enumerazioni</span><span class="sxs-lookup"><span data-stu-id="26e17-123">Enumerations</span></span>

<span data-ttu-id="26e17-124">Nome API</span><span class="sxs-lookup"><span data-stu-id="26e17-124">API Name</span></span>

<span data-ttu-id="26e17-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26e17-125">Header</span></span>

<span data-ttu-id="26e17-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="26e17-126">Library</span></span>

[<span data-ttu-id="26e17-127">**COLORDATATYPE**</span><span class="sxs-lookup"><span data-stu-id="26e17-127">**COLORDATATYPE**</span></span>](/windows/win32/api/icm/ne-icm-colordatatype)

<span data-ttu-id="26e17-128">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-128">icm.h</span></span>

<span data-ttu-id="26e17-129">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-129">mscms.lib</span></span>

[<span data-ttu-id="26e17-130">**COLORPROFILESUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="26e17-130">**COLORPROFILESUBTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colorprofilesubtype)

<span data-ttu-id="26e17-131">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-131">icm.h</span></span>

<span data-ttu-id="26e17-132">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-132">mscms.lib</span></span>

[<span data-ttu-id="26e17-133">**COLORPROFILETYPE**</span><span class="sxs-lookup"><span data-stu-id="26e17-133">**COLORPROFILETYPE**</span></span>](/windows/win32/api/icm/ne-icm-colorprofiletype)

<span data-ttu-id="26e17-134">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-134">icm.h</span></span>

<span data-ttu-id="26e17-135">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-135">mscms.lib</span></span>

[<span data-ttu-id="26e17-136">**\_ambito di \_ gestione del profilo WCS \_**</span><span class="sxs-lookup"><span data-stu-id="26e17-136">**WCS\_PROFILE\_MANAGEMENT\_SCOPE**</span></span>](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)

<span data-ttu-id="26e17-137">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-137">icm.h</span></span>

<span data-ttu-id="26e17-138">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-138">mscms.lib</span></span>



 



<span data-ttu-id="26e17-139">Funzioni</span><span class="sxs-lookup"><span data-stu-id="26e17-139">Functions</span></span>

<span data-ttu-id="26e17-140">Nome API</span><span class="sxs-lookup"><span data-stu-id="26e17-140">API Name</span></span>

<span data-ttu-id="26e17-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26e17-141">Header</span></span>

<span data-ttu-id="26e17-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="26e17-142">Library</span></span>

[<span data-ttu-id="26e17-143">**WcsAssociateColorProfileWithDevice**</span><span class="sxs-lookup"><span data-stu-id="26e17-143">**WcsAssociateColorProfileWithDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

<span data-ttu-id="26e17-144">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-144">icm.h</span></span>

<span data-ttu-id="26e17-145">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-145">mscms.lib</span></span>

[<span data-ttu-id="26e17-146">**WcsCheckColors**</span><span class="sxs-lookup"><span data-stu-id="26e17-146">**WcsCheckColors**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

<span data-ttu-id="26e17-147">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-147">icm.h</span></span>

<span data-ttu-id="26e17-148">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-148">mscms.lib</span></span>

[<span data-ttu-id="26e17-149">**WcsCreateIccProfile**</span><span class="sxs-lookup"><span data-stu-id="26e17-149">**WcsCreateIccProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)

<span data-ttu-id="26e17-150">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-150">icm.h</span></span>

<span data-ttu-id="26e17-151">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-151">mscms.lib</span></span>

[<span data-ttu-id="26e17-152">**WcsDisassociateColorProfileFromDevice**</span><span class="sxs-lookup"><span data-stu-id="26e17-152">**WcsDisassociateColorProfileFromDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice)

<span data-ttu-id="26e17-153">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-153">icm.h</span></span>

<span data-ttu-id="26e17-154">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-154">mscms.lib</span></span>

[<span data-ttu-id="26e17-155">**WcsEnumColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="26e17-155">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)

<span data-ttu-id="26e17-156">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-156">icm.h</span></span>

<span data-ttu-id="26e17-157">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-157">mscms.lib</span></span>

[<span data-ttu-id="26e17-158">**WcsEnumColorProfilesSize**</span><span class="sxs-lookup"><span data-stu-id="26e17-158">**WcsEnumColorProfilesSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)

<span data-ttu-id="26e17-159">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-159">icm.h</span></span>

<span data-ttu-id="26e17-160">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-160">mscms.lib</span></span>

[<span data-ttu-id="26e17-161">**WcsGetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="26e17-161">**WcsGetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)

<span data-ttu-id="26e17-162">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-162">icm.h</span></span>

<span data-ttu-id="26e17-163">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-163">mscms.lib</span></span>

[<span data-ttu-id="26e17-164">**WcsGetDefaultColorProfileSize**</span><span class="sxs-lookup"><span data-stu-id="26e17-164">**WcsGetDefaultColorProfileSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize)

<span data-ttu-id="26e17-165">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-165">icm.h</span></span>

<span data-ttu-id="26e17-166">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-166">mscms.lib</span></span>

[<span data-ttu-id="26e17-167">**WcsGetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="26e17-167">**WcsGetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

<span data-ttu-id="26e17-168">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-168">icm.h</span></span>

<span data-ttu-id="26e17-169">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-169">mscms.lib</span></span>

[<span data-ttu-id="26e17-170">**WcsGetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="26e17-170">**WcsGetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

<span data-ttu-id="26e17-171">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-171">icm.h</span></span>

<span data-ttu-id="26e17-172">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-172">mscms.lib</span></span>

[<span data-ttu-id="26e17-173">**WcsOpenColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="26e17-173">**WcsOpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew)

<span data-ttu-id="26e17-174">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-174">icm.h</span></span>

<span data-ttu-id="26e17-175">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-175">mscms.lib</span></span>

[<span data-ttu-id="26e17-176">**WcsSetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="26e17-176">**WcsSetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile)

<span data-ttu-id="26e17-177">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-177">icm.h</span></span>

<span data-ttu-id="26e17-178">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-178">mscms.lib</span></span>

[<span data-ttu-id="26e17-179">**WcsSetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="26e17-179">**WcsSetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent)

<span data-ttu-id="26e17-180">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-180">icm.h</span></span>

<span data-ttu-id="26e17-181">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-181">mscms.lib</span></span>

[<span data-ttu-id="26e17-182">**WcsSetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="26e17-182">**WcsSetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)

<span data-ttu-id="26e17-183">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-183">icm.h</span></span>

<span data-ttu-id="26e17-184">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-184">mscms.lib</span></span>

[<span data-ttu-id="26e17-185">**WcsTranslateColors**</span><span class="sxs-lookup"><span data-stu-id="26e17-185">**WcsTranslateColors**</span></span>](/windows/win32/api/icm/nf-icm-wcstranslatecolors)

<span data-ttu-id="26e17-186">ICM. h</span><span class="sxs-lookup"><span data-stu-id="26e17-186">icm.h</span></span>

<span data-ttu-id="26e17-187">mscms. lib</span><span class="sxs-lookup"><span data-stu-id="26e17-187">mscms.lib</span></span>



 



<span data-ttu-id="26e17-188">Interfacce e relative funzioni</span><span class="sxs-lookup"><span data-stu-id="26e17-188">Interfaces and Their Functions</span></span>

<span data-ttu-id="26e17-189">Nome API</span><span class="sxs-lookup"><span data-stu-id="26e17-189">API Name</span></span>

<span data-ttu-id="26e17-190">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26e17-190">Header</span></span>

<span data-ttu-id="26e17-191">Libreria</span><span class="sxs-lookup"><span data-stu-id="26e17-191">Library</span></span>

[<span data-ttu-id="26e17-192">**IDeviceModelPlugin**</span><span class="sxs-lookup"><span data-stu-id="26e17-192">**IDeviceModelPlugin**</span></span>](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)

<span data-ttu-id="26e17-193">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-193">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-194">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-194">N/A</span></span>

[<span data-ttu-id="26e17-195">**IDeviceModelPlugin::ColorimetricToDeviceColors**</span><span class="sxs-lookup"><span data-stu-id="26e17-195">**IDeviceModelPlugin::ColorimetricToDeviceColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolors)

<span data-ttu-id="26e17-196">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-196">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-197">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-197">N/A</span></span>

[<span data-ttu-id="26e17-198">**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**</span><span class="sxs-lookup"><span data-stu-id="26e17-198">**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack)

<span data-ttu-id="26e17-199">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-199">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-200">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-200">N/A</span></span>

[<span data-ttu-id="26e17-201">**IDeviceModelPlugin::D eviceToColorimetricColors**</span><span class="sxs-lookup"><span data-stu-id="26e17-201">**IDeviceModelPlugin::DeviceToColorimetricColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-devicetocolorimetriccolors)

<span data-ttu-id="26e17-202">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-202">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-203">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-203">N/A</span></span>

[<span data-ttu-id="26e17-204">**IDeviceModelPlugin::GetGamutBoundaryMesh**</span><span class="sxs-lookup"><span data-stu-id="26e17-204">**IDeviceModelPlugin::GetGamutBoundaryMesh**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymesh)

<span data-ttu-id="26e17-205">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-205">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-206">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-206">N/A</span></span>

[<span data-ttu-id="26e17-207">**IDeviceModelPlugin::GetGamutBoundaryMeshSize**</span><span class="sxs-lookup"><span data-stu-id="26e17-207">**IDeviceModelPlugin::GetGamutBoundaryMeshSize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymeshsize)

<span data-ttu-id="26e17-208">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-208">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-209">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-209">N/A</span></span>

[<span data-ttu-id="26e17-210">**IDeviceModelPlugin::GetNeutralAxis**</span><span class="sxs-lookup"><span data-stu-id="26e17-210">**IDeviceModelPlugin::GetNeutralAxis**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis)

<span data-ttu-id="26e17-211">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-211">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-212">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-212">N/A</span></span>

[<span data-ttu-id="26e17-213">**IDeviceModelPlugin::GetNeutralAxisSize**</span><span class="sxs-lookup"><span data-stu-id="26e17-213">**IDeviceModelPlugin::GetNeutralAxisSize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxissize)

<span data-ttu-id="26e17-214">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-214">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-215">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-215">N/A</span></span>

[<span data-ttu-id="26e17-216">**IDeviceModelPlugin::GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="26e17-216">**IDeviceModelPlugin::GetNumChannels**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getnumchannels)

<span data-ttu-id="26e17-217">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-217">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-218">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-218">N/A</span></span>

[<span data-ttu-id="26e17-219">**IDeviceModelPlugin::GetPrimarySamples**</span><span class="sxs-lookup"><span data-stu-id="26e17-219">**IDeviceModelPlugin::GetPrimarySamples**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getprimarysamples)

<span data-ttu-id="26e17-220">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-220">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-221">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-221">N/A</span></span>

[<span data-ttu-id="26e17-222">**IDeviceModelPlugin:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="26e17-222">**IDeviceModelPlugin::Initialize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-initialize)

<span data-ttu-id="26e17-223">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-223">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-224">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-224">N/A</span></span>

[<span data-ttu-id="26e17-225">**IDeviceModelPlugin::SetTransformDeviceModelInfo**</span><span class="sxs-lookup"><span data-stu-id="26e17-225">**IDeviceModelPlugin::SetTransformDeviceModelInfo**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-settransformdevicemodelinfo)

<span data-ttu-id="26e17-226">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-226">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-227">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-227">N/A</span></span>

[<span data-ttu-id="26e17-228">**IGamutMapModelPlugin**</span><span class="sxs-lookup"><span data-stu-id="26e17-228">**IGamutMapModelPlugin**</span></span>](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-igamutmapmodelplugin)

<span data-ttu-id="26e17-229">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-229">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-230">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-230">N/A</span></span>

[<span data-ttu-id="26e17-231">**IGamutMapModelPlugin:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="26e17-231">**IGamutMapModelPlugin::Initialize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-initialize)

<span data-ttu-id="26e17-232">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-232">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-233">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-233">N/A</span></span>

[<span data-ttu-id="26e17-234">**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**</span><span class="sxs-lookup"><span data-stu-id="26e17-234">**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-sourcetodestinationappearancecolors)

<span data-ttu-id="26e17-235">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-235">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-236">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-236">N/A</span></span>



 



<span data-ttu-id="26e17-237">Strutture</span><span class="sxs-lookup"><span data-stu-id="26e17-237">Structures</span></span>

<span data-ttu-id="26e17-238">Nome API</span><span class="sxs-lookup"><span data-stu-id="26e17-238">API Name</span></span>

<span data-ttu-id="26e17-239">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26e17-239">Header</span></span>

<span data-ttu-id="26e17-240">Libreria</span><span class="sxs-lookup"><span data-stu-id="26e17-240">Library</span></span>

[<span data-ttu-id="26e17-241">**BlackInformation**</span><span class="sxs-lookup"><span data-stu-id="26e17-241">**BlackInformation**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)

<span data-ttu-id="26e17-242">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-242">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-243">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-243">N/A</span></span>

[<span data-ttu-id="26e17-244">**GamutBoundaryDescription**</span><span class="sxs-lookup"><span data-stu-id="26e17-244">**GamutBoundaryDescription**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutboundarydescription)

<span data-ttu-id="26e17-245">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-245">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-246">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-246">N/A</span></span>

[<span data-ttu-id="26e17-247">**XYZColorF**</span><span class="sxs-lookup"><span data-stu-id="26e17-247">**XYZColorF**</span></span>](https://www.bing.com/search?q=**XYZColorF**)

<span data-ttu-id="26e17-248">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-248">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-249">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-249">N/A</span></span>

[<span data-ttu-id="26e17-250">**JChColorF**</span><span class="sxs-lookup"><span data-stu-id="26e17-250">**JChColorF**</span></span>](https://www.bing.com/search?q=**JChColorF**)

<span data-ttu-id="26e17-251">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-251">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-252">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-252">N/A</span></span>

[<span data-ttu-id="26e17-253">**JabColorF**</span><span class="sxs-lookup"><span data-stu-id="26e17-253">**JabColorF**</span></span>](https://www.bing.com/search?q=**JabColorF**)

<span data-ttu-id="26e17-254">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-254">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-255">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-255">N/A</span></span>

[<span data-ttu-id="26e17-256">**GamutShell**</span><span class="sxs-lookup"><span data-stu-id="26e17-256">**GamutShell**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshell)

<span data-ttu-id="26e17-257">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-257">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-258">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-258">N/A</span></span>

[<span data-ttu-id="26e17-259">**GamutShellTriangle**</span><span class="sxs-lookup"><span data-stu-id="26e17-259">**GamutShellTriangle**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshelltriangle)

<span data-ttu-id="26e17-260">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-260">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-261">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-261">N/A</span></span>

[<span data-ttu-id="26e17-262">**PrimaryJabColors**</span><span class="sxs-lookup"><span data-stu-id="26e17-262">**PrimaryJabColors**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryjabcolors)

<span data-ttu-id="26e17-263">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-263">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-264">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-264">N/A</span></span>

[<span data-ttu-id="26e17-265">**PrimaryXYZColors**</span><span class="sxs-lookup"><span data-stu-id="26e17-265">**PrimaryXYZColors**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryxyzcolors)

<span data-ttu-id="26e17-266">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="26e17-266">WcsPlugIn.h</span></span>

<span data-ttu-id="26e17-267">N/D</span><span class="sxs-lookup"><span data-stu-id="26e17-267">N/A</span></span>



 

 

 