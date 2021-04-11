---
description: Determina il prodotto della matrice di traduzione calcolata determinata dai fattori specificati (x, y e z) e dalla matrice corrente.
ms.assetid: d4752a6c-2114-4016-a69f-dcc561d2c76b
title: 'Metodo ID3DXMATRIXStack:: TranslateLocal (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.TranslateLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 784e623ae47dfece9b395d423437fb6ce661b223
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235098"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx9mathh"></a><span data-ttu-id="b3d25-103">Metodo ID3DXMATRIXStack:: TranslateLocal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b3d25-103">ID3DXMATRIXStack::TranslateLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="b3d25-104">Determina il prodotto della matrice di traduzione calcolata determinata dai fattori specificati (x, y e z) e dalla matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="b3d25-104">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3d25-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3d25-105">Syntax</span></span>


```C++
HRESULT TranslateLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="b3d25-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3d25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3d25-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3d25-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3d25-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3d25-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3d25-109">Fattore di conversione nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="b3d25-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="b3d25-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3d25-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3d25-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3d25-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3d25-112">Fattore di conversione nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="b3d25-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="b3d25-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3d25-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3d25-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3d25-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3d25-115">Fattore di conversione nella direzione z.</span><span class="sxs-lookup"><span data-stu-id="b3d25-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3d25-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3d25-116">Return value</span></span>

<span data-ttu-id="b3d25-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b3d25-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b3d25-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b3d25-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3d25-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3d25-119">Remarks</span></span>

<span data-ttu-id="b3d25-120">Questo metodo consente di moltiplicare a sinistra la matrice corrente con la matrice di traduzione calcolata (la trasformazione è relativa all'origine locale dell'oggetto).</span><span class="sxs-lookup"><span data-stu-id="b3d25-120">This method left-multiplies the current matrix with the computed translation matrix (transformation is about the local origin of the object).</span></span>


```
    
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="b3d25-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3d25-121">Requirements</span></span>



| <span data-ttu-id="b3d25-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3d25-122">Requirement</span></span> | <span data-ttu-id="b3d25-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b3d25-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d25-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3d25-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b3d25-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3d25-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b3d25-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="b3d25-126">Library</span></span><br/> | <dl> <span data-ttu-id="b3d25-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3d25-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b3d25-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3d25-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3d25-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="b3d25-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="b3d25-130">**ID3DXMATRIXStack:: translate**</span><span class="sxs-lookup"><span data-stu-id="b3d25-130">**ID3DXMATRIXStack::Translate**</span></span>](id3dxmatrixstack--translate.md)
</dt> </dl>

 

 
