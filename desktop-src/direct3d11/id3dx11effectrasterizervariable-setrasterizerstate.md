---
title: Metodo ID3DX11EffectRasterizerVariable SetRasterizerState (D3dx11effect. h)
description: Imposta lo stato del rasterizzatore.
ms.assetid: b2cd93fb-77bb-4a39-b686-7b8f683c9172
keywords:
- Metodo SetRasterizerState Direct3D 11
- Metodo SetRasterizerState Direct3D 11, interfaccia ID3DX11EffectRasterizerVariable
- Interfaccia ID3DX11EffectRasterizerVariable Direct3D 11, metodo SetRasterizerState
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.SetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1f44df653339f274207bfa4283fc8470c8844f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235220"
---
# <a name="id3dx11effectrasterizervariablesetrasterizerstate-method"></a><span data-ttu-id="8416c-106">Metodo ID3DX11EffectRasterizerVariable:: SetRasterizerState</span><span class="sxs-lookup"><span data-stu-id="8416c-106">ID3DX11EffectRasterizerVariable::SetRasterizerState method</span></span>

<span data-ttu-id="8416c-107">Imposta lo stato del rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="8416c-107">Sets the rasterizer state.</span></span>

## <a name="syntax"></a><span data-ttu-id="8416c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8416c-108">Syntax</span></span>


```C++
HRESULT SetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState *pRasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="8416c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8416c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8416c-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="8416c-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="8416c-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8416c-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8416c-112">Indicizzare in una matrice di interfacce di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="8416c-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="8416c-113">Se è presente una sola interfaccia di rasterizzazione, usare 0.</span><span class="sxs-lookup"><span data-stu-id="8416c-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="8416c-114">*pRasterizerState*</span><span class="sxs-lookup"><span data-stu-id="8416c-114">*pRasterizerState*</span></span> 
</dt> <dd>

<span data-ttu-id="8416c-115">Tipo: **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\***</span><span class="sxs-lookup"><span data-stu-id="8416c-115">Type: **[**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\***</span></span>

<span data-ttu-id="8416c-116">Puntatore a un'interfaccia [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate) .</span><span class="sxs-lookup"><span data-stu-id="8416c-116">Pointer to an [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8416c-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8416c-117">Return value</span></span>

<span data-ttu-id="8416c-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8416c-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8416c-119">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8416c-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8416c-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="8416c-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8416c-121">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="8416c-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8416c-122">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="8416c-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8416c-123">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8416c-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8416c-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8416c-124">Requirements</span></span>



| <span data-ttu-id="8416c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8416c-125">Requirement</span></span> | <span data-ttu-id="8416c-126">Valore</span><span class="sxs-lookup"><span data-stu-id="8416c-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8416c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8416c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8416c-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8416c-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8416c-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="8416c-129">Library</span></span><br/> | <dl> <span data-ttu-id="8416c-130"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="8416c-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8416c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8416c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8416c-132">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="8416c-132">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

