---
title: Metodo getdesc ID3DX11EffectType (D3dx11effect. h)
description: Ottenere una descrizione del tipo di effetto.
ms.assetid: 08a8a1b6-fe2d-431b-a0e4-d628f0ceb1a0
keywords:
- Metodo getdesc Direct3D 11
- Metodo getdesc Direct3D 11, interfaccia ID3DX11EffectType
- Interfaccia ID3DX11EffectType Direct3D 11, metodo getdesc
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1ee52e4c6628c00b0155e5bd3081b6c4fd8c46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996241"
---
# <a name="id3dx11effecttypegetdesc-method"></a><span data-ttu-id="f880a-106">Metodo ID3DX11EffectType:: getdesc</span><span class="sxs-lookup"><span data-stu-id="f880a-106">ID3DX11EffectType::GetDesc method</span></span>

<span data-ttu-id="f880a-107">Ottenere una descrizione del tipo di effetto.</span><span class="sxs-lookup"><span data-stu-id="f880a-107">Get an effect-type description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f880a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f880a-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_TYPE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="f880a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f880a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f880a-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="f880a-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="f880a-111">Tipo: **[ **D3DX11 \_ Effect \_ Type \_ desc**](d3dx11-effect-type-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="f880a-111">Type: **[**D3DX11\_EFFECT\_TYPE\_DESC**](d3dx11-effect-type-desc.md)\***</span></span>

<span data-ttu-id="f880a-112">Puntatore a una descrizione del tipo di effetto.</span><span class="sxs-lookup"><span data-stu-id="f880a-112">A pointer to an effect-type description.</span></span> <span data-ttu-id="f880a-113">Vedere [**la \_ \_ \_ Descrizione del tipo di effetto D3DX11**](d3dx11-effect-type-desc.md).</span><span class="sxs-lookup"><span data-stu-id="f880a-113">See [**D3DX11\_EFFECT\_TYPE\_DESC**](d3dx11-effect-type-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f880a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f880a-114">Return value</span></span>

<span data-ttu-id="f880a-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f880a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f880a-116">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f880a-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f880a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f880a-117">Remarks</span></span>

<span data-ttu-id="f880a-118">La descrizione della variabile di effetto contiene i dati relativi a nome, annotazioni, semantica, flag e offset del buffer del tipo di effetto.</span><span class="sxs-lookup"><span data-stu-id="f880a-118">The effect-variable description contains data about the name, annotations, semantic, flags and buffer offset of the effect type.</span></span>

> [!Note]  
> <span data-ttu-id="f880a-119">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="f880a-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f880a-120">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="f880a-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f880a-121">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f880a-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f880a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f880a-122">Requirements</span></span>



| <span data-ttu-id="f880a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f880a-123">Requirement</span></span> | <span data-ttu-id="f880a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f880a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f880a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f880a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f880a-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f880a-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f880a-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="f880a-127">Library</span></span><br/> | <dl> <span data-ttu-id="f880a-128"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="f880a-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f880a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f880a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f880a-130">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="f880a-130">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

 





