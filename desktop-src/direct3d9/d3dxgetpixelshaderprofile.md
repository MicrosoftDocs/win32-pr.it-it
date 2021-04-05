---
description: Restituisce il nome del profilo HLSL (High-Level Shader Language) più alto supportato da un determinato dispositivo.
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: Funzione D3DXGetPixelShaderProfile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetPixelShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ad1f430a95b1ff2173dceb1e0561dccf3d0ee88d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969352"
---
# <a name="d3dxgetpixelshaderprofile-function"></a><span data-ttu-id="2ff91-103">D3DXGetPixelShaderProfile (funzione)</span><span class="sxs-lookup"><span data-stu-id="2ff91-103">D3DXGetPixelShaderProfile function</span></span>

<span data-ttu-id="2ff91-104">Restituisce il nome del profilo HLSL (High-Level Shader Language) più alto supportato da un determinato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2ff91-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff91-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ff91-105">Syntax</span></span>


```C++
LPCSTR D3DXGetPixelShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="2ff91-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ff91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ff91-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ff91-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff91-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2ff91-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2ff91-109">Puntatore al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2ff91-109">Pointer to the device.</span></span> <span data-ttu-id="2ff91-110">Vedere [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="2ff91-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ff91-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ff91-111">Return value</span></span>

<span data-ttu-id="2ff91-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ff91-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ff91-113">Nome del profilo HLSL.</span><span class="sxs-lookup"><span data-stu-id="2ff91-113">The HLSL profile name.</span></span>

<span data-ttu-id="2ff91-114">Se il dispositivo non supporta i pixel shader, la funzione restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="2ff91-114">If the device does not support pixel shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ff91-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ff91-115">Remarks</span></span>

<span data-ttu-id="2ff91-116">Un profilo shader specifica la versione dell'assembly shader da usare e le funzionalità disponibili per il compilatore HLSL durante la compilazione di uno shader.</span><span class="sxs-lookup"><span data-stu-id="2ff91-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="2ff91-117">Nella tabella seguente sono elencati i profili di pixel shader supportati.</span><span class="sxs-lookup"><span data-stu-id="2ff91-117">The following table lists the pixel shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2ff91-118">Profilo shader</span><span class="sxs-lookup"><span data-stu-id="2ff91-118">Shader Profile</span></span></th>
<th><span data-ttu-id="2ff91-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ff91-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ff91-120">ps_1_1</span><span class="sxs-lookup"><span data-stu-id="2ff91-120">ps_1_1</span></span></td>
<td><span data-ttu-id="2ff91-121">Compilare per ps_1_1 versione.</span><span class="sxs-lookup"><span data-stu-id="2ff91-121">Compile to ps_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ff91-122">ps_1_2</span><span class="sxs-lookup"><span data-stu-id="2ff91-122">ps_1_2</span></span></td>
<td><span data-ttu-id="2ff91-123">Compilare per ps_1_2 versione.</span><span class="sxs-lookup"><span data-stu-id="2ff91-123">Compile to ps_1_2 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ff91-124">ps_1_3</span><span class="sxs-lookup"><span data-stu-id="2ff91-124">ps_1_3</span></span></td>
<td><span data-ttu-id="2ff91-125">Compilare per ps_1_3 versione.</span><span class="sxs-lookup"><span data-stu-id="2ff91-125">Compile to ps_1_3 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ff91-126">ps_1_4</span><span class="sxs-lookup"><span data-stu-id="2ff91-126">ps_1_4</span></span></td>
<td><span data-ttu-id="2ff91-127">Compilare per ps_1_4 versione.</span><span class="sxs-lookup"><span data-stu-id="2ff91-127">Compile to ps_1_4 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ff91-128">ps_2_0</span><span class="sxs-lookup"><span data-stu-id="2ff91-128">ps_2_0</span></span></td>
<td><span data-ttu-id="2ff91-129">Compilare per ps_2_0 versione.</span><span class="sxs-lookup"><span data-stu-id="2ff91-129">Compile to ps_2_0 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ff91-130">ps_2_a</span><span class="sxs-lookup"><span data-stu-id="2ff91-130">ps_2_a</span></span></td>
<td><span data-ttu-id="2ff91-131">Uguale al profilo ps_2_0, con le seguenti funzionalità aggiuntive disponibili per il compilatore come destinazione:</span><span class="sxs-lookup"><span data-stu-id="2ff91-131">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="2ff91-132">Il numero di registri temporanei (r #) è maggiore o uguale a 22.</span><span class="sxs-lookup"><span data-stu-id="2ff91-132">Number of Temporary Registers (r#) is greater than or equal to 22.</span></span></li>
<li><span data-ttu-id="2ff91-133">Swizzle di origine arbitrario.</span><span class="sxs-lookup"><span data-stu-id="2ff91-133">Arbitrary source swizzle.</span></span></li>
<li><span data-ttu-id="2ff91-134">Istruzioni per la sfumatura: DSX, DSY.</span><span class="sxs-lookup"><span data-stu-id="2ff91-134">Gradient instructions: dsx, dsy.</span></span></li>
<li><span data-ttu-id="2ff91-135">Predicazione.</span><span class="sxs-lookup"><span data-stu-id="2ff91-135">Predication.</span></span></li>
<li><span data-ttu-id="2ff91-136">Nessun limite di lettura della trama dipendente.</span><span class="sxs-lookup"><span data-stu-id="2ff91-136">No dependent texture read limit.</span></span></li>
<li><span data-ttu-id="2ff91-137">Nessun limite per il numero di istruzioni di trama.</span><span class="sxs-lookup"><span data-stu-id="2ff91-137">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ff91-138">ps_2_b</span><span class="sxs-lookup"><span data-stu-id="2ff91-138">ps_2_b</span></span></td>
<td><span data-ttu-id="2ff91-139">Uguale al profilo ps_2_0, con le seguenti funzionalità aggiuntive disponibili per il compilatore come destinazione:</span><span class="sxs-lookup"><span data-stu-id="2ff91-139">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="2ff91-140">Il numero di registri temporanei (r #) è maggiore o uguale a 32.</span><span class="sxs-lookup"><span data-stu-id="2ff91-140">Number of Temporary Registers (r#) is greater than or equal to 32.</span></span></li>
<li><span data-ttu-id="2ff91-141">Nessun limite per il numero di istruzioni di trama.</span><span class="sxs-lookup"><span data-stu-id="2ff91-141">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ff91-142">ps_3_0</span><span class="sxs-lookup"><span data-stu-id="2ff91-142">ps_3_0</span></span></td>
<td><span data-ttu-id="2ff91-143">Compilare per ps_3_0 versione.</span><span class="sxs-lookup"><span data-stu-id="2ff91-143">Compile to ps_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2ff91-144">Per ulteriori informazioni sulle differenze tra le versioni dello shader, vedere [differenze di pixel shader](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2ff91-144">For more information about the differences between shader versions, see [Pixel Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ff91-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ff91-145">Requirements</span></span>



| <span data-ttu-id="2ff91-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ff91-146">Requirement</span></span> | <span data-ttu-id="2ff91-147">Valore</span><span class="sxs-lookup"><span data-stu-id="2ff91-147">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff91-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ff91-148">Header</span></span><br/>  | <dl> <span data-ttu-id="2ff91-149"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ff91-149"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2ff91-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="2ff91-150">Library</span></span><br/> | <dl> <span data-ttu-id="2ff91-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ff91-151"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2ff91-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ff91-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ff91-153">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="2ff91-153">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
