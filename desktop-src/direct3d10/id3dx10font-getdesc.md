---
description: Ottiene una descrizione dell'oggetto del tipo di carattere corrente.
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: 'Metodo ID3DX10Font:: getdesc (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDesc
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 59a7e361ebb6254fcc49eab30ff44ab39c38fd76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323162"
---
# <a name="id3dx10fontgetdesc-method"></a><span data-ttu-id="c4034-103">Metodo ID3DX10Font:: getdesc</span><span class="sxs-lookup"><span data-stu-id="c4034-103">ID3DX10Font::GetDesc method</span></span>

<span data-ttu-id="c4034-104">Ottiene una descrizione dell'oggetto del tipo di carattere corrente.</span><span class="sxs-lookup"><span data-stu-id="c4034-104">Get a description of the current font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4034-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4034-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="c4034-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4034-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4034-107">*pDesc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4034-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4034-108">Tipo: **[ **d3dx10 \_ Font \_ desc**](d3dx10-font-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="c4034-108">Type: **[**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md)\***</span></span>

<span data-ttu-id="c4034-109">Puntatore a una struttura del [**tipo di carattere d3dx10 che \_ \_**](d3dx10-font-desc.md) descrive l'oggetto del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="c4034-109">Pointer to a [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md) structure that describes the font object.</span></span> <span data-ttu-id="c4034-110">Se viene definito UNICODE, viene restituito un puntatore a un \_ DESCW D3DX10FONT; in caso contrario, viene restituito un puntatore a un D3DX10FONT \_ Desca.</span><span class="sxs-lookup"><span data-stu-id="c4034-110">If UNICODE is defined, a pointer to a D3DX10FONT\_DESCW is returned; otherwise a pointer to a D3DX10FONT\_DESCA is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4034-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4034-111">Return value</span></span>

<span data-ttu-id="c4034-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4034-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4034-113">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c4034-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c4034-114">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c4034-114">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4034-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4034-115">Remarks</span></span>

<span data-ttu-id="c4034-116">Questo metodo descrive gli oggetti Font Unicode se è definito UNICODE.</span><span class="sxs-lookup"><span data-stu-id="c4034-116">This method describes Unicode font objects if UNICODE is defined.</span></span> <span data-ttu-id="c4034-117">In caso contrario, viene chiamato getdesca, che restituisce un puntatore alla \_ struttura D3DX10FONT Desca.</span><span class="sxs-lookup"><span data-stu-id="c4034-117">Otherwise GetDescA is called, which returns a pointer to the D3DX10FONT\_DESCA structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4034-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4034-118">Requirements</span></span>



| <span data-ttu-id="c4034-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4034-119">Requirement</span></span> | <span data-ttu-id="c4034-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c4034-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4034-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4034-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c4034-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4034-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4034-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4034-123">Library</span></span><br/> | <dl> <span data-ttu-id="c4034-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4034-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4034-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4034-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4034-126">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="c4034-126">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="c4034-127">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="c4034-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




