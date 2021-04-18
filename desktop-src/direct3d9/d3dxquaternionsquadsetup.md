---
description: Imposta i punti di controllo per l'interpolazione quadrangolare sferica.
ms.assetid: f800d457-8546-49a1-800e-e5c27af96710
title: Funzione D3DXQuaternionSquadSetup (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 04bae9dafbb9df90fdcccee830a1eecb64c1430f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322487"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx9mathh"></a><span data-ttu-id="6a5b8-103">Funzione D3DXQuaternionSquadSetup (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="6a5b8-103">D3DXQuaternionSquadSetup function (D3dx9math.h)</span></span>

<span data-ttu-id="6a5b8-104">Imposta i punti di controllo per l'interpolazione quadrangolare sferica.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-104">Sets up control points for spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a5b8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a5b8-105">Syntax</span></span>


```C++
void D3DXQuaternionSquadSetup(
  _Out_       D3DXQUATERNION *pAOut,
  _Out_       D3DXQUATERNION *pBOut,
  _Out_       D3DXQUATERNION *pCOut,
  _In_  const D3DXQUATERNION *pQ0,
  _In_  const D3DXQUATERNION *pQ1,
  _In_  const D3DXQUATERNION *pQ2,
  _In_  const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a><span data-ttu-id="6a5b8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a5b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a5b8-107">*pAOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6a5b8-107">*pAOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5b8-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a5b8-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6a5b8-109">Puntatore a AOut.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-109">Pointer to AOut.</span></span>

</dd> <dt>

<span data-ttu-id="6a5b8-110">*pBOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6a5b8-110">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5b8-111">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a5b8-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6a5b8-112">Puntatore all'attacco.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-112">Pointer to BOut.</span></span>

</dd> <dt>

<span data-ttu-id="6a5b8-113">*pCOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6a5b8-113">*pCOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5b8-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a5b8-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6a5b8-115">Puntatore a COut.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-115">Pointer to COut.</span></span>

</dd> <dt>

<span data-ttu-id="6a5b8-116">*pQ0* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a5b8-116">*pQ0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5b8-117">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="6a5b8-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6a5b8-118">Puntatore al punto di controllo di input, Q0.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-118">Pointer to the input control point, Q0.</span></span>

</dd> <dt>

<span data-ttu-id="6a5b8-119">*pQ1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a5b8-119">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5b8-120">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="6a5b8-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6a5b8-121">Puntatore al punto di controllo di input, Q1.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-121">Pointer to the input control point, Q1.</span></span>

</dd> <dt>

<span data-ttu-id="6a5b8-122">*pQ2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a5b8-122">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5b8-123">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="6a5b8-123">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6a5b8-124">Puntatore al punto di controllo di input, Q2.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-124">Pointer to the input control point, Q2.</span></span>

</dd> <dt>

<span data-ttu-id="6a5b8-125">*pQ3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a5b8-125">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5b8-126">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="6a5b8-126">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6a5b8-127">Puntatore al punto di controllo di input, Q3.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-127">Pointer to the input control point, Q3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a5b8-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a5b8-128">Return value</span></span>

<span data-ttu-id="6a5b8-129">No.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-129">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a5b8-130">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="6a5b8-130">Remarks</span></span>

<span data-ttu-id="6a5b8-131">Questa funzione accetta quattro punti di controllo, che vengono forniti agli input pQ0, pQ1, pQ2 e pQ3.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-131">This function takes four control points, which are supplied to the inputs pQ0, pQ1, pQ2, and pQ3.</span></span> <span data-ttu-id="6a5b8-132">La funzione modifica quindi questi valori per trovare una curva che scorre lungo il percorso più breve.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-132">The function then alters these values to find a curve that flows along the shortest path.</span></span> <span data-ttu-id="6a5b8-133">I valori di Q0, Q2 e Q3 vengono calcolati come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-133">The values of q0, q2, and q3 are calculated as shown below.</span></span>


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



<span data-ttu-id="6a5b8-134">Dopo aver calcolato i nuovi valori Q, i valori per AOut, BOut e COut vengono calcolati come segue:</span><span class="sxs-lookup"><span data-stu-id="6a5b8-134">Having calculated the new Q values, the values for AOut, BOut, and COut are calculated as follows:</span></span>

<span data-ttu-id="6a5b8-135">AOut = Q1 \* e<sup> \[ -0,25 \ \* (\ LN \[ Exp (Q1) \* Q2 \] \ + \ LN \[ Exp (Q1) \* Q0 \] \) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="6a5b8-135">AOut = q1 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q1)\*q2\]\ +\ Ln\[Exp(q1)\*q0\]\ )\ \]</sup></span></span>

<span data-ttu-id="6a5b8-136">BOut = Q2 \* e<sup> \[ -0,25 \ \* (\ LN \[ Exp (Q2) \* Q3 \] \ + \ LN \[ Exp (Q2) \* Q1 \] \) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="6a5b8-136">BOut = q2 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q2)\*q3\]\ +\ Ln\[Exp(q2)\*q1\]\ )\ \]</sup></span></span>

<span data-ttu-id="6a5b8-137">COut = Q2</span><span class="sxs-lookup"><span data-stu-id="6a5b8-137">COut = q2</span></span>

> [!Note]  
> <span data-ttu-id="6a5b8-138">Ln è il metodo API [**D3DXQuaternionLn**](d3dxquaternionln.md) e exp è il metodo API [**D3DXQuaternionExp**](d3dxquaternionexp.md).</span><span class="sxs-lookup"><span data-stu-id="6a5b8-138">Ln is the API method [**D3DXQuaternionLn**](d3dxquaternionln.md) and Exp is the API method [**D3DXQuaternionExp**](d3dxquaternionexp.md).</span></span>

 

<span data-ttu-id="6a5b8-139">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-139">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

### <a name="examples"></a><span data-ttu-id="6a5b8-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="6a5b8-140">Examples</span></span>

<span data-ttu-id="6a5b8-141">Nell'esempio seguente viene illustrato come utilizzare un set di chiavi Quaternion (q0, Q1, Q2, Q3) per calcolare i punti quadrangolari interni (A, B, C).</span><span class="sxs-lookup"><span data-stu-id="6a5b8-141">The following example shows how to use a set of quaternion keys (Q0, Q1, Q2, Q3) to compute the inner quadrangle points (A, B, C).</span></span> <span data-ttu-id="6a5b8-142">In questo modo si garantisce che le tangenti siano continue tra i segmenti adiacenti.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-142">This ensures that the tangents are continuous across adjacent segments.</span></span>


```
      A     B
Q0    Q1    Q2    Q3
```



<span data-ttu-id="6a5b8-143">Nell'esempio di codice riportato di seguito viene illustrato come è possibile interpolare tra Q1 e Q2.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-143">The following code example demonstrates how you can interpolate between Q1 and Q2.</span></span>


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
> -   <span data-ttu-id="6a5b8-144">C è +/-Q2 a seconda del risultato della funzione.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-144">C is +/- Q2 depending on the result of the function.</span></span>
> -   <span data-ttu-id="6a5b8-145">QT è il risultato della funzione.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-145">Qt is the result of the function.</span></span>
>
> <span data-ttu-id="6a5b8-146">Il risultato è una rotazione di 45 gradi intorno all'asse z per time = 0,5.</span><span class="sxs-lookup"><span data-stu-id="6a5b8-146">The result is a rotation of 45 degrees around the z-axis for time = 0.5.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6a5b8-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a5b8-147">Requirements</span></span>



| <span data-ttu-id="6a5b8-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a5b8-148">Requirement</span></span> | <span data-ttu-id="6a5b8-149">Valore</span><span class="sxs-lookup"><span data-stu-id="6a5b8-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a5b8-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a5b8-150">Header</span></span><br/>  | <dl> <span data-ttu-id="6a5b8-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a5b8-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6a5b8-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="6a5b8-152">Library</span></span><br/> | <dl> <span data-ttu-id="6a5b8-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a5b8-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6a5b8-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a5b8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a5b8-155">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="6a5b8-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6a5b8-156">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="6a5b8-156">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




