---
description: Disegna una striscia di linea nello spazio dello schermo. L'input è sotto forma di matrice che definisce i punti (di D3DXVECTOR2) nell'elenco di righe.
ms.assetid: 10ad5af5-fb57-46ef-a89f-7a05dcf58826
title: 'ID3DXLine: Metodo Raw:D (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0a7492fb2128e0d9ec402d5211c20d5569ceb506
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323477"
---
# <a name="id3dxlinedraw-method"></a><span data-ttu-id="ec5c9-104">ID3DXLine::D Metodo Raw</span><span class="sxs-lookup"><span data-stu-id="ec5c9-104">ID3DXLine::Draw method</span></span>

<span data-ttu-id="ec5c9-105">Disegna una striscia di linea nello spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="ec5c9-105">Draws a line strip in screen space.</span></span> <span data-ttu-id="ec5c9-106">L'input è sotto forma di matrice che definisce i punti (di [**D3DXVECTOR2**](d3dxvector2.md)) nell'elenco di righe.</span><span class="sxs-lookup"><span data-stu-id="ec5c9-106">Input is in the form of an array that defines points (of [**D3DXVECTOR2**](d3dxvector2.md)) on the line strip.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec5c9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec5c9-107">Syntax</span></span>


```C++
HRESULT Draw(
  [in] const D3DXVECTOR2 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a><span data-ttu-id="ec5c9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec5c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec5c9-109">*pVertexList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec5c9-109">*pVertexList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec5c9-110">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="ec5c9-110">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="ec5c9-111">Matrice di vertici che costituiscono la riga.</span><span class="sxs-lookup"><span data-stu-id="ec5c9-111">Array of vertices that make up the line.</span></span> <span data-ttu-id="ec5c9-112">Vedere [**D3DXVECTOR2**](d3dxvector2.md).</span><span class="sxs-lookup"><span data-stu-id="ec5c9-112">See [**D3DXVECTOR2**](d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec5c9-113">*dwVertexListCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec5c9-113">*dwVertexListCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec5c9-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ec5c9-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ec5c9-115">Numero di vertici nell'elenco dei vertici.</span><span class="sxs-lookup"><span data-stu-id="ec5c9-115">Number of vertices in the vertex list.</span></span>

</dd> <dt>

<span data-ttu-id="ec5c9-116">*Colore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec5c9-116">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec5c9-117">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="ec5c9-117">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="ec5c9-118">Colore della linea.</span><span class="sxs-lookup"><span data-stu-id="ec5c9-118">Color of the line.</span></span> <span data-ttu-id="ec5c9-119">Vedere [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="ec5c9-119">See [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec5c9-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec5c9-120">Return value</span></span>

<span data-ttu-id="ec5c9-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ec5c9-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ec5c9-122">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ec5c9-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ec5c9-123">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="ec5c9-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec5c9-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec5c9-124">Requirements</span></span>



| <span data-ttu-id="ec5c9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec5c9-125">Requirement</span></span> | <span data-ttu-id="ec5c9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="ec5c9-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec5c9-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec5c9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ec5c9-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec5c9-128"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="ec5c9-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="ec5c9-129">Library</span></span><br/> | <dl> <span data-ttu-id="ec5c9-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec5c9-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ec5c9-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec5c9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec5c9-132">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="ec5c9-132">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
