---
description: 'Metodo ID3DXMATRIXStack::P ush (D3DX10.h): aggiunge una matrice nello stack.'
ms.assetid: 8660047f-64bc-4b34-8270-3087412db942
title: Metodo ID3DXMATRIXStack::P ush (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Push
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9c248fdaed8235c383388a52172021921e2c78d8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107918"
---
# <a name="id3dxmatrixstackpush-method-d3dx10h"></a><span data-ttu-id="97e10-103">Metodo ID3DXMATRIXStack::P ush (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="97e10-103">ID3DXMATRIXStack::Push method (D3DX10.h)</span></span>

<span data-ttu-id="97e10-104">Aggiunge una matrice nello stack.</span><span class="sxs-lookup"><span data-stu-id="97e10-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="97e10-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97e10-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="97e10-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="97e10-106">Parameters</span></span>

<span data-ttu-id="97e10-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="97e10-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="97e10-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97e10-108">Return value</span></span>

<span data-ttu-id="97e10-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="97e10-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="97e10-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="97e10-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="97e10-111">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="97e10-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="97e10-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="97e10-112">Remarks</span></span>

<span data-ttu-id="97e10-113">Questo metodo incrementa il conteggio degli elementi nello stack di 1, duplicando la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="97e10-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="97e10-114">Lo stack crescerà dinamicamente quando vengono aggiunti più elementi.</span><span class="sxs-lookup"><span data-stu-id="97e10-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="97e10-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97e10-115">Requirements</span></span>



| <span data-ttu-id="97e10-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="97e10-116">Requirement</span></span> | <span data-ttu-id="97e10-117">Valore</span><span class="sxs-lookup"><span data-stu-id="97e10-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97e10-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97e10-118">Header</span></span><br/>  | <dl> <span data-ttu-id="97e10-119"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="97e10-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="97e10-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="97e10-120">Library</span></span><br/> | <dl> <span data-ttu-id="97e10-121"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="97e10-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97e10-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97e10-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97e10-123">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="97e10-123">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="97e10-124">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="97e10-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




