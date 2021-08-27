---
title: Firme radice di esempio
description: La sezione seguente illustra le firme radice che variano in complessità da vuota a completa.
ms.assetid: 493D35C9-2A90-4688-BD7E-74B9EB2B4E72
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2332a6efb36b309c5dc74a8578a0be9d2f46298375c309872cae8718d5bc5950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118529412"
---
# <a name="example-root-signatures"></a>Firme radice di esempio

La sezione seguente illustra le firme radice che variano in complessità da vuota a completa.

-   [Firma radice vuota](#an-empty-root-signature)
-   [Una costante](#one-constant)
-   [Aggiunta di una radice Constant Buffer View](#adding-a-root-constant-buffer-view)
-   [Tabelle dei descrittori di associazione](#binding-descriptor-tables)
-   [Firma radice più complessa](#a-more-complex-root-signature)
-   [Visualizzazioni delle risorse shader di streaming](#streaming-shader-resource-views)
-   [Argomenti correlati](#related-topics)

## <a name="an-empty-root-signature"></a>Firma radice vuota

![una firma radice vuota non ha associazioni](images/root-tables-0.png)

È improbabile che una firma radice vuota sia utile, ma potrebbe essere usata in un semplice passaggio di rendering con l'uso solo dell'assembler di input e dei vertici e pixel shader minimi che non accedono ad alcun descrittore. Sono disponibili anche le fasi blend, target di rendering e depth-stencil, anche con una firma radice vuota.

## <a name="one-constant"></a>Una costante

![una singola costante radice](images/root-tables-constant.png)

Lo slot di associazione API è il punto in cui l'argomento radice per questo parametro verrà associato al momento del record dell'elenco comandi. Il numero di slot di associazione API è implicito, in base all'ordine dei parametri nella firma radice (il primo è sempre zero). Lo slot di binding HLSL è il punto in cui lo shader visualizza il parametro radice. Il tipo ("uint" nell'esempio precedente) non è noto all'hardware, ma è solo un commento nell'immagine. L'hardware visualizza semplicemente il singolo valore DWORD come contenuto.

Per associare una costante in fase di record command-list, viene usato un comando simile al seguente:

``` syntax
pCmdList->SetComputeRoot32BitConstant(0,seed); // 0 is the parameter index, seed is used by the shaders
```

## <a name="adding-a-root-constant-buffer-view"></a>Aggiunta di una radice Constant Buffer View

![aggiunge una visualizzazione del buffer costante alla firma radice](images/root-tables-cbv.png)

Questo esempio illustra due costanti radice e un Constant Buffer View radice (CBV) che costa due slot DWORD.

Per associare una visualizzazione del buffer costante, usare un comando come il seguente. Si noti che il primo parametro (2) è lo slot visualizzato nell'immagine. In genere una matrice di costanti viene impostata e quindi resa disponibile per gli shader in b0 come CBV.

``` syntax
pCmdList->SetGraphicsRootConstantBufferView(2,GPUVAForCurrDynamicConstants);
```

## <a name="binding-descriptor-tables"></a>Tabelle dei descrittori di associazione

![aggiunge tabelle descrittore alla firma radice](images/root-tables-2.png)

Questo esempio illustra l'uso di due tabelle descrittori. una che dichiara una tabella di cinque descrittori che saranno disponibili in fase di esecuzione in un heap dei descrittori UAV CBV SRV e l'altra dichiara una tabella di due descrittori che verranno visualizzati in fase di esecuzione in un heap descrittore del \_ \_ campionatore.

Per associare le tabelle dei descrittori durante la registrazione di un elenco di comandi.

``` syntax
pCmdList->SetComputeRootDescriptorTable(1, handleToCurrentMaterialDataInHeap);
pCmdList->SetComputeRootDescriptorTable(2, handleToCurrentMaterialDataInSamplerHeap);
```

Un'altra funzionalità della firma radice è la costante radice float4 con quattro DWORD di dimensioni. Il comando seguente associa solo le due DWORD intermedie delle quattro.

``` syntax
pCmdList->SetComputeRoot32BitConstants(0,2,myFloat2Array,1);  // 2 constants starting at offset 1 (middle 2 values in float4)
```

## <a name="a-more-complex-root-signature"></a>Firma radice più complessa

![una firma radice complessa con molti elementi](images/root-tables-3.png)

Questo esempio mostra una firma radice densa con la maggior parte dei tipi di voci. Due delle tabelle dei descrittori (in corrispondenza degli slot 3 e 6) includono matrici di dimensioni non associati. In questo caso, l'applicazione deve toccare solo i descrittori validi in un heap. Gli array non associati o molto grandi richiedono il livello hardware 2+ del supporto dell'associazione di risorse.

Sono disponibili due campionatori statici (associati senza richiedere slot di firma radice).

Nello slot 9, UAV u4 e UAV u5 vengono dichiarati allo stesso offset della tabella del descrittore. Questo è l'uso di un descrittore con alias, un descrittore in memoria verrà visualizzato come u4 e u5 negli shader HLSL. In questo caso lo shader deve essere compilato con l'opzione ALIAS MAY DELLE RISORSE SHADER D3D10 o \_ \_ con \_ \_ l'opzione o `/res_may_alias` in FXC. I descrittori con alias consentono di associare un descrittore a più punti di associazione, senza dover apportare modifiche agli shader.

## <a name="streaming-shader-resource-views"></a>Visualizzazioni delle risorse shader di streaming

![visualizzazioni delle risorse shader di streaming in questa firma radice](images/root-tables-4.png)

Questa firma radice illustra uno scenario in cui tutti gli SRV vengono trasmessi da e in un array di grandi dimensioni. In fase di esecuzione, una tabella del descrittore può essere impostata una sola volta quando viene impostata la firma radice. Tutte le operazioni di lettura della trama vengono quindi eseguite tramite l'indicizzazione nella matrice tramite costanti immesse tramite i primi argomenti radice. È necessario un solo heap del descrittore e viene aggiornato solo quando le trame vengono trasmesse in ingresso o in uscita da slot di descrittori liberi.

Gli offset del descrittore nell'heap di grandi dimensioni vengono identificati dagli shader usando le costanti nelle viste constant buffer. Ad esempio, se a uno shader viene assegnato un ID materiale, può indicizzare in un'unica matrice di grandi dimensioni usando la costante per accedere al descrittore richiesto (che fa riferimento alla trama richiesta).

Questo scenario richiede hardware con binding di risorse tier2+.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Livelli hardware di associazione delle risorse](hardware-support.md)
</dt> <dt>

[Associazione di risorse in HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Firme radice](root-signatures.md)
</dt> </dl>

 

 




