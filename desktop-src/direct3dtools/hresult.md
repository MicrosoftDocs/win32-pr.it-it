---
description: Valori HRESULT personalizzati per l'interfaccia di acquisizione di diagnostica della grafica.
MS-HAID: vspixengine.Hresult
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione HRESULT
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 246FA53F-FF5B-44E1-BABB-F45AE0212687
api_name:
- Hresult
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3d5419feb0acb5967132fbb804a9bbc11bfa4248
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521569"
---
# <a name="span-idvspixenginehresultspanhresult-enumeration"></a><span data-ttu-id="e9e60-103"><span id="vspixengine.hresult"></span>Enumerazione HRESULT</span><span class="sxs-lookup"><span data-stu-id="e9e60-103"><span id="vspixengine.hresult"></span>Hresult enumeration</span></span>

<span data-ttu-id="e9e60-104">Valori HRESULT personalizzati per l'interfaccia di acquisizione di diagnostica della grafica.</span><span class="sxs-lookup"><span data-stu-id="e9e60-104">Custom HRESULT values for the graphics diagnostics capture interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9e60-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9e60-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="e9e60-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="e9e60-106">Constants</span></span>

<span data-ttu-id="e9e60-107"><span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="e9e60-107"><span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX\_S\_OK**</span></span>  
<span data-ttu-id="e9e60-108">HRESULT comune che indica che l'operazione è riuscita come previsto.</span><span class="sxs-lookup"><span data-stu-id="e9e60-108">A common HRESULT which indicates that the operation succeeded as expected.</span></span>

<span data-ttu-id="e9e60-109"><span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX \_ S \_ false**</span><span class="sxs-lookup"><span data-stu-id="e9e60-109"><span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX\_S\_FALSE**</span></span>  
<span data-ttu-id="e9e60-110">HRESULT comune che indica che l'operazione ha avuto esito positivo, ma in un modo diverso rispetto a quello previsto.</span><span class="sxs-lookup"><span data-stu-id="e9e60-110">A common HRESULT which indicates that the operation succeeded, but in a different way than was expected.</span></span>

<span data-ttu-id="e9e60-111"><span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**\_file di errore pix \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="e9e60-111"><span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**PIX\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="e9e60-112">HRESULT personalizzato che non è stato trovato nel file degli errori di Echo \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e9e60-112">A custom HRESULT that echos ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="e9e60-113"><span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**errore PIX- \_ \_ ambiente non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-113"><span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**PIX\_ERROR\_BAD\_ENVIRONMENT**</span></span>  
<span data-ttu-id="e9e60-114">HRESULT personalizzato che Echos ERROR \_ male \_ Environment.</span><span class="sxs-lookup"><span data-stu-id="e9e60-114">A custom HRESULT that echos ERROR\_BAD\_ENVIRONMENT.</span></span>

<span data-ttu-id="e9e60-115"><span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**\_formato errore pix non \_ valido \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-115"><span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**PIX\_ERROR\_BAD\_FORMAT**</span></span>  
<span data-ttu-id="e9e60-116">HRESULT personalizzato che echi il formato errore non \_ valido \_ .</span><span class="sxs-lookup"><span data-stu-id="e9e60-116">A custom HRESULT that echos ERROR\_BAD\_FORMAT.</span></span>

<span data-ttu-id="e9e60-117"><span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**\_violazione della \_ condivisione degli errori di pix \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-117"><span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**PIX\_ERROR\_SHARING\_VIOLATION**</span></span>  
<span data-ttu-id="e9e60-118">HRESULT personalizzato che Echos viola la violazione della condivisione degli errori \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e9e60-118">A custom HRESULT that echos ERROR\_SHARING\_VIOLATION.</span></span>

<span data-ttu-id="e9e60-119"><span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**\_disco errore \_ pix \_ completo**</span><span class="sxs-lookup"><span data-stu-id="e9e60-119"><span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**PIX\_ERROR\_DISK\_FULL**</span></span>  
<span data-ttu-id="e9e60-120">HRESULT personalizzato che echi il disco di errore \_ \_ pieno.</span><span class="sxs-lookup"><span data-stu-id="e9e60-120">A custom HRESULT that echos ERROR\_DISK\_FULL.</span></span>

<span data-ttu-id="e9e60-121"><span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**\_ \_ altri dati sull'errore pix \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-121"><span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**PIX\_ERROR\_MORE\_DATA**</span></span>  
<span data-ttu-id="e9e60-122">HRESULT personalizzato che Echos segnala l'errore di \_ altri \_ dati.</span><span class="sxs-lookup"><span data-stu-id="e9e60-122">A custom HRESULT that echos ERROR\_MORE\_DATA.</span></span>

<span data-ttu-id="e9e60-123"><span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**\_criteri di \_ \_ debug \_ Kit \_ mancanti in Pix E mancante**</span><span class="sxs-lookup"><span data-stu-id="e9e60-123"><span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**PIX\_E\_MISSING\_DEBUG\_KITS\_POLICY**</span></span>  
<span data-ttu-id="e9e60-124">HRESULT personalizzato che indica che i criteri di debug Kit risultano mancanti.</span><span class="sxs-lookup"><span data-stu-id="e9e60-124">A custom HRESULT which indicates that the Debug Kits policy is missing.</span></span>

<span data-ttu-id="e9e60-125"><span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**\_versione pix E \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-125"><span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**PIX\_E\_INVALID\_VERSION**</span></span>  
<span data-ttu-id="e9e60-126">HRESULT personalizzato che indica che è in uso una versione non valida.</span><span class="sxs-lookup"><span data-stu-id="e9e60-126">A custom HRESULT which indicates that an invalid version is being used.</span></span>

