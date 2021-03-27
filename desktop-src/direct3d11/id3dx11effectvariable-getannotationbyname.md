---
title: Metodo ID3DX11EffectVariable GetAnnotationByName (D3dx11effect. h)
description: Ottenere un'annotazione in base al nome. | Metodo ID3DX11EffectVariable GetAnnotationByName (D3dx11effect. h)
ms.assetid: 0ca3df07-c721-48c4-9422-f6af24acbaef
keywords:
- Metodo GetAnnotationByName Direct3D 11
- Metodo GetAnnotationByName Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37efcd773728e563a4112f61a7c6c965d05bad4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355119"
---
# <a name="id3dx11effectvariablegetannotationbyname-method"></a><span data-ttu-id="a3485-107">Metodo ID3DX11EffectVariable:: GetAnnotationByName</span><span class="sxs-lookup"><span data-stu-id="a3485-107">ID3DX11EffectVariable::GetAnnotationByName method</span></span>

<span data-ttu-id="a3485-108">Ottenere un'annotazione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="a3485-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3485-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3485-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="a3485-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3485-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3485-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="a3485-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="a3485-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a3485-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a3485-113">Nome dell'annotazione.</span><span class="sxs-lookup"><span data-stu-id="a3485-113">The annotation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3485-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3485-114">Return value</span></span>

<span data-ttu-id="a3485-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3485-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="a3485-116">Puntatore a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="a3485-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="a3485-117">Si noti che se l'annotazione non viene trovata, il **ID3DX11EffectVariable** restituito sarà vuoto.</span><span class="sxs-lookup"><span data-stu-id="a3485-117">Note that if the annotation is not found the **ID3DX11EffectVariable** returned will be empty.</span></span> <span data-ttu-id="a3485-118">È necessario chiamare il metodo [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md) per determinare se l'annotazione è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="a3485-118">The [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) method should be called to determine whether the annotation was found.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3485-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3485-119">Remarks</span></span>

<span data-ttu-id="a3485-120">Annonations può essere collegato a una tecnica, a un passaggio o a una variabile globale.</span><span class="sxs-lookup"><span data-stu-id="a3485-120">Annonations can be attached to a technique, a pass, or a global variable.</span></span>

> [!Note]  
> <span data-ttu-id="a3485-121">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="a3485-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a3485-122">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="a3485-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a3485-123">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a3485-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a3485-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3485-124">Requirements</span></span>



| <span data-ttu-id="a3485-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3485-125">Requirement</span></span> | <span data-ttu-id="a3485-126">Valore</span><span class="sxs-lookup"><span data-stu-id="a3485-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3485-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3485-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a3485-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3485-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a3485-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="a3485-129">Library</span></span><br/> | <dl> <span data-ttu-id="a3485-130"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="a3485-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3485-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3485-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3485-132">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="a3485-132">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

