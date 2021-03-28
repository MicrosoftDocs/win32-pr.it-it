---
title: esempio (SM4-ASM)
description: Campiona i dati dall'elemento/trama specificato utilizzando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato. | esempio (SM4-ASM)
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397aba4a165f13721e73f87da82cff3e8918e33b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969193"
---
# <a name="sample-sm4---asm"></a>esempio (SM4-ASM)

Campiona i dati dall'elemento/trama specificato utilizzando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato.



| aoffimmi di esempio \[ \_ (u, v, w) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler |
|--------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[nell' \] indirizzo del risultato dell'operazione.<br/>                                      |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] un set di coordinate di trama. Per ulteriori informazioni, vedere la sezione **osservazioni** .<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] un registro di trama. Per ulteriori informazioni, vedere la sezione **osservazioni** .<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[in \] un registro del campionatore. Per ulteriori informazioni, vedere la sezione **osservazioni** .<br/>           |



 

## <a name="remarks"></a>Commenti

I dati di origine possono provenire da qualsiasi tipo di risorsa, ad eccezione dei buffer.

*srcAddress* fornisce il set di coordinate di trama necessarie per eseguire l'esempio, come valori a virgola mobile che fanno riferimento allo spazio normalizzato nella trama. Le modalità di wrapping degli indirizzi (wrap, mirror, Clamp/Border e così via) vengono applicate per le coordinate di trama \[ al di fuori di 0... 1 \] intervallo, tratto dagli Stati del campionatore \# e applicate dopo l'applicazione di un offset di indirizzo alle coordinate di trama.

