---
title: Metodo ID3DX11EffectRasterizerVariable GetRasterizerState (D3dx11effect. h)
description: Ottenere un puntatore a un'interfaccia di rasterizzazione.
ms.assetid: 4b8515e0-b79a-4572-9142-07c50a8839b8
keywords:
- Metodo GetRasterizerState Direct3D 11
- Metodo GetRasterizerState Direct3D 11, interfaccia ID3DX11EffectRasterizerVariable
- Interfaccia ID3DX11EffectRasterizerVariable Direct3D 11, metodo GetRasterizerState
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972140a8f74a3e5a6728429faddacc253aaa6c9d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982627"
---
# <a name="id3dx11effectrasterizervariablegetrasterizerstate-method"></a><span data-ttu-id="f7f90-106">Metodo ID3DX11EffectRasterizerVariable:: GetRasterizerState</span><span class="sxs-lookup"><span data-stu-id="f7f90-106">ID3DX11EffectRasterizerVariable::GetRasterizerState method</span></span>

<span data-ttu-id="f7f90-107">Ottenere un puntatore a un'interfaccia di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="f7f90-107">Get a pointer to a rasterizer interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7f90-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7f90-108">Syntax</span></span>


```C++
HRESULT GetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState **ppRasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="f7f90-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7f90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7f90-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="f7f90-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="f7f90-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f7f90-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f7f90-112">Indicizzare in una matrice di interfacce di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="f7f90-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="f7f90-113">Se è presente una sola interfaccia di rasterizzazione, usare 0.</span><span class="sxs-lookup"><span data-stu-id="f7f90-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="f7f90-114">*ppRasterizerState*</span><span class="sxs-lookup"><span data-stu-id="f7f90-114">*ppRasterizerState*</span></span> 
</dt> <dd>

<span data-ttu-id="f7f90-115">Tipo: **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="f7f90-115">Type: **[**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\*\***</span></span>

<span data-ttu-id="f7f90-116">Indirizzo di un puntatore a un'interfaccia di rasterizzazione (vedere [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)).</span><span class="sxs-lookup"><span data-stu-id="f7f90-116">The address of a pointer to a rasterizer interface (see [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7f90-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7f90-117">Return value</span></span>

<span data-ttu-id="f7f90-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f7f90-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f7f90-119">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f7f90-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f7f90-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7f90-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f7f90-121">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="f7f90-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f7f90-122">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="f7f90-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f7f90-123">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f7f90-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f7f90-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7f90-124">Requirements</span></span>



| <span data-ttu-id="f7f90-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7f90-125">Requirement</span></span> | <span data-ttu-id="f7f90-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f7f90-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f90-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7f90-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f7f90-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7f90-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f7f90-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="f7f90-129">Library</span></span><br/> | <dl> <span data-ttu-id="f7f90-130"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="f7f90-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7f90-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7f90-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7f90-132">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="f7f90-132">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

