---
description: Descrive i dati contenuti nell'enumerazione.
ms.assetid: 6d494fe6-fcd5-4e71-939c-257978b41499
title: Enumerazione D3DXPARAMETER_TYPE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 16ff89feb694bb6aae550422b6f9546c2268fc07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354154"
---
# <a name="d3dxparameter_type-enumeration"></a><span data-ttu-id="8e5db-103">\_Enumerazione del tipo D3DXPARAMETER</span><span class="sxs-lookup"><span data-stu-id="8e5db-103">D3DXPARAMETER\_TYPE enumeration</span></span>

<span data-ttu-id="8e5db-104">Descrive i dati contenuti nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="8e5db-104">Describes the data contained by the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e5db-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e5db-105">Syntax</span></span>


```C++
typedef enum D3DXPARAMETER_TYPE { 
  D3DXPT_VOID,
  D3DXPT_BOOL,
  D3DXPT_INT,
  D3DXPT_FLOAT,
  D3DXPT_STRING,
  D3DXPT_TEXTURE,
  D3DXPT_TEXTURE1D,
  D3DXPT_TEXTURE2D,
  D3DXPT_TEXTURE3D,
  D3DXPT_TEXTURECUBE,
  D3DXPT_SAMPLER,
  D3DXPT_SAMPLER1D,
  D3DXPT_SAMPLER2D,
  D3DXPT_SAMPLER3D,
  D3DXPT_SAMPLERCUBE,
  D3DXPT_PIXELSHADER,
  D3DXPT_VERTEXSHADER,
  D3DXPT_PIXELFRAGMENT,
  D3DXPT_VERTEXFRAGMENT,
  D3DXPT_UNSUPPORTED,
  D3DXPT_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_TYPE, *LPD3DXPARAMETER_TYPE;
```



