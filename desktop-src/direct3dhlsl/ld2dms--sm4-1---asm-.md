---
title: ld2dms (SM 4.1-ASM)
description: Legge singoli campioni da trame multicampionate bidimensionali.
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9dd03b7c07f3fb25294dd0ad6aa382eb203560
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117205"
---
# <a name="ld2dms-sm41---asm"></a>ld2dms (SM 4.1-ASM)

Legge singoli campioni da trame multicampionate bidimensionali.



| ld2dms \[ \_ aoffimmi (u, v) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , sampleIndex (operando scalare) |
|------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[nell' \] indirizzo del risultato dell'operazione. <br/>                                                                 |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[nelle \] coordinate di trama necessarie per eseguire l'esempio.<br/>                                                    |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] un registro di trama (t \# ) che deve essere stato dichiarato che identifica la trama o il buffer da cui recuperare<br/> |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[in \] Idendifies gli esempi per leggere da *srcResource*.<br/>                                                       |



 

## <a name="remarks"></a>Commenti

Questa istruzione è un'alternativa semplificata all'istruzione di [esempio](sample--sm4---asm-.md) . Recupera i dati dalla trama specificata senza filtrare, ad esempio il campionamento dei punti, usando il valore integer *srcAddress* e *sampleIndex* fornito.

*srcAddress* fornisce il set di coordinate di trama necessarie per eseguire l'esempio sotto forma di interi senza segno. Se *srcAddress* non è compreso nell'intervallo \[ 0... ( \# Texels in Dimension-1) \] , **ld2dms** restituisce sempre 0 in tutti i componenti presenti nel formato della risorsa e i valori predefiniti (0, 0, 0, 1.0 f/0x00000001) per i componenti mancanti.

*sampleIndex* non deve essere un valore letterale. Il conteggio multisample non deve essere specificato nella risorsa di trama e funziona con le visualizzazioni depth o stencil.

Un'applicazione che desidera un controllo più flessibile sul comportamento degli indirizzi non compresi nell'intervallo deve invece utilizzare l'istruzione di **esempio** , in quanto rispetta il comportamento di ritorno a capo/mirroring/morsetto/bordo definito come stato del campionatore.

*srcAddress. b* (post-swizzle) viene ignorato per Texture2Ds. Se il valore non è compreso nell'intervallo degli indici di matrice disponibili \[ 0... ( dimensione della matrice-1) \] , quindi **ld2dms** restituisce sempre 0 in tutti i componenti presenti nel formato della risorsa e i valori predefiniti (0, 0, 0, 1.0 f/0x00000001) per i componenti mancanti.

Per le matrici Texture2D, *srcAddress. b* (post-swizzle) fornisce l'indice della matrice. Oherwise ha lo stesso comportamento di Texture2D.

*srcAddress. a* (post-swizzle) viene sempre ignorato. Il compilatore HLSL non restituirà mai alcun elemento.

*srcResource* è un registro di trama (t \# ) che deve essere stato dichiarato (22.3.11), identificando la trama da cui recuperare.

Il recupero da t \# a cui non è associato alcun elemento restituisce 0 per tutti i componenti.

### <a name="address-offset"></a>Offset indirizzo

Il \[ \_ suffisso aoffimmi (u, v, w) facoltativo \] (offset indirizzo per intero immediato) indica che le coordinate di trama per il **ld2dms** devono essere sottoposte a offset in base a un set di valori costanti integer dello spazio Texel immediatamente specificato. I valori letterali sono un set di numeri di complemento a 4 bit, con intervallo di valori integer \[ -8, 7 \] .

Gli offset vengono aggiunti alle coordinate di trama, nello spazio Texel.

Gli offset degli indirizzi non vengono applicati lungo l'asse delle matrici di matrici Texture1D/2D.

I componenti *\_ aoffimmi v, w* vengono ignorati per Texture1Ds.

Il componente *\_ aoffimmi w* viene ignorato per Texture2Ds.

Poiché le coordinate di trama per **ld2dms** sono interi senza segno, se l'offset fa sì che l'indirizzo vada al di sotto di zero, verrà eseguito il wrapping a un indirizzo di grandi dimensioni e il risultato sarà un accesso fuori limite, che come **LD** restituisce 0 in tutti i componenti presenti nel formato della risorsa e i valori predefiniti (0, 0, 0, 1.0 f/0x00000001) per i componenti

### <a name="sample-number"></a>Numero di esempio

**ld2dms** è disponibile per l'uso in qualsiasi risorsa. **ld2dms** funziona in modo identico a **LD** tranne che nelle risorse multsample 2D, usando l'operando *sampleIndex* aggiuntivo (basato su 0) per identificare l'esempio da leggere dalla risorsa.

Il risultato della specifica di un *sampleIndex* che supera il numero di campioni nella risorsa non è definito, ma non può restituire dati all'esterno dello spazio degli indirizzi del contesto di dispositivo.

### <a name="return-type-control"></a>Controllo tipo restituito

Il formato dei dati restituito da **ld2dms** al registro di destinazione viene determinato in modo analogo a quanto descritto per l'istruzione di **esempio** . Si basa sul formato associato al parametro *srcResource* (t \# ).

Come per l'istruzione di **esempio** , i valori restituiti per **ld2dms** sono 4 vettori con impostazioni predefinite specifiche del formato per i componenti non presenti nel formato. Il swizzle in *srcResource* determina come swizzle il risultato a 4 componenti restituito dal caricamento della trama, dopo il quale. mask su *dest* determina quali componenti in *dest* vengono aggiornati.

Quando un valore float a 32 bit viene letto da **ld2dms** in un registro a 32 bit, i bit non vengono modificati; ovvero i valori denormali rimangono denormalizzati. Questo è diverso dall'istruzione di **esempio** .

### <a name="miscellaneous-details"></a>Dettagli vari

Poiché non esiste alcun filtro associato a questa istruzione, concetti come la distorsione del LOD non si applicano. Di conseguenza non è presente alcun parametro del *campionatore \#* .

### <a name="restrictions"></a>Restrizioni

-   *srcResource* deve essere un \# Registro t e non TextureCube, Texture1D o Texture1DArray. *srcResource* non può essere un ConstantBuffer, che non può essere associato a \# registri t.
-   L'indirizzamento relativo in *srcResource* non è consentito.
-   *srcAddress* e *sampleIndex* devono essere un registro temp (r \# /x \# ), Constant (CB \# ) o input (v \# ).
-   il valore di *dest* deve essere un registro temp (r \# /x \# ) o output (o \* \# ).

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
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





