---
title: Struttura D3DX11_PASS_DESC (D3dx11effect. h)
description: Descrive un passaggio di effetto, che contiene lo stato della pipeline.
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- Struttura D3DX11_PASS_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4d7f10268db0515b2f7e3772332b34427ba67a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982550"
---
# <a name="d3dx11_pass_desc-structure"></a><span data-ttu-id="870c5-104">D3DX11 \_ pass \_ desc-struttura</span><span class="sxs-lookup"><span data-stu-id="870c5-104">D3DX11\_PASS\_DESC structure</span></span>

<span data-ttu-id="870c5-105">Descrive un passaggio di effetto, che contiene lo stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="870c5-105">Describes an effect pass, which contains pipeline state.</span></span>

## <a name="syntax"></a><span data-ttu-id="870c5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="870c5-106">Syntax</span></span>


```C++
typedef struct _D3DX11_PASS_DESC {
  LPCSTR Name;
  UINT   Annotations;
  BYTE   *pIAInputSignature;
  SIZE_T IAInputSignatureSize;
  UINT   StencilRef;
  UINT   SampleMask;
  FLOAT  BlendFactor[4];
} D3DX11_PASS_DESC;
```



## <a name="members"></a><span data-ttu-id="870c5-107">Members</span><span class="sxs-lookup"><span data-stu-id="870c5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="870c5-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="870c5-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="870c5-109">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="870c5-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="870c5-110">Nome del passaggio (**null** se non anonimo).</span><span class="sxs-lookup"><span data-stu-id="870c5-110">Name of this pass (**NULL** if not anonymous).</span></span>

</dd> <dt>

<span data-ttu-id="870c5-111">**annotazioni**</span><span class="sxs-lookup"><span data-stu-id="870c5-111">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="870c5-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="870c5-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="870c5-113">Numero di annotazioni in questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="870c5-113">Number of annotations on this pass.</span></span>

</dd> <dt>

<span data-ttu-id="870c5-114">**pIAInputSignature**</span><span class="sxs-lookup"><span data-stu-id="870c5-114">**pIAInputSignature**</span></span>
</dt> <dd>

<span data-ttu-id="870c5-115">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="870c5-115">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="870c5-116">Firma da vertex shader o geometry shader (se non è presente alcun vertex shader) o **null** se non esiste alcun vertex shader.</span><span class="sxs-lookup"><span data-stu-id="870c5-116">Signature from the vertex shader or geometry shader (if there is no vertex shader) or **NULL** if neither exists.</span></span>

</dd> <dt>

<span data-ttu-id="870c5-117">**IAInputSignatureSize**</span><span class="sxs-lookup"><span data-stu-id="870c5-117">**IAInputSignatureSize**</span></span>
</dt> <dd>

<span data-ttu-id="870c5-118">Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="870c5-118">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="870c5-119">Dimensioni singature in byte.</span><span class="sxs-lookup"><span data-stu-id="870c5-119">Singature size in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="870c5-120">**StencilRef**</span><span class="sxs-lookup"><span data-stu-id="870c5-120">**StencilRef**</span></span>
</dt> <dd>

<span data-ttu-id="870c5-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="870c5-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="870c5-122">Il valore di riferimento stencil usato nello stato di stencil Depth.</span><span class="sxs-lookup"><span data-stu-id="870c5-122">The stencil-reference value used in the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="870c5-123">**SampleMask**</span><span class="sxs-lookup"><span data-stu-id="870c5-123">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="870c5-124">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="870c5-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="870c5-125">Maschera di esempio per lo stato di Blend.</span><span class="sxs-lookup"><span data-stu-id="870c5-125">The sample mask for the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="870c5-126">**BlendFactor**</span><span class="sxs-lookup"><span data-stu-id="870c5-126">**BlendFactor**</span></span>
</dt> <dd>

<span data-ttu-id="870c5-127">Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="870c5-127">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="870c5-128">Fattori di Blend per componente (RGBA) per lo stato di Blend.</span><span class="sxs-lookup"><span data-stu-id="870c5-128">The per-component blend factors (RGBA) for the blend state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="870c5-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="870c5-129">Remarks</span></span>

<span data-ttu-id="870c5-130">D3DX11 \_ pass \_ desc viene usato con [**ID3DX11EffectPass:: getdesc**](id3dx11effectpass-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="870c5-130">D3DX11\_PASS\_DESC is used with [**ID3DX11EffectPass::GetDesc**](id3dx11effectpass-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="870c5-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="870c5-131">Requirements</span></span>



| <span data-ttu-id="870c5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="870c5-132">Requirement</span></span> | <span data-ttu-id="870c5-133">Valore</span><span class="sxs-lookup"><span data-stu-id="870c5-133">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="870c5-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="870c5-134">Header</span></span><br/> | <dl> <span data-ttu-id="870c5-135"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="870c5-135"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="870c5-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="870c5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="870c5-137">Strutture Effects 11</span><span class="sxs-lookup"><span data-stu-id="870c5-137">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

