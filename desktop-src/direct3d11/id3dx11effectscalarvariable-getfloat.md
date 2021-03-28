---
title: Metodo GetFloat ID3DX11EffectScalarVariable (D3dx11effect. h)
description: Ottenere una variabile a virgola mobile.
ms.assetid: 0416db40-5e70-44e4-905f-86f49a9b58b8
keywords:
- Metodo GetFloat Direct3D 11
- Metodo GetFloat Direct3D 11, interfaccia ID3DX11EffectScalarVariable
- Interfaccia ID3DX11EffectScalarVariable Direct3D 11, Metodo GetFloat
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetFloat
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1d8f7ae63bc8312c2432e50f5b6dcfeccdf525
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355744"
---
# <a name="id3dx11effectscalarvariablegetfloat-method"></a><span data-ttu-id="804c3-106">Metodo ID3DX11EffectScalarVariable:: GetFloat</span><span class="sxs-lookup"><span data-stu-id="804c3-106">ID3DX11EffectScalarVariable::GetFloat method</span></span>

<span data-ttu-id="804c3-107">Ottenere una variabile a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="804c3-107">Get a floating-point variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="804c3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="804c3-108">Syntax</span></span>


```C++
HRESULT GetFloat(
   float *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="804c3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="804c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="804c3-110">*pValue*</span><span class="sxs-lookup"><span data-stu-id="804c3-110">*pValue*</span></span> 
</dt> <dd>

<span data-ttu-id="804c3-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="804c3-111">Type: **float\***</span></span>

<span data-ttu-id="804c3-112">Puntatore alla variabile.</span><span class="sxs-lookup"><span data-stu-id="804c3-112">A pointer to the variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="804c3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="804c3-113">Return value</span></span>

<span data-ttu-id="804c3-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="804c3-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="804c3-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="804c3-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="804c3-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="804c3-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="804c3-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="804c3-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="804c3-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="804c3-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="804c3-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="804c3-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="804c3-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="804c3-120">Requirements</span></span>



| <span data-ttu-id="804c3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="804c3-121">Requirement</span></span> | <span data-ttu-id="804c3-122">Valore</span><span class="sxs-lookup"><span data-stu-id="804c3-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="804c3-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="804c3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="804c3-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="804c3-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="804c3-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="804c3-125">Library</span></span><br/> | <dl> <span data-ttu-id="804c3-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="804c3-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="804c3-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="804c3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="804c3-128">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="804c3-128">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

 





