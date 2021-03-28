---
title: Funzione D3DX11CreateEffectFromMemory (D3dx11effect. h)
description: Crea un effetto da un file o un effetto binario.
ms.assetid: 4aa65efb-4c6b-4faf-b48f-01329bdff6cd
keywords:
- Funzione D3DX11CreateEffectFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateEffectFromMemory
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467d2094a7124b96a08c7bab6d7a4209deee9996
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996011"
---
# <a name="d3dx11createeffectfrommemory-function"></a><span data-ttu-id="9cad5-104">D3DX11CreateEffectFromMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="9cad5-104">D3DX11CreateEffectFromMemory function</span></span>

<span data-ttu-id="9cad5-105">Crea un effetto da un file o un effetto binario.</span><span class="sxs-lookup"><span data-stu-id="9cad5-105">Creates an effect from a binary effect or file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cad5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9cad5-106">Syntax</span></span>


```C++
HRESULT D3DX11CreateEffectFromMemory(
   void          *pData,
   SIZE_T        DataLength,
   UINT          FXFlags,
   ID3D11Device  *pDevice,
   ID3DX11Effect **ppEffect
);
```



## <a name="parameters"></a><span data-ttu-id="9cad5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9cad5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cad5-108">*pData*</span><span class="sxs-lookup"><span data-stu-id="9cad5-108">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="9cad5-109">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="9cad5-109">Type: **void\***</span></span>

<span data-ttu-id="9cad5-110">BLOB di dati degli effetti compilati.</span><span class="sxs-lookup"><span data-stu-id="9cad5-110">Blob of compiled effect data.</span></span>

</dd> <dt>

<span data-ttu-id="9cad5-111">*DataLength*</span><span class="sxs-lookup"><span data-stu-id="9cad5-111">*DataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="9cad5-112">Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9cad5-112">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9cad5-113">Lunghezza del BLOB di dati.</span><span class="sxs-lookup"><span data-stu-id="9cad5-113">Length of the data blob.</span></span>

</dd> <dt>

<span data-ttu-id="9cad5-114">*FXFlags*</span><span class="sxs-lookup"><span data-stu-id="9cad5-114">*FXFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="9cad5-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9cad5-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9cad5-116">Nessun flag di effetto esistente.</span><span class="sxs-lookup"><span data-stu-id="9cad5-116">No effect flags exist.</span></span> <span data-ttu-id="9cad5-117">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="9cad5-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="9cad5-118">*pDevice*</span><span class="sxs-lookup"><span data-stu-id="9cad5-118">*pDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="9cad5-119">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="9cad5-119">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="9cad5-120">Puntatore a [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) su cui creare le risorse di effetto.</span><span class="sxs-lookup"><span data-stu-id="9cad5-120">Pointer to the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) on which to create Effect resources.</span></span>

</dd> <dt>

<span data-ttu-id="9cad5-121">*ppEffect*</span><span class="sxs-lookup"><span data-stu-id="9cad5-121">*ppEffect*</span></span> 
</dt> <dd>

<span data-ttu-id="9cad5-122">Tipo: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9cad5-122">Type: **[**ID3DX11Effect**](id3dx11effect.md)\*\***</span></span>

<span data-ttu-id="9cad5-123">Indirizzo dell'interfaccia [**ID3DX11Effect**](id3dx11effect.md) appena creata.</span><span class="sxs-lookup"><span data-stu-id="9cad5-123">Address of the newly created [**ID3DX11Effect**](id3dx11effect.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cad5-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9cad5-124">Return value</span></span>

<span data-ttu-id="9cad5-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9cad5-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9cad5-126">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9cad5-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9cad5-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="9cad5-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9cad5-128">È necessario usare [Effects 11 source](https://github.com/Microsoft/FX11) per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="9cad5-128">You must use [Effects 11 source](https://github.com/Microsoft/FX11) to build your effects-type application.</span></span> <span data-ttu-id="9cad5-129">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9cad5-129">For more info about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9cad5-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cad5-130">Requirements</span></span>



| <span data-ttu-id="9cad5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cad5-131">Requirement</span></span> | <span data-ttu-id="9cad5-132">Valore</span><span class="sxs-lookup"><span data-stu-id="9cad5-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cad5-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9cad5-133">Header</span></span><br/> | <dl> <span data-ttu-id="9cad5-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cad5-134"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cad5-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9cad5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cad5-136">Funzioni Effects 11</span><span class="sxs-lookup"><span data-stu-id="9cad5-136">Effects 11 Functions</span></span>](d3d11-graphics-reference-effects11-functions.md)
</dt> </dl>

 

