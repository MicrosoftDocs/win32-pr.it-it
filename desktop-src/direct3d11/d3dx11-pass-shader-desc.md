---
title: Struttura D3DX11_PASS_SHADER_DESC (D3dx11effect. h)
description: Descrive un passaggio di effetto.
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- Struttura D3DX11_PASS_SHADER_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cac6e842dabeaabc60451737fae56eb2cb61915
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982547"
---
# <a name="d3dx11_pass_shader_desc-structure"></a><span data-ttu-id="ecd2b-104">D3DX11 \_ passare la \_ \_ struttura desc shader</span><span class="sxs-lookup"><span data-stu-id="ecd2b-104">D3DX11\_PASS\_SHADER\_DESC structure</span></span>

<span data-ttu-id="ecd2b-105">Descrive un passaggio di effetto.</span><span class="sxs-lookup"><span data-stu-id="ecd2b-105">Describes an effect pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecd2b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecd2b-106">Syntax</span></span>


```C++
typedef struct _D3DX11_PASS_SHADER_DESC {
  ID3DX11EffectShaderVariable *pShaderVariable;
  UINT                        ShaderIndex;
} D3DX11_PASS_SHADER_DESC;
```



## <a name="members"></a><span data-ttu-id="ecd2b-107">Members</span><span class="sxs-lookup"><span data-stu-id="ecd2b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ecd2b-108">**pShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="ecd2b-108">**pShaderVariable**</span></span>
</dt> <dd>

<span data-ttu-id="ecd2b-109">Tipo: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="ecd2b-109">Type: **[**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="ecd2b-110">Variabile da cui proviene questo shader.</span><span class="sxs-lookup"><span data-stu-id="ecd2b-110">The variable that this shader came from.</span></span>

</dd> <dt>

<span data-ttu-id="ecd2b-111">**ShaderIndex**</span><span class="sxs-lookup"><span data-stu-id="ecd2b-111">**ShaderIndex**</span></span>
</dt> <dd>

<span data-ttu-id="ecd2b-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ecd2b-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ecd2b-113">Elemento di pShaderVariable (se una matrice) o 0 se non applicabile.</span><span class="sxs-lookup"><span data-stu-id="ecd2b-113">The element of pShaderVariable (if an array) or 0 if not applicable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ecd2b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ecd2b-114">Remarks</span></span>

<span data-ttu-id="ecd2b-115">D3DX11 \_ pass \_ shader \_ desc viene usato con i metodi [**ID3DX11EffectPass**](id3dx11effectpass.md) Get \* ShaderDesc.</span><span class="sxs-lookup"><span data-stu-id="ecd2b-115">D3DX11\_PASS\_SHADER\_DESC is used with [**ID3DX11EffectPass**](id3dx11effectpass.md) Get\*ShaderDesc methods.</span></span>

<span data-ttu-id="ecd2b-116">Se si tratta di un'assegnazione shader inline, l'interfaccia restituita sarà una variabile shader anonima, che non può essere recuperata in altro modo.</span><span class="sxs-lookup"><span data-stu-id="ecd2b-116">If this is an inline shader assignment, the returned interface will be an anonymous shader variable, which is not retrievable any other way.</span></span> <span data-ttu-id="ecd2b-117">Il nome nella variabile Description sarà "$Anonymous".</span><span class="sxs-lookup"><span data-stu-id="ecd2b-117">It's name in the variable description will be "$Anonymous".</span></span> <span data-ttu-id="ecd2b-118">Se non è presente alcuna assegnazione di questo tipo nel blocco Pass, pShaderVariable! = **null**, ma pShaderVariable->IsValid () = = **false**.</span><span class="sxs-lookup"><span data-stu-id="ecd2b-118">If there is no assignment of this type in the pass block, pShaderVariable != **NULL**, but pShaderVariable->IsValid() == **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecd2b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecd2b-119">Requirements</span></span>



| <span data-ttu-id="ecd2b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecd2b-120">Requirement</span></span> | <span data-ttu-id="ecd2b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ecd2b-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecd2b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ecd2b-122">Header</span></span><br/> | <dl> <span data-ttu-id="ecd2b-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecd2b-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecd2b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecd2b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecd2b-125">Strutture Effects 11</span><span class="sxs-lookup"><span data-stu-id="ecd2b-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

