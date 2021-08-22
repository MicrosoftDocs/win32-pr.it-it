---
title: ld2dms (sm4.1 - asm)
description: Legge singoli esempi da trame multidimensionali bidimensionali.
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17d00b3d6cdc3640f0b8d5266bd6dc8fd6dafefaf10cf47b500011cfe952d4ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043789"
---
# <a name="ld2dms-sm41---asm"></a>ld2dms (sm4.1 - asm)

Legge singoli esempi da trame multidimensionali bidimensionali.



| ld2dms \[ \_ aoffimmi(u,v) \] dest \[ \] .mask, srcAddress \[ .swizzle, \] srcResource \[ .swizzle, \] sampleIndex (operando scalare) |
|------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Indirizzo del risultato dell'operazione. <br/>                                                                 |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] Le coordinate della trama necessarie per eseguire l'esempio.<br/>                                                    |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] Un registro trame (t ) che deve essere stato dichiarato identificando la trama o \# il buffer da recuperare<br/> |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[in \] Idendifica gli esempi da leggere da *srcResource*.<br/>                                                       |



 

## <a name="remarks"></a>Commenti

Questa istruzione è un'alternativa semplificata [all'istruzione di](sample--sm4---asm-.md) esempio. Recupera i dati dall'oggetto Texture specificato senza filtri (ad esempio campionamento di punti) usando i valori integer *srcAddress* e *sampleIndex specificati.*

*srcAddress* fornisce il set di coordinate di trama necessarie per eseguire l'esempio sotto forma di interi senza segno. Se *srcAddress* non è compreso nell'intervallo \[ 0...( \# texels nella dimensione -1) , ld2dms restituisce sempre 0 in tutti i componenti presenti nel formato della risorsa e il valore predefinito \] (0,0,0,1.0f/0x00000001) per i componenti mancanti. 

*sampleIndex* non deve essere un valore letterale. Il numero di più campioni non deve essere specificato nella risorsa trama e funziona con le visualizzazioni di profondità o di stencil.

Un'applicazione che desidera un controllo più flessibile sul comportamento  degli indirizzi non compreso nell'intervallo deve invece usare l'istruzione di esempio, in quanto rispetta il comportamento di wrapping/mirror/clamp/border definito come stato del campionatore.

*srcAddress.b* (post-swizzle) viene ignorato per Texture2Ds. Se il valore non è compreso nell'intervallo di indici di matrice disponibili \[ 0...( array size-1) , quindi ld2dms restituisce sempre 0 in tutti i componenti presenti nel formato della risorsa e il valore predefinito \] (0,0,0,1.0f/0x00000001) per i componenti mancanti. 

Per le matrici Texture2D, *srcAddress.b* (post-swizzle) fornisce l'indice della matrice. In senso antiorario ha lo stesso comportamento di Texture2D.

*srcAddress.a* (post-swizzle) viene sempre ignorato. Il compilatore HLSL non restituisce mai alcun risultato.

*srcResource* è un registro trame (t ) che deve essere stato \# dichiarato(22.3.11), identificando la trama da cui recuperare.

Il recupero da t \# a cui non è associato alcun elemento restituisce 0 per tutti i componenti.

### <a name="address-offset"></a>Offset dell'indirizzo

Il suffisso \[ \_ facoltativo aoffimmi(u,v,w) (offset dell'indirizzo per intero immediato) indica che le coordinate di trama per \] **gli ld2dms** devono essere offset da un set di valori costanti interi dello spazio texel immediato forniti. I valori letterali sono un set di numeri di complemento a 4 bit 2, con intervallo intero \[ -8,7. \]

Gli offset vengono aggiunti alle coordinate della trama, nello spazio texel.

Gli offset degli indirizzi non vengono applicati lungo l'asse delle matrici Texture1D/2D.

I *\_ componenti aoffimmi v,w* vengono ignorati per Texture1Ds.

Il *\_ componente aoffimmi w* viene ignorato per Texture2Ds.

Poiché le coordinate della trama per **ld2dms** sono interi senza segno, se l'offset fa sì che l'indirizzo sia inferiore a zero, verrà restituito un indirizzo di grandi dimensioni e verrà restituito un accesso non compreso nell'intervallo, che come **ld** restituisce 0 in tutti i componenti presenti nel formato della risorsa e le impostazioni predefinite (0,0,0,1,0f/0x00000001) per i componenti mancanti.

### <a name="sample-number"></a>Numero di esempio

**ld2dms** è disponibile per l'uso in qualsiasi risorsa. **ld2dms** funziona in modo identico a **ld,** ad eccezione delle risorse multsample 2D, usando l'operando *sampleIndex* aggiuntivo (basato su 0) per identificare l'esempio da leggere dalla risorsa.

Il risultato della specifica di *un oggetto sampleIndex* che supera il numero di campioni nella risorsa non è definito, ma non può restituire dati all'esterno dello spazio di indirizzi del contesto di dispositivo.

### <a name="return-type-control"></a>Controllo del tipo restituito

Il formato dei dati restituito **da ld2dms** al registro di destinazione è determinato nello stesso modo descritto per l'istruzione **di** esempio. Si basa sul formato associato al *parametro srcResource* (t \# ).

Come per l'istruzione **di** esempio, i valori restituiti per **ld2dms** sono a 4 vettori con valori predefiniti specifici del formato per i componenti non presenti nel formato. Lo swizzle in *srcResource* determina come scorrere il risultato a 4 componenti che torna dal carico della trama, dopo il quale .mask su *dest* determina quali componenti in *dest* vengono aggiornati.

Quando un valore float a 32 bit viene letto da **ld2dms** in un registro a 32 bit, i bit non vengono toccati; in altri, i valori denormali rimangono denormali. Questa operazione è diversa **dall'istruzione di** esempio.

### <a name="miscellaneous-details"></a>Dettagli vari

Poiché a questa istruzione non sono associati filtri, concetti come la distorsione lod non si applicano. Di conseguenza non esiste alcun *parametro s del \# campionatore.*

### <a name="restrictions"></a>Restrizioni

-   *srcResource* deve essere un registro t \# e non un oggetto TextureCube, Texture1D o Texture1DArray. *srcResource* non può essere un ConstantBuffer, che non può essere associato a registri \# t.
-   L'indirizzamento relativo *in srcResource* non è consentito.
-   *srcAddress* e *sampleIndex* devono essere temp (r \# \# /x), constant (cb \# ) o input (v ) \# register.
-   *dest* deve essere un registro temporaneo (r /x ) o \# di output \# (o \* \# ).

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Shader Model 4 Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





