---
title: Struttura D3DX11_EFFECT_SHADER_DESC (D3dx11effect. h)
description: Descrive un effetto shader.
ms.assetid: 4377eec6-f331-4cad-bf16-189d6296f886
keywords:
- Struttura D3DX11_EFFECT_SHADER_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c518d4f7930d0651e519d23218121b8ed4bed288
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886319"
---
# <a name="d3dx11_effect_shader_desc-structure"></a><span data-ttu-id="68275-104">\_ \_ Struttura desc shader Effect \_ D3DX11</span><span class="sxs-lookup"><span data-stu-id="68275-104">D3DX11\_EFFECT\_SHADER\_DESC structure</span></span>

<span data-ttu-id="68275-105">Descrive un effetto shader.</span><span class="sxs-lookup"><span data-stu-id="68275-105">Describes an effect shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="68275-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68275-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_SHADER_DESC {
  const BYTE *pInputSignature;
  BOOL       IsInline;
  const BYTE *pBytecode;
  UINT       BytecodeLength;
  LPCSTR     SODecls[D3D11_SO_STREAM_COUNT];
  UINT       RasterizedStream;
  UINT       NumInputSignatureEntries;
  UINT       NumOutputSignatureEntries;
  UINT       NumPatchConstantSignatureEntries;
} D3DX11_EFFECT_SHADER_DESC;
```



## <a name="members"></a><span data-ttu-id="68275-107">Members</span><span class="sxs-lookup"><span data-stu-id="68275-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="68275-108">**pInputSignature**</span><span class="sxs-lookup"><span data-stu-id="68275-108">**pInputSignature**</span></span>
</dt> <dd>

<span data-ttu-id="68275-109">Tipo: **const [**byte**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="68275-109">Type: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="68275-110">Passato a CreateInputLayout.</span><span class="sxs-lookup"><span data-stu-id="68275-110">Passed into CreateInputLayout.</span></span> <span data-ttu-id="68275-111">Valido solo in un vertex shader o in un geometry shader.</span><span class="sxs-lookup"><span data-stu-id="68275-111">Only valid on a vertex shader or geometry shader.</span></span> <span data-ttu-id="68275-112">Vedere [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="68275-112">See [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).</span></span>

</dd> <dt>

<span data-ttu-id="68275-113">**IsInline**</span><span class="sxs-lookup"><span data-stu-id="68275-113">**IsInline**</span></span>
</dt> <dd>

<span data-ttu-id="68275-114">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="68275-114">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="68275-115">**True** se lo shader è definito inline; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="68275-115">**TRUE** is the shader is defined inline; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="68275-116">**pBytecode**</span><span class="sxs-lookup"><span data-stu-id="68275-116">**pBytecode**</span></span>
</dt> <dd>

<span data-ttu-id="68275-117">Tipo: **const [**byte**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="68275-117">Type: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="68275-118">Bytecode dello shader.</span><span class="sxs-lookup"><span data-stu-id="68275-118">Shader bytecode.</span></span>

</dd> <dt>

<span data-ttu-id="68275-119">**BytecodeLength**</span><span class="sxs-lookup"><span data-stu-id="68275-119">**BytecodeLength**</span></span>
</dt> <dd>

<span data-ttu-id="68275-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="68275-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="68275-121">Lunghezza di pBytecode.</span><span class="sxs-lookup"><span data-stu-id="68275-121">The length of pBytecode.</span></span>

</dd> <dt>

<span data-ttu-id="68275-122">**SODecls**</span><span class="sxs-lookup"><span data-stu-id="68275-122">**SODecls**</span></span>
</dt> <dd>

<span data-ttu-id="68275-123">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="68275-123">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="68275-124">Stringa di dichiarazione del flusso in uscita (per la geometria shader con).</span><span class="sxs-lookup"><span data-stu-id="68275-124">Stream out declaration string (for geometry shader with SO).</span></span>

</dd> <dt>

<span data-ttu-id="68275-125">**RasterizedStream**</span><span class="sxs-lookup"><span data-stu-id="68275-125">**RasterizedStream**</span></span>
</dt> <dd>

<span data-ttu-id="68275-126">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="68275-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="68275-127">Indica il flusso rasterizzato.</span><span class="sxs-lookup"><span data-stu-id="68275-127">Indicates which stream is rasterized.</span></span> <span data-ttu-id="68275-128">D3D11 Geometry shaders può restituire fino a quattro flussi di dati, uno dei quali può essere rasterizzato.</span><span class="sxs-lookup"><span data-stu-id="68275-128">D3D11 geometry shaders can output up to four streams of data, one of which can be rasterized.</span></span>

</dd> <dt>

<span data-ttu-id="68275-129">**NumInputSignatureEntries**</span><span class="sxs-lookup"><span data-stu-id="68275-129">**NumInputSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="68275-130">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="68275-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="68275-131">Numero di voci nella firma di input.</span><span class="sxs-lookup"><span data-stu-id="68275-131">Number of entries in the input signature.</span></span>

</dd> <dt>

<span data-ttu-id="68275-132">**NumOutputSignatureEntries**</span><span class="sxs-lookup"><span data-stu-id="68275-132">**NumOutputSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="68275-133">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="68275-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="68275-134">Numero di voci nella firma di output.</span><span class="sxs-lookup"><span data-stu-id="68275-134">Number of entries in the output signature.</span></span>

</dd> <dt>

<span data-ttu-id="68275-135">**NumPatchConstantSignatureEntries**</span><span class="sxs-lookup"><span data-stu-id="68275-135">**NumPatchConstantSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="68275-136">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="68275-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="68275-137">Numero di voci nella firma costante della patch.</span><span class="sxs-lookup"><span data-stu-id="68275-137">Number of entries in the patch constant signature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68275-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="68275-138">Remarks</span></span>

<span data-ttu-id="68275-139">D3DX11 \_ Effect \_ shader \_ desc viene usato con [**ID3DX11EffectShaderVariable:: GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).</span><span class="sxs-lookup"><span data-stu-id="68275-139">D3DX11\_EFFECT\_SHADER\_DESC is used with [**ID3DX11EffectShaderVariable::GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68275-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68275-140">Requirements</span></span>



| <span data-ttu-id="68275-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="68275-141">Requirement</span></span> | <span data-ttu-id="68275-142">Valore</span><span class="sxs-lookup"><span data-stu-id="68275-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="68275-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68275-143">Header</span></span><br/> | <dl> <span data-ttu-id="68275-144"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="68275-144"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68275-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68275-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68275-146">Strutture Effects 11</span><span class="sxs-lookup"><span data-stu-id="68275-146">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

