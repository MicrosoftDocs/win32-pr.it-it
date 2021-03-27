---
title: Metodo ID3DX11EffectTechnique GetPassByName (D3dx11effect. h)
description: Ottenere un passaggio per nome.
ms.assetid: 07c7502e-2af9-4898-8cd4-106d6814fb85
keywords:
- Metodo GetPassByName Direct3D 11
- Metodo GetPassByName Direct3D 11, interfaccia ID3DX11EffectTechnique
- Interfaccia ID3DX11EffectTechnique Direct3D 11, metodo GetPassByName
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84bbe9b954efff12e458ee6172665118a7b8ede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995972"
---
# <a name="id3dx11effecttechniquegetpassbyname-method"></a><span data-ttu-id="834c0-106">Metodo ID3DX11EffectTechnique:: GetPassByName</span><span class="sxs-lookup"><span data-stu-id="834c0-106">ID3DX11EffectTechnique::GetPassByName method</span></span>

<span data-ttu-id="834c0-107">Ottenere un passaggio per nome.</span><span class="sxs-lookup"><span data-stu-id="834c0-107">Get a pass by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="834c0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="834c0-108">Syntax</span></span>


```C++
ID3DX11EffectPass* GetPassByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="834c0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="834c0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="834c0-110">*Nome*</span><span class="sxs-lookup"><span data-stu-id="834c0-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="834c0-111">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="834c0-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="834c0-112">Nome del passaggio.</span><span class="sxs-lookup"><span data-stu-id="834c0-112">The name of the pass.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="834c0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="834c0-113">Return value</span></span>

<span data-ttu-id="834c0-114">Tipo: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***</span><span class="sxs-lookup"><span data-stu-id="834c0-114">Type: **[**ID3DX11EffectPass**](id3dx11effectpass.md)\***</span></span>

<span data-ttu-id="834c0-115">Puntatore a un [**ID3DX11EffectPass**](id3dx11effectpass.md).</span><span class="sxs-lookup"><span data-stu-id="834c0-115">A pointer to an [**ID3DX11EffectPass**](id3dx11effectpass.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="834c0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="834c0-116">Remarks</span></span>

<span data-ttu-id="834c0-117">Una tecnica contiene uno o più passaggi. ottenere un pass usando un nome o un indice.</span><span class="sxs-lookup"><span data-stu-id="834c0-117">A technique contains one or more passes; get a pass using a name or an index.</span></span>

> [!Note]  
> <span data-ttu-id="834c0-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="834c0-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="834c0-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="834c0-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="834c0-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="834c0-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="834c0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="834c0-121">Requirements</span></span>



| <span data-ttu-id="834c0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="834c0-122">Requirement</span></span> | <span data-ttu-id="834c0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="834c0-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="834c0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="834c0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="834c0-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="834c0-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="834c0-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="834c0-126">Library</span></span><br/> | <dl> <span data-ttu-id="834c0-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="834c0-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="834c0-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="834c0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="834c0-129">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="834c0-129">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

