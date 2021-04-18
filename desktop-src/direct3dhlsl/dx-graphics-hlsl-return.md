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
# <a name="return-statement"></a>Istruzione return

Un'istruzione return segnala la fine di una funzione.



|                   |
|-------------------|
| \[valore restituito \] ; |



 

L'istruzione return più semplice restituisce il controllo dalla funzione al programma chiamante. non restituisce alcun valore.


```
void main()
{
    return ;
}
```



Tuttavia, un'istruzione Return può restituire uno o più valori. In questo esempio viene restituito un valore letterale:


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



In questo esempio viene restituito il risultato scalare di un'espressione.


```
return  light.enabled = true ;
```



In questo esempio viene restituito un vettore a quattro componenti costruito da una variabile locale e un valore letterale.


```
return  float4(color.rgb, 1) ;
```



In questo esempio viene restituito un vettore a quattro componenti costruito dal risultato restituito da una funzione intrinseca, insieme ai valori letterali.


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



In questo esempio viene restituita una struttura che contiene uno o più membri.


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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




