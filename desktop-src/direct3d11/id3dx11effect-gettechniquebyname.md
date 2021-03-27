---
title: Metodo ID3DX11Effect GetTechniqueByName (D3dx11effect. h)
description: Ottenere una tecnica in base al nome. | Metodo ID3DX11Effect GetTechniqueByName (D3dx11effect. h)
ms.assetid: 0f7fa02c-dfbf-4971-86ad-3429f99f84e0
keywords:
- Metodo GetTechniqueByName Direct3D 11
- Metodo GetTechniqueByName Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetTechniqueByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d26b6067352d4ca898cc1fc970524040d407bda1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982418"
---
# <a name="id3dx11effectgettechniquebyname-method"></a><span data-ttu-id="8a1fa-107">Metodo ID3DX11Effect:: GetTechniqueByName</span><span class="sxs-lookup"><span data-stu-id="8a1fa-107">ID3DX11Effect::GetTechniqueByName method</span></span>

<span data-ttu-id="8a1fa-108">Ottenere una tecnica in base al nome.</span><span class="sxs-lookup"><span data-stu-id="8a1fa-108">Get a technique by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a1fa-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a1fa-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="8a1fa-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a1fa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a1fa-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="8a1fa-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="8a1fa-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a1fa-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8a1fa-113">Nome della tecnica.</span><span class="sxs-lookup"><span data-stu-id="8a1fa-113">The name of the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a1fa-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a1fa-114">Return value</span></span>

<span data-ttu-id="8a1fa-115">Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a1fa-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="8a1fa-116">Puntatore a un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="8a1fa-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span> <span data-ttu-id="8a1fa-117">Se non viene trovata una tecnica con il nome appropriato, viene restituita una tecnica non valida.</span><span class="sxs-lookup"><span data-stu-id="8a1fa-117">If a technique with the appropriate name is not found an invalid technique is returned.</span></span> <span data-ttu-id="8a1fa-118">Per determinare se è valido, è necessario chiamare [**ID3DX11EffectTechnique:: IsValid**](id3dx11effecttechnique-isvalid.md) sulla tecnica restituita.</span><span class="sxs-lookup"><span data-stu-id="8a1fa-118">[**ID3DX11EffectTechnique::IsValid**](id3dx11effecttechnique-isvalid.md) should be called on the returned technique to determine whether it is valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a1fa-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a1fa-119">Remarks</span></span>

<span data-ttu-id="8a1fa-120">Un effetto contiene una o più tecniche. ogni tecnica contiene uno o più passaggi.</span><span class="sxs-lookup"><span data-stu-id="8a1fa-120">An effect contains one or more techniques; each technique contains one or more passes.</span></span> <span data-ttu-id="8a1fa-121">È possibile accedere a una tecnica usando il nome o un indice.</span><span class="sxs-lookup"><span data-stu-id="8a1fa-121">You can access a technique using its name or with an index.</span></span>

> [!Note]  
> <span data-ttu-id="8a1fa-122">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="8a1fa-122">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8a1fa-123">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="8a1fa-123">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8a1fa-124">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8a1fa-124">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8a1fa-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a1fa-125">Requirements</span></span>



| <span data-ttu-id="8a1fa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a1fa-126">Requirement</span></span> | <span data-ttu-id="8a1fa-127">Valore</span><span class="sxs-lookup"><span data-stu-id="8a1fa-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1fa-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a1fa-128">Header</span></span><br/>  | <dl> <span data-ttu-id="8a1fa-129"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a1fa-129"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8a1fa-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="8a1fa-130">Library</span></span><br/> | <dl> <span data-ttu-id="8a1fa-131"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="8a1fa-131"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a1fa-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a1fa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a1fa-133">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="8a1fa-133">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

