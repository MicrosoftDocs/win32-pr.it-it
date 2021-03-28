---
title: Metodo getMatrix ID3DX11EffectMatrixVariable (D3dx11effect. h)
description: Ottenere una matrice.
ms.assetid: 1d0b20f2-6e43-414d-a161-65ce13bef1e0
keywords:
- Metodo getMatrix Direct3D 11
- Metodo getMatrix Direct3D 11, interfaccia ID3DX11EffectMatrixVariable
- Interfaccia ID3DX11EffectMatrixVariable Direct3D 11, metodo getMatrix
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14c2f196c4072d7f81a75045fe4703bf51ea338
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058639"
---
# <a name="id3dx11effectmatrixvariablegetmatrix-method"></a><span data-ttu-id="5fbdb-106">Metodo ID3DX11EffectMatrixVariable:: getMatrix</span><span class="sxs-lookup"><span data-stu-id="5fbdb-106">ID3DX11EffectMatrixVariable::GetMatrix method</span></span>

<span data-ttu-id="5fbdb-107">Ottenere una matrice.</span><span class="sxs-lookup"><span data-stu-id="5fbdb-107">Get a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fbdb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5fbdb-108">Syntax</span></span>


```C++
HRESULT GetMatrix(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="5fbdb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5fbdb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fbdb-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="5fbdb-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="5fbdb-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="5fbdb-111">Type: **float\***</span></span>

<span data-ttu-id="5fbdb-112">Puntatore al primo elemento di una matrice.</span><span class="sxs-lookup"><span data-stu-id="5fbdb-112">A pointer to the first element in a matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fbdb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5fbdb-113">Return value</span></span>

<span data-ttu-id="5fbdb-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5fbdb-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5fbdb-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5fbdb-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5fbdb-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="5fbdb-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5fbdb-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="5fbdb-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5fbdb-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="5fbdb-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5fbdb-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5fbdb-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5fbdb-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fbdb-120">Requirements</span></span>



| <span data-ttu-id="5fbdb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fbdb-121">Requirement</span></span> | <span data-ttu-id="5fbdb-122">Valore</span><span class="sxs-lookup"><span data-stu-id="5fbdb-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fbdb-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fbdb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5fbdb-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fbdb-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5fbdb-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="5fbdb-125">Library</span></span><br/> | <dl> <span data-ttu-id="5fbdb-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="5fbdb-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fbdb-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fbdb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fbdb-128">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="5fbdb-128">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





