---
title: ResInfo (SM4-ASM)
description: Eseguire una query sulle dimensioni di una determinata risorsa di input.
ms.assetid: 5D549AC6-E0CB-4395-953C-5E5ECEEE234D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a252195a4b59ed791f6ac625fe1d95bbd9925f1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398227"
---
# <a name="resinfo-sm4---asm"></a>ResInfo (SM4-ASM)

Eseguire una query sulle dimensioni di una determinata risorsa di input.



| ResInfo \[ \_ uint \|\_rcpFloat \] dest \[ . mask \] , srcMipLevel. Select \_ Component, srcResource \[ . Swizzle\] |
|-----------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                                               |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[nell' \] indirizzo del risultato dell'operazione.<br/>                             |
| <span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*<br/> | \[nel \] livello MIP.<br/>                                                          |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] una \# \# trama di input t o u per la quale vengono eseguite query sulle dimensioni. <br/> |



 

## <a name="remarks"></a>Commenti

*srcMipLevel* viene letto come Unsigned Integer scalare, quindi è necessario un selettore di componenti singolo per il registro di origine, se non è un valore scalare immediato.

*dest* riceve \[ la larghezza, l'altezza, la profondità o la dimensione della matrice, Total-MIP-Count \] , selezionato dalla maschera di scrittura.

I valori di larghezza, altezza e profondità restituiti sono per il livello MIP selezionato dal parametro *srcMipLevel* e sono in numero di Texel, indipendentemente dalle dimensioni dei dati Texel. Per le risorse multisample (texture2D \[ array \] MS \# ), le dimensioni e l'altezza vengono restituite anche nei Texel, non negli esempi.

Il numero totale MIP restituito in *dest. w* non è influenzato dal parametro *srcMipLevel* .

Per UAV (u \# ), il numero di livelli MIP è sempre 1.

Tutti gli aspetti di questa istruzione sono basati sulle caratteristiche della visualizzazione risorse associate a t \# /u \# , non alla risorsa di base sottostante.

I valori restituiti sono tutti a virgola mobile, a meno che non \_ venga usato il modificatore uint, nel qual caso i valori restituiti sono tutti numeri interi. Se \_ viene usato il modificatore rcpFloat, tutti i valori restituiti sono a virgola mobile e la larghezza, l'altezza e la profondità vengono restituiti come reciproci (1.0 f/Width, 1.0 f/Height, 1.0 f/depth), incluso inf se Width/Height/depth sono 0 dal comportamento *srcMipLevel* out-of-range. Il \_ modificatore rcpFloat si applica solo ai valori di larghezza, altezza e profondità restituiti e non si applica ai valori impostati su 0 e pertanto non restituiti e non si applica anche alle dimensioni della matrice restituite.

Swizzle in *srcResource* consente di swizzled arbitrariamente i valori restituiti prima che vengano scritti nella destinazione.

Se *srcResource* è un Texture1D, la larghezza viene restituita in *dest. x* e *dest. YZ* viene impostato su 0.

Se *srcResource* è un Texture1DArray, la larghezza viene restituita in *dest. x*, la dimensione della matrice viene restituita in *dest. y* e *dest. z* è impostato su 0.

Se *srcResource* è un Texture2D, la larghezza e l'altezza vengono restituite in *dest. XY* e *dest. z* è impostato su 0.

Se *srcResource* è un Texture2DArray, la larghezza e l'altezza vengono restituite in *dest. XY* e la dimensione della matrice viene restituita in *dest. z*.

Se *srcResource* è un Texture3D, viene restituita la larghezza, l'altezza e la profondità in *dest.xyz*.

Se *srcResource* è un TextureCube, la larghezza e l'altezza delle dimensioni del singolo cubo vengono restituite in *dest. XY* e *dest. z* è impostato su 0.

Se *srcResource* è un TextureCubeArray, la larghezza e l'altezza delle singole dimensioni del cubo vengono restituite in *dest. XY*. *dest. z* è impostato su un valore non definito.

Se il morsetto MIP per risorsa è stato specificato in *srcResource*, ResInfo restituisce sempre il numero totale di mipmap nella visualizzazione per il conteggio MIP, indipendentemente dal morsetto. Tuttavia, se le dimensioni di un determinato miplevel sono richieste da ResInfo e miplevel è stato bloccato, ad esempio un morsetto di 2,2 significa che MIPS 0 e 1 sono stati bloccati, le dimensioni restituite non sono definite. Alcune implementazioni restituiranno il comportamento fuori limite specificato per ResInfo quando miplevel non è compreso nell'intervallo. Altre implementazioni restituiranno le dimensioni del MIP come se non fosse stato bloccato.

### <a name="restrictions"></a>Restrizioni

-   *srcResource* deve essere un \# Registro t o u \# che non sia un buffer, ma è una trama \* .
-   L'indirizzamento relativo di *srcResource* non è consentito.
-   *srcMipLevel* deve usare un selettore di componente singolo se non è un controllo immediato scalare.
-   Il recupero da t \# o u \# a cui non è associato alcun elemento restituisce 0 per Width, Height, depth o arraySize e Total-MIP-Count. Il \_ modificatore rcpFloat viene comunque rispettato in questo caso, restituendo quindi inf per i valori restituiti applicabili.
-   Se *srcMipLevel* non è compreso nell'intervallo del numero disponibile di mipLevels nella risorsa, il comportamento per la dimensione restituita (*dest.xyz*) è identico a quello di una \# risorsa t o u non associata \# . Il numero totale di MIP viene comunque restituito in *dest. w* in questo caso.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





