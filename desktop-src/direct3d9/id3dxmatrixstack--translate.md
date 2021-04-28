---
description: 'Metodo ID3DXMATRIXStack::Translate (D3dx9math.h): determina il prodotto della matrice corrente e della matrice di traslazione calcolata determinata dai fattori specifici (x, y e z).'
ms.assetid: e0ac72a2-9970-433e-9026-aa79edc8261c
title: Metodo ID3DXMATRIXStack::Translate (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Translate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7fadad95e8e72691a0e030ed89eedc745de2be43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093339"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx9mathh"></a><span data-ttu-id="a13e7-103">Metodo ID3DXMATRIXStack::Translate (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="a13e7-103">ID3DXMATRIXStack::Translate method (D3dx9math.h)</span></span>

<span data-ttu-id="a13e7-104">Determina il prodotto della matrice corrente e la matrice di traslazione calcolata determinata dai fattori (x, y e z) specifici.</span><span class="sxs-lookup"><span data-stu-id="a13e7-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="a13e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a13e7-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="a13e7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a13e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a13e7-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a13e7-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13e7-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a13e7-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a13e7-109">Fattore di traslazione nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="a13e7-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="a13e7-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a13e7-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13e7-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a13e7-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a13e7-112">Fattore di traslazione nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="a13e7-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="a13e7-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a13e7-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13e7-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a13e7-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a13e7-115">Fattore di traslazione nella direzione z.</span><span class="sxs-lookup"><span data-stu-id="a13e7-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a13e7-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a13e7-116">Return value</span></span>

<span data-ttu-id="a13e7-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a13e7-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a13e7-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a13e7-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a13e7-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="a13e7-119">Remarks</span></span>

<span data-ttu-id="a13e7-120">Questo metodo moltiplica a destra la matrice corrente con la matrice di traslazione calcolata (la trasformazione riguarda l'origine globale corrente).</span><span class="sxs-lookup"><span data-stu-id="a13e7-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="a13e7-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a13e7-121">Requirements</span></span>



| <span data-ttu-id="a13e7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a13e7-122">Requirement</span></span> | <span data-ttu-id="a13e7-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a13e7-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a13e7-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a13e7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a13e7-125"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="a13e7-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a13e7-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="a13e7-126">Library</span></span><br/> | <dl> <span data-ttu-id="a13e7-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a13e7-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a13e7-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a13e7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a13e7-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="a13e7-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="a13e7-130">**ID3DXMATRIXStack::TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="a13e7-130">**ID3DXMATRIXStack::TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)
</dt> </dl>

 

 
