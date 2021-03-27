---
title: Metodo ID3DX11EffectTechnique GetAnnotationByName (D3dx11effect. h)
description: Ottenere un'annotazione in base al nome. | Metodo ID3DX11EffectTechnique GetAnnotationByName (D3dx11effect. h)
ms.assetid: 3a9e1fa7-4586-42d6-a723-3140f29a01b4
keywords:
- Metodo GetAnnotationByName Direct3D 11
- Metodo GetAnnotationByName Direct3D 11, interfaccia ID3DX11EffectTechnique
- Interfaccia ID3DX11EffectTechnique Direct3D 11, metodo GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae5a7c24d392bd034dfcd69fb67723c9492f982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355124"
---
# <a name="id3dx11effecttechniquegetannotationbyname-method"></a><span data-ttu-id="afada-107">Metodo ID3DX11EffectTechnique:: GetAnnotationByName</span><span class="sxs-lookup"><span data-stu-id="afada-107">ID3DX11EffectTechnique::GetAnnotationByName method</span></span>

<span data-ttu-id="afada-108">Ottenere un'annotazione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="afada-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="afada-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afada-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="afada-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="afada-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afada-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="afada-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="afada-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="afada-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="afada-113">Nome dell'annotazione.</span><span class="sxs-lookup"><span data-stu-id="afada-113">Name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afada-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="afada-114">Return value</span></span>

<span data-ttu-id="afada-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="afada-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="afada-116">Puntatore a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="afada-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="afada-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="afada-117">Remarks</span></span>

<span data-ttu-id="afada-118">Usare un'annotazione per alleghi una parte di metadati a una tecnica.</span><span class="sxs-lookup"><span data-stu-id="afada-118">Use an annotation to attach a piece of metadata to a technique.</span></span>

> [!Note]  
> <span data-ttu-id="afada-119">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="afada-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="afada-120">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="afada-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="afada-121">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="afada-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="afada-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afada-122">Requirements</span></span>



| <span data-ttu-id="afada-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="afada-123">Requirement</span></span> | <span data-ttu-id="afada-124">Valore</span><span class="sxs-lookup"><span data-stu-id="afada-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afada-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="afada-125">Header</span></span><br/>  | <dl> <span data-ttu-id="afada-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="afada-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="afada-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="afada-127">Library</span></span><br/> | <dl> <span data-ttu-id="afada-128"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="afada-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afada-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afada-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afada-130">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="afada-130">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

