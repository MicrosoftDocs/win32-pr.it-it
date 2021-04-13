---
description: Creare il migliore dispositivo Direct3D e una catena di scambio.
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: Funzione D3DX10CreateDeviceAndSwapChain (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDeviceAndSwapChain
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: fe71aeae91f8c43966e0fda2d2f430c7908f2855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355549"
---
# <a name="d3dx10createdeviceandswapchain-function"></a><span data-ttu-id="78c7d-103">D3DX10CreateDeviceAndSwapChain (funzione)</span><span class="sxs-lookup"><span data-stu-id="78c7d-103">D3DX10CreateDeviceAndSwapChain function</span></span>

<span data-ttu-id="78c7d-104">Creare il migliore dispositivo Direct3D e una catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="78c7d-104">Create the best Direct3D device and a swap chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="78c7d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78c7d-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateDeviceAndSwapChain(
  _In_  IDXGIAdapter         *pAdapter,
  _In_  D3D10_DRIVER_TYPE    DriverType,
  _In_  HMODULE              Software,
  _In_  UINT                 Flags,
  _In_  DXGI_SWAP_CHAIN_DESC *pSwapChainDesc,
  _Out_ IDXGISwapChain       **ppSwapChain,
  _Out_ ID3D10Device         **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="78c7d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="78c7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78c7d-107">*pAdapter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78c7d-107">*pAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78c7d-108">Tipo: **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span><span class="sxs-lookup"><span data-stu-id="78c7d-108">Type: **[**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span></span>

<span data-ttu-id="78c7d-109">Puntatore a un [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).</span><span class="sxs-lookup"><span data-stu-id="78c7d-109">Pointer to a [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).</span></span>

</dd> <dt>

<span data-ttu-id="78c7d-110">*DriverType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78c7d-110">*DriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78c7d-111">Tipo: **[ **\_ \_ tipo di driver D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span><span class="sxs-lookup"><span data-stu-id="78c7d-111">Type: **[**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span></span>

<span data-ttu-id="78c7d-112">Tipo di driver per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78c7d-112">The type of driver for the device.</span></span> <span data-ttu-id="78c7d-113">Vedere [**\_ \_ tipo di driver D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).</span><span class="sxs-lookup"><span data-stu-id="78c7d-113">See [**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).</span></span>

</dd> <dt>

<span data-ttu-id="78c7d-114">*Software* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="78c7d-114">*Software* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78c7d-115">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78c7d-115">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78c7d-116">Handle per la DLL che implementa un rasterizzatore software.</span><span class="sxs-lookup"><span data-stu-id="78c7d-116">A handle to the DLL that implements a software rasterizer.</span></span> <span data-ttu-id="78c7d-117">Deve essere **null** se DriverType è non software.</span><span class="sxs-lookup"><span data-stu-id="78c7d-117">Must be **NULL** if DriverType is non-software.</span></span> <span data-ttu-id="78c7d-118">Il HMODULE di una DLL può essere ottenuto con [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)o [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="78c7d-118">The HMODULE of a DLL can be obtained with [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa), or [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="78c7d-119">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78c7d-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78c7d-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78c7d-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78c7d-121">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="78c7d-121">Optional.</span></span> <span data-ttu-id="78c7d-122">Flag di creazione del dispositivo (vedere [**D3D10 \_ Create \_ Device \_ flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)) che Abilita i [livelli API](d3d10-graphics-programming-guide-api-features-layers.md).</span><span class="sxs-lookup"><span data-stu-id="78c7d-122">Device creation flags (see [**D3D10\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)) that enable [API layers](d3d10-graphics-programming-guide-api-features-layers.md).</span></span> <span data-ttu-id="78c7d-123">Questi flag possono essere OR bit per bit.</span><span class="sxs-lookup"><span data-stu-id="78c7d-123">These flags can be bitwise OR'd together.</span></span>

</dd> <dt>

<span data-ttu-id="78c7d-124">*pSwapChainDesc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78c7d-124">*pSwapChainDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78c7d-125">Tipo: **[ **DXGI \_ scambio \_ catena \_ desc**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***</span><span class="sxs-lookup"><span data-stu-id="78c7d-125">Type: **[**DXGI\_SWAP\_CHAIN\_DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***</span></span>

<span data-ttu-id="78c7d-126">Descrizione della catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="78c7d-126">Description of the swap chain.</span></span> <span data-ttu-id="78c7d-127">Vedere [**DXGI \_ swap \_ Chain \_ desc**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc).</span><span class="sxs-lookup"><span data-stu-id="78c7d-127">See [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc).</span></span>

</dd> <dt>

<span data-ttu-id="78c7d-128">*ppSwapChain* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="78c7d-128">*ppSwapChain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78c7d-129">Tipo: **[ **IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***</span><span class="sxs-lookup"><span data-stu-id="78c7d-129">Type: **[**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***</span></span>

<span data-ttu-id="78c7d-130">Indirizzo di un puntatore a un [**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).</span><span class="sxs-lookup"><span data-stu-id="78c7d-130">Address of a pointer to an [**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).</span></span>

</dd> <dt>

<span data-ttu-id="78c7d-131">*ppDevice* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="78c7d-131">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78c7d-132">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="78c7d-132">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="78c7d-133">Indirizzo di un puntatore a un' [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) che riceverà il dispositivo appena creato.</span><span class="sxs-lookup"><span data-stu-id="78c7d-133">Address of a pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) that will receive the newly created device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78c7d-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78c7d-134">Return value</span></span>

<span data-ttu-id="78c7d-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78c7d-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78c7d-136">Questo metodo restituisce uno dei seguenti [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="78c7d-136">This method returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="78c7d-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="78c7d-137">Remarks</span></span>

<span data-ttu-id="78c7d-138">Per creare il dispositivo migliore, questo metodo implementa più di un'opzione di creazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78c7d-138">To create the best device, this method implements more than one device creation option.</span></span> <span data-ttu-id="78c7d-139">In primo luogo, il metodo tenta di creare un dispositivo 10,1 (e una catena di scambio).</span><span class="sxs-lookup"><span data-stu-id="78c7d-139">First, the method attempts to create a 10.1 device (and swap chain).</span></span> <span data-ttu-id="78c7d-140">Se l'operazione ha esito negativo, il metodo tenta di creare un dispositivo 10,0.</span><span class="sxs-lookup"><span data-stu-id="78c7d-140">If that fails, the method attempts to create a 10.0 device.</span></span> <span data-ttu-id="78c7d-141">Se l'operazione ha esito negativo, il metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="78c7d-141">If that fails, the method will fail.</span></span> <span data-ttu-id="78c7d-142">Se l'applicazione deve creare solo un dispositivo 10,1 o solo un dispositivo 10,0, usare queste API:</span><span class="sxs-lookup"><span data-stu-id="78c7d-142">If your application needs to create only a 10.1 device, or a 10.0 device only, use these APIs instead:</span></span>

-   <span data-ttu-id="78c7d-143">Usare [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) per creare un dispositivo Direct3D 10,0 (solo) e una catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="78c7d-143">Use [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) to create a Direct3D 10.0 (only) device and swap chain.</span></span>
-   <span data-ttu-id="78c7d-144">Usare [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) per creare un dispositivo Direct3D 10,1 (solo) e una catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="78c7d-144">Use [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) to create a Direct3D 10.1 (only) device and swap chain.</span></span>

<span data-ttu-id="78c7d-145">Questo metodo richiede Windows Vista Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="78c7d-145">This method requires Windows Vista Service Pack 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="78c7d-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78c7d-146">Requirements</span></span>



| <span data-ttu-id="78c7d-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="78c7d-147">Requirement</span></span> | <span data-ttu-id="78c7d-148">Valore</span><span class="sxs-lookup"><span data-stu-id="78c7d-148">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78c7d-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78c7d-149">Header</span></span><br/> | <dl> <span data-ttu-id="78c7d-150"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="78c7d-150"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78c7d-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78c7d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c7d-152">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="78c7d-152">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
