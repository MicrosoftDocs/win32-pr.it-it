---
description: Restituisce il nome del profilo HLSL (High-Level Shader Language) più alto supportato da un determinato dispositivo.
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: Funzione D3DXGetVertexShaderProfile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetVertexShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 34f7ccaeba60bdd1d7c512cee3fb4da29289408a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322653"
---
# <a name="d3dxgetvertexshaderprofile-function"></a><span data-ttu-id="eae07-103">D3DXGetVertexShaderProfile (funzione)</span><span class="sxs-lookup"><span data-stu-id="eae07-103">D3DXGetVertexShaderProfile function</span></span>

<span data-ttu-id="eae07-104">Restituisce il nome del profilo HLSL (High-Level Shader Language) più alto supportato da un determinato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eae07-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="eae07-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eae07-105">Syntax</span></span>


```C++
LPCSTR D3DXGetVertexShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="eae07-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eae07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eae07-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eae07-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eae07-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="eae07-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="eae07-109">Puntatore al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eae07-109">Pointer to the device.</span></span> <span data-ttu-id="eae07-110">Vedere [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="eae07-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eae07-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eae07-111">Return value</span></span>

<span data-ttu-id="eae07-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eae07-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eae07-113">Nome del profilo HLSL.</span><span class="sxs-lookup"><span data-stu-id="eae07-113">The HLSL profile name.</span></span>

<span data-ttu-id="eae07-114">Se il dispositivo non supporta vertex shader, la funzione restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="eae07-114">If the device does not support vertex shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="eae07-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="eae07-115">Remarks</span></span>

<span data-ttu-id="eae07-116">Un profilo shader specifica la versione dell'assembly shader da usare e le funzionalità disponibili per il compilatore HLSL durante la compilazione di uno shader.</span><span class="sxs-lookup"><span data-stu-id="eae07-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="eae07-117">La tabella seguente elenca i profili vertex shader supportati.</span><span class="sxs-lookup"><span data-stu-id="eae07-117">The following table lists the vertex shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eae07-118">Profilo shader</span><span class="sxs-lookup"><span data-stu-id="eae07-118">Shader Profile</span></span></th>
<th><span data-ttu-id="eae07-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eae07-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eae07-120">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="eae07-120">vs_1_1</span></span></td>
<td><span data-ttu-id="eae07-121">Compilare per vs_1_1 versione.</span><span class="sxs-lookup"><span data-stu-id="eae07-121">Compile to vs_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eae07-122">vs_2_0</span><span class="sxs-lookup"><span data-stu-id="eae07-122">vs_2_0</span></span></td>
<td><span data-ttu-id="eae07-123">Compilare per vs_2_0 versione.</span><span class="sxs-lookup"><span data-stu-id="eae07-123">Compile to vs_2_0 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eae07-124">vs_2_a</span><span class="sxs-lookup"><span data-stu-id="eae07-124">vs_2_a</span></span></td>
<td><span data-ttu-id="eae07-125">Uguale al profilo vs_2_0, con le seguenti funzionalità aggiuntive disponibili per il compilatore come destinazione:</span><span class="sxs-lookup"><span data-stu-id="eae07-125">Same as the vs_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="eae07-126">Il numero di registri temporanei (r #) è maggiore o uguale a 13.</span><span class="sxs-lookup"><span data-stu-id="eae07-126">Number of Temporary Registers (r#) is greater than or equal to 13.</span></span></li>
<li><span data-ttu-id="eae07-127">Istruzione di controllo dinamico del flusso.</span><span class="sxs-lookup"><span data-stu-id="eae07-127">Dynamic flow control instruction.</span></span></li>
<li><span data-ttu-id="eae07-128">Predicazione.</span><span class="sxs-lookup"><span data-stu-id="eae07-128">Predication.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eae07-129">vs_3_0</span><span class="sxs-lookup"><span data-stu-id="eae07-129">vs_3_0</span></span></td>
<td><span data-ttu-id="eae07-130">Compilare per vs_3_0 versione.</span><span class="sxs-lookup"><span data-stu-id="eae07-130">Compile to vs_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="eae07-131">Per altre informazioni sulle differenze tra le versioni dello shader, vedere [differenze di vertex shader](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).</span><span class="sxs-lookup"><span data-stu-id="eae07-131">For more information about the differences between shader versions, see [Vertex Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eae07-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eae07-132">Requirements</span></span>



| <span data-ttu-id="eae07-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="eae07-133">Requirement</span></span> | <span data-ttu-id="eae07-134">Valore</span><span class="sxs-lookup"><span data-stu-id="eae07-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eae07-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eae07-135">Header</span></span><br/>  | <dl> <span data-ttu-id="eae07-136"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="eae07-136"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="eae07-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="eae07-137">Library</span></span><br/> | <dl> <span data-ttu-id="eae07-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eae07-138"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="eae07-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eae07-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eae07-140">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="eae07-140">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
