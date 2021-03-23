---
title: Firme radice di esempio
description: Nella sezione seguente vengono illustrate le firme radice che variano in complessità da vuote a completamente complete.
ms.assetid: 493D35C9-2A90-4688-BD7E-74B9EB2B4E72
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d09d355cc1c96d77670c5536400f0b3f93c097
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103407"
---
# <a name="example-root-signatures"></a>Firme radice di esempio

Nella sezione seguente vengono illustrate le firme radice che variano in complessità da vuote a completamente complete.

-   [Firma radice vuota](#an-empty-root-signature)
-   [Una costante](#one-constant)
-   [Aggiunta di un Constant Buffer View radice](#adding-a-root-constant-buffer-view)
-   [Binding di tabelle descrittori](#binding-descriptor-tables)
-   [Firma radice più complessa](#a-more-complex-root-signature)
-   [Streaming di visualizzazioni delle risorse dello shader](#streaming-shader-resource-views)
-   [Argomenti correlati](#related-topics)

## <a name="an-empty-root-signature"></a>Firma radice vuota

![una firma radice vuota non contiene associazioni](images/root-tables-0.png)

È improbabile che una firma radice vuota sia utile, ma può essere usata in un passaggio di rendering semplice con l'uso solo dell'assembler di input e di vertex shader e pixel shader minimi che non accedono a nessun descrittore. Sono disponibili anche la fase di Blend, la destinazione di rendering e le fasi di stencil Depth, anche con una firma radice vuota.

## <a name="one-constant"></a>Una costante

![una singola costante radice](images/root-tables-constant.png)

Lo slot di associazione API è il punto in cui l'argomento radice per questo parametro verrà associato in fase di record dell'elenco dei comandi. Il numero degli slot di associazione API è implicito, in base all'ordine dei parametri nella firma radice (il primo è sempre zero). Lo slot di binding HLSL è il punto in cui verrà visualizzato il parametro radice. Il tipo ("uint" nell'esempio precedente) non è noto all'hardware ma è semplicemente un commento nell'immagine, l'hardware visualizzerà semplicemente il valore DWORD singolo come contenuto.

Per associare una costante in fase di record dell'elenco di comandi, viene usato un comando simile al seguente:

``` syntax
pCmdList->SetComputeRoot32BitConstant(0,seed); // 0 is the parameter index, seed is used by the shaders
```

## <a name="adding-a-root-constant-buffer-view"></a>Aggiunta di un Constant Buffer View radice

![aggiunge una visualizzazione del buffer costante alla firma radice](images/root-tables-cbv.png)

Questo esempio mostra due costanti radice e un Constant Buffer View radice (CBV) che costa due slot DWORD.

Per associare una visualizzazione del buffer costante, usare un comando simile al seguente. Si noti che il primo parametro (2) è lo slot visualizzato nell'immagine. In genere, una matrice di costanti verrà configurata e resa disponibile per gli shader a B0 come CBV.

``` syntax
pCmdList->SetGraphicsRootConstantBufferView(2,GPUVAForCurrDynamicConstants);
```

## <a name="binding-descriptor-tables"></a>Binding di tabelle descrittori

![aggiunge le tabelle dei descrittori alla firma radice](images/root-tables-2.png)

In questo esempio viene illustrato l'utilizzo di due tabelle dei descrittori. uno che dichiara una tabella di cinque descrittori che saranno disponibili in fase di esecuzione in un \_ heap del \_ descrittore CBV SRV UAV e un altro che dichiara una tabella di due descrittori che verranno visualizzati in fase di esecuzione in un heap descrittore del campionatore.

Per associare le tabelle dei descrittori durante la registrazione di un elenco di comandi.

``` syntax
pCmdList->SetComputeRootDescriptorTable(1, handleToCurrentMaterialDataInHeap);
pCmdList->SetComputeRootDescriptorTable(2, handleToCurrentMaterialDataInSamplerHeap);
```

Un'altra funzionalità della firma radice è la costante radice float4 che rappresenta quattro DWORD di dimensioni. Il comando che segue associa solo i due DWORD centrali dei quattro.

``` syntax
pCmdList->SetComputeRoot32BitConstants(0,2,myFloat2Array,1);  // 2 constants starting at offset 1 (middle 2 values in float4)
```

## <a name="a-more-complex-root-signature"></a>Firma radice più complessa

![firma radice complessa con molti elementi](images/root-tables-3.png)

Questo esempio mostra una firma radice densa con la maggior parte dei tipi di voci. Due delle tabelle dei descrittori (negli slot 3 e 6) includono matrici di dimensioni non vincolate. Il fardello è che l'applicazione deve solo toccare descrittori validi in un heap. Per le matrici non vincolate o di dimensioni molto grandi, è necessario il livello hardware 2 + del supporto per l'associazione di risorse.

Sono disponibili due Samplers statici (associati senza richiedere slot di firma radice).

A slot 9, UAV U4 e UAV U5 vengono dichiarati con lo stesso offset della tabella descrittore. Questo è l'uso di un descrittore con alias, un descrittore in memoria verrà visualizzato sia come U4 che come U5 negli shader HLSL. In questo caso lo shader deve essere compilato con l'opzione di \_ alias risorse dello shader D3D10 \_ \_ \_ o l' `/res_may_alias` opzione o in fxc. I descrittori con alias consentono di associare un descrittore a più punti di binding, senza dover apportare alcuna modifica agli shader.

## <a name="streaming-shader-resource-views"></a>Streaming di visualizzazioni delle risorse dello shader

![flusso di viste delle risorse dello shader in questa firma radice](images/root-tables-4.png)

Questa firma radice illustra uno scenario in cui tutti SRVs vengono trasmessi in e da una matrice di grandi dimensioni. In fase di esecuzione è possibile impostare una tabella dei descrittori una volta quando la firma radice è impostata. Quindi, tutte le letture di trama vengono eseguite indicizzando la matrice tramite costanti alimentate tramite i primi argomenti radice. È necessario solo un singolo heap del descrittore e viene aggiornato solo quando le trame vengono trasmesse in o da slot descrittore gratuiti.

Gli offset del descrittore nell'heap di grandi dimensioni sono identificati da shader che usano le costanti nelle visualizzazioni del buffer costante. Se, ad esempio, a uno shader viene assegnato un ID materiale, può indicizzare in una matrice di grandi dimensioni usando la costante per accedere al descrittore richiesto, che fa riferimento alla trama richiesta.

Questo scenario richiede hardware con associazione di risorse livello 2 +.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Livelli hardware di associazione di risorse](hardware-support.md)
</dt> <dt>

[Associazione di risorse in HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Firme radice](root-signatures.md)
</dt> </dl>

 

 




