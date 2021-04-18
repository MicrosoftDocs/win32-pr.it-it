---
description: Ottiene una descrizione dell'oggetto del tipo di carattere corrente. GetDescW e getdesca sono identici a questo metodo, ad eccezione del fatto che un puntatore viene restituito a una \_ struttura D3DXFONT DESCW o D3DXFONT \_ desca, rispettivamente.
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: 'Metodo ID3DXFont:: getdesc (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3310971e360fb9994a30d62349d3e7e4b764c7d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322618"
---
# <a name="id3dxfontgetdesc-method"></a><span data-ttu-id="744d7-104">Metodo ID3DXFont:: getdesc</span><span class="sxs-lookup"><span data-stu-id="744d7-104">ID3DXFont::GetDesc method</span></span>

<span data-ttu-id="744d7-105">Ottiene una descrizione dell'oggetto del tipo di carattere corrente.</span><span class="sxs-lookup"><span data-stu-id="744d7-105">Gets a description of the current font object.</span></span> <span data-ttu-id="744d7-106">GetDescW e getdesca sono identici a questo metodo, ad eccezione del fatto che un puntatore viene restituito a una struttura [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) o **D3DXFONT \_ Desca** , rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="744d7-106">GetDescW and GetDescA are identical to this method, except that a pointer is returned to a [**D3DXFONT\_DESCW**](d3dxfont-desc.md) or **D3DXFONT\_DESCA** structure, respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="744d7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="744d7-107">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="744d7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="744d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="744d7-109">*pDesc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="744d7-109">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="744d7-110">Tipo: **[ **D3DXFONT \_ desc**](d3dxfont-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="744d7-110">Type: **[**D3DXFONT\_DESC**](d3dxfont-desc.md)\***</span></span>

<span data-ttu-id="744d7-111">Puntatore a una struttura [**D3DXFONT \_ desc**](d3dxfont-desc.md) che descrive l'oggetto del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="744d7-111">Pointer to a [**D3DXFONT\_DESC**](d3dxfont-desc.md) structure that describes the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="744d7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="744d7-112">Return value</span></span>

<span data-ttu-id="744d7-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="744d7-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="744d7-114">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="744d7-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="744d7-115">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="744d7-115">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="744d7-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="744d7-116">Remarks</span></span>

<span data-ttu-id="744d7-117">Questo metodo descrive gli oggetti Font Unicode se è definito UNICODE.</span><span class="sxs-lookup"><span data-stu-id="744d7-117">This method describes Unicode font objects if UNICODE is defined.</span></span> <span data-ttu-id="744d7-118">In caso contrario, viene chiamato getdesca, che restituisce un puntatore alla struttura [**D3DXFONT \_ Desca**](d3dxfont-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="744d7-118">Otherwise GetDescA is called, which returns a pointer to the [**D3DXFONT\_DESCA**](d3dxfont-desc.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="744d7-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="744d7-119">Requirements</span></span>



| <span data-ttu-id="744d7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="744d7-120">Requirement</span></span> | <span data-ttu-id="744d7-121">Valore</span><span class="sxs-lookup"><span data-stu-id="744d7-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="744d7-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="744d7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="744d7-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="744d7-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="744d7-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="744d7-124">Library</span></span><br/> | <dl> <span data-ttu-id="744d7-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="744d7-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="744d7-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="744d7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="744d7-127">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="744d7-127">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 