*srcResource* è un registro di trama (t \# ). Si tratta semplicemente di un segnaposto per una trama, incluso il tipo di dati restituito della risorsa da campionare. Tutte queste informazioni sono dichiarate nel preambolo dello shader. La risorsa effettiva da campionare è associata allo shader all'esterno dello slot \# (per t \# ).

*srcSampler* è uno o più registri del campionatore. Si tratta semplicemente di un segnaposto per una raccolta di controlli di filtro, ad esempio Point vs. Linear, mapping MIP e i controlli di wrapping degli indirizzi.

Il set di informazioni necessarie per l'hardware per eseguire il campionamento è suddiviso in due parti ortogonali. In primo luogo, il registro di trama fornisce informazioni sul tipo di dati di origine, ad esempio informazioni sulla presenza o meno di dati SRGB nella trama. Fa anche riferimento alla memoria effettivamente campionata. In secondo luogo, il registro campionatore definisce la modalità di filtro da applicare.

### <a name="array-resources"></a>Risorse di matrice

Per le matrici Texture1D, il componente g *srcAddress* (POS-swizzle) seleziona la sezione della matrice da cui recuperare. Questo viene sempre considerato come un valore float scalato, invece dello spazio normalizzato per le coordinate di trama standard e viene applicato un arrotondamento al valore più vicino, seguito da un morsetto all'intervallo di BufferArray disponibile.

Per le matrici Texture2D, il componente *srcAddress* b (POS-swizzle) seleziona la sezione della matrice da cui eseguire il recupero; in caso contrario, usando la stessa semantica descritta per le matrici Texture1D.

### <a name="address-offset"></a>Offset indirizzo

Il \[ \_ suffisso aoffimmi (u, v, w) facoltativo \] (offset indirizzo per intero immediato) indica che le coordinate di trama per l'esempio devono essere sottoposte a offset in base a un set di valori costanti integer dello spazio Texel immediatamente specificato. I valori letterali sono un set di numeri di complemento a 4 bit, con intervallo di valori integer \[ -8, 7 \] . Questo modificatore viene definito per tutte le risorse, incluse le matrici Texture1D/2D e Texture3D, ma non è definito per TextureCube.

L'hardware può trarre vantaggio dalla conoscenza immediata che un attraversamento di un footprint di Texel su una posizione comune viene eseguito da un set di istruzioni di esempio. Questo può essere trasmesso usando \_ aoffimmi (u, v, w).

Gli offset vengono aggiunti alle coordinate di trama, nello spazio Texel, rispetto a ogni miplevel a cui si accede. Quindi, anche se le coordinate di trama vengono fornite come valori float normalizzati, l'offset applica un offset integer dello spazio Texel.

Gli offset degli indirizzi non vengono applicati lungo l'asse delle matrici di matrici Texture1D/2D.

\_i componenti aoffimmi v, w vengono ignorati per Texture1Ds.

\_il componente aoffimmi w viene ignorato per Texture2Ds.

Le modalità di wrapping degli indirizzi (wrap, mirror, Clamp/Border e così via) dagli Stati del campionatore \# vengono applicate dopo che è stato applicato un offset di indirizzo alle coordinate di trama.

### <a name="return-type-control"></a>Controllo tipo restituito

Il formato di dati restituito dall'esempio al registro di destinazione è determinato dal formato di risorsa ( \_ formato DXGI \* ) associato al parametro *srcResource* (t \# ). Se, ad esempio, l'oggetto t specificato \# è stato associato a una risorsa nel formato DXGI \_ Format \_ A8B8G8R8 \_ UNORM \_ sRGB, l'operazione di campionamento convertirà texel campionati da gamma 2,0 a 1,0, applica filtro e il risultato verrà scritto nel registro di destinazione come valori a virgola mobile nell'intervallo \[ 0.. 1 \] .

I valori restituiti sono 4 vettori (con impostazioni predefinite specifiche del formato per i componenti non presenti nel formato). Swizzle in *srcResource* determina come swizzle il risultato a 4 componenti restituito dall'esempio di trama/filtro, dopo il quale. mask on *dest* determina i componenti in *dest* che vengono aggiornati.

Quando l' **esempio** legge un valore float a 32 bit in un registro a 32 bit, con il campionamento dei punti (nessun filtro), è possibile che non vengano scaricati i valori denormalizzati, ma in caso contrario i numeri non vengono modificati. Se l'incertezza con i valori denormalizzati del campionamento dei punti è un problema per un'applicazione, usare l'istruzione [LD](ld--sm4---asm-.md) , che garantisce che i valori float a 32 bit siano letti senza modifiche.

### <a name="lod-calculation"></a>Calcolo LOD

Per informazioni dettagliate su come vengono calcolati i derivati nel processo di determinazione di LOD per il filtro, vedere [derivare \_ RTX](deriv-rtx--sm4---asm-.md) e [derivare \_ valore](deriv-rty--sm4---asm-.md). L'istruzione di **esempio** calcola in modo implicito i derivati sulle coordinate di trama utilizzando la stessa definizione utilizzata dalle istruzioni di **derivazione** dello shader. Questa operazione non si applica alle istruzioni [Sample \_ l](sample-l--sm4---asm-.md) o [ \_ d Sample](sample-d--sm4---asm-.md) . Per queste istruzioni, i LOD o i derivati vengono forniti direttamente dall'applicazione.

Per l'istruzione di **esempio** , le implementazioni possono scegliere di condividere lo stesso calcolo di LOD in tutti i 4 pixel in un timbro 2x2 (ma non in un'area più grande) o di eseguire calcoli LOD per pixel.

### <a name="miscellaneous-details"></a>Dettagli vari

Per il buffer & Texture1D, i componenti *srcAddress* . GBA (POS-swizzle) vengono ignorati. Per le matrici Texture1D, i componenti *srcAddress* . BA (POS-swizzle) vengono ignorati. Per Texture2Ds, *srcAddress* . un componente (POS-swizzle) viene ignorato.

Il recupero da uno slot di input a cui non è associato alcun elemento restituisce 0 per tutti i componenti.

### <a name="restrictions"></a>Restrizioni

-   *srcResource* deve essere un \# Registro t. *srcResource* non può essere un ConstantBuffer, che non può essere associato a \# registri t.
-   *srcSampler* deve essere un \# registro s.
-   L'indirizzamento relativo in *srcResource* o *srcSampler* non è consentito.
-   *srcAddress* deve essere un registro temp (r \# /X \# ), constantBuffer (CB \# ), input (v \# ) o un valore immediato.
-   il valore di *dest* deve essere un registro temp (r \# /x \# ) o output (o \* \# ).
-   \_aoffimmi (u, v, w) non è consentito per TextureCubes.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





