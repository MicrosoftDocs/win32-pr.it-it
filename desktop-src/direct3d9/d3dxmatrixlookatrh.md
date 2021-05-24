---
description: 'Funzione D3DXMatrixLookAtRH (D3dx9math.h): crea una matrice di visualizzazione con la mano destra.'
ms.assetid: 10198bb9-a77e-4482-be6e-cc5f76eff30b
title: Funzione D3DXMatrixLookAtRH (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44b3a738de31edf373deb65ea9991e1e1502f47c
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335605"
---
# <a name="d3dxmatrixlookatrh-function-d3dx9mathh"></a><span data-ttu-id="8ce79-103">Funzione D3DXMatrixLookAtRH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="8ce79-103">D3DXMatrixLookAtRH function (D3dx9math.h)</span></span>

<span data-ttu-id="8ce79-104">Compila una matrice di visualizzazione con la mano destra.</span><span class="sxs-lookup"><span data-stu-id="8ce79-104">Builds a right-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ce79-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ce79-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="8ce79-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ce79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ce79-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8ce79-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ce79-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ce79-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8ce79-109">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8ce79-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8ce79-110">*pEye* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8ce79-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ce79-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ce79-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8ce79-112">Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che definisce il punto dell'occhio.</span><span class="sxs-lookup"><span data-stu-id="8ce79-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="8ce79-113">Questo valore viene usato nella traduzione.</span><span class="sxs-lookup"><span data-stu-id="8ce79-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="8ce79-114">*pAt* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8ce79-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ce79-115">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ce79-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8ce79-116">Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che definisce la destinazione di sguardo della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="8ce79-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="8ce79-117">*pUp* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8ce79-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ce79-118">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ce79-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8ce79-119">Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che definisce l'oggetto corrente, in genere \[ 0, 1, \] 0.</span><span class="sxs-lookup"><span data-stu-id="8ce79-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ce79-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ce79-120">Return value</span></span>

<span data-ttu-id="8ce79-121">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ce79-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8ce79-122">Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta una matrice di visualizzazione a destra.</span><span class="sxs-lookup"><span data-stu-id="8ce79-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ce79-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ce79-123">Remarks</span></span>

<span data-ttu-id="8ce79-124">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="8ce79-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="8ce79-125">In questo modo, la **funzione D3DXMatrixLookAtRH** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="8ce79-125">In this way, the **D3DXMatrixLookAtRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="8ce79-126">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="8ce79-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x            yaxis.x            zaxis.x           0
 xaxis.y            yaxis.y            zaxis.y           0
 xaxis.z            yaxis.z            zaxis.z           0
 -dot(xaxis, eye)   -dot(yaxis, eye)   -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="8ce79-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ce79-127">Requirements</span></span>



| <span data-ttu-id="8ce79-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ce79-128">Requirement</span></span> | <span data-ttu-id="8ce79-129">Valore</span><span class="sxs-lookup"><span data-stu-id="8ce79-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ce79-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ce79-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8ce79-131"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="8ce79-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8ce79-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="8ce79-132">Library</span></span><br/> | <dl> <span data-ttu-id="8ce79-133"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ce79-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8ce79-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ce79-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ce79-135">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="8ce79-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8ce79-136">**D3DXMatrixLookAtLH**</span><span class="sxs-lookup"><span data-stu-id="8ce79-136">**D3DXMatrixLookAtLH**</span></span>](d3dxmatrixlookatlh.md)
</dt> </dl>

 

 




