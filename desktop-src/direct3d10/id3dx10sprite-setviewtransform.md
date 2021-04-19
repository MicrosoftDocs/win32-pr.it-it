---
description: Impostare la trasformazione visualizzazione che si applica a tutti gli sprite.
ms.assetid: 0420b141-46c7-4409-a0c4-67d1e8e02cd4
title: 'Metodo ID3DX10Sprite:: SetViewTransform (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.SetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 62ec2129d441acaa0719d2e64c02b4cc57370c8b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323741"
---
# <a name="id3dx10spritesetviewtransform-method"></a><span data-ttu-id="f9b76-103">Metodo ID3DX10Sprite:: SetViewTransform</span><span class="sxs-lookup"><span data-stu-id="f9b76-103">ID3DX10Sprite::SetViewTransform method</span></span>

<span data-ttu-id="f9b76-104">Impostare la trasformazione visualizzazione che si applica a tutti gli sprite.</span><span class="sxs-lookup"><span data-stu-id="f9b76-104">Set the view transform that applies to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9b76-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9b76-105">Syntax</span></span>


```C++
HRESULT SetViewTransform(
  [in] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a><span data-ttu-id="f9b76-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9b76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9b76-107">*pViewTransform* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9b76-107">*pViewTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9b76-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f9b76-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f9b76-109">Puntatore a un D3DXMATRIX che contiene una trasformazione dello sprite dallo spazio globale originale.</span><span class="sxs-lookup"><span data-stu-id="f9b76-109">Pointer to a D3DXMATRIX that contains a transform of the sprite from the original world space.</span></span> <span data-ttu-id="f9b76-110">Usare questa trasformazione per ridimensionare, ruotare o trasformare lo sprite.</span><span class="sxs-lookup"><span data-stu-id="f9b76-110">Use this transform to scale, rotate, or transform the sprite.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9b76-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9b76-111">Return value</span></span>

<span data-ttu-id="f9b76-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f9b76-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f9b76-113">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f9b76-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f9b76-114">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f9b76-114">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9b76-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9b76-115">Requirements</span></span>



| <span data-ttu-id="f9b76-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9b76-116">Requirement</span></span> | <span data-ttu-id="f9b76-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f9b76-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b76-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9b76-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f9b76-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9b76-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9b76-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="f9b76-120">Library</span></span><br/> | <dl> <span data-ttu-id="f9b76-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9b76-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9b76-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9b76-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9b76-123">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="f9b76-123">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="f9b76-124">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="f9b76-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
