---
title: Load (oggetto trama DirectX HLSL)
description: Legge i dati texel senza filtri o campionamenti.
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ba394fb13fd98793401b29e6343ef4fa9ff0194b7a86f22dda1e58439737b34b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119865"
---
# <a name="load-directx-hlsl-texture-object"></a>Load (oggetto trama DirectX HLSL)

Legge i dati texel senza filtri o campionamenti.



<table>
<tbody>
<tr class="odd">
<td>ret Object.Load(<dl> typeX Location,<br />
[typeX SampleIndex, ]<br />
[typeX Offset ]<br />
</dl>);</td>
</tr>
</tbody>
</table>

typeX indica che esistono quattro tipi possibili: **int**, **int2**, **int3** o **int4**.

 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Oggetto*
</dt> <dd>

Tipo [di oggetto trama](dx-graphics-hlsl-to-type.md) (ad eccezione di TextureCube o TextureCubeArray).

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Posizione*
</dt> <dd>

\[in \] Coordinate trama; l'ultimo componente specifica il livello mipmap. Questo metodo usa un sistema di coordinate basato su 0 e non un sistema UV 0.0-1.0. Il tipo di argomento dipende dal tipo texture-object.



| Tipo di oggetto                                  | Tipo di parametro |
|----------------------------------------------|----------------|
| Buffer                                       | int            |
| Texture1D, Texture2DMS                       | int2           |
| Texture1DArray, Texture 2D, Texture2DMSArray | int3           |
| Texture2DArray, Texture3D                    | int4           |



 

Ad esempio, per accedere a una trama 2D, specificare le coordinate UV per i primi due componenti e un livello mipmap per il terzo componente.

> [!Note]  
> Quando una o più coordinate in *Location* superano le dimensioni del livello u, v o w mipmap della trama, **Load** restituisce zero in tutti i componenti. Direct3D garantisce la restituzione di zero per qualsiasi risorsa a cui si accede al di fuori dei limiti.

 

</dd> <dt>

<span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*
</dt> <dd>

\[in \] Un indice di campionamento facoltativo.



| Tipo di trama                                                                                                   | Tipo di parametro |
|----------------------------------------------------------------------------------------------------------------|----------------|
| Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray | non supportato  |
| Texture2DMS, Texture2DMSArray¹                                                                                 | int            |



 

> [!Note]  
> *SampleIndex* è disponibile solo per trame multi-campione.

 

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*compensare*
</dt> <dd>

\[in \] Offset facoltativo applicato alle coordinate della trama prima del campionamento. Il tipo di offset dipende dal tipo texture-object e deve essere statico.



| Tipo di trama                                             | Tipo di parametro |
|----------------------------------------------------------|----------------|
| Texture1D, Texture1DArray                                | int            |
| Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray | int2           |
| Texture3D, Texture2DArray                                | int3           |



 

> [!Note]  
> Se si usa *Offset* con trame a più campioni, è necessario specificare anche *SampleIndex*.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il tipo restituito corrisponde al tipo nella *dichiarazione Object.* Ad esempio, un oggetto Texture2D dichiarato come "Texture2d myTexture;" ha un valore restituito <uint4> di tipo **uint4**.

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1¹ | ps \_ 4 \_ 0 | ps \_ 4 \_ 1¹ | gs \_ 4 \_ 0 | gs \_ 4 \_ 1¹ |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

-   Shader Model 4.1 è disponibile in Direct3D 10.1 o versione successiva.

## <a name="example"></a>Esempio

Questo esempio di codice parziale deriva dal file Paint.fx in [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).


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

[Oggetto texture](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




