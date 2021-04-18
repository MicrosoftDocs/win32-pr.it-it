---
description: Imposta i punti di controllo per l'interpolazione quadrangolare sferica.
ms.assetid: c66227bd-8cc1-4173-9dc2-5aab9d57301e
title: Funzione D3DXQuaternionSquadSetup (D3DX10Math. h)
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
ms.openlocfilehash: 4a0683bce3642b0300e68be348d8aed39b3c333d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323335"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx10mathh"></a><span data-ttu-id="bc41b-103">Funzione D3DXQuaternionSquadSetup (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="bc41b-103">D3DXQuaternionSquadSetup function (D3DX10Math.h)</span></span>

<span data-ttu-id="bc41b-104">Imposta i punti di controllo per l'interpolazione quadrangolare sferica.</span><span class="sxs-lookup"><span data-stu-id="bc41b-104">Sets up control points for spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc41b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc41b-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="bc41b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc41b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc41b-107">*pAOut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc41b-107">*pAOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc41b-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc41b-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bc41b-109">Puntatore a AOut.</span><span class="sxs-lookup"><span data-stu-id="bc41b-109">Pointer to AOut.</span></span>

</dd> <dt>

<span data-ttu-id="bc41b-110">*pBOut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc41b-110">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc41b-111">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc41b-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bc41b-112">Puntatore all'attacco.</span><span class="sxs-lookup"><span data-stu-id="bc41b-112">Pointer to BOut.</span></span>

</dd> <dt>

<span data-ttu-id="bc41b-113">*pCOut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc41b-113">*pCOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc41b-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc41b-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bc41b-115">Puntatore a COut.</span><span class="sxs-lookup"><span data-stu-id="bc41b-115">Pointer to COut.</span></span>

</dd> <dt>

<span data-ttu-id="bc41b-116">*pQ0* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc41b-116">*pQ0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc41b-117">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="bc41b-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bc41b-118">Puntatore al punto di controllo di input, Q0.</span><span class="sxs-lookup"><span data-stu-id="bc41b-118">Pointer to the input control point, Q0.</span></span>

</dd> <dt>

<span data-ttu-id="bc41b-119">*pQ1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc41b-119">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc41b-120">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="bc41b-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bc41b-121">Puntatore al punto di controllo di input, Q1.</span><span class="sxs-lookup"><span data-stu-id="bc41b-121">Pointer to the input control point, Q1.</span></span>

</dd> <dt>

<span data-ttu-id="bc41b-122">*pQ2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc41b-122">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc41b-123">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="bc41b-123">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bc41b-124">Puntatore al punto di controllo di input, Q2.</span><span class="sxs-lookup"><span data-stu-id="bc41b-124">Pointer to the input control point, Q2.</span></span>

</dd> <dt>

<span data-ttu-id="bc41b-125">*pQ3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc41b-125">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc41b-126">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="bc41b-126">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bc41b-127">Puntatore al punto di controllo di input, Q3.</span><span class="sxs-lookup"><span data-stu-id="bc41b-127">Pointer to the input control point, Q3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc41b-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc41b-128">Return value</span></span>

<span data-ttu-id="bc41b-129">No.</span><span class="sxs-lookup"><span data-stu-id="bc41b-129">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc41b-130">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="bc41b-130">Remarks</span></span>

<span data-ttu-id="bc41b-131">Questa funzione accetta quattro punti di controllo, che vengono forniti agli input pQ0, pQ1, pQ2 e pQ3.</span><span class="sxs-lookup"><span data-stu-id="bc41b-131">This function takes four control points, which are supplied to the inputs pQ0, pQ1, pQ2, and pQ3.</span></span> <span data-ttu-id="bc41b-132">La funzione modifica quindi questi valori per trovare una curva che scorre lungo il percorso più breve.</span><span class="sxs-lookup"><span data-stu-id="bc41b-132">The function then alters these values to find a curve that flows along the shortest path.</span></span> <span data-ttu-id="bc41b-133">I valori di Q0, Q2 e Q3 vengono calcolati come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="bc41b-133">The values of q0, q2, and q3 are calculated as shown below.</span></span>


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



<span data-ttu-id="bc41b-134">Dopo aver calcolato i nuovi valori Q, i valori per AOut, BOut e COut vengono calcolati come segue:</span><span class="sxs-lookup"><span data-stu-id="bc41b-134">Having calculated the new Q values, the values for AOut, BOut, and COut are calculated as follows:</span></span>

<span data-ttu-id="bc41b-135">AOut = Q1 \* e<sup> \[ -0,25 \ \* (\ LN \[ Exp (Q1) \* Q2 \] \ + \ LN \[ Exp (Q1) \* Q0 \] \) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="bc41b-135">AOut = q1 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q1)\*q2\]\ +\ Ln\[Exp(q1)\*q0\]\ )\ \]</sup></span></span>

