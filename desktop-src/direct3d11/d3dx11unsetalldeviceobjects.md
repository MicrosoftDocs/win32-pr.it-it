---
title: Funzione D3DX11UnsetAllDeviceObjects (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di usare questa funzione, è consigliabile usare il metodo sul ID3D11DeviceContext ClearState.
ms.assetid: 0e52bbca-f171-477f-89b0-ba56a2cfa096
keywords:
- Funzione D3DX11UnsetAllDeviceObjects Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11UnsetAllDeviceObjects
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8ac7e33bfef7f8470f616ac07b3aa90463f3f3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355339"
---
# <a name="d3dx11unsetalldeviceobjects-function"></a><span data-ttu-id="84fe9-105">D3DX11UnsetAllDeviceObjects (funzione)</span><span class="sxs-lookup"><span data-stu-id="84fe9-105">D3DX11UnsetAllDeviceObjects function</span></span>

> [!Note]  
> <span data-ttu-id="84fe9-106">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="84fe9-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="84fe9-107">Invece di usare questa funzione, è consigliabile usare il metodo [**sul ID3D11DeviceContext:: ClearState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) .</span><span class="sxs-lookup"><span data-stu-id="84fe9-107">Instead of using this function, we recommend that you use the [**ID3D11DeviceContext::ClearState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) method.</span></span>

 

<span data-ttu-id="84fe9-108">Rimuove tutte le risorse dal dispositivo impostando i relativi puntatori su **null**.</span><span class="sxs-lookup"><span data-stu-id="84fe9-108">Removes all resources from the device by setting their pointers to **NULL**.</span></span> <span data-ttu-id="84fe9-109">Questa operazione deve essere chiamata durante l'arresto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="84fe9-109">This should be called during shutdown of your application.</span></span> <span data-ttu-id="84fe9-110">Consente di assicurare che, quando si rilasciano tutte le relative risorse, nessuna delle quali è associata al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84fe9-110">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="84fe9-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84fe9-111">Syntax</span></span>


```C++
HRESULT D3DX11UnsetAllDeviceObjects(
  _In_ ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="84fe9-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="84fe9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84fe9-113">*pContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84fe9-113">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84fe9-114">Tipo: **[ **sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="84fe9-114">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="84fe9-115">Puntatore a un oggetto [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="84fe9-115">Pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84fe9-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84fe9-116">Return value</span></span>

<span data-ttu-id="84fe9-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="84fe9-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="84fe9-118">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="84fe9-118">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84fe9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84fe9-119">Requirements</span></span>



| <span data-ttu-id="84fe9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="84fe9-120">Requirement</span></span> | <span data-ttu-id="84fe9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="84fe9-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84fe9-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84fe9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="84fe9-123"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="84fe9-123"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="84fe9-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="84fe9-124">Library</span></span><br/> | <dl> <span data-ttu-id="84fe9-125"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84fe9-125"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="84fe9-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84fe9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84fe9-127">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="84fe9-127">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





