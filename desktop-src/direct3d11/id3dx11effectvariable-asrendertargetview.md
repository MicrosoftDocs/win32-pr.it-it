---
title: Metodo ID3DX11EffectVariable AsRenderTargetView (D3dx11effect. h)
description: Ottenere una variabile di visualizzazione della destinazione di rendering.
ms.assetid: 1eec342e-267a-4eab-886a-a309758065c7
keywords:
- Metodo AsRenderTargetView Direct3D 11
- Metodo AsRenderTargetView Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo AsRenderTargetView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRenderTargetView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca6270503ff786b3f4a319e3f068ba76acada7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996321"
---
# <a name="id3dx11effectvariableasrendertargetview-method"></a><span data-ttu-id="b4b11-106">Metodo ID3DX11EffectVariable:: AsRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="b4b11-106">ID3DX11EffectVariable::AsRenderTargetView method</span></span>

<span data-ttu-id="b4b11-107">Ottenere una variabile di visualizzazione della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="b4b11-107">Get a render-target-view variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b11-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4b11-108">Syntax</span></span>


```C++
ID3DX11EffectRenderTargetViewVariable* AsRenderTargetView();
```



## <a name="parameters"></a><span data-ttu-id="b4b11-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4b11-109">Parameters</span></span>

<span data-ttu-id="b4b11-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b4b11-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b4b11-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4b11-111">Return value</span></span>

<span data-ttu-id="b4b11-112">Tipo: **[ **ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="b4b11-112">Type: **[**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)\***</span></span>

<span data-ttu-id="b4b11-113">Puntatore a una variabile di visualizzazione della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="b4b11-113">A pointer to a render-target-view variable.</span></span> <span data-ttu-id="b4b11-114">Vedere [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md).</span><span class="sxs-lookup"><span data-stu-id="b4b11-114">See [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4b11-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4b11-115">Remarks</span></span>

<span data-ttu-id="b4b11-116">Questo metodo restituisce una versione della variabile di effetto che è stata specializzata in una variabile di visualizzazione della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="b4b11-116">This method returns a version of the effect variable that has been specialized to a render-target-view variable.</span></span> <span data-ttu-id="b4b11-117">Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile Effect non contiene dati di visualizzazione della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="b4b11-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain render-target-view data.</span></span>

<span data-ttu-id="b4b11-118">Per verificare la validità dell'oggetto restituito, le applicazioni possono chiamare [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="b4b11-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="b4b11-119">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="b4b11-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b4b11-120">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="b4b11-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b4b11-121">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b4b11-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b4b11-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4b11-122">Requirements</span></span>



| <span data-ttu-id="b4b11-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4b11-123">Requirement</span></span> | <span data-ttu-id="b4b11-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b4b11-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b11-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4b11-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b4b11-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4b11-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b4b11-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="b4b11-127">Library</span></span><br/> | <dl> <span data-ttu-id="b4b11-128"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="b4b11-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4b11-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4b11-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4b11-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="b4b11-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





