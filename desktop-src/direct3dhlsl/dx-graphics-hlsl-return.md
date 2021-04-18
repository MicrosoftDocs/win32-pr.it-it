---
title: Istruzione return
description: Un'istruzione return segnala la fine di una funzione.
ms.assetid: e6c097af-ba0b-4abc-8099-69882ced1e18
keywords:
- Istruzione return HLSL
topic_type:
- apiref
api_name:
- return Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 525abf6d815d2073ee39a6bc6a5a81120cf652ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104976194"
---
# <a name="return-statement"></a><span data-ttu-id="21af1-104">Istruzione return</span><span class="sxs-lookup"><span data-stu-id="21af1-104">return Statement</span></span>

<span data-ttu-id="21af1-105">Un'istruzione return segnala la fine di una funzione.</span><span class="sxs-lookup"><span data-stu-id="21af1-105">A return statement signals the end of a function.</span></span>



|                   |
|-------------------|
| <span data-ttu-id="21af1-106">\[valore restituito \] ;</span><span class="sxs-lookup"><span data-stu-id="21af1-106">return \[value\];</span></span> |



 

<span data-ttu-id="21af1-107">L'istruzione return più semplice restituisce il controllo dalla funzione al programma chiamante. non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="21af1-107">The simplest return statement returns control from the function to the calling program; it returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="21af1-108">Tuttavia, un'istruzione Return può restituire uno o più valori.</span><span class="sxs-lookup"><span data-stu-id="21af1-108">However, a return statement can return one or more values.</span></span> <span data-ttu-id="21af1-109">In questo esempio viene restituito un valore letterale:</span><span class="sxs-lookup"><span data-stu-id="21af1-109">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="21af1-110">In questo esempio viene restituito il risultato scalare di un'espressione.</span><span class="sxs-lookup"><span data-stu-id="21af1-110">This example returns the scalar result of an expression.</span></span>


```
return  light.enabled = true ;
```



<span data-ttu-id="21af1-111">In questo esempio viene restituito un vettore a quattro componenti costruito da una variabile locale e un valore letterale.</span><span class="sxs-lookup"><span data-stu-id="21af1-111">This example returns a four-component vector that is constructed from a local variable and a literal.</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="21af1-112">In questo esempio viene restituito un vettore a quattro componenti costruito dal risultato restituito da una funzione intrinseca, insieme ai valori letterali.</span><span class="sxs-lookup"><span data-stu-id="21af1-112">This example returns a four-component vector that is constructed from the result that is returned from an intrinsic function, together with literal values.</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="21af1-113">In questo esempio viene restituita una struttura che contiene uno o più membri.</span><span class="sxs-lookup"><span data-stu-id="21af1-113">This example returns a structure that contains one or more members.</span></span>


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="see-also"></a><span data-ttu-id="21af1-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21af1-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21af1-115">Funzioni (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="21af1-115">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




