---
title: Modificatori per ps_2_0 e precedenti
description: I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritta nel registro di destinazione. Informazioni sui modificatori per ps_2_0 e successive.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6875789c40a2f0fab2987927662658a821de5742b2473b7947250cfb11da8155
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982891"
---
# <a name="modifiers-for-ps_2_0-and-above"></a>Modificatori per ps \_ 2 \_ 0 e superiore

I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritta nel registro di destinazione.

Questa sezione contiene informazioni di riferimento per i modificatori di istruzione implementati da pixel shader versione 2 \_ 0 e successive.



| Name                                     | Sintassi     | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------------------------|------------|------|------|-------|------|-------|
| [Baricentro](#centroid)                    | \_Baricentro | x    | x    | x     | x    | x     |
| [Precisione \_ parziale](#partial-precision) | \_Pp       | x    | x    | x     | x    | x     |
| [Saturazione](#saturate)                    | \_Sab      | x    | x    | x     | x    | x     |



 

## <a name="centroid"></a>Baricentro

Il modificatore centroide è un modificatore facoltativo che consente di stringere l'interpolazione dell'attributo all'interno dell'intervallo della primitiva quando un centro pixel multicampione non è coperto dalla primitiva. Questa operazione è visibile in [Campionamento centroid](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).

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



Inoltre, a qualsiasi [registro colori di input](dx9-graphics-reference-asm-ps-registers-input-color.md) (v ) dichiarato con una semantica dei colori verrà applicato \# automaticamente il centroid. Non è garantito che le sfumature calcolate dagli attributi campionati al centroide siano accurate.

## <a name="partial-precision"></a>Precisione parziale

Il modificatore di istruzione di precisione parziale (pp) indica le aree in cui la precisione parziale è accettabile, a condizione \_ che l'implementazione sottostante la supporti. Le implementazioni sono sempre libere di ignorare il modificatore ed eseguire le operazioni interessate con precisione completa.

Il \_ modificatore pp può verificarsi in due contesti:

-   In una dichiarazione di coordinate di trama per consentire il passaggio delle coordinate della trama pixel shader in forma di precisione parziale. Ciò consente, ad esempio, l'uso di coordinate di trama per inoltrare i dati di colore al pixel shader, che può essere più veloce con precisione parziale rispetto alla precisione completa in alcune implementazioni. In assenza di questo modificatore, le coordinate della trama devono essere passate con precisione completa.
-   In qualsiasi istruzione, incluse le istruzioni di caricamento delle trame. Ciò indica che l'implementazione può eseguire l'istruzione con precisione parziale e archiviare un risultato di precisione parziale. In assenza di un modificatore esplicito, l'istruzione deve essere eseguita con precisione completa (indipendentemente dalla precisione di input).

Esempi:


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a>Saturazione

Il modificatore di istruzione \_ saturate (sat) satura (o clamp) il risultato dell'istruzione nell'intervallo 0, 1 prima di scrivere nel registro \[ \] di destinazione.

Il modificatore di istruzione sat può essere usato con qualsiasi istruzione \_ ad eccezione di [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md)e qualsiasi istruzione tex. \*

Per ps \_ 2 \_ 0, ps 2 x e \_ \_ ps \_ 2 \_ sw, \_ [](dx9-graphics-reference-asm-ps-registers-output-color.md) [](dx9-graphics-reference-asm-ps-registers-output-depth.md)il modificatore di istruzione sat non può essere usato con istruzioni che scrivono in registri di output ( Registro colori output o Registro profondità output ). Questa restrizione non si applica a ps \_ 3 \_ 0 e successive.

Esempio:


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




