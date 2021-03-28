---
title: Metodo ID3DX11EffectGroup GetAnnotationByName (D3dx11effect. h)
description: Ottenere un'annotazione in base al nome. | Metodo ID3DX11EffectGroup GetAnnotationByName (D3dx11effect. h)
ms.assetid: c526a249-fb56-47bb-a0c2-b829a1da88e8
keywords:
- Metodo GetAnnotationByName Direct3D 11
- Metodo GetAnnotationByName Direct3D 11, interfaccia ID3DX11EffectGroup
- Interfaccia ID3DX11EffectGroup Direct3D 11, metodo GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1880983785fcfea8a4cda4aa09c8baec2cfebf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995960"
---
# <a name="id3dx11effectgroupgetannotationbyname-method"></a><span data-ttu-id="6aa75-107">Metodo ID3DX11EffectGroup:: GetAnnotationByName</span><span class="sxs-lookup"><span data-stu-id="6aa75-107">ID3DX11EffectGroup::GetAnnotationByName method</span></span>

<span data-ttu-id="6aa75-108">Ottenere un'annotazione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="6aa75-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aa75-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6aa75-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="6aa75-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6aa75-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aa75-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="6aa75-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="6aa75-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6aa75-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6aa75-113">Nome dell'elemento Annotation.</span><span class="sxs-lookup"><span data-stu-id="6aa75-113">The name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aa75-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6aa75-114">Return value</span></span>

<span data-ttu-id="6aa75-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="6aa75-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="6aa75-116">Puntatore a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="6aa75-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="6aa75-117">Si noti che se l'annotazione non viene trovata, il **ID3DX11EffectVariable** restituito sarà vuoto.</span><span class="sxs-lookup"><span data-stu-id="6aa75-117">Note that if the annotation is not found the **ID3DX11EffectVariable** returned will be empty.</span></span> <span data-ttu-id="6aa75-118">È necessario chiamare il metodo [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md) per determinare se l'annotazione è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="6aa75-118">The [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) method should be called to determine whether the annotation was found.</span></span>

## <a name="remarks"></a><span data-ttu-id="6aa75-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6aa75-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6aa75-120">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="6aa75-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6aa75-121">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="6aa75-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6aa75-122">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6aa75-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6aa75-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6aa75-123">Requirements</span></span>



| <span data-ttu-id="6aa75-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6aa75-124">Requirement</span></span> | <span data-ttu-id="6aa75-125">Valore</span><span class="sxs-lookup"><span data-stu-id="6aa75-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6aa75-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6aa75-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6aa75-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6aa75-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6aa75-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="6aa75-128">Library</span></span><br/> | <dl> <span data-ttu-id="6aa75-129"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="6aa75-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6aa75-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6aa75-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aa75-131">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="6aa75-131">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

