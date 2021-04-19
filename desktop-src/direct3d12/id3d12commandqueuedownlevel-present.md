---
title: ID3D12CommandQueueDownlevel::P metodo reinviato
description: Copia il contenuto da una risorsa Direct3D 12 Texture2D in una finestra. | ID3D12CommandQueueDownlevel::P metodo reinviato
keywords:
- Metodo Present
- Metodo Present, interfaccia ID3D12CommandQueueDownlevel
- Interfaccia ID3D12CommandQueueDownlevel, metodo Present
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel.Present
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: a6c74685911e52a671eaeb02645754a45b8d647e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323125"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a><span data-ttu-id="c95a8-107">ID3D12CommandQueueDownlevel::P metodo reinviato</span><span class="sxs-lookup"><span data-stu-id="c95a8-107">ID3D12CommandQueueDownlevel::Present method</span></span>

<span data-ttu-id="c95a8-108">Copia il contenuto da una risorsa Direct3D 12 Texture2D in una finestra.</span><span class="sxs-lookup"><span data-stu-id="c95a8-108">Copies contents from a Direct3D 12 Texture2D resource into a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="c95a8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c95a8-109">Syntax</span></span>

```cpp
HRESULT Present
    ID3D12GraphicsCommandList *pOpenCommandList,
    ID3D12Resource *pSourceTex2D,
    HWND hWindow,
    D3D12_DOWNLEVEL_PRESENT_FLAGS Flags
);
```

## <a name="parameters"></a><span data-ttu-id="c95a8-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c95a8-110">Parameters</span></span>

`pOpenCommandList`

<span data-ttu-id="c95a8-111">Tipo: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="c95a8-111">Type: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="c95a8-112">Elenco di comandi aperti, che consente a Direct3D 12 di accodare un comando presente in e quindi di chiuderlo e inviarlo.</span><span class="sxs-lookup"><span data-stu-id="c95a8-112">An open command list, which Direct3D 12 enqueues a Present command onto, and then closes and submits for you.</span></span>

`pSourceTex2D`

<span data-ttu-id="c95a8-113">Tipo: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="c95a8-113">Type: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="c95a8-114">Risorsa contenente il contenuto desiderato da visualizzare, con dimensione [**D3D12 della \_ dimensione della risorsa \_ \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)e un formato uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="c95a8-114">A resource containing your desired contents to display, with dimension [**D3D12\_RESOURCE\_DIMENSION\_TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension), and a format that is one of the following.</span></span>

* <span data-ttu-id="c95a8-115">DXGI_FORMAT_R16G16B16A16_FLOAT</span><span class="sxs-lookup"><span data-stu-id="c95a8-115">DXGI_FORMAT_R16G16B16A16_FLOAT</span></span>
* <span data-ttu-id="c95a8-116">DXGI_FORMAT_R10G10B10A2_UNORM</span><span class="sxs-lookup"><span data-stu-id="c95a8-116">DXGI_FORMAT_R10G10B10A2_UNORM</span></span>
* <span data-ttu-id="c95a8-117">DXGI_FORMAT_R8G8B8A8_UNORM</span><span class="sxs-lookup"><span data-stu-id="c95a8-117">DXGI_FORMAT_R8G8B8A8_UNORM</span></span>
* <span data-ttu-id="c95a8-118">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</span><span class="sxs-lookup"><span data-stu-id="c95a8-118">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</span></span>
* <span data-ttu-id="c95a8-119">DXGI_FORMAT_B8G8R8X8_UNORM</span><span class="sxs-lookup"><span data-stu-id="c95a8-119">DXGI_FORMAT_B8G8R8X8_UNORM</span></span>
* <span data-ttu-id="c95a8-120">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM</span><span class="sxs-lookup"><span data-stu-id="c95a8-120">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM</span></span>
* <span data-ttu-id="c95a8-121">DXGI_FORMAT_B8G8R8A8_UNORM</span><span class="sxs-lookup"><span data-stu-id="c95a8-121">DXGI_FORMAT_B8G8R8A8_UNORM</span></span>
* <span data-ttu-id="c95a8-122">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</span><span class="sxs-lookup"><span data-stu-id="c95a8-122">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</span></span>

`hWindow`

<span data-ttu-id="c95a8-123">Tipo: **[HWND](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c95a8-123">Type: **[HWND](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c95a8-124">Handle per la finestra in cui deve essere visualizzato il contenuto.</span><span class="sxs-lookup"><span data-stu-id="c95a8-124">The handle to the window where the contents should be displayed.</span></span>

`Flags`

<span data-ttu-id="c95a8-125">Tipo: **[D3D12 \_ i \_ \_ flag presenti](d3d12_downlevel_present_flags.md) di livello inferiore**</span><span class="sxs-lookup"><span data-stu-id="c95a8-125">Type: **[D3D12\_DOWNLEVEL\_PRESENT\_FLAGS](d3d12_downlevel_present_flags.md)**</span></span>

<span data-ttu-id="c95a8-126">Flag per modificare l'operazione **corrente** .</span><span class="sxs-lookup"><span data-stu-id="c95a8-126">Flags to modify the **Present** operation.</span></span>

## <a name="return-value"></a><span data-ttu-id="c95a8-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c95a8-127">Return value</span></span>

<span data-ttu-id="c95a8-128">Restituisce **S_OK** in caso di esito positivo, altrimenti un HRESULT non riuscito.</span><span class="sxs-lookup"><span data-stu-id="c95a8-128">Returns **S_OK** on success, or else a failing HRESULT.</span></span>

## <a name="requirements"></a><span data-ttu-id="c95a8-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c95a8-129">Requirements</span></span>

| <span data-ttu-id="c95a8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c95a8-130">Requirement</span></span> | <span data-ttu-id="c95a8-131">Valore</span><span class="sxs-lookup"><span data-stu-id="c95a8-131">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="c95a8-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c95a8-132">Header</span></span> | <span data-ttu-id="c95a8-133">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="c95a8-133">d3d12downlevel.h</span></span> |
| <span data-ttu-id="c95a8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c95a8-134">DLL</span></span>    | <span data-ttu-id="c95a8-135">D3D12.dll (solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="c95a8-135">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="c95a8-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c95a8-136">See also</span></span>
* [<span data-ttu-id="c95a8-137">ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="c95a8-137">ID3D12CommandQueueDownlevel</span></span>](id3d12commandqueuedownlevel.md)
* [<span data-ttu-id="c95a8-138">Interfacce Direct3D 12 su Windows 7</span><span class="sxs-lookup"><span data-stu-id="c95a8-138">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="c95a8-139">Guida di riferimento a Direct3D 12 per Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="c95a8-139">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="c95a8-140">Direct3D 12 in Windows 7</span><span class="sxs-lookup"><span data-stu-id="c95a8-140">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
