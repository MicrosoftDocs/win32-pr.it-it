---
description: Questa funzione, che crea un oggetto di Reflection shader per il recupero di informazioni su uno shader compilato, non esiste più. Usare invece D3DReflect o D3D11Reflect.
ms.assetid: 7090418c-1940-4f07-b075-937e3399613c
title: Funzione D3DX10ReflectShader (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ReflectShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 15201bcbde2792bbd31cbf4dad7b87d7ddac5053
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322771"
---
# <a name="d3dx10reflectshader-function"></a><span data-ttu-id="8b764-104">D3DX10ReflectShader (funzione)</span><span class="sxs-lookup"><span data-stu-id="8b764-104">D3DX10ReflectShader function</span></span>

<span data-ttu-id="8b764-105">Questa funzione, che crea un oggetto di Reflection shader per il recupero di informazioni su uno shader compilato, non esiste più.</span><span class="sxs-lookup"><span data-stu-id="8b764-105">This function -- which creates a shader-reflection object for retrieving information about a compiled shader -- no longer exists.</span></span> <span data-ttu-id="8b764-106">Usare invece [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) o [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).</span><span class="sxs-lookup"><span data-stu-id="8b764-106">Instead, use [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) or [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b764-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b764-107">Syntax</span></span>


```C++
HRESULT D3DX10ReflectShader(
  _In_  const void                    *pShaderBytecode,
  _In_        SIZE_T                  BytecodeLength,
  _Out_       ID3D10ShaderReflection1 **ppReflector
);
```



## <a name="parameters"></a><span data-ttu-id="8b764-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b764-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b764-109">*pShaderBytecode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b764-109">*pShaderBytecode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b764-110">Tipo: **const \* void**</span><span class="sxs-lookup"><span data-stu-id="8b764-110">Type: **const void\***</span></span>

<span data-ttu-id="8b764-111">Puntatore allo shader compilato.</span><span class="sxs-lookup"><span data-stu-id="8b764-111">A pointer to the compiled shader.</span></span> <span data-ttu-id="8b764-112">Per ottenere questo puntatore, vedere [ottenere un puntatore a uno shader compilato](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span><span class="sxs-lookup"><span data-stu-id="8b764-112">To get this pointer see [Getting a Pointer to a Compiled Shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b764-113">*BytecodeLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b764-113">*BytecodeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b764-114">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b764-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b764-115">Lunghezza di pShaderBytecode.</span><span class="sxs-lookup"><span data-stu-id="8b764-115">Length of pShaderBytecode.</span></span>

</dd> <dt>

<span data-ttu-id="8b764-116">*ppReflector* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b764-116">*ppReflector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b764-117">Tipo: **[ **ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***</span><span class="sxs-lookup"><span data-stu-id="8b764-117">Type: **[**ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***</span></span>

<span data-ttu-id="8b764-118">Indirizzo di un'interfaccia di Reflection shader (vedere [**interfaccia ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)).</span><span class="sxs-lookup"><span data-stu-id="8b764-118">Address of a shader reflection interface (see [**ID3D10ShaderReflection1 Interface**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1).)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b764-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b764-119">Return value</span></span>

<span data-ttu-id="8b764-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8b764-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8b764-121">Restituisce uno dei seguenti [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8b764-121">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8b764-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b764-122">Remarks</span></span>

<span data-ttu-id="8b764-123">Di seguito è riportato un esempio di creazione di un oggetto di Reflection shader.</span><span class="sxs-lookup"><span data-stu-id="8b764-123">Here is an example of creating a shader-reflection object.</span></span> <span data-ttu-id="8b764-124">Nell'esempio si presuppone che si inizi con uno shader compilato (visualizzato come</span><span class="sxs-lookup"><span data-stu-id="8b764-124">The example assumes you start with a compiled shader (shown as</span></span>


```
pVSBuf
```



<span data-ttu-id="8b764-125">come è possibile vedere nell' [esempio HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="8b764-125">which you can see in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span></span>


```
ID3D10ShaderReflection1* pIShaderReflection1 = NULL;
D3D10_SHADER_DESC desc;
hr = D3D10ReflectShader( (void*) pVSBuf->GetBufferPointer(), pVSBuf->GetBufferSize(),
    &pIShaderReflection1 );
if( pIShaderReflection1 )
{
    pIShaderReflection1->GetDesc( &desc );
}
```



## <a name="requirements"></a><span data-ttu-id="8b764-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b764-126">Requirements</span></span>



| <span data-ttu-id="8b764-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b764-127">Requirement</span></span> | <span data-ttu-id="8b764-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8b764-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b764-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b764-129">Header</span></span><br/> | <dl> <span data-ttu-id="8b764-130"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b764-130"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b764-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b764-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b764-132">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="8b764-132">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
