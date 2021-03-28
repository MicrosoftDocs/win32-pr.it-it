---
title: Metodo ID3DX11EffectRasterizerVariable UndoSetRasterizerState (D3dx11effect. h)
description: Ripristina uno stato di rasterizzazione impostato in precedenza.
ms.assetid: 2801479c-cb70-4950-9888-73e271b669aa
keywords:
- Metodo UndoSetRasterizerState Direct3D 11
- Metodo UndoSetRasterizerState Direct3D 11, interfaccia ID3DX11EffectRasterizerVariable
- Interfaccia ID3DX11EffectRasterizerVariable Direct3D 11, metodo UndoSetRasterizerState
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.UndoSetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed05aa7380a1fb08bbd12d36328d33fa64fb7500
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235219"
---
# <a name="id3dx11effectrasterizervariableundosetrasterizerstate-method"></a><span data-ttu-id="c69cc-106">Metodo ID3DX11EffectRasterizerVariable:: UndoSetRasterizerState</span><span class="sxs-lookup"><span data-stu-id="c69cc-106">ID3DX11EffectRasterizerVariable::UndoSetRasterizerState method</span></span>

<span data-ttu-id="c69cc-107">Ripristina uno stato di rasterizzazione impostato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c69cc-107">Reverts a previously set rasterizer state.</span></span>

## <a name="syntax"></a><span data-ttu-id="c69cc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c69cc-108">Syntax</span></span>


```C++
HRESULT UndoSetRasterizerState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="c69cc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c69cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c69cc-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="c69cc-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="c69cc-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c69cc-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c69cc-112">Indicizzare in una matrice di interfacce di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="c69cc-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="c69cc-113">Se è presente una sola interfaccia di rasterizzazione, usare 0.</span><span class="sxs-lookup"><span data-stu-id="c69cc-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c69cc-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c69cc-114">Return value</span></span>

<span data-ttu-id="c69cc-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c69cc-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c69cc-116">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c69cc-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c69cc-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c69cc-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c69cc-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="c69cc-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c69cc-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="c69cc-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c69cc-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c69cc-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c69cc-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c69cc-121">Requirements</span></span>



| <span data-ttu-id="c69cc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c69cc-122">Requirement</span></span> | <span data-ttu-id="c69cc-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c69cc-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c69cc-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c69cc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c69cc-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c69cc-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c69cc-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="c69cc-126">Library</span></span><br/> | <dl> <span data-ttu-id="c69cc-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="c69cc-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c69cc-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c69cc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c69cc-129">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="c69cc-129">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

