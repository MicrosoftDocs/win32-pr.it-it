---
description: Recupera la superficie condivisa DirectX che esegue il backup di una finestra specificata. Per aggiornare il contenuto della finestra, è possibile scrivere questa superficie.
ms.assetid: 500CF5B4-0D56-4201-91F4-7333E45DACEE
title: DwmDxGetWindowSharedSurface (funzione)
ms.topic: reference
ms.date: 11/27/2018
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmDxGetWindowSharedSurface
ms.openlocfilehash: 15e7829383ce23e5bc06bb61ab9c0c224ab18182
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309434"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a><span data-ttu-id="4ea5c-104">DwmDxGetWindowSharedSurface (funzione)</span><span class="sxs-lookup"><span data-stu-id="4ea5c-104">DwmDxGetWindowSharedSurface function</span></span>

<span data-ttu-id="4ea5c-105">Recupera la superficie condivisa DirectX che esegue il backup di una finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-105">Retrieves the DirectX shared surface backing a given window.</span></span> <span data-ttu-id="4ea5c-106">Per aggiornare il contenuto della finestra, è possibile scrivere questa superficie.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-106">This surface can be written to in order to update the contents of the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ea5c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ea5c-107">Syntax</span></span>

```C++
HRESULT WINAPI DwmDxGetWindowSharedSurface(
  _In_     HWND        hwnd,
  _In_     LUID        luidAdapter,
  _In_opt_ HMONITOR    hmonitorAssociation,
  _In_     DWORD       dwFlags,
  _Inout_  DXGI_FORMAT *pfmtWindow,
  _Out_    HANDLE      *phDxSurface,
  _Out_    UINT64      *puiUpdateId
);
```

## <a name="parameters"></a><span data-ttu-id="4ea5c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ea5c-108">Parameters</span></span>

`hwnd`

<span data-ttu-id="4ea5c-109">[**HWND**](/windows/desktop/winprog/windows-data-types) che specifica la finestra da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-109">An [**HWND**](/windows/desktop/winprog/windows-data-types) specifying the window to be updated.</span></span>

`luidAdapter`

<span data-ttu-id="4ea5c-110">[**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) dell'adapter in cui deve trovarsi la superficie.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-110">The [**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) of the adapter where the surface should be located.</span></span>

`hmonitorAssociation`

<span data-ttu-id="4ea5c-111">Riservato.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-111">Reserved.</span></span>

`dwFlags`

<span data-ttu-id="4ea5c-112">Questo parametro può essere uno dei valori seguenti oppure una combinazione OR bit per bit di più valori laddove appropriato.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-112">This parameter can be one of the following values, or a bitwise OR combination of multiple values where appropriate.</span></span>

| <span data-ttu-id="4ea5c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="4ea5c-113">Value</span></span> | <span data-ttu-id="4ea5c-114">Significato</span><span class="sxs-lookup"><span data-stu-id="4ea5c-114">Meaning</span></span> |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <span data-ttu-id="4ea5c-115"><dt>**DWM \_ \_ \_ Attesa del flag di reindirizzamento**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4ea5c-115"><dt>**DWM\_REDIRECTION\_FLAG\_WAIT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="4ea5c-116">Fa in modo che la funzione blocchi fino a quando non viene superata una sincronizzazione verticale (VSync) dall'ultima volta che la funzione è stata chiamata correttamente.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-116">Causes the function to block until a vertical synchronization (VSync) has passed since the last time the function was called successfully.</span></span> |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <span data-ttu-id="4ea5c-117"><dt>**DWM \_ \_Supporto del flag \_ di Reindirizzamento \_ presente \_ alla \_ \_ superficie GDI**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="4ea5c-117"><dt>**DWM\_REDIRECTION\_FLAG\_SUPPORT\_PRESENT\_TO\_GDI\_SURFACE**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="4ea5c-118">Indica che l'applicazione chiamante è in grado di presentare a una superficie condivisa GDI.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-118">Indicates that the calling application is capable of presenting to a GDI shared surface.</span></span> |

`pfmtWindow`

<span data-ttu-id="4ea5c-119">In input, il formato desiderato della superficie.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-119">On input, the desired format of the surface.</span></span> <span data-ttu-id="4ea5c-120">Nell'output, il formato effettivo della superficie restituita.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-120">On output, the actual format of the returned surface.</span></span>

`phDxSurface`

<span data-ttu-id="4ea5c-121">Nell'output, l'handle condiviso per la superficie.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-121">On output, the shared handle to the surface.</span></span>

`puiUpdateId`

<span data-ttu-id="4ea5c-122">Nell'output, ID dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-122">On output, the ID of the update.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ea5c-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ea5c-123">Return value</span></span>

<span data-ttu-id="4ea5c-124">Questa funzione può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-124">This function can return one of these values.</span></span>

