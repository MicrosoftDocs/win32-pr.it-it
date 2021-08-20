---
title: esempio (sm4 - asm)
description: Campionare i dati dall'elemento/trama specificato usando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato. | esempio (sm4 - asm)
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b6fabb75c819bb2a95fcf500799fd1e8153d6dabfe66d33ba04c518c949fa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671881"
---
# <a name="sample-sm4---asm"></a>esempio (sm4 - asm)

Campionare i dati dall'elemento/trama specificato usando l'indirizzo specificato e la modalità di filtro identificata dal campionatore specificato.



| sample \[ \_ aoffimmi(u,v,w) \] dest \[ \] .mask, srcAddress \[ .swizzle, \] srcResource \[ .swizzle, \] srcSampler |
|--------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Indirizzo del risultato dell'operazione.<br/>                                      |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] Un set di coordinate della trama. Per altre informazioni, vedere **la sezione** Osservazioni.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] Un registro trame. Per altre informazioni, vedere **la sezione** Osservazioni.<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[in \] Un registro sampler. Per altre informazioni, vedere **la sezione** Osservazioni.<br/>           |



 

## <a name="remarks"></a>Commenti

I dati di origine possono derivare da qualsiasi tipo di risorsa, diverso da Buffer.

*srcAddress* fornisce il set di coordinate di trama necessarie per eseguire l'esempio, in quanto i valori a virgola mobile che fanno riferimento allo spazio normalizzato nella trama. Le modalità di wrapping degli indirizzi (wrap/mirror/clamp/border e così via) vengono applicate per le coordinate di trama esterne all'intervallo 0...1, prese dallo stato (s) del campionatore e applicate dopo l'applicazione di qualsiasi offset di indirizzo alle coordinate della \[ \] \# trama.

