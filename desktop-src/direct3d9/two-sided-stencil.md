---
description: I volumi shadow vengono utilizzati per disegnare le ombre con il buffer dello stencil.
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: Stencil Two-Sided (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b238c4b778b9894029764032e76b60c476a891a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304361"
---
# <a name="two-sided-stencil-direct3d-9"></a>Stencil Two-Sided (Direct3D 9)

I volumi shadow vengono utilizzati per disegnare le ombre con il buffer dello stencil. Tramite l'applicazione vengono calcolati i volumi shadow di cui viene eseguito il cast dalla geometria occlusione, calcolando i bordi della siluetta e estrattando i bordi dalla luce in un set di volumi 3D. Questi volumi vengono quindi sottoposti a rendering due volte nel buffer dello stencil.

Il primo rendering disegna i poligoni rivolte verso il futuro e incrementa i valori del buffer dello stencil. Il secondo oggetto render disegna i poligoni sul retro del volume shadow e decrementa i valori del buffer dello stencil. In genere, tutti i valori incrementati e decrementati vengono annullati. Tuttavia, la scena è già stata sottoposta a rendering con la geometria normale causando la mancata riuscita del test del buffer z durante il rendering del volume shadow. I valori rimanenti nel buffer dello stencil corrispondono ai pixel presenti nell'ombreggiatura. Questi rimanenti contenuti del buffer dello stencil vengono usati come maschera, per alfa-blend di un quadrato nero di grandi dimensioni, che include tutto il doppio nella scena. Con il buffer dello stencil che funge da maschera, il risultato è quello di scurire i pixel presenti nelle ombreggiature.

Ciò significa che la geometria dell'ombreggiatura viene disegnata due volte per ogni sorgente di luce, di conseguenza la pressione sulla velocità effettiva del vertice della GPU. La funzionalità stencil a due lati è stata progettata per attenuare questa situazione. In questo approccio sono disponibili due set di stato dello stencil, denominati di seguito, uno per i triangoli in primo piano e l'altro per i triangoli rivolti verso il retro. In questo modo viene disegnato un solo passaggio per ogni volume ombreggiato, per luce.

Le modifiche all'API sono limitate a un nuovo set di Stati di rendering. Il nuovo stato di rendering \_ D3DRS \_ \_ StencilMODE a due lati può essere impostato su **true** o **false**. È **false** per impostazione predefinita, ovvero il comportamento corrente (DirectX 8). Quando questa impostazione è impostata su **true** (funzionerà solo se \_ è impostato D3DSTENCILCAPS TWOSIDED), gli Stati di rendering seguenti si applicano solo ai triangoli anteriori (in senso orario).



| Stato di rendering        | Descrizione                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| \_STENCILFAIL D3DRS  | D3DSTENCILOP da eseguire se il test dello stencil non riesce.                                                |
| \_STENCILZFAIL D3DRS | D3DSTENCILOP da eseguire se il test di stencil supera e il test z ha esito negativo.                              |
| \_STENCILPASS D3DRS  | D3DSTENCILOP da eseguire se vengono superati sia lo stencil che i test z.                                     |
| \_STENCILFUNC D3DRS  | D3DCMPFUNC FN. Il test di stencil viene superato se ((Ref & mask) stencilfn (stencil & mask)) è true. |



 

Un nuovo set di Stati di rendering si applica ai triangoli rivolti al back-end (in senso antiorario).



| Stato di rendering             | Descrizione                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| D3DRS \_ CCW \_ STENCILFAIL  | D3DSTENCILOP da eseguire se il test dello stencil non riesce.                                                      |
| D3DRS \_ CCW \_ STENCILZFAIL | D3DSTENCILOP da eseguire se il test di stencil supera e il test z ha esito negativo.                                    |
| D3DRS \_ CCW \_ STENCILPASS  | D3DSTENCILOP da eseguire se vengono superati sia lo stencil che i test z.                                           |
| D3DRS \_ CCW \_ STENCILFUNC  | Funzione D3DCMPFUNC. Il test di stencil viene superato se ((Ref & mask) stencilfn (stencil & mask)) è true. |



 

Gli Stati di rendering degli stencil rimanenti si applicano sempre ai triangoli in senso orario e in senso antiorario.

\_Il D3DRS \_ a due lati \_ StencilMODE viene ignorato per gli sprite di linee e punti, il che significa che il comportamento è invariato da DirectX 8. Gli \_ Stati di rendering dello stencil D3DRS CCW \_ \* vengono ignorati.

Un nuovo bit di estremità indica se il dispositivo supporta questa funzionalità. Si prevede che i driver che non supportano questa funzionalità ignorino questi nuovi Stati di rendering. Tutti gli altri bit di estremità dello stencil si applicano a entrambe le modalità di memorizzazione nel buffer dello stencil. Poiché lo \_ \_ stencil con due lati implica la possibilità di creare con D3DCULLMODE \_ None set, il limite corrispondente deve essere impostato dal driver se supporta questa nuova modalità stencil. Microsoft Windows Hardware Quality Labs (WHQL) dovrebbe applicare questa operazione.

Nuovi Stati di rendering:


```
D3DRS_Two_Sided_StencilMODE // BOOL (default is FALSE)
D3DRS_CCW_STENCILFAIL     // Same default as D3DRS_STENCILFAIL
D3DRS_CCW_STENCILZFAIL    // Same default as D3DRS_STENCILZFAIL
D3DRS_CCW_STENCILPASS     // Same default as D3DRS_STENCILPASS
D3DRS_CCW_STENCILFUNC     // Same default as D3DRS_STENCILFUNC
```



Nuovo Cap:


```
D3DSTENCILCAPS_TWOSIDED // a flag on D3DCAPS9.StencilCaps
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tecniche del buffer dello stencil](stencil-buffer-techniques.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
