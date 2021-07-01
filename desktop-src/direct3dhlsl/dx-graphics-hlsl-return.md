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
ms.openlocfilehash: 876c69f3ecfcf1ee1c8391ccc503b2316056b37a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119586"
---
# <a name="return-statement"></a><span data-ttu-id="14a0f-104">Istruzione return</span><span class="sxs-lookup"><span data-stu-id="14a0f-104">return Statement</span></span>

<span data-ttu-id="14a0f-105">Un'istruzione return segnala la fine di una funzione.</span><span class="sxs-lookup"><span data-stu-id="14a0f-105">A return statement signals the end of a function.</span></span>

<span data-ttu-id="14a0f-106">valore \[ restituito \] ;</span><span class="sxs-lookup"><span data-stu-id="14a0f-106">return \[value\];</span></span>



 

<span data-ttu-id="14a0f-107">L'istruzione return più semplice restituisce il controllo dalla funzione al programma chiamante. non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="14a0f-107">The simplest return statement returns control from the function to the calling program; it returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="14a0f-108">Tuttavia, un'istruzione return può restituire uno o più valori.</span><span class="sxs-lookup"><span data-stu-id="14a0f-108">However, a return statement can return one or more values.</span></span> <span data-ttu-id="14a0f-109">Questo esempio restituisce un valore letterale:</span><span class="sxs-lookup"><span data-stu-id="14a0f-109">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="14a0f-110">In questo esempio viene restituito il risultato scalare di un'espressione.</span><span class="sxs-lookup"><span data-stu-id="14a0f-110">This example returns the scalar result of an expression.</span></span>


```
return  light.enabled = true ;
```



<span data-ttu-id="14a0f-111">Questo esempio restituisce un vettore a quattro componenti costruito da una variabile locale e da un valore letterale.</span><span class="sxs-lookup"><span data-stu-id="14a0f-111">This example returns a four-component vector that is constructed from a local variable and a literal.</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="14a0f-112">Questo esempio restituisce un vettore a quattro componenti costruito dal risultato restituito da una funzione intrinseca, insieme ai valori letterali.</span><span class="sxs-lookup"><span data-stu-id="14a0f-112">This example returns a four-component vector that is constructed from the result that is returned from an intrinsic function, together with literal values.</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="14a0f-113">In questo esempio viene restituita una struttura contenente uno o più membri.</span><span class="sxs-lookup"><span data-stu-id="14a0f-113">This example returns a structure that contains one or more members.</span></span>


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



## <a name="see-also"></a><span data-ttu-id="14a0f-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="14a0f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a0f-115">Funzioni (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="14a0f-115">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