## <a name="constants"></a><span data-ttu-id="8e5db-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="8e5db-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8e5db-107"><span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT \_ void**</span><span class="sxs-lookup"><span data-stu-id="8e5db-107"><span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT\_VOID**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-108">Il parametro è un puntatore void.</span><span class="sxs-lookup"><span data-stu-id="8e5db-108">Parameter is a void pointer.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-109"><span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**\_Bool D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-109"><span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**D3DXPT\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-110">Il parametro è un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="8e5db-110">Parameter is a Boolean.</span></span> <span data-ttu-id="8e5db-111">Qualsiasi valore diverso da zero passato in [**ID3DXConstantTable::**](id3dxconstanttable--setbool.md)SetValue, [**ID3DXConstantTable:: SetBoolArray**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable:: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: sevector**](id3dxconstanttable--setvector.md)o [**ID3DXConstantTable:: SetVectorArray**](id3dxconstanttable--setvectorarray.md) verrà mappato a 1 (true) prima di essere scritto nella tabella delle costanti; in caso contrario, il valore verrà impostato su 0 nella tabella Constant.</span><span class="sxs-lookup"><span data-stu-id="8e5db-111">Any non-zero value passed into [**ID3DXConstantTable::SetBool**](id3dxconstanttable--setbool.md), [**ID3DXConstantTable::SetBoolArray**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable::SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md), or [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) will be mapped to 1 (TRUE) before being written into the constant table; otherwise, the value will be set to 0 in the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-112"><span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**\_Int D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-112"><span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT\_INT**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-113">Il parametro è un numero intero.</span><span class="sxs-lookup"><span data-stu-id="8e5db-113">Parameter is an integer.</span></span> <span data-ttu-id="8e5db-114">Tutti i valori a virgola mobile passati in [**ID3DXConstantTable:: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: sevector**](id3dxconstanttable--setvector.md)o [**ID3DXConstantTable:: SetVectorArray**](id3dxconstanttable--setvectorarray.md) verranno arrotondati (a zero posizioni decimali) prima di essere scritti nella tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="8e5db-114">Any floating-point values passed into [**ID3DXConstantTable::SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md), or [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) will be rounded off (to zero decimal places) before being written into the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-115"><span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**\_Float D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-115"><span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT\_FLOAT**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-116">Il parametro è un numero a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="8e5db-116">Parameter is a floating-point number.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-117"><span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**\_Stringa D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-117"><span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**D3DXPT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-118">Il parametro è una stringa.</span><span class="sxs-lookup"><span data-stu-id="8e5db-118">Parameter is a string.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-119"><span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**\_Trama D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-119"><span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**D3DXPT\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-120">Il parametro è una trama.</span><span class="sxs-lookup"><span data-stu-id="8e5db-120">Parameter is a texture.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-121"><span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**\_TEXTURE1D D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-121"><span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT\_TEXTURE1D**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-122">Il parametro è una trama 1D.</span><span class="sxs-lookup"><span data-stu-id="8e5db-122">Parameter is a 1D texture.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-123"><span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**\_TEXTURE2D D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-123"><span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT\_TEXTURE2D**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-124">Il parametro è una trama 2D.</span><span class="sxs-lookup"><span data-stu-id="8e5db-124">Parameter is a 2D texture.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-125"><span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**\_TEXTURE3D D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-125"><span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT\_TEXTURE3D**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-126">Il parametro è una trama 3D.</span><span class="sxs-lookup"><span data-stu-id="8e5db-126">Parameter is a 3D texture.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-127"><span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**\_TEXTURECUBE D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-127"><span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT\_TEXTURECUBE**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-128">Il parametro è una trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="8e5db-128">Parameter is a cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-129"><span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**\_Campionatore D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-129"><span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**D3DXPT\_SAMPLER**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-130">Il parametro è un campionatore.</span><span class="sxs-lookup"><span data-stu-id="8e5db-130">Parameter is a sampler.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-131"><span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**\_SAMPLER1D D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-131"><span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT\_SAMPLER1D**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-132">Il parametro è un campionatore 1D.</span><span class="sxs-lookup"><span data-stu-id="8e5db-132">Parameter is a 1D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-133"><span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**\_SAMPLER2D D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-133"><span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT\_SAMPLER2D**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-134">Il parametro è un campionatore 2D.</span><span class="sxs-lookup"><span data-stu-id="8e5db-134">Parameter is a 2D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-135"><span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**\_SAMPLER3D D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-135"><span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT\_SAMPLER3D**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-136">Il parametro è un campionatore 3D.</span><span class="sxs-lookup"><span data-stu-id="8e5db-136">Parameter is a 3D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-137"><span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**\_SAMPLERCUBE D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-137"><span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT\_SAMPLERCUBE**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-138">Il parametro è un sampler del cubo.</span><span class="sxs-lookup"><span data-stu-id="8e5db-138">Parameter is a cube sampler.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-139"><span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**\_PIXELSHADER D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-139"><span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT\_PIXELSHADER**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-140">Il parametro è un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="8e5db-140">Parameter is a pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-141"><span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**\_VERTEXSHADER D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-141"><span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT\_VERTEXSHADER**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-142">Il parametro è un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="8e5db-142">Parameter is a vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-143"><span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**\_PIXELFRAGMENT D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-143"><span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT\_PIXELFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-144">Il parametro è un frammento pixel shader.</span><span class="sxs-lookup"><span data-stu-id="8e5db-144">Parameter is a pixel shader fragment.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-145"><span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**\_VERTEXFRAGMENT D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="8e5db-145"><span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT\_VERTEXFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-146">Il parametro è un frammento del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="8e5db-146">Parameter is a vertex shader fragment.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-147"><span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="8e5db-147"><span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT\_UNSUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-148">Il parametro non è supportato.</span><span class="sxs-lookup"><span data-stu-id="8e5db-148">Parameter is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8e5db-149"><span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8e5db-149"><span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="8e5db-150">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8e5db-150">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="8e5db-151">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8e5db-151">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="8e5db-152">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8e5db-152">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e5db-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e5db-153">Requirements</span></span>



| <span data-ttu-id="8e5db-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e5db-154">Requirement</span></span> | <span data-ttu-id="8e5db-155">Valore</span><span class="sxs-lookup"><span data-stu-id="8e5db-155">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e5db-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e5db-156">Header</span></span><br/> | <dl> <span data-ttu-id="8e5db-157"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e5db-157"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e5db-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e5db-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e5db-159">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="8e5db-159">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="8e5db-160">**\_TYPEINFO D3DXSHADER**</span><span class="sxs-lookup"><span data-stu-id="8e5db-160">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="8e5db-161">**D3DXCONSTANT \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="8e5db-161">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




