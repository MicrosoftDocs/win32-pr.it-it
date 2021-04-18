---
description: Creare il migliore dispositivo Direct3D 10 che rappresenta la scheda di visualizzazione. Se è possibile creare un dispositivo compatibile con Direct3D 10,1, sarà possibile acquisire un puntatore di interfaccia ID3D10Device1 dal puntatore all'interfaccia del dispositivo restituito.
ms.assetid: 1af8f4e5-a59e-403a-95d2-069b91bad93e
title: Funzione D3DX10CreateDevice (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDevice
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 38236a48cdd5197f7f19ef9be3f6fc0f1faca72c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323312"
---
# <a name="d3dx10createdevice-function"></a><span data-ttu-id="35dba-104">D3DX10CreateDevice (funzione)</span><span class="sxs-lookup"><span data-stu-id="35dba-104">D3DX10CreateDevice function</span></span>

<span data-ttu-id="35dba-105">Creare il migliore dispositivo Direct3D 10 che rappresenta la scheda di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="35dba-105">Create the best Direct3D 10 device that represents the display adapter.</span></span> <span data-ttu-id="35dba-106">Se è possibile creare un dispositivo compatibile con Direct3D 10,1, sarà possibile acquisire un puntatore di [**interfaccia ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) dal puntatore all'interfaccia del dispositivo restituito.</span><span class="sxs-lookup"><span data-stu-id="35dba-106">If a Direct3D 10.1-compatible device can be created, it will be possible to acquire an [**ID3D10Device1 Interface**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) pointer from the returned device interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="35dba-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35dba-107">Syntax</span></span>


```C++
HRESULT D3DX10CreateDevice(
  _In_  IDXGIAdapter      *pAdapter,
  _In_  D3D10_DRIVER_TYPE DriverType,
  _In_  HMODULE           Software,
  _In_  UINT              Flags,
  _Out_ ID3D10Device      **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="35dba-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="35dba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35dba-109">*pAdapter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35dba-109">*pAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35dba-110">Tipo: **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span><span class="sxs-lookup"><span data-stu-id="35dba-110">Type: **[**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***</span></span>

<span data-ttu-id="35dba-111">Puntatore alla scheda di visualizzazione (vedere l'interfaccia [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) ) quando si crea un dispositivo hardware. in caso contrario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="35dba-111">Pointer to the display adapter (see the [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) interface) when creating a hardware device; otherwise set this parameter to **NULL**.</span></span> <span data-ttu-id="35dba-112">Se durante la creazione di un dispositivo hardware viene specificato **null** , Direct3D utilizzerà il primo Adapter enumerato dall'interfaccia [**IDXGIFactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) .</span><span class="sxs-lookup"><span data-stu-id="35dba-112">If **NULL** is specified when creating a hardware device, Direct3D will use the first adapter enumerated by the [**IDXGIFactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) interface.</span></span>

</dd> <dt>

<span data-ttu-id="35dba-113">*DriverType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35dba-113">*DriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35dba-114">Tipo: **[ **\_ \_ tipo di driver D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span><span class="sxs-lookup"><span data-stu-id="35dba-114">Type: **[**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**</span></span>

<span data-ttu-id="35dba-115">Il tipo di driver del dispositivo (vedere l'enumerazione del [**\_ \_ tipo di driver D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) ).</span><span class="sxs-lookup"><span data-stu-id="35dba-115">The device-driver type (see the [**D3D10\_DRIVER\_TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) enumeration).</span></span> <span data-ttu-id="35dba-116">Il tipo di driver determina il tipo di dispositivo che si creerà.</span><span class="sxs-lookup"><span data-stu-id="35dba-116">The driver type determines the type of device you will create.</span></span>

</dd> <dt>

<span data-ttu-id="35dba-117">*Software* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="35dba-117">*Software* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35dba-118">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35dba-118">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35dba-119">Handle per un modulo caricato che implementa un driver software, ad esempio D3D10Ref.dll.</span><span class="sxs-lookup"><span data-stu-id="35dba-119">A handle to a loaded module that implements a software driver (such as D3D10Ref.dll).</span></span> <span data-ttu-id="35dba-120">Per ottenere un handle, chiamare la funzione [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .</span><span class="sxs-lookup"><span data-stu-id="35dba-120">To get a handle, call the [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) function.</span></span>

</dd> <dt>

<span data-ttu-id="35dba-121">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35dba-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35dba-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35dba-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35dba-123">Flag di creazione del dispositivo (vedere l'enumerazione [**D3D10 \_ Create \_ Device \_ flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) ) che Abilita i [livelli API](d3d10-graphics-programming-guide-api-features-layers.md).</span><span class="sxs-lookup"><span data-stu-id="35dba-123">Device creation flags (see the [**D3D10\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) enumeration) that enable [API layers](d3d10-graphics-programming-guide-api-features-layers.md).</span></span> <span data-ttu-id="35dba-124">Questi flag possono essere OR bit per bit.</span><span class="sxs-lookup"><span data-stu-id="35dba-124">These flags can be bitwise OR'd together.</span></span>

</dd> <dt>

<span data-ttu-id="35dba-125">*ppDevice* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="35dba-125">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35dba-126">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="35dba-126">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="35dba-127">Indirizzo di un puntatore al dispositivo creato (vedere l'interfaccia [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).</span><span class="sxs-lookup"><span data-stu-id="35dba-127">Address of a pointer to the device created (see the [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35dba-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35dba-128">Return value</span></span>

<span data-ttu-id="35dba-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="35dba-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="35dba-130">Questa funzione restituisce uno dei seguenti [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="35dba-130">This function returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="35dba-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="35dba-131">Remarks</span></span>

<span data-ttu-id="35dba-132">Questa funzione tenta di creare il dispositivo migliore per l'hardware.</span><span class="sxs-lookup"><span data-stu-id="35dba-132">This function attempts to create the best device for the hardware.</span></span> <span data-ttu-id="35dba-133">In primo luogo, la funzione tenta di creare un dispositivo 10,1.</span><span class="sxs-lookup"><span data-stu-id="35dba-133">First, the function attempts to create a 10.1 device.</span></span> <span data-ttu-id="35dba-134">Se non è possibile creare un dispositivo 10,1, la funzione tenta di creare un dispositivo 10,0.</span><span class="sxs-lookup"><span data-stu-id="35dba-134">If a 10.1 device cannot be created, the function attempts to create a 10.0 device.</span></span> <span data-ttu-id="35dba-135">Se nessuno dei due dispositivi viene creato correttamente, la funzione restituisce E ha \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="35dba-135">If neither device is successfully created, the function returns E\_FAIL.</span></span>

<span data-ttu-id="35dba-136">Se l'applicazione deve creare solo un dispositivo 10,1 o un dispositivo 10,0, usare invece le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="35dba-136">If your application needs to create only a 10.1 device, or a 10.0 device only, use the following functions instead:</span></span>

-   <span data-ttu-id="35dba-137">Usare la funzione [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) per creare solo un dispositivo Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="35dba-137">Use the [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) function to create a Direct3D 10.0 device only.</span></span>
-   <span data-ttu-id="35dba-138">Usare la funzione [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) per creare solo un dispositivo Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="35dba-138">Use the [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) function to create a Direct3D 10.1 device only.</span></span>
-   <span data-ttu-id="35dba-139">Usare la funzione [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) per ottenere un puntatore a interfaccia [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) da un puntatore a interfaccia [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .</span><span class="sxs-lookup"><span data-stu-id="35dba-139">Use the [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) function to get an [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) interface pointer from an [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface pointer.</span></span>

<span data-ttu-id="35dba-140">Un dispositivo Direct3D 10,1 può essere creato solo in computer che eseguono Windows Vista Service Pack 1 o versione successiva e con hardware compatibile con Direct3D 10,1 installato.</span><span class="sxs-lookup"><span data-stu-id="35dba-140">A Direct3D 10.1 device can only be created on computers running Windows Vista Service Pack 1 or later, and with Direct3D 10.1-compatible hardware installed.</span></span> <span data-ttu-id="35dba-141">Tuttavia, è lecito chiamare questa funzione nei computer che eseguono qualsiasi versione di Windows in cui è installata la DLL D3DX10.</span><span class="sxs-lookup"><span data-stu-id="35dba-141">However, it is legal to call this function on computers running any version of Windows that has the D3DX10 DLL installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="35dba-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35dba-142">Requirements</span></span>



| <span data-ttu-id="35dba-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="35dba-143">Requirement</span></span> | <span data-ttu-id="35dba-144">Valore</span><span class="sxs-lookup"><span data-stu-id="35dba-144">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35dba-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35dba-145">Header</span></span><br/> | <dl> <span data-ttu-id="35dba-146"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="35dba-146"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35dba-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35dba-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35dba-148">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="35dba-148">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
