---
title: resinfo (sm4 - asm)
description: Esegue una query delle dimensioni di una determinata risorsa di input.
ms.assetid: 5D549AC6-E0CB-4395-953C-5E5ECEEE234D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb23a6790c113702e59fc53f85a4d838907fe5ff658c29d83e37e3f620a9dc79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095321"
---
# <a name="resinfo-sm4---asm"></a>resinfo (sm4 - asm)

Esegue una query delle dimensioni di una determinata risorsa di input.



| resinfo \[ \_ uint\|\_rcpFloat \] dest \[ .mask \] , srcMipLevel.select \_ component, srcResource \[ .swizzle\] |
|-----------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                                               |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Indirizzo del risultato dell'operazione.<br/>                             |
| <span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*<br/> | \[in \] Il livello mip.<br/>                                                          |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] una trama di input t o u per la quale vengono sottoposti a query le \# \# dimensioni. <br/> |



 

## <a name="remarks"></a>Commenti

*srcMipLevel* viene letto come un intero senza segno scalare, quindi è necessario un selettore di componente singolo per il registro di origine, se non è un valore immediato scalare.

*dest* riceve \[ larghezza, altezza, profondità o dimensione della matrice, total-mip-count, selezionato dalla maschera di \] scrittura.

I valori di larghezza, altezza e profondità restituiti sono per il livello mip selezionato dal parametro *srcMipLevel* e sono in numero di texel, indipendentemente dalle dimensioni dei dati texel. Per le risorse multicampionamento (texture2D Array MS), anche la larghezza e l'altezza vengono restituite \[ \] in \# texel, non in campioni.

Il conteggio mip totale restituito in *dest.w* non è interessato dal *parametro srcMipLevel.*

Per gli UAV (u \# ), il numero di livelli mip è sempre 1.

Tutti gli aspetti di questa istruzione sono basati sulle caratteristiche della visualizzazione risorse associata a t \# /u \# , non alla risorsa di base sottostante.

I valori restituiti sono tutti a virgola mobile, a meno che non venga usato il modificatore uint, nel qual caso \_ i valori restituiti sono tutti numeri interi. Se si usa il modificatore rcpFloat, tutti i valori restituiti sono a virgola mobile e larghezza, altezza e profondità vengono restituiti come \_ reciproci (1,0f/width, 1,0f/height, 1,0f/depth), incluso INF se width/height/depth è 0 dal comportamento *srcMipLevel* non compreso nell'intervallo. Il modificatore rcpFloat si applica solo ai valori restituiti di larghezza, altezza e profondità e non ai valori impostati su 0 e quindi non restituiti e non si applica anche ai valori restituiti dalle dimensioni della \_ matrice.

Lo swizzle in *srcResource* consente di eseguire lo swizzle arbitrario dei valori restituiti prima che siano scritti nella destinazione.

Se *srcResource* è texture1D, la larghezza viene restituita in *dest.x* e *dest.yz* è impostato su 0.

Se *srcResource* è un oggetto Texture1DArray, la larghezza viene restituita in *dest.x*, le dimensioni della matrice vengono restituite in *dest.y* e *dest.z* è impostato su 0.

Se *srcResource* è texture2D, la larghezza e l'altezza vengono restituite in *dest.xy* e *dest.z* è impostato su 0.

Se *srcResource* è un oggetto Texture2DArray, la larghezza e l'altezza vengono restituite in *dest.xy* e le dimensioni della matrice vengono restituite in *dest.z.*

Se *srcResource* è un oggetto Texture3D, la larghezza, l'altezza e la profondità vengono restituite in *dest.xyz*.

Se *srcResource* è un oggetto TextureCube, la larghezza e l'altezza delle singole dimensioni della faccia del cubo vengono restituite in *dest.xy* e *dest.z* viene impostato su 0.

Se *srcResource è* un oggetto TextureCubeArray, la larghezza e l'altezza delle singole dimensioni della faccia del cubo vengono restituite in *dest.xy.* *dest.z* è impostato su un valore non definito.

Se è stato specificato un mip clamp per risorsa in *srcResource,* resinfo restituisce sempre il numero totale di mipmap nella visualizzazione per il conteggio mip, indipendentemente dalla chiappa. Tuttavia, se le dimensioni di un determinato miplevel sono richieste da resinfo e miplevel è stato disattivato (ad esempio, un'affreccia di 2,2 significa che mip 0 e 1 sono stati disattivati), le dimensioni restituite non sono definite. Alcune implementazioni restituiranno il comportamento fuori intervallo specificato per resinfo quando miplevel non è compreso nell'intervallo. Altre implementazioni restituiranno le dimensioni del mip come se non fosse stata ancorata.

### <a name="restrictions"></a>Restrizioni

-   *srcResource* deve essere un registro t o u che \# non è un \# buffer, ma è un oggetto \* Texture.
-   L'indirizzamento relativo *di srcResource* non è consentito.
-   *srcMipLevel* deve usare un selettore di componente singolo se non è un valore scalare immediato.
-   Il recupero da t o u a cui non è associato alcun valore restituisce 0 per \# \# width, height, depth o arraysize e total-mip-count. Il modificatore rcpFloat viene comunque rispettato in questo caso, quindi viene restituito \_ INF per i valori restituiti applicabili.
-   Se *srcMipLevel* non è compreso nell'intervallo del numero disponibile di miplevel nella risorsa, il comportamento per la dimensione restituita (*dest.xyz*) è identico a quello di una risorsa t o u non \# \# associata. Il conteggio mip totale viene comunque restituito in *dest.w* per questo caso.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





