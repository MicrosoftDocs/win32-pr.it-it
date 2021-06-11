---
title: Modificatori per ps_2_0 e superiori
description: I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritta nel registro di destinazione. Informazioni sui modificatori per ps_2_0 e successive.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc8ed91f8e103ebbab7c43ffe53201f0e1d5dfcf
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989286"
---
# <a name="modifiers-for-ps_2_0-and-above"></a>Modificatori per ps \_ 2 \_ 0 e superiori

I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritta nel registro di destinazione.

Questa sezione contiene informazioni di riferimento per i modificatori di istruzione implementati pixel shader versione 2 \_ 0 e successive.



| Name                                     | Sintassi     | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------------------------|------------|------|------|-------|------|-------|
| [Baricentro](#centroid)                    | \_Baricentro | x    | x    | x     | x    | x     |
| [Precisione \_ parziale](#partial-precision) | \_Pp       | x    | x    | x     | x    | x     |
| [Saturazione](#saturate)                    | \_Sab      | x    | x    | x     | x    | x     |



 

## <a name="centroid"></a>Baricentro

Il modificatore centroide è un modificatore facoltativo che stringe l'interpolazione degli attributi all'interno dell'intervallo della primitiva quando un centro pixel multicampionamento non è coperto dalla primitiva. Questa operazione può essere osservata in [Campionamento centroide.](https://msdn.microsoft.com/library/ee415231(VS.85).aspx)

È possibile applicare il modificatore centroide a un'istruzione di assembly, come illustrato di seguito:


```
dcl_texcoord0_centroid v0
```



È anche possibile applicare il modificatore centroide a una semantica, come illustrato di seguito:


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



Inoltre, a qualsiasi [registro colori di input](dx9-graphics-reference-asm-ps-registers-input-color.md) (v ) dichiarato con una semantica dei colori verrà applicato \# automaticamente il centroide. Non è garantito che le sfumature calcolate da attributi campionati al centroide siano accurate.

## <a name="partial-precision"></a>Precisione parziale

Il modificatore di istruzione di precisione parziale (pp) indica le aree in cui la precisione parziale è accettabile, a condizione \_ che l'implementazione sottostante la supporti. Le implementazioni sono sempre liberi di ignorare il modificatore ed eseguire le operazioni interessate con la massima precisione.

Il \_ modificatore pp può verificarsi in due contesti:

-   In una dichiarazione di coordinate di trama per consentire il passaggio delle coordinate della trama pixel shader in forma a precisione parziale. Ciò consente, ad esempio, l'uso di coordinate di trama per inoltrare i dati di colore al pixel shader, che può essere più veloce con precisione parziale rispetto alla precisione completa in alcune implementazioni. In assenza di questo modificatore, le coordinate della trama devono essere passate con precisione completa.
-   In qualsiasi istruzione, incluse le istruzioni di caricamento della trama. Ciò indica che l'implementazione può eseguire l'istruzione con precisione parziale e archiviare un risultato di precisione parziale. In assenza di un modificatore esplicito, l'istruzione deve essere eseguita con precisione completa (indipendentemente dalla precisione di input).

Esempi:


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a>Saturazione

Il modificatore di istruzione satura ( sat) satura (o stringe) il risultato dell'istruzione nell'intervallo \_ 0, 1 prima di scrivere nel registro \[ \] di destinazione.

Il modificatore di istruzione sat può essere usato con qualsiasi istruzione tranne \_ [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md)e qualsiasi istruzione tex. \*

Per ps \_ 2 \_ 0, ps 2 x e \_ \_ ps \_ 2 \_ sw, \_ [](dx9-graphics-reference-asm-ps-registers-output-color.md) [](dx9-graphics-reference-asm-ps-registers-output-depth.md)il modificatore di istruzione sat non può essere usato con istruzioni che scrivono in registri di output (Output Color Register o Output Depth Register). Questa restrizione non si applica a ps \_ 3 \_ 0 e versione superiore.

Esempio:


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




