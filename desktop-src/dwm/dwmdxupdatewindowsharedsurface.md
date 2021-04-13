---
description: Notifica a DWM un aggiornamento in ingresso a una superficie condivisa della finestra.
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: DwmDxUpdateWindowSharedSurface (funzione)
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
- DwmDxUpdateWindowSharedSurface
ms.openlocfilehash: 7649e96fb3a16458b518d0fc2c6dd09725a4b0ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528129"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a><span data-ttu-id="d0028-103">DwmDxUpdateWindowSharedSurface (funzione)</span><span class="sxs-lookup"><span data-stu-id="d0028-103">DwmDxUpdateWindowSharedSurface function</span></span>

<span data-ttu-id="d0028-104">Notifica a DWM un aggiornamento in ingresso a una superficie condivisa della finestra.</span><span class="sxs-lookup"><span data-stu-id="d0028-104">Notifies the DWM of an incoming update to a window shared surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0028-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0028-105">Syntax</span></span>

```C++
HRESULT WINAPI DwmDxUpdateWindowSharedSurface(
  _In_     HWND     hwnd,
  _In_     UINT64   uiUpdateId,
  _In_     DWORD    dwFlags,
  _In_opt_ HMONITOR hmonitorAssociation,
  _In_     RECT     *prc
);
```

## <a name="parameters"></a><span data-ttu-id="d0028-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0028-106">Parameters</span></span>

`hwnd`

<span data-ttu-id="d0028-107">[**HWND**](/windows/desktop/winprog/windows-data-types) che specifica la finestra da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="d0028-107">An [**HWND**](/windows/desktop/winprog/windows-data-types) specifying the window being updated.</span></span>

`uiUpdateId`

<span data-ttu-id="d0028-108">ID aggiornamento recuperato da [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).</span><span class="sxs-lookup"><span data-stu-id="d0028-108">The update ID retrieved from [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).</span></span>

`dwFlags`

<span data-ttu-id="d0028-109">Riservato.</span><span class="sxs-lookup"><span data-stu-id="d0028-109">Reserved.</span></span>

`hmonitorAssociation`

<span data-ttu-id="d0028-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="d0028-110">Reserved.</span></span>

`prc`

<span data-ttu-id="d0028-111">Rect della finestra da aggiornare, nello spazio delle coordinate della finestra.</span><span class="sxs-lookup"><span data-stu-id="d0028-111">The rect of the window being updated, in window coordinate space.</span></span> <span data-ttu-id="d0028-112">Un rettangolo NULL indica che non è stata aggiornata alcuna area.</span><span class="sxs-lookup"><span data-stu-id="d0028-112">A NULL rectangle indicates that no region was updated.</span></span>

## <a name="return-value"></a><span data-ttu-id="d0028-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0028-113">Return value</span></span>

<span data-ttu-id="d0028-114">**S \_ OK** se ha esito positivo, in caso contrario un HRESULT non riuscito **.**</span><span class="sxs-lookup"><span data-stu-id="d0028-114">**S\_OK** if successful, otherwise a FAILED **HRESULT.**</span></span>

## <a name="remarks"></a><span data-ttu-id="d0028-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0028-115">Remarks</span></span>

<span data-ttu-id="d0028-116">Questa API è destinata all'implementazione di un driver o di un runtime di grafica.</span><span class="sxs-lookup"><span data-stu-id="d0028-116">This API is intended for implementing a graphics driver or runtime.</span></span> <span data-ttu-id="d0028-117">Un'applicazione non può chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="d0028-117">An application may not call this method.</span></span> <span data-ttu-id="d0028-118">Questa documentazione è valida solo per Windows 7 e questa API non esiste né si comporta in modo analogo in altre versioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="d0028-118">This documentation is only valid for Windows 7, and this API is not guaranteed to exist nor behave in a similar manner on other versions of Windows.</span></span> <span data-ttu-id="d0028-119">Questa funzione non è presente in alcuna intestazione o libreria a collegamento statico e si trova in corrispondenza dell'ordinale 101 in dwmapi.dll.</span><span class="sxs-lookup"><span data-stu-id="d0028-119">This function is not present in any header or static-link library, and it is located at ordinal 101 in dwmapi.dll.</span></span>

<span data-ttu-id="d0028-120">Questo metodo deve essere chiamato solo dopo che [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) restituisce **S \_ OK** e deve essere chiamato in tale scenario, indipendentemente dal fatto che la superficie venga aggiornata o meno.</span><span class="sxs-lookup"><span data-stu-id="d0028-120">This method should only ever be called after [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) returns **S\_OK**, and must be called in that scenario, regardless of whether the surface is updated or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0028-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0028-121">Requirements</span></span>

| <span data-ttu-id="d0028-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0028-122">Requirement</span></span> | <span data-ttu-id="d0028-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d0028-123">Value</span></span> |
|-|-|
| <span data-ttu-id="d0028-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0028-124">Minimum supported client</span></span> | <span data-ttu-id="d0028-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d0028-125">Windows 7 \[desktop apps only\]</span></span> |
| <span data-ttu-id="d0028-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0028-126">Minimum supported server</span></span> | <span data-ttu-id="d0028-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d0028-127">None supported</span></span> |
| <span data-ttu-id="d0028-128">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d0028-128">End of client support</span></span> | <span data-ttu-id="d0028-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d0028-129">Windows 7</span></span> |
| <span data-ttu-id="d0028-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0028-130">Header</span></span> | <span data-ttu-id="d0028-131">N/D</span><span class="sxs-lookup"><span data-stu-id="d0028-131">N/A</span></span> |
| <span data-ttu-id="d0028-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d0028-132">DLL</span></span> | <span data-ttu-id="d0028-133">Dwmapi.dll</span><span class="sxs-lookup"><span data-stu-id="d0028-133">Dwmapi.dll</span></span> |
