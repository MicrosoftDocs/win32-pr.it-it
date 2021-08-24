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
ms.openlocfilehash: b8b7a8cc846e165c1c0bafa435bd4f4fe655ace5605b03b9821a08109fd65431
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726461"
---
# <a name="return-statement"></a>Istruzione return

Un'istruzione return segnala la fine di una funzione.

valore \[ restituito \] ;



 

L'istruzione return più semplice restituisce il controllo dalla funzione al programma chiamante. non restituisce alcun valore.


```
void main()
{
    return ;
}
```



Tuttavia, un'istruzione return può restituire uno o più valori. Questo esempio restituisce un valore letterale:


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



Questo esempio restituisce un vettore a quattro componenti costruito da una variabile locale e da un valore letterale.


```
return  float4(color.rgb, 1) ;
```



Questo esempio restituisce un vettore a quattro componenti costruito dal risultato restituito da una funzione intrinseca, insieme ai valori letterali.


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



In questo esempio viene restituita una struttura contenente uno o più membri.


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

 

 




