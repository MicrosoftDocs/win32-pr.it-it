---
description: Disegna una striscia di linea nello spazio dello schermo con una matrice di trasformazione input specificata.
ms.assetid: 869dc705-8162-4cd9-ac6a-c0ce32f430c3
title: Metodo ID3DXLine::D rawTransform (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.DrawTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52407a8c92e626f8fe4d2df817017f81806cbae9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323476"
---
# <a name="id3dxlinedrawtransform-method"></a><span data-ttu-id="df58d-103">ID3DXLine::D Metodo rawTransform</span><span class="sxs-lookup"><span data-stu-id="df58d-103">ID3DXLine::DrawTransform method</span></span>

<span data-ttu-id="df58d-104">Disegna una striscia di linea nello spazio dello schermo con una matrice di trasformazione input specificata.</span><span class="sxs-lookup"><span data-stu-id="df58d-104">Draws a line strip in screen space with a specified input transformation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="df58d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df58d-105">Syntax</span></span>


```C++
HRESULT DrawTransform(
  [in] const D3DXVECTOR3 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in] const D3DXMATRIX  *pTransform,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a><span data-ttu-id="df58d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="df58d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df58d-107">*pVertexList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df58d-107">*pVertexList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df58d-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="df58d-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="df58d-109">Matrice di vertici che costituiscono la riga.</span><span class="sxs-lookup"><span data-stu-id="df58d-109">Array of vertices that make up the line.</span></span> <span data-ttu-id="df58d-110">Vedere [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="df58d-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="df58d-111">*dwVertexListCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df58d-111">*dwVertexListCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df58d-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df58d-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df58d-113">Numero di vertici nell'elenco dei vertici.</span><span class="sxs-lookup"><span data-stu-id="df58d-113">Number of vertices in the vertex list.</span></span>

</dd> <dt>

<span data-ttu-id="df58d-114">*pTransform* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df58d-114">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df58d-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="df58d-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="df58d-116">Matrice scale, Rotate e translate (SRT) per la trasformazione dei punti.</span><span class="sxs-lookup"><span data-stu-id="df58d-116">A scale, rotate, and translate (SRT) matrix for transforming the points.</span></span> <span data-ttu-id="df58d-117">Vedere [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="df58d-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span> <span data-ttu-id="df58d-118">Se questa matrice è una matrice di proiezione, tutte le righe di Stippled verranno disegnate con un modello punteggiatura con la prospettiva corretta.</span><span class="sxs-lookup"><span data-stu-id="df58d-118">If this matrix is a projection matrix, any stippled lines will be drawn with a perspective-correct stippling pattern.</span></span> <span data-ttu-id="df58d-119">In alternativa, è possibile trasformare i vertici e usare [**ID3DXLine::D RAW**](id3dxline--draw.md) per tracciare la riga con un modello stipple senza prospettive-correct.</span><span class="sxs-lookup"><span data-stu-id="df58d-119">Or, you can transform the vertices and use [**ID3DXLine::Draw**](id3dxline--draw.md) to draw the line with a nonperspective-correct stipple pattern.</span></span>

</dd> <dt>

<span data-ttu-id="df58d-120">*Colore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df58d-120">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df58d-121">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="df58d-121">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="df58d-122">Colore della linea.</span><span class="sxs-lookup"><span data-stu-id="df58d-122">Color of the line.</span></span> <span data-ttu-id="df58d-123">Vedere [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="df58d-123">See [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df58d-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df58d-124">Return value</span></span>

<span data-ttu-id="df58d-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df58d-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df58d-126">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="df58d-126">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="df58d-127">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="df58d-127">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="df58d-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df58d-128">Requirements</span></span>



| <span data-ttu-id="df58d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="df58d-129">Requirement</span></span> | <span data-ttu-id="df58d-130">Valore</span><span class="sxs-lookup"><span data-stu-id="df58d-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df58d-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df58d-131">Header</span></span><br/>  | <dl> <span data-ttu-id="df58d-132"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="df58d-132"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="df58d-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="df58d-133">Library</span></span><br/> | <dl> <span data-ttu-id="df58d-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df58d-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="df58d-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df58d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df58d-136">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="df58d-136">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
