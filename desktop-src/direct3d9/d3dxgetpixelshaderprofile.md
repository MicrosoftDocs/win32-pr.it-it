---
description: 'Funzione D3DXGetPixelShaderProfile: restituisce il nome del profilo HLSL (High Level Shader Language) più alto supportato da un determinato dispositivo.'
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: Funzione D3DXGetPixelShaderProfile (D3DX9Shader.h)
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
ms.openlocfilehash: 7d24e19d49a8a96f91847892f519ef6c06d25ef5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114438"
---
# <a name="d3dxgetpixelshaderprofile-function"></a><span data-ttu-id="20805-103">Funzione D3DXGetPixelShaderProfile</span><span class="sxs-lookup"><span data-stu-id="20805-103">D3DXGetPixelShaderProfile function</span></span>

<span data-ttu-id="20805-104">Restituisce il nome del profilo HLSL (High-Level Shader Language) più alto supportato da un determinato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20805-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="20805-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20805-105">Syntax</span></span>


```C++
LPCSTR D3DXGetPixelShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="20805-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="20805-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20805-107">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="20805-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20805-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="20805-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="20805-109">Puntatore al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20805-109">Pointer to the device.</span></span> <span data-ttu-id="20805-110">Vedere [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="20805-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20805-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20805-111">Return value</span></span>

<span data-ttu-id="20805-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20805-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20805-113">Nome del profilo HLSL.</span><span class="sxs-lookup"><span data-stu-id="20805-113">The HLSL profile name.</span></span>

<span data-ttu-id="20805-114">Se il dispositivo non supporta pixel shader, la funzione restituisce **NULL.**</span><span class="sxs-lookup"><span data-stu-id="20805-114">If the device does not support pixel shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="20805-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="20805-115">Remarks</span></span>

<span data-ttu-id="20805-116">Un profilo shader specifica la versione dell'assembly shader da usare e le funzionalità disponibili per il compilatore HLSL durante la compilazione di uno shader.</span><span class="sxs-lookup"><span data-stu-id="20805-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="20805-117">Nella tabella seguente sono elencati pixel shader profili supportati.</span><span class="sxs-lookup"><span data-stu-id="20805-117">The following table lists the pixel shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20805-118">Profilo shader</span><span class="sxs-lookup"><span data-stu-id="20805-118">Shader Profile</span></span></th>
<th><span data-ttu-id="20805-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20805-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="20805-120">ps_1_1</span><span class="sxs-lookup"><span data-stu-id="20805-120">ps_1_1</span></span></td>
<td><span data-ttu-id="20805-121">Eseguire la compilazione ps_1_1 versione.</span><span class="sxs-lookup"><span data-stu-id="20805-121">Compile to ps_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20805-122">ps_1_2</span><span class="sxs-lookup"><span data-stu-id="20805-122">ps_1_2</span></span></td>
<td><span data-ttu-id="20805-123">Compilare per ps_1_2 versione.</span><span class="sxs-lookup"><span data-stu-id="20805-123">Compile to ps_1_2 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20805-124">ps_1_3</span><span class="sxs-lookup"><span data-stu-id="20805-124">ps_1_3</span></span></td>
<td><span data-ttu-id="20805-125">Compilare per ps_1_3 versione.</span><span class="sxs-lookup"><span data-stu-id="20805-125">Compile to ps_1_3 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20805-126">ps_1_4</span><span class="sxs-lookup"><span data-stu-id="20805-126">ps_1_4</span></span></td>
<td><span data-ttu-id="20805-127">Eseguire la compilazione ps_1_4 versione.</span><span class="sxs-lookup"><span data-stu-id="20805-127">Compile to ps_1_4 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20805-128">ps_2_0</span><span class="sxs-lookup"><span data-stu-id="20805-128">ps_2_0</span></span></td>
<td><span data-ttu-id="20805-129">Eseguire la compilazione ps_2_0 versione.</span><span class="sxs-lookup"><span data-stu-id="20805-129">Compile to ps_2_0 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20805-130">ps_2_a</span><span class="sxs-lookup"><span data-stu-id="20805-130">ps_2_a</span></span></td>
<td><span data-ttu-id="20805-131">Uguale al profilo ps_2_0, con le funzionalità aggiuntive seguenti disponibili per il compilatore come destinazione:</span><span class="sxs-lookup"><span data-stu-id="20805-131">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="20805-132">Il numero di registri temporanei (r#) è maggiore o uguale a 22.</span><span class="sxs-lookup"><span data-stu-id="20805-132">Number of Temporary Registers (r#) is greater than or equal to 22.</span></span></li>
<li><span data-ttu-id="20805-133">Swizzle di origine arbitrario.</span><span class="sxs-lookup"><span data-stu-id="20805-133">Arbitrary source swizzle.</span></span></li>
<li><span data-ttu-id="20805-134">Istruzioni per la sfumatura: dsx, dsy.</span><span class="sxs-lookup"><span data-stu-id="20805-134">Gradient instructions: dsx, dsy.</span></span></li>
<li><span data-ttu-id="20805-135">Predicazione.</span><span class="sxs-lookup"><span data-stu-id="20805-135">Predication.</span></span></li>
<li><span data-ttu-id="20805-136">Nessun limite di lettura della trama dipendente.</span><span class="sxs-lookup"><span data-stu-id="20805-136">No dependent texture read limit.</span></span></li>
<li><span data-ttu-id="20805-137">Nessun limite per il numero di istruzioni di trama.</span><span class="sxs-lookup"><span data-stu-id="20805-137">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20805-138">ps_2_b</span><span class="sxs-lookup"><span data-stu-id="20805-138">ps_2_b</span></span></td>
<td><span data-ttu-id="20805-139">Uguale al profilo ps_2_0, con le funzionalità aggiuntive seguenti disponibili per il compilatore come destinazione:</span><span class="sxs-lookup"><span data-stu-id="20805-139">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="20805-140">Il numero di registri temporanei (r#) è maggiore o uguale a 32.</span><span class="sxs-lookup"><span data-stu-id="20805-140">Number of Temporary Registers (r#) is greater than or equal to 32.</span></span></li>
<li><span data-ttu-id="20805-141">Nessun limite per il numero di istruzioni di trama.</span><span class="sxs-lookup"><span data-stu-id="20805-141">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20805-142">ps_3_0</span><span class="sxs-lookup"><span data-stu-id="20805-142">ps_3_0</span></span></td>
<td><span data-ttu-id="20805-143">Compilare per ps_3_0 versione.</span><span class="sxs-lookup"><span data-stu-id="20805-143">Compile to ps_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="20805-144">Per altre informazioni sulle differenze tra le versioni dello shader, vedere [Differenze di pixel shader.](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md)</span><span class="sxs-lookup"><span data-stu-id="20805-144">For more information about the differences between shader versions, see [Pixel Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20805-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20805-145">Requirements</span></span>



| <span data-ttu-id="20805-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="20805-146">Requirement</span></span> | <span data-ttu-id="20805-147">Valore</span><span class="sxs-lookup"><span data-stu-id="20805-147">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20805-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20805-148">Header</span></span><br/>  | <dl> <span data-ttu-id="20805-149"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="20805-149"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="20805-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="20805-150">Library</span></span><br/> | <dl> <span data-ttu-id="20805-151"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="20805-151"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="20805-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20805-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20805-153">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="20805-153">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