*srcResource* è un registro trame (t \# ). Si tratta semplicemente di un segnaposto per una trama, incluso il tipo di dati restituito della risorsa campionata. Tutte queste informazioni vengono dichiarate nel preambolo shader. La risorsa effettiva da campionare è associata esternamente allo shader nello slot \# (per t \# ).

*srcSampler* è un registro sampler.s. Si tratta semplicemente di un segnaposto per una raccolta di controlli di filtro, ad esempio controlli punto/lineare, mipmapping e ritorno a capo degli indirizzi.

Il set di informazioni necessarie per l'hardware per eseguire il campionamento è suddiviso in due parti ortogonali. In primo luogo, il registro trame fornisce informazioni sul tipo di dati di origine, tra cui, ad esempio, informazioni sul fatto che la trama contenga dati SRGB. Fa anche riferimento alla memoria effettiva campionata. In secondo piano, il registro sampler definisce la modalità di filtro da applicare.

### <a name="array-resources"></a>Risorse della matrice

Per Matrici Texture1D, il *componente srcAddress* g (POS-swizzle) seleziona la sezione di matrice da cui recuperare. Questo valore viene sempre considerato come un valore float ridimensionato, anziché come spazio normalizzato per le coordinate di trama standard, e viene applicato un arrotondamento al valore più vicino, seguito da un fissamento all'intervallo BufferArray disponibile.

Per le matrici Texture2D, il componente *srcAddress* b (POS-swizzle) seleziona la sezione di matrice da cui recuperare, in caso contrario usando la stessa semantica descritta per Matrici Texture1D .

### <a name="address-offset"></a>Offset dell'indirizzo

Il suffisso \[ \_ facoltativo aoffimmi(u,v,w) (offset dell'indirizzo per intero immediato) indica che le coordinate della trama per l'esempio devono essere offset da un set di valori costanti dello spazio \] texel immediato forniti. I valori letterali sono un set di numeri di complemento a 4 bit 2, con intervallo intero \[ -8,7. \] Questo modificatore è definito per tutte le risorse, incluse le matrici Texture1D/2D e Texture3D, ma non è definito per TextureCube.

L'hardware può sfruttare la conoscenza immediata che un attraversamento su un footprint di texel su una posizione comune viene eseguito da un set di istruzioni di esempio. Questo può essere trasmesso usando \_ aoffimmi(u,v,w).

Gli offset vengono aggiunti alle coordinate della trama, nello spazio texel, rispetto a ogni miplevel a cui si accede. Pertanto, anche se le coordinate della trama vengono fornite come valori float normalizzati, l'offset applica un offset intero texel-space.

Gli offset degli indirizzi non vengono applicati lungo l'asse delle matrici Texture1D/2D.

\_I componenti aoffimmi v,w vengono ignorati per Texture1Ds.

\_Il componente aoffimmi w viene ignorato per Texture2Ds.

Le modalità di wrapping degli indirizzi (wrap/mirror/clamp/border e così via) dello stato del campionatore (s) vengono applicate dopo l'applicazione di qualsiasi offset di indirizzo \# alle coordinate della trama.

### <a name="return-type-control"></a>Controllo del tipo restituito

Il formato dei dati restituito dall'esempio al registro di destinazione è determinato dal formato di risorsa (DXGI FORMAT ) associato al \_ \* parametro *srcResource* (t \# ). Ad esempio, se l'oggetto t specificato è stato associato a una risorsa con formato \# DXGI \_ FORMAT A8B8G8R8 UNORM SRGB, l'operazione di campionamento converte i texel campionati da \_ \_ gamma \_ 2.0 a 1.0, applica il filtro e il risultato verrà scritto nel registro di destinazione come valori a virgola mobile nell'intervallo \[ 0..1 \] .

I valori restituiti sono a 4 vettori (con valori predefiniti specifici del formato per i componenti non presenti nel formato ). Lo swizzle in *srcResource* determina come scorrere il risultato a 4 componenti che torna dal campione/filtro della trama, dopo di che .mask su *dest* determina quali componenti in *dest* vengono aggiornati.

Quando **sample** legge un valore float a 32 bit in un registro a 32 bit, con campionamento in punti (nessun filtro), può o meno scaricare valori denormali, ma in caso contrario i numeri non vengono modificati. Se l'incertezza con i valori denormali di campionamento dei punti è un problema per un'applicazione, usare l'istruzione [ld,](ld--sm4---asm-.md) che garantisce che i valori float a 32 bit siano letti senza modifiche.

### <a name="lod-calculation"></a>Calcolo LOD

Per informazioni dettagliate sul modo in cui vengono calcolati i derivati nel processo di determinazione del lod per il filtro, vedere [deriv \_ rtx](deriv-rtx--sm4---asm-.md) e [deriv \_ rty.](deriv-rty--sm4---asm-.md) **L'istruzione** di esempio calcola in modo implicito i derivati sulle coordinate della trama usando la stessa definizione utilizzata nelle istruzioni **deriv** Shader. Questo non si applica alle [istruzioni \_ l o](sample-l--sm4---asm-.md) d [ \_ di](sample-d--sm4---asm-.md) esempio. Per queste istruzioni, loD o derivati vengono forniti direttamente dall'applicazione.

Per  l'istruzione di esempio, le implementazioni possono scegliere di condividere lo stesso calcolo LOD in tutti i 4 pixel in un stamp 2x2 (ma non in un'area più grande) o di eseguire calcoli LOD per pixel.

### <a name="miscellaneous-details"></a>Dettagli vari

Per i & Texture1D, i *componenti srcAddress* .gba (POS-swizzle) vengono ignorati. Per le matrici Texture1D, i *componenti srcAddress* .ba (POS-swizzle) vengono ignorati. Per Texture2Ds, *il componente srcAddress* .a (POS-swizzle) viene ignorato.

Il recupero da uno slot di input a cui non è associato alcun elemento restituisce 0 per tutti i componenti.

### <a name="restrictions"></a>Restrizioni

-   *srcResource* deve essere un registro \# t. *srcResource* non può essere un ConstantBuffer, che non può essere associato a registri \# t.
-   *srcSampler* deve essere un registro \# s.
-   L'indirizzamento relativo *in srcResource* o *srcSampler* non è consentito.
-   *srcAddress* deve essere un registro temporaneo (r \# \# /x), constantBuffer (cb), \# input (v ) o valori \# immediati.
-   *dest* deve essere un registro temporaneo (r /x ) o \# di output \# (o \* \# ).
-   \_aoffimmi(u,v,w) non è consentito per TextureCubes.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Shader Model 4 Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