<span data-ttu-id="bc41b-136">BOut = Q2 \* e<sup> \[ -0,25 \ \* (\ LN \[ Exp (Q2) \* Q3 \] \ + \ LN \[ Exp (Q2) \* Q1 \] \) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="bc41b-136">BOut = q2 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q2)\*q3\]\ +\ Ln\[Exp(q2)\*q1\]\ )\ \]</sup></span></span>

<span data-ttu-id="bc41b-137">COut = Q2</span><span class="sxs-lookup"><span data-stu-id="bc41b-137">COut = q2</span></span>

> [!Note]  
> <span data-ttu-id="bc41b-138">Ln è il metodo API [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) e exp è il metodo API [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).</span><span class="sxs-lookup"><span data-stu-id="bc41b-138">Ln is the API method [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) and Exp is the API method [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).</span></span>

 

<span data-ttu-id="bc41b-139">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="bc41b-139">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

### <a name="examples"></a><span data-ttu-id="bc41b-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="bc41b-140">Examples</span></span>

<span data-ttu-id="bc41b-141">Nell'esempio seguente viene illustrato come utilizzare un set di chiavi Quaternion (q0, Q1, Q2, Q3) per calcolare i punti quadrangolari interni (A, B, C).</span><span class="sxs-lookup"><span data-stu-id="bc41b-141">The following example shows how to use a set of quaternion keys (Q0, Q1, Q2, Q3) to compute the inner quadrangle points (A, B, C).</span></span> <span data-ttu-id="bc41b-142">In questo modo si garantisce che le tangenti siano continue tra i segmenti adiacenti.</span><span class="sxs-lookup"><span data-stu-id="bc41b-142">This ensures that the tangents are continuous across adjacent segments.</span></span>


```
      A     B
Q0    Q1    Q2    Q3
```



<span data-ttu-id="bc41b-143">Nell'esempio di codice riportato di seguito viene illustrato come è possibile interpolare tra Q1 e Q2.</span><span class="sxs-lookup"><span data-stu-id="bc41b-143">The following code example demonstrates how you can interpolate between Q1 and Q2.</span></span>


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
> -   <span data-ttu-id="bc41b-144">C è +/-Q2 a seconda del risultato della funzione.</span><span class="sxs-lookup"><span data-stu-id="bc41b-144">C is +/- Q2 depending on the result of the function.</span></span>
> -   <span data-ttu-id="bc41b-145">QT è il risultato della funzione.</span><span class="sxs-lookup"><span data-stu-id="bc41b-145">Qt is the result of the function.</span></span>
>
> <span data-ttu-id="bc41b-146">Il risultato è una rotazione di 45 gradi intorno all'asse z per time = 0,5.</span><span class="sxs-lookup"><span data-stu-id="bc41b-146">The result is a rotation of 45 degrees around the z-axis for time = 0.5.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bc41b-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc41b-147">Requirements</span></span>



| <span data-ttu-id="bc41b-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc41b-148">Requirement</span></span> | <span data-ttu-id="bc41b-149">Valore</span><span class="sxs-lookup"><span data-stu-id="bc41b-149">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc41b-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc41b-150">Header</span></span><br/>  | <dl> <span data-ttu-id="bc41b-151"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc41b-151"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="bc41b-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="bc41b-152">Library</span></span><br/> | <dl> <span data-ttu-id="bc41b-153"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc41b-153"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bc41b-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc41b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc41b-155">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="bc41b-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
