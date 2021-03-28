---
title: Metodo ID3DX11EffectVectorVariable GetFloatVector (D3dx11effect. h)
description: Ottenere un vettore a quattro componenti che contiene dati a virgola mobile.
ms.assetid: 980c85db-0d40-49e0-99d0-5049fdf62540
keywords:
- Metodo GetFloatVector Direct3D 11
- Metodo GetFloatVector Direct3D 11, interfaccia ID3DX11EffectVectorVariable
- Interfaccia ID3DX11EffectVectorVariable Direct3D 11, metodo GetFloatVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetFloatVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0ce1ea07a2cbbb2826101e80d013b7f6bd02ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969453"
---
# <a name="id3dx11effectvectorvariablegetfloatvector-method"></a><span data-ttu-id="b5552-106">Metodo ID3DX11EffectVectorVariable:: GetFloatVector</span><span class="sxs-lookup"><span data-stu-id="b5552-106">ID3DX11EffectVectorVariable::GetFloatVector method</span></span>

<span data-ttu-id="b5552-107">Ottenere un vettore a quattro componenti che contiene dati a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="b5552-107">Get a four-component vector that contains floating-point data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5552-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5552-108">Syntax</span></span>


```C++
HRESULT GetFloatVector(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="b5552-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5552-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5552-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="b5552-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="b5552-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="b5552-111">Type: **float\***</span></span>

<span data-ttu-id="b5552-112">Puntatore al primo componente.</span><span class="sxs-lookup"><span data-stu-id="b5552-112">A pointer to the first component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5552-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5552-113">Return value</span></span>

<span data-ttu-id="b5552-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5552-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5552-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b5552-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5552-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5552-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b5552-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="b5552-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b5552-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="b5552-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b5552-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b5552-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b5552-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5552-120">Requirements</span></span>



| <span data-ttu-id="b5552-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5552-121">Requirement</span></span> | <span data-ttu-id="b5552-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b5552-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5552-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5552-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b5552-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5552-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b5552-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5552-125">Library</span></span><br/> | <dl> <span data-ttu-id="b5552-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="b5552-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5552-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5552-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5552-128">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="b5552-128">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

 





