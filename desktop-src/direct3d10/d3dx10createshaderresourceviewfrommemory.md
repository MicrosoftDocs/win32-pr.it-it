---
description: Creare una visualizzazione risorse shader da un file in memoria.
ms.assetid: 8316987f-75b4-4cee-a1f2-10bee77a28e6
title: Funzione D3DX10CreateShaderResourceViewFromMemory (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ca3cf26d54d37ab3e3a2141ba7c3e4ea9fdd533f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761974"
---
# <a name="d3dx10createshaderresourceviewfrommemory-function"></a><span data-ttu-id="8e203-103">D3DX10CreateShaderResourceViewFromMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="8e203-103">D3DX10CreateShaderResourceViewFromMemory function</span></span>

<span data-ttu-id="8e203-104">Creare una visualizzazione risorse shader da un file in memoria.</span><span class="sxs-lookup"><span data-stu-id="8e203-104">Create a shader-resource view from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e203-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e203-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromMemory(
  _In_  ID3D10Device             *pDevice,
  _In_  LPCVOID                  pSrcData,
  _In_  SIZE_T                   SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="8e203-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e203-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e203-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e203-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e203-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="8e203-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="8e203-109">Un puntatore al dispositivo (vedere [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) che utilizzerà la risorsa.</span><span class="sxs-lookup"><span data-stu-id="8e203-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="8e203-110">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e203-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e203-111">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e203-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e203-112">Puntatore al file in memoria che contiene la visualizzazione delle risorse dello shader.</span><span class="sxs-lookup"><span data-stu-id="8e203-112">Pointer to the file in memory that contains the shader-resource view.</span></span>

</dd> <dt>

<span data-ttu-id="8e203-113">*SrcDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e203-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e203-114">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e203-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e203-115">Dimensioni del file in memoria.</span><span class="sxs-lookup"><span data-stu-id="8e203-115">Size of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="8e203-116">*pLoadInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e203-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e203-117">Tipo: **[ **d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e203-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="8e203-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8e203-118">Optional.</span></span> <span data-ttu-id="8e203-119">Identifica le caratteristiche di una trama (vedere [**d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="8e203-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="8e203-120">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e203-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e203-121">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e203-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="8e203-122">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="8e203-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="8e203-123">Se viene specificato **null** , questa funzione verrà comportata in modo sincrono e non verrà restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="8e203-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="8e203-124">*ppShaderResourceView* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8e203-124">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e203-125">Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="8e203-125">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="8e203-126">Indirizzo di un puntatore alla visualizzazione delle risorse dello shader appena creata.</span><span class="sxs-lookup"><span data-stu-id="8e203-126">Address of a pointer to the newly created shader resource view.</span></span> <span data-ttu-id="8e203-127">Vedere [**interfaccia ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="8e203-127">See [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="8e203-128">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8e203-128">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e203-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="8e203-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="8e203-130">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="8e203-130">A pointer to the return value.</span></span> <span data-ttu-id="8e203-131">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="8e203-131">May be **NULL**.</span></span> <span data-ttu-id="8e203-132">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="8e203-132">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e203-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e203-133">Return value</span></span>

<span data-ttu-id="8e203-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8e203-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8e203-135">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8e203-135">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e203-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e203-136">Requirements</span></span>



| <span data-ttu-id="8e203-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e203-137">Requirement</span></span> | <span data-ttu-id="8e203-138">Valore</span><span class="sxs-lookup"><span data-stu-id="8e203-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e203-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e203-139">Header</span></span><br/>  | <dl> <span data-ttu-id="8e203-140"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e203-140"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="8e203-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="8e203-141">Library</span></span><br/> | <dl> <span data-ttu-id="8e203-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e203-142"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8e203-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e203-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e203-144">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="8e203-144">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="8e203-145">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="8e203-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
