---
description: Ottiene il valore della scala del pattern stipple.
ms.assetid: cf80ae8c-493d-4f35-b4f9-5981e64cc842
title: 'Metodo ID3DXLine:: GetPatternScale (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 14a9919ede81eb64b844e1882725e37359ad6738
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104402030"
---
# <a name="id3dxlinegetpatternscale-method"></a><span data-ttu-id="27857-103">Metodo ID3DXLine:: GetPatternScale</span><span class="sxs-lookup"><span data-stu-id="27857-103">ID3DXLine::GetPatternScale method</span></span>

<span data-ttu-id="27857-104">Ottiene il valore della scala del pattern stipple.</span><span class="sxs-lookup"><span data-stu-id="27857-104">Gets the stipple-pattern scale value.</span></span>

## <a name="syntax"></a><span data-ttu-id="27857-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27857-105">Syntax</span></span>


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a><span data-ttu-id="27857-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="27857-106">Parameters</span></span>

<span data-ttu-id="27857-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="27857-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="27857-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27857-108">Return value</span></span>

<span data-ttu-id="27857-109">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27857-109">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="27857-110">Restituisce il valore usato per ridimensionare il pattern stipple.</span><span class="sxs-lookup"><span data-stu-id="27857-110">Returns the value used to scale the stipple-pattern.</span></span> <span data-ttu-id="27857-111">1,0 f è il valore predefinito e non rappresenta alcun ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="27857-111">1.0f is the default value and represents no scaling.</span></span> <span data-ttu-id="27857-112">Un valore inferiore a 1,0 f compatta il criterio e un valore maggiore di 1,0 estende il modello.</span><span class="sxs-lookup"><span data-stu-id="27857-112">A value less than 1.0f shrinks the pattern, and a value greater than 1.0 stretches the pattern.</span></span>

## <a name="requirements"></a><span data-ttu-id="27857-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27857-113">Requirements</span></span>



| <span data-ttu-id="27857-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="27857-114">Requirement</span></span> | <span data-ttu-id="27857-115">Valore</span><span class="sxs-lookup"><span data-stu-id="27857-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27857-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27857-116">Header</span></span><br/>  | <dl> <span data-ttu-id="27857-117"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="27857-117"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="27857-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="27857-118">Library</span></span><br/> | <dl> <span data-ttu-id="27857-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27857-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="27857-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27857-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27857-121">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="27857-121">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="27857-122">**ID3DXLine::SetPatternScale**</span><span class="sxs-lookup"><span data-stu-id="27857-122">**ID3DXLine::SetPatternScale**</span></span>](id3dxline--setpatternscale.md)
</dt> </dl>

 

 
