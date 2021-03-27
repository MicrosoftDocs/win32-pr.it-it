---
title: Metodo ID3DX11EffectVariable AsScalar (D3dx11effect. h)
description: Ottenere una variabile scalare.
ms.assetid: 5cc02fb3-351a-4309-9145-1ed7d759a650
keywords:
- Metodo AsScalar Direct3D 11
- Metodo AsScalar Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo AsScalar
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsScalar
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e455250ae99075af449793d634fd6b3c2fafc4b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762389"
---
# <a name="id3dx11effectvariableasscalar-method"></a><span data-ttu-id="3f1fc-106">Metodo ID3DX11EffectVariable:: AsScalar</span><span class="sxs-lookup"><span data-stu-id="3f1fc-106">ID3DX11EffectVariable::AsScalar method</span></span>

<span data-ttu-id="3f1fc-107">Ottenere una variabile scalare.</span><span class="sxs-lookup"><span data-stu-id="3f1fc-107">Get a scalar variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f1fc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f1fc-108">Syntax</span></span>


```C++
ID3DX11EffectScalarVariable* AsScalar();
```



## <a name="parameters"></a><span data-ttu-id="3f1fc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f1fc-109">Parameters</span></span>

<span data-ttu-id="3f1fc-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3f1fc-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3f1fc-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f1fc-111">Return value</span></span>

<span data-ttu-id="3f1fc-112">Tipo: **[ **ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f1fc-112">Type: **[**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md)\***</span></span>

<span data-ttu-id="3f1fc-113">Puntatore a una variabile scalare.</span><span class="sxs-lookup"><span data-stu-id="3f1fc-113">A pointer to a scalar variable.</span></span> <span data-ttu-id="3f1fc-114">Vedere [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md).</span><span class="sxs-lookup"><span data-stu-id="3f1fc-114">See [**ID3DX11EffectScalarVariable**](id3dx11effectscalarvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3f1fc-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f1fc-115">Remarks</span></span>

<span data-ttu-id="3f1fc-116">AsScalar restituisce una versione della variabile Effect specializzata in una variabile scalare.</span><span class="sxs-lookup"><span data-stu-id="3f1fc-116">AsScalar returns a version of the effect variable that has been specialized to a scalar variable.</span></span> <span data-ttu-id="3f1fc-117">Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile Effect non contiene dati scalari.</span><span class="sxs-lookup"><span data-stu-id="3f1fc-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain scalar data.</span></span>

<span data-ttu-id="3f1fc-118">Per verificare la validità dell'oggetto restituito, le applicazioni possono chiamare [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="3f1fc-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="3f1fc-119">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="3f1fc-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3f1fc-120">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="3f1fc-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3f1fc-121">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3f1fc-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3f1fc-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f1fc-122">Requirements</span></span>



| <span data-ttu-id="3f1fc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f1fc-123">Requirement</span></span> | <span data-ttu-id="3f1fc-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3f1fc-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f1fc-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f1fc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3f1fc-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f1fc-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3f1fc-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="3f1fc-127">Library</span></span><br/> | <dl> <span data-ttu-id="3f1fc-128"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="3f1fc-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f1fc-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f1fc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f1fc-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="3f1fc-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





