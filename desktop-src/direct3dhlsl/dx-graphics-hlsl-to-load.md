---
title: Load (oggetto trama DirectX HLSL)
description: Legge i dati di Texel senza filtro o campionamento.
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 08d3964788a238492ff7d5189544603b35808465
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "104123318"
---
# <a name="load-directx-hlsl-texture-object"></a>Load (oggetto trama DirectX HLSL)

Legge i dati di Texel senza filtro o campionamento.



<table>
<tbody>
<tr class="odd">
<td>RET Object. Load (<dl> Percorso typeX,<br />
[typeX SampleIndex,]<br />
[offset typeX]<br />
</dl>);</td>
</tr>
</tbody>
</table>

typeX indica che ci sono quattro tipi possibili: **int**, **int2**, **INT3** o **INT4**.

 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Oggetto*
</dt> <dd>

Un tipo di [oggetto trama](dx-graphics-hlsl-to-type.md) (ad eccezione di TextureCube o TextureCubeArray).

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Percorso*
</dt> <dd>

\[nelle \] coordinate di trama; l'ultimo componente specifica il livello mipmap. Questo metodo usa un sistema di coordinate basato su 0 e non un sistema UV 0,0-1.0. Il tipo di argomento dipende dal tipo di oggetto trama.



| Tipo di oggetto                                  | Tipo di parametro |
|----------------------------------------------|----------------|
| Buffer                                       | INT            |
| Texture1D, Texture2DMS                       | int2           |
| Texture1DArray, trama 2D, Texture2DMSArray | int3           |
| Texture2DArray, Texture3D                    | int4           |



 

Ad esempio, per accedere a una trama 2D, fornire le coordinate UV per i primi due componenti e un livello di mipmap per il terzo componente.

> [!Note]  
> Quando una o più coordinate nella *posizione* superano le dimensioni del livello u, v o w mipmap della trama, **Load** restituisce zero in tutti i componenti. Direct3D garantisce che restituisca zero per tutte le risorse a cui si accede fuori limite.

 

</dd> <dt>

<span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*
</dt> <dd>

\[in \] un indice di campionamento facoltativo.



| Tipo di trama                                                                                                   | Tipo di parametro |
|----------------------------------------------------------------------------------------------------------------|----------------|
| Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray | non supportato  |
| Texture2DMS, Texture2DMSArray ¹                                                                                 | INT            |



 

> [!Note]  
> *SampleIndex* è disponibile solo per le trame multicampionamento.

 

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*
</dt> <dd>

\[in \] un offset facoltativo applicato alle coordinate di trama prima del campionamento. Il tipo di offset dipende dal tipo di oggetto trama e deve essere statico.



| Tipo di trama                                             | Tipo di parametro |
|----------------------------------------------------------|----------------|
| Texture1D, Texture1DArray                                | INT            |
| Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray | int2           |
| Texture3D, Texture2DArray                                | int3           |



 

> [!Note]  
> Se si usa l' *offset* con trame multicampionamento, è necessario specificare anche *SampleIndex*.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il tipo restituito corrisponde al tipo nella dichiarazione dell' *oggetto* . Ad esempio, un oggetto Texture2D dichiarato come "Texture2d <uint4> texture;" ha un valore restituito di tipo **uint4**.

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1 ¹ | PS \_ 4 \_ 0 | PS \_ 4 \_ 1 ¹ | GS \_ 4 \_ 0 | GS \_ 4 \_ 1 ¹ |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

-   Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.

## <a name="example"></a>Esempio

Questo esempio di codice parziale viene dal file Paint. FX nell' [esempio AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).


```
// Object Declarations
Buffer<float4> g_ParticleBuffer;

// Shader body calling the intrinsic function
float4 PSPaint(PSQuadIn input) : SV_Target
{       
    ... 
    for( int i=g_ParticleStart; i<g_NumParticles; i+=g_ParticleStep )
    {
        ... 
        // load the particle
        float4 particlePos = g_ParticleBuffer.Load( i*4 );
        float4 particleColor = g_ParticleBuffer.Load( (i*4) + 2 );
        ...     
    }
    ...
}   
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Texture-oggetto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