<span data-ttu-id="e9e60-127"><span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX \_ E \_ uso di \_ DCOMP**</span><span class="sxs-lookup"><span data-stu-id="e9e60-127"><span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX\_E\_USING\_DCOMP**</span></span>  
<span data-ttu-id="e9e60-128">HRESULT personalizzato che indica che DirectComposition è in uso (l'acquisizione di DirectComposition non è supportata).</span><span class="sxs-lookup"><span data-stu-id="e9e60-128">A custom HRESULT which indicates that DirectComposition is in use (capture of DirectComposition is not supported.)</span></span>

<span data-ttu-id="e9e60-129"><span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX \_ E \_ uso di \_ DIRECTWRITE**</span><span class="sxs-lookup"><span data-stu-id="e9e60-129"><span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX\_E\_USING\_DIRECTWRITE**</span></span>  
<span data-ttu-id="e9e60-130">HRESULT personalizzato che indica che DirectWrite è in uso (l'acquisizione di DirectWrite non è supportata).</span><span class="sxs-lookup"><span data-stu-id="e9e60-130">A custom HRESULT which indicates that DirectWrite is in use (capture of DirectWrite is not supported.)</span></span>

<span data-ttu-id="e9e60-131"><span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX \_ E \_ uso di \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="e9e60-131"><span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX\_E\_USING\_D3D9**</span></span>  
<span data-ttu-id="e9e60-132">HRESULT personalizzato che indica che Direct3D9 è in uso (l'acquisizione di Direct3D9 non è supportata in Windows 10).</span><span class="sxs-lookup"><span data-stu-id="e9e60-132">A custom HRESULT which indicates that Direct3D9 is in use (capture of Direct3D9 is not supported in Windows 10.)</span></span>

<span data-ttu-id="e9e60-133"><span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**\_ \_ \_ creazione shader per pix E cant \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-133"><span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**PIX\_E\_CANT\_CREATE\_SHADER**</span></span>  
<span data-ttu-id="e9e60-134">HRESULT personalizzato che indica che non è possibile creare uno shader specificato.</span><span class="sxs-lookup"><span data-stu-id="e9e60-134">A custom HRESULT which indicates that a specified shader can't be created.</span></span>

<span data-ttu-id="e9e60-135"><span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX \_ E \_ uso di \_ D2D**</span><span class="sxs-lookup"><span data-stu-id="e9e60-135"><span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX\_E\_USING\_D2D**</span></span>  
<span data-ttu-id="e9e60-136">HRESULT personalizzato che indica che Direct2D è in uso (l'acquisizione di Direct2D non è supportata).</span><span class="sxs-lookup"><span data-stu-id="e9e60-136">A custom HRESULT which indicates that Direct2D is in use (capture of Direct2D is not supported.)</span></span>

<span data-ttu-id="e9e60-137"><span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX \_ E \_ nessun \_ frame**</span><span class="sxs-lookup"><span data-stu-id="e9e60-137"><span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX\_E\_NO\_FRAMES**</span></span>  
<span data-ttu-id="e9e60-138">HRESULT personalizzato che indica che non sono stati acquisiti frame.</span><span class="sxs-lookup"><span data-stu-id="e9e60-138">A custom HRESULT which indicates that no frames have been captured.</span></span>

<span data-ttu-id="e9e60-139"><span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX \_ E \_ Disabilita \_ Spy**</span><span class="sxs-lookup"><span data-stu-id="e9e60-139"><span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX\_E\_DISABLE\_SPY**</span></span>  

<span data-ttu-id="e9e60-140"><span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX \_ E \_ WIN8LOG \_ su \_ win7**</span><span class="sxs-lookup"><span data-stu-id="e9e60-140"><span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX\_E\_WIN8LOG\_ON\_WIN7**</span></span>  
<span data-ttu-id="e9e60-141">HRESULT personalizzato che indica che non è possibile riprodurre Windows 8 vsglog in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e9e60-141">A custom HRESULT which indicates that a Windows 8 vsglog cannot be played back on Windows 7.</span></span>

<span data-ttu-id="e9e60-142"><span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**\_traccia dello \_ shader di compilazione E \_ pix \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-142"><span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**PIX\_E\_BUILD\_SHADER\_TRACE**</span></span>  
<span data-ttu-id="e9e60-143">HRESULT personalizzato che indica che si è verificato un errore durante la compilazione della traccia dello shader.</span><span class="sxs-lookup"><span data-stu-id="e9e60-143">A custom HRESULT which indicates that there was an error building the shader trace.</span></span>

<span data-ttu-id="e9e60-144"><span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**PIX \_ E \_ Nessuna \_ \_ visualizzazione dati \_ CS**</span><span class="sxs-lookup"><span data-stu-id="e9e60-144"><span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**PIX\_E\_NO\_CS\_DATA\_VISUALIZATION**</span></span>  
<span data-ttu-id="e9e60-145">HRESULT personalizzato che indica che non è presente alcuna visualizzazione dei dati di compute shader.</span><span class="sxs-lookup"><span data-stu-id="e9e60-145">A custom HRESULT which indicates that there is no compute shader data visualization.</span></span>

<span data-ttu-id="e9e60-146"><span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**SDK non corrispondente a PIX \_ E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-146"><span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**PIX\_E\_MISMATCH\_SDK**</span></span>  
<span data-ttu-id="e9e60-147">HRESULT personalizzato che indica una mancata corrispondenza con l'SDK corrente.</span><span class="sxs-lookup"><span data-stu-id="e9e60-147">A custom HRESULT which indicates that there is a mismatch with the current SDK.</span></span>

<span data-ttu-id="e9e60-148"><span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**PIX \_ E \_ possibile \_ mancata corrispondenza dell' \_ SDK**</span><span class="sxs-lookup"><span data-stu-id="e9e60-148"><span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**PIX\_E\_POSSIBLE\_MISMATCH\_SDK**</span></span>  
<span data-ttu-id="e9e60-149">HRESULT personalizzato che indica una possibile mancata corrispondenza con l'SDK corrente.</span><span class="sxs-lookup"><span data-stu-id="e9e60-149">A custom HRESULT which indicates that there is a possible mismatch with the current SDK.</span></span>

<span data-ttu-id="e9e60-150"><span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**\_pixel non \_ rilevabile \_ E pix**</span><span class="sxs-lookup"><span data-stu-id="e9e60-150"><span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**PIX\_E\_UNDETECTABLE\_PIXEL**</span></span>  
<span data-ttu-id="e9e60-151">HRESULT personalizzato che indica la presenza di un pixel non rilevabile.</span><span class="sxs-lookup"><span data-stu-id="e9e60-151">A custom HRESULT which indicates that there is an undetectable pixel.</span></span>

<span data-ttu-id="e9e60-152"><span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**DEBUG di PIX \_ E \_ cant \_ \_ shader \_ con \_ \_ semantica di valori di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-152"><span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**PIX\_E\_CANT\_DEBUG\_SHADER\_USING\_SYSTEM\_VALUE\_SEMANTICS**</span></span>  
<span data-ttu-id="e9e60-153">HRESULT personalizzato che indica che non è possibile eseguire il debug di Sahder utilizzando la semantica di valori di sistema.</span><span class="sxs-lookup"><span data-stu-id="e9e60-153">A custom HRESULT which indicates that the sahder can't be debugged using system value semantics.</span></span>

<span data-ttu-id="e9e60-154"><span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**PIX \_ S \_ UPDATEAVAILABLE**</span><span class="sxs-lookup"><span data-stu-id="e9e60-154"><span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**PIX\_S\_UPDATEAVAILABLE**</span></span>  
<span data-ttu-id="e9e60-155">HRESULT personalizzato che indica che è disponibile un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="e9e60-155">A custom HRESULT which indicates that there is an update available.</span></span>

<span data-ttu-id="e9e60-156"><span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**\_stato DXGI pix- \_ \_ nessun \_ Reindirizzamento**</span><span class="sxs-lookup"><span data-stu-id="e9e60-156"><span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**PIX\_DXGI\_STATUS\_NO\_REDIRECTION**</span></span>  
<span data-ttu-id="e9e60-157">HRESULT personalizzato che Echos DXGI \_ non è stato \_ \_ reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="e9e60-157">A custom HRESULT that echos DXGI\_STATUS\_NO\_REDIRECTION.</span></span>

<span data-ttu-id="e9e60-158"><span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**\_stato DXGI \_ pix \_ senza \_ \_ accesso desktop**</span><span class="sxs-lookup"><span data-stu-id="e9e60-158"><span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**PIX\_DXGI\_STATUS\_NO\_DESKTOP\_ACCESS**</span></span>  
<span data-ttu-id="e9e60-159">HRESULT personalizzato che Echos DXGI \_ \_ non ha \_ \_ accesso al desktop.</span><span class="sxs-lookup"><span data-stu-id="e9e60-159">A custom HRESULT that echos DXGI\_STATUS\_NO\_DESKTOP\_ACCESS.</span></span>

<span data-ttu-id="e9e60-160"><span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**\_ \_ \_ origine VIDPN della grafica dello stato DXGI pix \_ \_ \_ in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="e9e60-160"><span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**PIX\_DXGI\_STATUS\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE**</span></span>  
<span data-ttu-id="e9e60-161">HRESULT personalizzato che Echos DXGI \_ status \_ Graphics \_ VIDPN \_ source \_ in \_ uso.</span><span class="sxs-lookup"><span data-stu-id="e9e60-161">A custom HRESULT that echos DXGI\_STATUS\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE.</span></span>

<span data-ttu-id="e9e60-162"><span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**\_ \_ modalità stato DXGI \_ pix \_ modificata**</span><span class="sxs-lookup"><span data-stu-id="e9e60-162"><span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**PIX\_DXGI\_STATUS\_MODE\_CHANGED**</span></span>  
<span data-ttu-id="e9e60-163">HRESULT personalizzato che Echos DXGI \_ status \_ mode \_ modificato.</span><span class="sxs-lookup"><span data-stu-id="e9e60-163">A custom HRESULT that echos DXGI\_STATUS\_MODE\_CHANGED.</span></span>

<span data-ttu-id="e9e60-164"><span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**\_ \_ \_ modifica della modalità di stato DXGI pix \_ \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="e9e60-164"><span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**PIX\_DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS**</span></span>  
<span data-ttu-id="e9e60-165">È stato modificato un HRESULT personalizzato che Echos DXGI \_ status \_ mode \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e9e60-165">A custom HRESULT that echos DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS.</span></span>

<span data-ttu-id="e9e60-166"><span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**\_UNOCCLUDED DXGI \_ stato \_ pix**</span><span class="sxs-lookup"><span data-stu-id="e9e60-166"><span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**PIX\_DXGI\_STATUS\_UNOCCLUDED**</span></span>  
<span data-ttu-id="e9e60-167">HRESULT personalizzato che echi DXGI \_ stato \_ UNOCCLUDED.</span><span class="sxs-lookup"><span data-stu-id="e9e60-167">A custom HRESULT that echos DXGI\_STATUS\_UNOCCLUDED.</span></span>

<span data-ttu-id="e9e60-168"><span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**il \_ progetto DDA di stato DXGI di pix \_ \_ \_ è \_ ancora \_ in linea**</span><span class="sxs-lookup"><span data-stu-id="e9e60-168"><span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**PIX\_DXGI\_STATUS\_DDA\_WAS\_STILL\_DRAWING**</span></span>  
<span data-ttu-id="e9e60-169">È ancora in uso un HRESULT personalizzato che Echos DXGI \_ status \_ DDA sta \_ \_ ancora \_ disegnando.</span><span class="sxs-lookup"><span data-stu-id="e9e60-169">A custom HRESULT that echos DXGI\_STATUS\_DDA\_WAS\_STILL\_DRAWING.</span></span>

<span data-ttu-id="e9e60-170"><span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX \_ E \_ NOTIMPL**</span><span class="sxs-lookup"><span data-stu-id="e9e60-170"><span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX\_E\_NOTIMPL**</span></span>  
<span data-ttu-id="e9e60-171">HRESULT personalizzato che Echos E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="e9e60-171">A custom HRESULT that echos E\_NOTIMPL.</span></span>

<span data-ttu-id="e9e60-172"><span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX \_ E \_ nointerface**</span><span class="sxs-lookup"><span data-stu-id="e9e60-172"><span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX\_E\_NOINTERFACE**</span></span>  
<span data-ttu-id="e9e60-173">HRESULT personalizzato che Echos E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="e9e60-173">A custom HRESULT that echos E\_NOINTERFACE.</span></span>

<span data-ttu-id="e9e60-174"><span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**\_puntatore pix E \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-174"><span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**PIX\_E\_POINTER**</span></span>  
<span data-ttu-id="e9e60-175">HRESULT personalizzato che Echos E \_ pointer.</span><span class="sxs-lookup"><span data-stu-id="e9e60-175">A custom HRESULT that echos E\_POINTER.</span></span>

<span data-ttu-id="e9e60-176"><span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**interruzione di PIX \_ E \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-176"><span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**PIX\_E\_ABORT**</span></span>  
<span data-ttu-id="e9e60-177">HRESULT personalizzato che ECHO E \_ Abort.</span><span class="sxs-lookup"><span data-stu-id="e9e60-177">A custom HRESULT that echos E\_ABORT.</span></span>

<span data-ttu-id="e9e60-178"><span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**PIX \_ E \_ Fail**</span><span class="sxs-lookup"><span data-stu-id="e9e60-178"><span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**PIX\_E\_FAIL**</span></span>  
<span data-ttu-id="e9e60-179">HRESULT personalizzato che Echos E ha \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e9e60-179">A custom HRESULT that echos E\_FAIL.</span></span>

<span data-ttu-id="e9e60-180"><span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX \_ E \_ imprevisto**</span><span class="sxs-lookup"><span data-stu-id="e9e60-180"><span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX\_E\_UNEXPECTED**</span></span>  
<span data-ttu-id="e9e60-181">HRESULT personalizzato che Echos E \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="e9e60-181">A custom HRESULT that echos E\_UNEXPECTED.</span></span>

<span data-ttu-id="e9e60-182"><span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX \_ E \_ AccessDenied**</span><span class="sxs-lookup"><span data-stu-id="e9e60-182"><span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX\_E\_ACCESSDENIED**</span></span>  
<span data-ttu-id="e9e60-183">HRESULT personalizzato che Echos E \_ AccessDenied.</span><span class="sxs-lookup"><span data-stu-id="e9e60-183">A custom HRESULT that echos E\_ACCESSDENIED.</span></span>

<span data-ttu-id="e9e60-184"><span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**\_handle pix E \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-184"><span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**PIX\_E\_HANDLE**</span></span>  
<span data-ttu-id="e9e60-185">HRESULT personalizzato che Echos E \_ gestisce.</span><span class="sxs-lookup"><span data-stu-id="e9e60-185">A custom HRESULT that echos E\_HANDLE.</span></span>

<span data-ttu-id="e9e60-186"><span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**PIX \_ E \_ OutOfMemory**</span><span class="sxs-lookup"><span data-stu-id="e9e60-186"><span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**PIX\_E\_OUTOFMEMORY**</span></span>  
<span data-ttu-id="e9e60-187">HRESULT personalizzato che Echos E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="e9e60-187">A custom HRESULT that echos E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="e9e60-188"><span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX \_ E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="e9e60-188"><span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX\_E\_INVALIDARG**</span></span>  
<span data-ttu-id="e9e60-189">HRESULT personalizzato che Echos E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="e9e60-189">A custom HRESULT that echos E\_INVALIDARG.</span></span>

<span data-ttu-id="e9e60-190"><span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**\_ \_ disco errori Xbox \_ pix \_ completo**</span><span class="sxs-lookup"><span data-stu-id="e9e60-190"><span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**PIX\_XBOX\_ERROR\_DISK\_FULL**</span></span>  
<span data-ttu-id="e9e60-191">HRESULT personalizzato che indica che il disco è pieno.</span><span class="sxs-lookup"><span data-stu-id="e9e60-191">A custom HRESULT which indicates that the disk is full.</span></span>

<span data-ttu-id="e9e60-192"><span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**\_ \_ indirizzo di posta elettronica pix \_ \_ in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="e9e60-192"><span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**PIX\_WS\_E\_ADDRESS\_IN\_USE**</span></span>  
<span data-ttu-id="e9e60-193">HRESULT personalizzato che indica che l'indirizzo è già in uso.</span><span class="sxs-lookup"><span data-stu-id="e9e60-193">A custom HRESULT which indicates that the address is already in use.</span></span>

<span data-ttu-id="e9e60-194"><span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**\_criteri dei \_ \_ Kit mancanti \_ \_ per pix WS E**</span><span class="sxs-lookup"><span data-stu-id="e9e60-194"><span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**PIX\_WS\_E\_MISSING\_KITS\_POLICY**</span></span>  
<span data-ttu-id="e9e60-195">HRESULT personalizzato che indica che l'indirizzo non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="e9e60-195">A custom HRESULT which indicates that the address is not available.</span></span>

<span data-ttu-id="e9e60-196"><span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**PIX \_ te \_ FAILEDTOLOADSOFTWAREMODULE**</span><span class="sxs-lookup"><span data-stu-id="e9e60-196"><span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**PIX\_TE\_FAILEDTOLOADSOFTWAREMODULE**</span></span>  
<span data-ttu-id="e9e60-197">HRESULT personalizzato che indica che non è stato possibile caricare un modulo software necessario.</span><span class="sxs-lookup"><span data-stu-id="e9e60-197">A custom HRESULT which indicates that a necessary software module failed to load.</span></span>

<span data-ttu-id="e9e60-198"><span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**PIX \_ te \_ USEDSOFTWAREMODULETHATWASNTWARPORREF**</span><span class="sxs-lookup"><span data-stu-id="e9e60-198"><span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**PIX\_TE\_USEDSOFTWAREMODULETHATWASNTWARPORREF**</span></span>  
<span data-ttu-id="e9e60-199">HRESULT personalizzato che indica che il modulo software utilizzato non è il driver WARP o REF.</span><span class="sxs-lookup"><span data-stu-id="e9e60-199">A custom HRESULT which indicates that the used software module was not the WARP or REF driver.</span></span>

<span data-ttu-id="e9e60-200"><span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**PIX \_ te \_ CORRUPTEDFILE**</span><span class="sxs-lookup"><span data-stu-id="e9e60-200"><span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**PIX\_TE\_CORRUPTEDFILE**</span></span>  
<span data-ttu-id="e9e60-201">HRESULT personalizzato che indica che il file è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="e9e60-201">A custom HRESULT which indicates that the file is corrupted.</span></span>

<span data-ttu-id="e9e60-202"><span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**PIX \_ te \_ FAILEDTOOPENFILE**</span><span class="sxs-lookup"><span data-stu-id="e9e60-202"><span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**PIX\_TE\_FAILEDTOOPENFILE**</span></span>  
<span data-ttu-id="e9e60-203">HRESULT personalizzato che indica che non è stato possibile aprire il file.</span><span class="sxs-lookup"><span data-stu-id="e9e60-203">A custom HRESULT which indicates that the file failed to open.</span></span>

<span data-ttu-id="e9e60-204"><span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**PIX \_ te \_ CALLFAILEDONPLAYBACK**</span><span class="sxs-lookup"><span data-stu-id="e9e60-204"><span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**PIX\_TE\_CALLFAILEDONPLAYBACK**</span></span>  
<span data-ttu-id="e9e60-205">HRESULT personalizzato che indica che una chiamata non è riuscita durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="e9e60-205">A custom HRESULT which indicates that a call failed during playback.</span></span>

<span data-ttu-id="e9e60-206"><span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**PIX \_ te \_ UNKNOWNUUID**</span><span class="sxs-lookup"><span data-stu-id="e9e60-206"><span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**PIX\_TE\_UNKNOWNUUID**</span></span>  
<span data-ttu-id="e9e60-207">HRESULT personalizzato che indica che è stato rilevato un UUID sconosciuto; Questa operazione non dovrebbe mai verificarsi.</span><span class="sxs-lookup"><span data-stu-id="e9e60-207">A custom HRESULT which indicates that an unknown UUID was encountered; this should never occur.</span></span>

<span data-ttu-id="e9e60-208"><span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**PIX \_ te \_ NOTCAPTUREFILEORCORRUPTED**</span><span class="sxs-lookup"><span data-stu-id="e9e60-208"><span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**PIX\_TE\_NOTCAPTUREFILEORCORRUPTED**</span></span>  
<span data-ttu-id="e9e60-209">HRESULT personalizzato che indica che il file non è un file di acquisizione o è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="e9e60-209">A custom HRESULT which indicates that the file is not a capture file or is corrupted.</span></span>

<span data-ttu-id="e9e60-210"><span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX \_ te \_ NEWERFILE**</span><span class="sxs-lookup"><span data-stu-id="e9e60-210"><span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX\_TE\_NEWERFILE**</span></span>  

<span data-ttu-id="e9e60-211"><span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**PIX \_ te \_ OLDERFILE**</span><span class="sxs-lookup"><span data-stu-id="e9e60-211"><span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**PIX\_TE\_OLDERFILE**</span></span>  

<span data-ttu-id="e9e60-212"><span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**PIX \_ te \_ INVALIDMOMENT**</span><span class="sxs-lookup"><span data-stu-id="e9e60-212"><span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**PIX\_TE\_INVALIDMOMENT**</span></span>  

<span data-ttu-id="e9e60-213"><span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**\_driver di te non \_ valido \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-213"><span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**PIX\_TE\_BAD\_DRIVER**</span></span>  
<span data-ttu-id="e9e60-214">HRESULT personalizzato che indica che il driver non è valido.</span><span class="sxs-lookup"><span data-stu-id="e9e60-214">A custom HRESULT which indicates that the driver is bad.</span></span>

<span data-ttu-id="e9e60-215"><span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**\_errore \_ di accesso non è \_ possibile accedere \_ \_ a DEPTHSTENCIL nella \_ CPU**</span><span class="sxs-lookup"><span data-stu-id="e9e60-215"><span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**PIX\_ERROR\_CANT\_ACCESS\_DEPTHSTENCIL\_IN\_CPU**</span></span>  
<span data-ttu-id="e9e60-216">HRESULT personalizzato che indica che la CPU ha tentato di accedere al buffer di stencil Depth, causando un errore.</span><span class="sxs-lookup"><span data-stu-id="e9e60-216">A custom HRESULT which indicates that the CPU attempted to access the depth-stencil buffer, resulting in an error.</span></span>

<span data-ttu-id="e9e60-217"><span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**\_errore pix \_ risoluzione \_ della \_ trama multicampionata \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-217"><span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**PIX\_ERROR\_CANT\_RESOLVE\_MULTISAMPLED\_TEXTURE**</span></span>  
<span data-ttu-id="e9e60-218">HRESULT personalizzato che indica che si è verificato un tentativo di risolvere una trama multicampionata, causando un errore.</span><span class="sxs-lookup"><span data-stu-id="e9e60-218">A custom HRESULT which indicates that there was an attempt to resolve a multi-sampled texture, resulting in an error.</span></span>

<span data-ttu-id="e9e60-219"><span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**\_chiamata di \_ errore DXGI pix \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-219"><span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**PIX\_DXGI\_ERROR\_INVALID\_CALL**</span></span>  
<span data-ttu-id="e9e60-220">HRESULT personalizzato che Echos DXGI \_ errore \_ chiamata non valida \_ .</span><span class="sxs-lookup"><span data-stu-id="e9e60-220">A custom HRESULT that echos DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="e9e60-221"><span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**\_errore DXGI \_ pix \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="e9e60-221"><span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**PIX\_DXGI\_ERROR\_NOT\_FOUND**</span></span>  
<span data-ttu-id="e9e60-222">Errore HRESULT personalizzato che Echos DXGI non è stato \_ \_ \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="e9e60-222">A custom HRESULT that echos DXGI\_ERROR\_NOT\_FOUND.</span></span>

<span data-ttu-id="e9e60-223"><span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**\_ \_ \_ altri dati sull'errore DXGI pix \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-223"><span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**PIX\_DXGI\_ERROR\_MORE\_DATA**</span></span>  
<span data-ttu-id="e9e60-224">HRESULT personalizzato che Echos DXGI \_ \_ più \_ dati.</span><span class="sxs-lookup"><span data-stu-id="e9e60-224">A custom HRESULT that echos DXGI\_ERROR\_MORE\_DATA.</span></span>

<span data-ttu-id="e9e60-225"><span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**\_errore DXGI pix non \_ \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="e9e60-225"><span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**PIX\_DXGI\_ERROR\_UNSUPPORTED**</span></span>  
<span data-ttu-id="e9e60-226">HRESULT personalizzato che Echos DXGI \_ Error non è \_ supportato.</span><span class="sxs-lookup"><span data-stu-id="e9e60-226">A custom HRESULT that echos DXGI\_ERROR\_UNSUPPORTED.</span></span>

<span data-ttu-id="e9e60-227"><span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**\_dispositivo di \_ errore DXGI pix \_ \_ rimosso**</span><span class="sxs-lookup"><span data-stu-id="e9e60-227"><span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**PIX\_DXGI\_ERROR\_DEVICE\_REMOVED**</span></span>  
<span data-ttu-id="e9e60-228">HRESULT personalizzato che Echos DXGI \_ Error \_ Device \_ removed.</span><span class="sxs-lookup"><span data-stu-id="e9e60-228">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_REMOVED.</span></span>

<span data-ttu-id="e9e60-229"><span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**\_dispositivo di \_ errore DXGI pix \_ \_ bloccato**</span><span class="sxs-lookup"><span data-stu-id="e9e60-229"><span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**PIX\_DXGI\_ERROR\_DEVICE\_HUNG**</span></span>  
<span data-ttu-id="e9e60-230">HRESULT personalizzato che Echos DXGI \_ Error \_ Device è \_ bloccato.</span><span class="sxs-lookup"><span data-stu-id="e9e60-230">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_HUNG.</span></span>

<span data-ttu-id="e9e60-231"><span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**\_ripristino del \_ dispositivo con errore DXGI \_ pix \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-231"><span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**PIX\_DXGI\_ERROR\_DEVICE\_RESET**</span></span>  
<span data-ttu-id="e9e60-232">HRESULT personalizzato che Echos DXGI \_ Error \_ Reset del dispositivo \_ .</span><span class="sxs-lookup"><span data-stu-id="e9e60-232">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_RESET.</span></span>

<span data-ttu-id="e9e60-233"><span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**il \_ disegno dell'errore DXGI pix \_ \_ è \_ ancora \_ in linea**</span><span class="sxs-lookup"><span data-stu-id="e9e60-233"><span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**PIX\_DXGI\_ERROR\_WAS\_STILL\_DRAWING**</span></span>  
<span data-ttu-id="e9e60-234">Un HRESULT personalizzato che \_ \_ è ancora stato disegnato dall'errore Echos DXGI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e9e60-234">A custom HRESULT that echos DXGI\_ERROR\_WAS\_STILL\_DRAWING.</span></span>

<span data-ttu-id="e9e60-235"><span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**\_statistiche del frame di errore pix DXGI non \_ \_ \_ \_ contigue**</span><span class="sxs-lookup"><span data-stu-id="e9e60-235"><span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**PIX\_DXGI\_ERROR\_FRAME\_STATISTICS\_DISJOINT**</span></span>  
<span data-ttu-id="e9e60-236">HRESULT personalizzato che Echos DXGI \_ Error \_ frame \_ STATISTICs \_ disgiunto.</span><span class="sxs-lookup"><span data-stu-id="e9e60-236">A custom HRESULT that echos DXGI\_ERROR\_FRAME\_STATISTICS\_DISJOINT.</span></span>

<span data-ttu-id="e9e60-237"><span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**\_ \_ \_ \_ origine VIDPN della grafica dell'errore pix DXGI \_ \_ in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="e9e60-237"><span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**PIX\_DXGI\_ERROR\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE**</span></span>  
<span data-ttu-id="e9e60-238">HRESULT personalizzato che Echos DXGI \_ \_ Graphics Error \_ VIDPN \_ source \_ in \_ uso.</span><span class="sxs-lookup"><span data-stu-id="e9e60-238">A custom HRESULT that echos DXGI\_ERROR\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE.</span></span>

<span data-ttu-id="e9e60-239"><span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**\_ \_ \_ errore interno del driver di errore \_ pix DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-239"><span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**PIX\_DXGI\_ERROR\_DRIVER\_INTERNAL\_ERROR**</span></span>  
<span data-ttu-id="e9e60-240">HRESULT personalizzato che Echos DXGI \_ errore \_ interno del driver \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e9e60-240">A custom HRESULT that echos DXGI\_ERROR\_DRIVER\_INTERNAL\_ERROR.</span></span>

<span data-ttu-id="e9e60-241"><span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**\_errore DXGI pix non \_ \_ esclusivo**</span><span class="sxs-lookup"><span data-stu-id="e9e60-241"><span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**PIX\_DXGI\_ERROR\_NONEXCLUSIVE**</span></span>  
<span data-ttu-id="e9e60-242">HRESULT personalizzato che Echos DXGI \_ errore non \_ esclusivo.</span><span class="sxs-lookup"><span data-stu-id="e9e60-242">A custom HRESULT that echos DXGI\_ERROR\_NONEXCLUSIVE.</span></span>

<span data-ttu-id="e9e60-243"><span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**\_errore DXGI \_ pix \_ non \_ attualmente \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="e9e60-243"><span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**PIX\_DXGI\_ERROR\_NOT\_CURRENTLY\_AVAILABLE**</span></span>  
<span data-ttu-id="e9e60-244">HRESULT personalizzato che Echos DXGI \_ Error \_ non è \_ attualmente \_ disponibile.</span><span class="sxs-lookup"><span data-stu-id="e9e60-244">A custom HRESULT that echos DXGI\_ERROR\_NOT\_CURRENTLY\_AVAILABLE.</span></span>

<span data-ttu-id="e9e60-245"><span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**\_errore di DXGI pix \_ \_ \_ client remoto \_ scollegato**</span><span class="sxs-lookup"><span data-stu-id="e9e60-245"><span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**PIX\_DXGI\_ERROR\_REMOTE\_CLIENT\_DISCONNECTED**</span></span>  
<span data-ttu-id="e9e60-246">HRESULT personalizzato che Echos DXGI \_ Error \_ Remote \_ client \_ disconnesso.</span><span class="sxs-lookup"><span data-stu-id="e9e60-246">A custom HRESULT that echos DXGI\_ERROR\_REMOTE\_CLIENT\_DISCONNECTED.</span></span>

<span data-ttu-id="e9e60-247"><span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**\_OutOfMemory DXGI \_ \_ remoto errore \_ pix**</span><span class="sxs-lookup"><span data-stu-id="e9e60-247"><span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**PIX\_DXGI\_ERROR\_REMOTE\_OUTOFMEMORY**</span></span>  
<span data-ttu-id="e9e60-248">HRESULT personalizzato che Echos DXGI \_ \_ Remote Error \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="e9e60-248">A custom HRESULT that echos DXGI\_ERROR\_REMOTE\_OUTOFMEMORY.</span></span>

<span data-ttu-id="e9e60-249"><span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**\_ \_ \_ modifica della modalità di errore DXGI pix \_ \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="e9e60-249"><span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**PIX\_DXGI\_ERROR\_MODE\_CHANGE\_IN\_PROGRESS**</span></span>  
<span data-ttu-id="e9e60-250">HRESULT personalizzato che Echos DXGI \_ Error \_ mode \_ modifica \_ in \_ corso.</span><span class="sxs-lookup"><span data-stu-id="e9e60-250">A custom HRESULT that echos DXGI\_ERROR\_MODE\_CHANGE\_IN\_PROGRESS.</span></span>

<span data-ttu-id="e9e60-251"><span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**\_ \_ accesso agli errori di DXGI pix \_ \_ perso**</span><span class="sxs-lookup"><span data-stu-id="e9e60-251"><span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**PIX\_DXGI\_ERROR\_ACCESS\_LOST**</span></span>  
<span data-ttu-id="e9e60-252">Un HRESULT personalizzato che Echos \_ DXGI \_ l'accesso A errori \_ persi.</span><span class="sxs-lookup"><span data-stu-id="e9e60-252">A custom HRESULT that echos DXGI\_ERROR\_ACCESS\_LOST.</span></span>

<span data-ttu-id="e9e60-253"><span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**\_timeout di \_ \_ attesa errore DXGI pix \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-253"><span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**PIX\_DXGI\_ERROR\_WAIT\_TIMEOUT**</span></span>  
<span data-ttu-id="e9e60-254">HRESULT personalizzato che Echos DXGI \_ errore \_ di \_ timeout di attesa.</span><span class="sxs-lookup"><span data-stu-id="e9e60-254">A custom HRESULT that echos DXGI\_ERROR\_WAIT\_TIMEOUT.</span></span>

<span data-ttu-id="e9e60-255"><span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**\_sessione di \_ errore DXGI pix \_ \_ disconnessa**</span><span class="sxs-lookup"><span data-stu-id="e9e60-255"><span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**PIX\_DXGI\_ERROR\_SESSION\_DISCONNECTED**</span></span>  
<span data-ttu-id="e9e60-256">HRESULT personalizzato che Echos DXGI \_ Error \_ Session \_ disconnected.</span><span class="sxs-lookup"><span data-stu-id="e9e60-256">A custom HRESULT that echos DXGI\_ERROR\_SESSION\_DISCONNECTED.</span></span>

<span data-ttu-id="e9e60-257"><span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**l' \_ errore DXGI di pix viene limitato \_ \_ \_ a \_ output non \_ aggiornato**</span><span class="sxs-lookup"><span data-stu-id="e9e60-257"><span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**PIX\_DXGI\_ERROR\_RESTRICT\_TO\_OUTPUT\_STALE**</span></span>  
<span data-ttu-id="e9e60-258">Un HRESULT personalizzato che Echos DXGI \_ errore \_ limita l'output non \_ \_ \_ aggiornato.</span><span class="sxs-lookup"><span data-stu-id="e9e60-258">A custom HRESULT that echos DXGI\_ERROR\_RESTRICT\_TO\_OUTPUT\_STALE.</span></span>

<span data-ttu-id="e9e60-259"><span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**\_errore DXGI \_ pix \_ non in grado di \_ proteggere il \_ contenuto**</span><span class="sxs-lookup"><span data-stu-id="e9e60-259"><span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**PIX\_DXGI\_ERROR\_CANNOT\_PROTECT\_CONTENT**</span></span>  
<span data-ttu-id="e9e60-260">Un HRESULT personalizzato che Echos DXGI \_ Error \_ non può \_ proteggere il \_ contenuto.</span><span class="sxs-lookup"><span data-stu-id="e9e60-260">A custom HRESULT that echos DXGI\_ERROR\_CANNOT\_PROTECT\_CONTENT.</span></span>

<span data-ttu-id="e9e60-261"><span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**\_ \_ accesso agli errori di DXGI pix \_ \_ negato**</span><span class="sxs-lookup"><span data-stu-id="e9e60-261"><span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**PIX\_DXGI\_ERROR\_ACCESS\_DENIED**</span></span>  
<span data-ttu-id="e9e60-262">HRESULT personalizzato che Echos DXGI \_ ha \_ negato l'accesso \_ .</span><span class="sxs-lookup"><span data-stu-id="e9e60-262">A custom HRESULT that echos DXGI\_ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="e9e60-263"><span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**il \_ nome dell'errore DXGI pix \_ \_ \_ \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="e9e60-263"><span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**PIX\_DXGI\_ERROR\_NAME\_ALREADY\_EXISTS**</span></span>  
<span data-ttu-id="e9e60-264">Un HRESULT personalizzato che ha un nome di errore Echos DXGI \_ \_ \_ \_ esiste già.</span><span class="sxs-lookup"><span data-stu-id="e9e60-264">A custom HRESULT that echos DXGI\_ERROR\_NAME\_ALREADY\_EXISTS.</span></span>

<span data-ttu-id="e9e60-265"><span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**\_ \_ componente SDK per errori DXGI pix \_ \_ \_ mancante**</span><span class="sxs-lookup"><span data-stu-id="e9e60-265"><span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**PIX\_DXGI\_ERROR\_SDK\_COMPONENT\_MISSING**</span></span>  
<span data-ttu-id="e9e60-266">HRESULT personalizzato che Echos DXGI \_ Error \_ SDK \_ Component \_ mancante.</span><span class="sxs-lookup"><span data-stu-id="e9e60-266">A custom HRESULT that echos DXGI\_ERROR\_SDK\_COMPONENT\_MISSING.</span></span>

<span data-ttu-id="e9e60-267"><span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**\_WASSTILLDRAWING di \_ \_ errore DDI DXGI pix \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-267"><span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**PIX\_DXGI\_DDI\_ERR\_WASSTILLDRAWING**</span></span>  
<span data-ttu-id="e9e60-268">HRESULT personalizzato che Echos DXGI \_ DDI \_ \_ WASSTILLDRAWING Err.</span><span class="sxs-lookup"><span data-stu-id="e9e60-268">A custom HRESULT that echos DXGI\_DDI\_ERR\_WASSTILLDRAWING.</span></span>

<span data-ttu-id="e9e60-269"><span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**\_errore DDI DXGI di pix non \_ \_ \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="e9e60-269"><span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**PIX\_DXGI\_DDI\_ERR\_UNSUPPORTED**</span></span>  
<span data-ttu-id="e9e60-270">HRESULT personalizzato che Echos DXGI \_ DDI \_ Err non è \_ supportato.</span><span class="sxs-lookup"><span data-stu-id="e9e60-270">A custom HRESULT that echos DXGI\_DDI\_ERR\_UNSUPPORTED.</span></span>

<span data-ttu-id="e9e60-271"><span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**\_DXGI DDI di pix \_ Err non \_ \_ esclusivo**</span><span class="sxs-lookup"><span data-stu-id="e9e60-271"><span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**PIX\_DXGI\_DDI\_ERR\_NONEXCLUSIVE**</span></span>  
<span data-ttu-id="e9e60-272">HRESULT personalizzato che Echos DXGI \_ DDI \_ Err non è \_ esclusivo.</span><span class="sxs-lookup"><span data-stu-id="e9e60-272">A custom HRESULT that echos DXGI\_DDI\_ERR\_NONEXCLUSIVE.</span></span>

<span data-ttu-id="e9e60-273"><span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**\_Errore D3D10 \_ pix \_ troppi \_ \_ \_ oggetti stato \_ univoco**</span><span class="sxs-lookup"><span data-stu-id="e9e60-273"><span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**PIX\_D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS**</span></span>  
<span data-ttu-id="e9e60-274">HRESULT personalizzato che Echos D3D10 \_ errore di \_ troppi \_ oggetti di \_ \_ stato univoco \_ .</span><span class="sxs-lookup"><span data-stu-id="e9e60-274">A custom HRESULT that echos D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS.</span></span>

<span data-ttu-id="e9e60-275"><span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**\_File di \_ errore D3D10 pix \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="e9e60-275"><span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**PIX\_D3D10\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="e9e60-276">HRESULT personalizzato che Echos D3D10 \_ Error \_ file \_ non \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="e9e60-276">A custom HRESULT that echos D3D10\_ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="e9e60-277"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**\_Errore d3d11 \_ pix \_ troppi \_ \_ \_ oggetti stato \_ univoco**</span><span class="sxs-lookup"><span data-stu-id="e9e60-277"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**PIX\_D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS**</span></span>  
<span data-ttu-id="e9e60-278">HRESULT personalizzato che Echos D3D11 \_ errore di \_ troppi \_ oggetti di \_ \_ stato univoco \_ .</span><span class="sxs-lookup"><span data-stu-id="e9e60-278">A custom HRESULT that echos D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS.</span></span>

<span data-ttu-id="e9e60-279"><span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**\_File di \_ errore d3d11 pix \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="e9e60-279"><span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**PIX\_D3D11\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="e9e60-280">HRESULT personalizzato che Echos D3D11 \_ Error \_ file \_ non \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="e9e60-280">A custom HRESULT that echos D3D11\_ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="e9e60-281"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**\_Errore d3d11 \_ pix \_ troppi \_ \_ \_ oggetti visualizzazione \_ univoca**</span><span class="sxs-lookup"><span data-stu-id="e9e60-281"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**PIX\_D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_VIEW\_OBJECTS**</span></span>  
<span data-ttu-id="e9e60-282">HRESULT personalizzato che Echos D3D11 \_ errore di \_ troppi \_ \_ \_ oggetti visualizzazione univoca \_ .</span><span class="sxs-lookup"><span data-stu-id="e9e60-282">A custom HRESULT that echos D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_VIEW\_OBJECTS.</span></span>

<span data-ttu-id="e9e60-283"><span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**\_Mappa del \_ contesto posticipato dell'errore d3d11 di pix \_ \_ \_ \_ senza \_ \_ eliminazione iniziale**</span><span class="sxs-lookup"><span data-stu-id="e9e60-283"><span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**PIX\_D3D11\_ERROR\_DEFERRED\_CONTEXT\_MAP\_WITHOUT\_INITIAL\_DISCARD**</span></span>  
<span data-ttu-id="e9e60-284">HRESULT personalizzato che Echos D3D11 \_ errore \_ posticipato della \_ mappa del contesto \_ \_ senza \_ \_ eliminazione iniziale.</span><span class="sxs-lookup"><span data-stu-id="e9e60-284">A custom HRESULT that echos D3D11\_ERROR\_DEFERRED\_CONTEXT\_MAP\_WITHOUT\_INITIAL\_DISCARD.</span></span>

<span data-ttu-id="e9e60-285"><span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**\_chiamata di \_ \_ estrazione con errore pix \_**</span><span class="sxs-lookup"><span data-stu-id="e9e60-285"><span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**PIX\_ERROR\_OCCLUDED\_DRAW\_CALL**</span></span>  
<span data-ttu-id="e9e60-286">HRESULT personalizzato che indica che una chiamata di un progetto è stata completamente incompleta, causando un errore.</span><span class="sxs-lookup"><span data-stu-id="e9e60-286">A custom HRESULT which indicates that a draw call was entirely occluded, resulting in an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9e60-287">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9e60-287">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e9e60-288">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9e60-288">Header</span></span></p></td><td><span data-ttu-id="e9e60-289">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e9e60-289">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



