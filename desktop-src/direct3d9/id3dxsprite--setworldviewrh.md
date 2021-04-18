---
description: Imposta la trasformazione di visualizzazione globale a destra per uno sprite. È necessaria una chiamata a questo metodo prima di eseguire il Billboard o l'ordinamento degli sprite.
ms.assetid: 83654e9a-8991-49ec-ab28-cf9063126dbe
title: 'Metodo ID3DXSprite:: SetWorldViewRH (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewRH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7521f60f819829fc72ba907b57d4e4eb13682a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322967"
---
# <a name="id3dxspritesetworldviewrh-method"></a><span data-ttu-id="af634-104">Metodo ID3DXSprite:: SetWorldViewRH</span><span class="sxs-lookup"><span data-stu-id="af634-104">ID3DXSprite::SetWorldViewRH method</span></span>

<span data-ttu-id="af634-105">Imposta la trasformazione di visualizzazione globale a destra per uno sprite.</span><span class="sxs-lookup"><span data-stu-id="af634-105">Sets the right-handed world-view transform for a sprite.</span></span> <span data-ttu-id="af634-106">È necessaria una chiamata a questo metodo prima di eseguire il Billboard o l'ordinamento degli sprite.</span><span class="sxs-lookup"><span data-stu-id="af634-106">A call to this method is required before billboarding or sorting sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="af634-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af634-107">Syntax</span></span>


```C++
HRESULT SetWorldViewRH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a><span data-ttu-id="af634-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="af634-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af634-109">*pWorld* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af634-109">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af634-110">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="af634-110">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="af634-111">Puntatore a un [**D3DXMATRIX**](d3dxmatrix.md) che contiene una trasformazione globale.</span><span class="sxs-lookup"><span data-stu-id="af634-111">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a world transform.</span></span> <span data-ttu-id="af634-112">Se è **null**, la matrice di identità viene utilizzata per la trasformazione globale.</span><span class="sxs-lookup"><span data-stu-id="af634-112">If **NULL**, the identity matrix is used for the world transform.</span></span>

</dd> <dt>

<span data-ttu-id="af634-113">*pview* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af634-113">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af634-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="af634-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="af634-115">Puntatore a un [**D3DXMATRIX**](d3dxmatrix.md) che contiene una trasformazione visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="af634-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a view transform.</span></span> <span data-ttu-id="af634-116">Se è **null**, la matrice di identità viene utilizzata per la trasformazione della vista.</span><span class="sxs-lookup"><span data-stu-id="af634-116">If **NULL**, the identity matrix is used for the view transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af634-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af634-117">Return value</span></span>

<span data-ttu-id="af634-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af634-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af634-119">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="af634-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="af634-120">Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="af634-120">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="af634-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="af634-121">Remarks</span></span>

<span data-ttu-id="af634-122">Una chiamata a questo metodo (o a [**ID3DXSprite:: SetWorldViewLH**](id3dxsprite--setworldviewlh.md)) è obbligatoria se verrà eseguito il rendering dello sprite con [D3DXSprite \_ \_ Billboard](d3dxsprite.md), D3DXSprite \_ \_ Sort \_ Depth \_ FRONTTOBACK o D3DXSprite \_ \_ Sort \_ Depth \_ BACKTOFRONT flag value in [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).</span><span class="sxs-lookup"><span data-stu-id="af634-122">A call to this method (or to [**ID3DXSprite::SetWorldViewLH**](id3dxsprite--setworldviewlh.md)) is required if the sprite will be rendered with the [D3DXSprite\_\_BILLBOARD](d3dxsprite.md), D3DXSprite\_\_SORT\_DEPTH\_FRONTTOBACK, or D3DXSprite\_\_SORT\_DEPTH\_BACKTOFRONT flag value in [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af634-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af634-123">Requirements</span></span>



| <span data-ttu-id="af634-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="af634-124">Requirement</span></span> | <span data-ttu-id="af634-125">Valore</span><span class="sxs-lookup"><span data-stu-id="af634-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af634-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af634-126">Header</span></span><br/>  | <dl> <span data-ttu-id="af634-127"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="af634-127"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="af634-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="af634-128">Library</span></span><br/> | <dl> <span data-ttu-id="af634-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af634-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="af634-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af634-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af634-131">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="af634-131">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




