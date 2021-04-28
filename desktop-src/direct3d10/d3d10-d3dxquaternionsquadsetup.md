---
description: "Funzione D3DXQuaternionSquadSetup (D3DX10Math.h): configura i punti di controllo per l'interpolazione quadrangolare sferica."
ms.assetid: c66227bd-8cc1-4173-9dc2-5aab9d57301e
title: Funzione D3DXQuaternionSquadSetup (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquadSetup
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8d8a778473c0b07ef984facce9c42f947755a74a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108719"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx10mathh"></a><span data-ttu-id="29568-103">Funzione D3DXQuaternionSquadSetup (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="29568-103">D3DXQuaternionSquadSetup function (D3DX10Math.h)</span></span>

<span data-ttu-id="29568-104">Imposta i punti di controllo per l'interpolazione quadrangola sferica.</span><span class="sxs-lookup"><span data-stu-id="29568-104">Sets up control points for spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="29568-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29568-105">Syntax</span></span>


```C++
void D3DXQuaternionSquadSetup(
  _In_       D3DXQUATERNION *pAOut,
  _In_       D3DXQUATERNION *pBOut,
  _In_       D3DXQUATERNION *pCOut,
  _In_ const D3DXQUATERNION *pQ0,
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2,
  _In_ const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a><span data-ttu-id="29568-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="29568-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29568-107">*pAOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="29568-107">*pAOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29568-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="29568-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="29568-109">Puntatore ad AOut.</span><span class="sxs-lookup"><span data-stu-id="29568-109">Pointer to AOut.</span></span>

</dd> <dt>

<span data-ttu-id="29568-110">*pBOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="29568-110">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29568-111">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="29568-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="29568-112">Puntatore a BOut.</span><span class="sxs-lookup"><span data-stu-id="29568-112">Pointer to BOut.</span></span>

</dd> <dt>

<span data-ttu-id="29568-113">*pCOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="29568-113">*pCOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29568-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="29568-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="29568-115">Puntatore a COut.</span><span class="sxs-lookup"><span data-stu-id="29568-115">Pointer to COut.</span></span>

</dd> <dt>

<span data-ttu-id="29568-116">*pQ0* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="29568-116">*pQ0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29568-117">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="29568-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="29568-118">Puntatore al punto di controllo di input, Q0.</span><span class="sxs-lookup"><span data-stu-id="29568-118">Pointer to the input control point, Q0.</span></span>

</dd> <dt>

<span data-ttu-id="29568-119">*pQ1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="29568-119">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29568-120">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="29568-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="29568-121">Puntatore al punto di controllo di input, Q1.</span><span class="sxs-lookup"><span data-stu-id="29568-121">Pointer to the input control point, Q1.</span></span>

</dd> <dt>

<span data-ttu-id="29568-122">*pQ2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="29568-122">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29568-123">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="29568-123">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="29568-124">Puntatore al punto di controllo di input, Q2.</span><span class="sxs-lookup"><span data-stu-id="29568-124">Pointer to the input control point, Q2.</span></span>

</dd> <dt>

<span data-ttu-id="29568-125">*pQ3* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="29568-125">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29568-126">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="29568-126">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="29568-127">Puntatore al punto di controllo di input, Q3.</span><span class="sxs-lookup"><span data-stu-id="29568-127">Pointer to the input control point, Q3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29568-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29568-128">Return value</span></span>

<span data-ttu-id="29568-129">No.</span><span class="sxs-lookup"><span data-stu-id="29568-129">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="29568-130">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="29568-130">Remarks</span></span>

<span data-ttu-id="29568-131">Questa funzione accetta quattro punti di controllo, forniti agli input pQ0, pQ1, pQ2 e pQ3.</span><span class="sxs-lookup"><span data-stu-id="29568-131">This function takes four control points, which are supplied to the inputs pQ0, pQ1, pQ2, and pQ3.</span></span> <span data-ttu-id="29568-132">La funzione modifica quindi questi valori per trovare una curva che scorre lungo il percorso più breve.</span><span class="sxs-lookup"><span data-stu-id="29568-132">The function then alters these values to find a curve that flows along the shortest path.</span></span> <span data-ttu-id="29568-133">I valori di q0, q2 e q3 vengono calcolati come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="29568-133">The values of q0, q2, and q3 are calculated as shown below.</span></span>


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



<span data-ttu-id="29568-134">Dopo aver calcolato i nuovi valori Q, i valori per AOut, BOut e COut vengono calcolati come segue:</span><span class="sxs-lookup"><span data-stu-id="29568-134">Having calculated the new Q values, the values for AOut, BOut, and COut are calculated as follows:</span></span>

<span data-ttu-id="29568-135">AOut = q1 \* e<sup> \[ -0,25\ \* (\ Ln \[ Exp(q1) \* q2 \] \ +\ Ln \[ Exp(q1) \* q0 \ \] )\ \] </sup></span><span class="sxs-lookup"><span data-stu-id="29568-135">AOut = q1 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q1)\*q2\]\ +\ Ln\[Exp(q1)\*q0\]\ )\ \]</sup></span></span>

<span data-ttu-id="29568-136">BOut = q2 \* e<sup> \[ -0,25\ \* (\ Ln \[ Exp(q2) \* q3 \] \ +\ Ln \[ Exp(q2) \* q1 \ \] )\ \] </sup></span><span class="sxs-lookup"><span data-stu-id="29568-136">BOut = q2 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q2)\*q3\]\ +\ Ln\[Exp(q2)\*q1\]\ )\ \]</sup></span></span>

<span data-ttu-id="29568-137">COut = q2</span><span class="sxs-lookup"><span data-stu-id="29568-137">COut = q2</span></span>

> [!Note]  
> <span data-ttu-id="29568-138">Ln è il metodo API [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) e Exp è il metodo API [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).</span><span class="sxs-lookup"><span data-stu-id="29568-138">Ln is the API method [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) and Exp is the API method [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).</span></span>

 

<span data-ttu-id="29568-139">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="29568-139">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

### <a name="examples"></a><span data-ttu-id="29568-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="29568-140">Examples</span></span>

<span data-ttu-id="29568-141">L'esempio seguente illustra come usare un set di chiavi quaternione (Q0, Q1, Q2, Q3) per calcolare i punti quadrangolare interni (A, B, C).</span><span class="sxs-lookup"><span data-stu-id="29568-141">The following example shows how to use a set of quaternion keys (Q0, Q1, Q2, Q3) to compute the inner quadrangle points (A, B, C).</span></span> <span data-ttu-id="29568-142">Ciò garantisce che le tangenti siano continue tra segmenti adiacenti.</span><span class="sxs-lookup"><span data-stu-id="29568-142">This ensures that the tangents are continuous across adjacent segments.</span></span>


```
      A     B
Q0    Q1    Q2    Q3
```



<span data-ttu-id="29568-143">L'esempio di codice seguente illustra come è possibile eseguire l'interpolazione tra Q1 e Q2.</span><span class="sxs-lookup"><span data-stu-id="29568-143">The following code example demonstrates how you can interpolate between Q1 and Q2.</span></span>


```
// Rotation about the z-axis
D3DXQUATERNION Q0 = D3DXQUATERNION(0,  0, 0.707f, -.707f);
D3DXQUATERNION Q1 = D3DXQUATERNION(0,  0, 0.000f, 1.000f);
D3DXQUATERNION Q2 = D3DXQUATERNION(0,  0, 0.707f, 0.707f);
D3DXQUATERNION Q3 = D3DXQUATERNION(0,  0, 1.000f, 0.000f);
D3DXQUATERNION A, B, C, Qt;
FLOAT time = 0.5f;

D3DXQuaternionSquadSetup(&A, &B, &C, &Q0, &Q1, &Q2, &Q3);
D3DXQuaternionSquad(&Qt, &Q1, &A, &B, &C, time);
```



> [!Note]
>
> -   <span data-ttu-id="29568-144">C è +/- Q2 a seconda del risultato della funzione.</span><span class="sxs-lookup"><span data-stu-id="29568-144">C is +/- Q2 depending on the result of the function.</span></span>
> -   <span data-ttu-id="29568-145">Qt è il risultato della funzione .</span><span class="sxs-lookup"><span data-stu-id="29568-145">Qt is the result of the function.</span></span>
>
> <span data-ttu-id="29568-146">Il risultato è una rotazione di 45 gradi intorno all'asse z per il tempo = 0,5.</span><span class="sxs-lookup"><span data-stu-id="29568-146">The result is a rotation of 45 degrees around the z-axis for time = 0.5.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="29568-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29568-147">Requirements</span></span>



| <span data-ttu-id="29568-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="29568-148">Requirement</span></span> | <span data-ttu-id="29568-149">Valore</span><span class="sxs-lookup"><span data-stu-id="29568-149">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29568-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29568-150">Header</span></span><br/>  | <dl> <span data-ttu-id="29568-151"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="29568-151"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="29568-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="29568-152">Library</span></span><br/> | <dl> <span data-ttu-id="29568-153"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="29568-153"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="29568-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29568-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29568-155">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="29568-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