| <span data-ttu-id="4ea5c-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4ea5c-125">Return code</span></span> | <span data-ttu-id="4ea5c-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ea5c-126">Description</span></span> |
|-|-|
| <span data-ttu-id="4ea5c-127">**\_OK**</span><span class="sxs-lookup"><span data-stu-id="4ea5c-127">**S\_OK**</span></span> | <span data-ttu-id="4ea5c-128">La chiamata ha avuto esito positivo ed è necessario aggiornare la superficie, assicurandosi di passare l'ID aggiornamento a [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (nel membro **PresentHistoryToken** della struttura di **\_ rendering D3DKMT** quando viene inviato l'aggiornamento e quindi [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) deve essere chiamato con lo stesso ID di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-128">The call succeeded, and you should update the surface, being sure to pass the update ID to [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (in the **PresentHistoryToken** member of the **D3DKMT\_RENDER** structure when the update is submitted, and then [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) should be called with the same update ID.</span></span> <span data-ttu-id="4ea5c-129">Si noti che **DwmDxUpdateWindowSharedSurface** deve essere chiamato indipendentemente dal fatto che la superficie sia stata effettivamente aggiornata o meno.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-129">Note that **DwmDxUpdateWindowSharedSurface** should be called regardless of whether the surface was actually updated or not.</span></span> |
| <span data-ttu-id="4ea5c-130">**\_superficie di \_ \_ Reindirizzamento GDI \_ di DWM**</span><span class="sxs-lookup"><span data-stu-id="4ea5c-130">**DWM\_S\_GDI\_REDIRECTION\_SURFACE**</span></span> | <span data-ttu-id="4ea5c-131">La chiamata ha avuto esito positivo ed è necessario aggiornare la superficie chiamando [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)e impostando il **modello** del membro **PresentHistoryToken** su **D3DKMT \_ PM \_ reindirizzato \_ BLT** e specificando l'ID dell'aggiornamento nel membro **BLT** dell'Unione.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-131">The call succeeded, and you should update the surface by calling [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent), and setting **PresentHistoryToken** member's **Model** to **D3DKMT\_PM\_REDIRECTED\_BLT**, and providing the update ID in the **Blt** member of the union.</span></span> <span data-ttu-id="4ea5c-132">Questo valore viene restituito solo se in *dwFlags* è stato specificato il **\_ supporto del \_ flag di reindirizzamento DWM presente nella \_ \_ \_ \_ \_ superficie GDI** .</span><span class="sxs-lookup"><span data-stu-id="4ea5c-132">This value is only returned if **DWM\_REDIRECTION\_FLAG\_SUPPORT\_PRESENT\_TO\_GDI\_SURFACE** was specified in *dwFlags*.</span></span> |
| <span data-ttu-id="4ea5c-133">**\_Adapter DWM \_ E \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="4ea5c-133">**DWM\_E\_ADAPTER\_NOT\_FOUND**</span></span> | <span data-ttu-id="4ea5c-134">Il valore di *luidAdapter* non è valido.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-134">The value of *luidAdapter* is not valid.</span></span> |
| <span data-ttu-id="4ea5c-135">**DWM \_ E \_ COMPOSITIONDISABLED**</span><span class="sxs-lookup"><span data-stu-id="4ea5c-135">**DWM\_E\_COMPOSITIONDISABLED**</span></span> | <span data-ttu-id="4ea5c-136">DWM non è attualmente abilitato e l'applicazione deve presentare un altro modo.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-136">DWM is not currently enabled, and the application will need to present another way.</span></span> |

## <a name="remarks"></a><span data-ttu-id="4ea5c-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ea5c-137">Remarks</span></span>

<span data-ttu-id="4ea5c-138">Questa API è destinata all'implementazione di un driver o di un runtime di grafica.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-138">This API is intended for implementing a graphics driver or runtime.</span></span> <span data-ttu-id="4ea5c-139">Un'applicazione non può chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-139">An application may not call this method.</span></span> <span data-ttu-id="4ea5c-140">Questa documentazione è valida solo per Windows 7 e questa API non esiste né si comporta in modo analogo in altre versioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-140">This documentation is only valid for Windows 7, and this API is not guaranteed to exist nor behave in a similar manner on other versions of Windows.</span></span> <span data-ttu-id="4ea5c-141">Questa funzione non è presente in alcuna intestazione o libreria a collegamento statico e si trova in corrispondenza dell'ordinale 100 in dwmapi.dll.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-141">This function is not present in any header or static-link library, and it is located at ordinal 100 in dwmapi.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ea5c-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ea5c-142">Requirements</span></span>

| <span data-ttu-id="4ea5c-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ea5c-143">Requirement</span></span> | <span data-ttu-id="4ea5c-144">Valore</span><span class="sxs-lookup"><span data-stu-id="4ea5c-144">Value</span></span> |
|-|-|
| <span data-ttu-id="4ea5c-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ea5c-145">Minimum supported client</span></span> | <span data-ttu-id="4ea5c-146">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4ea5c-146">Windows 7 \[desktop apps only\]</span></span> |
| <span data-ttu-id="4ea5c-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ea5c-147">Minimum supported server</span></span> | <span data-ttu-id="4ea5c-148">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4ea5c-148">None supported</span></span> |
| <span data-ttu-id="4ea5c-149">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4ea5c-149">End of client support</span></span> | <span data-ttu-id="4ea5c-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4ea5c-150">Windows 7</span></span> |
| <span data-ttu-id="4ea5c-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ea5c-151">Header</span></span> | <span data-ttu-id="4ea5c-152">N/D</span><span class="sxs-lookup"><span data-stu-id="4ea5c-152">N/A</span></span> |
| <span data-ttu-id="4ea5c-153">DLL</span><span class="sxs-lookup"><span data-stu-id="4ea5c-153">DLL</span></span> | <span data-ttu-id="4ea5c-154">Dwmapi.dll</span><span class="sxs-lookup"><span data-stu-id="4ea5c-154">Dwmapi.dll</span></span> |
