---
description: Estende il pattern stipple lungo la direzione della riga.
ms.assetid: 411464db-d721-4252-bff3-bec57252273e
title: 'Metodo ID3DXLine:: SetPatternScale (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44c040a2e8899784bcea9b93bf0781afb39c2464
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235215"
---
# <a name="id3dxlinesetpatternscale-method"></a><span data-ttu-id="1c4b1-103">Metodo ID3DXLine:: SetPatternScale</span><span class="sxs-lookup"><span data-stu-id="1c4b1-103">ID3DXLine::SetPatternScale method</span></span>

<span data-ttu-id="1c4b1-104">Estende il pattern stipple lungo la direzione della riga.</span><span class="sxs-lookup"><span data-stu-id="1c4b1-104">Stretches the stipple pattern along the line direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c4b1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c4b1-105">Syntax</span></span>


```C++
HRESULT SetPatternScale(
  [in] FLOAT fPatternScale
);
```



## <a name="parameters"></a><span data-ttu-id="1c4b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c4b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c4b1-107">*fPatternScale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c4b1-107">*fPatternScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4b1-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c4b1-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c4b1-109">Valore di ridimensionamento del modello stipple.</span><span class="sxs-lookup"><span data-stu-id="1c4b1-109">Stipple pattern scaling value.</span></span> <span data-ttu-id="1c4b1-110">1,0 f è il valore predefinito e non rappresenta alcun ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="1c4b1-110">1.0f is the default value and represents no scaling.</span></span> <span data-ttu-id="1c4b1-111">Un valore inferiore a 1,0 f compatta il criterio e un valore maggiore di 1,0 estende il modello.</span><span class="sxs-lookup"><span data-stu-id="1c4b1-111">A value less than 1.0f shrinks the pattern, and a value greater than 1.0 stretches the pattern.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c4b1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c4b1-112">Return value</span></span>

<span data-ttu-id="1c4b1-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1c4b1-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1c4b1-114">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1c4b1-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1c4b1-115">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="1c4b1-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c4b1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c4b1-116">Requirements</span></span>



| <span data-ttu-id="1c4b1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c4b1-117">Requirement</span></span> | <span data-ttu-id="1c4b1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1c4b1-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c4b1-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c4b1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1c4b1-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c4b1-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="1c4b1-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="1c4b1-121">Library</span></span><br/> | <dl> <span data-ttu-id="1c4b1-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c4b1-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1c4b1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c4b1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c4b1-124">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="1c4b1-124">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
