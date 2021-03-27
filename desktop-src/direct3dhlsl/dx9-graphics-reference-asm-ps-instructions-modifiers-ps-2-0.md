---
title: Modificatori per ps_2_0 e versioni successive
description: I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritto nel registro di destinazione.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7141576b80b7a05a3e61ee9a98fa36958b1d5530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856985"
---
# <a name="modifiers-for-ps_2_0-and-above"></a>Modificatori per PS \_ 2 \_ 0 e versioni successive

I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritto nel registro di destinazione.

Questa sezione contiene informazioni di riferimento per i modificatori di istruzioni implementati da pixel shader versione 2 \_ 0 e successive.



| Name                                     | Sintassi     | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------------------------|------------|------|------|-------|------|-------|
| [Centro](#centroid)                    | \_centro | x    | x    | x     | x    | x     |
| [\_Precisione parziale](#partial-precision) | \_PP       | x    | x    | x     | x    | x     |
| [Saturazione](#saturate)                    | \_Sat      | x    | x    | x     | x    | x     |



 

## <a name="centroid"></a>Centro

Il modificatore del centro è un modificatore facoltativo che blocca l'interpolazione degli attributi all'interno dell'intervallo della primitiva quando un pixel Center multisample non è coperto dalla primitiva. Questo può essere visualizzato nel [campionamento](https://msdn.microsoft.com/library/ee415231(VS.85).aspx)del centro.

È possibile applicare il modificatore di baricentro a un'istruzione di assembly, come illustrato di seguito:


```
dcl_texcoord0_centroid v0
```



È anche possibile applicare il modificatore di baricentro a una semantica, come illustrato di seguito:


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



Inoltre, per qualsiasi [Registro dei colori di input](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) dichiarato con una semantica di colore verrà applicato automaticamente il baricentro. Non è garantita l'accuratezza delle sfumature calcolate in base agli attributi campionati di baricentro.

## <a name="partial-precision"></a>Precisione parziale

Il modificatore di istruzioni di precisione parziale ( \_ PP) indica le aree in cui la precisione parziale è accettabile, a condizione che l'implementazione sottostante la supporti. Le implementazioni sono sempre libere di ignorare il modificatore ed eseguire le operazioni interessate con la massima precisione.

Il \_ modificatore di PP può essere eseguito in due contesti:

-   In una dichiarazione di coordinata di trama per consentire il passaggio di coordinate di trama al pixel shader in formato a precisione parziale. Questo consente, ad esempio, l'uso di coordinate di trama per inoltrare i dati di colore al pixel shader, che può essere più veloce con precisione parziale rispetto alla precisione completa in alcune implementazioni. In assenza di questo modificatore, le coordinate di trama devono essere passate con la massima precisione.
-   In qualsiasi istruzione, incluse le istruzioni per il caricamento della trama. Ciò indica che l'implementazione è autorizzata a eseguire l'istruzione con precisione parziale e archiviare un risultato di precisione parziale. In assenza di un modificatore esplicito, l'istruzione deve essere eseguita a precisione completa (indipendentemente dalla precisione di input).

Esempi:


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a>Saturazione

Il modificatore di istruzioni di saturazione ( \_ Sat) satura (o clamp) il risultato dell'istruzione nell'intervallo \[ 0, 1 \] prima della scrittura nel registro di destinazione.

Il \_ modificatore di istruzioni Sat può essere usato con qualsiasi istruzione ad eccezione di [FRC-PS](frc---ps.md), [SinCos-PS](sincos---ps.md)ed eventuali \* istruzioni Tex.

Per PS \_ 2 \_ 0, PS \_ 2 \_ x e PS \_ 2 \_ SW, il \_ modificatore di istruzioni Sat non può essere usato con le istruzioni scritte in tutti i registri di output ([Registro colori di output](dx9-graphics-reference-asm-ps-registers-output-color.md) o [Registro profondità output](dx9-graphics-reference-asm-ps-registers-output-depth.md)). Questa restrizione non si applica a PS \_ 3 \_ 0 e versioni successive.

Esempio:


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




