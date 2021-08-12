---
description: I volumi ombreggiati vengono usati per disegnare ombreggiature con il buffer dello stencil.
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: Two-Sided Stencil (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bca0b960f96d1747b2b7ad51771276df2cfe1da1fa8ac9aa4d7c1ce8ea7c03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290511"
---
# <a name="two-sided-stencil-direct3d-9"></a>Two-Sided Stencil (Direct3D 9)

I volumi ombreggiati vengono usati per disegnare ombreggiature con il buffer dello stencil. L'applicazione calcola i volumi di ombreggiatura espressi dalla geometria occlusa, calcolando i bordi della lampadina ed estrudendoli dalla luce in un set di volumi 3D. Il rendering di questi volumi viene quindi eseguito due volte nel buffer degli stencil.

Il primo rendering disegna poligoni rivolti in avanti e incrementa i valori di stencil-buffer. Il secondo rendering disegna i poligoni rivolti all'indietro del volume dell'ombreggiatura e decrementa i valori del buffer dello stencil. In genere, tutti i valori incrementati e decrementati si annullano a vicenda. Tuttavia, il rendering della scena è già stato eseguito con una geometria normale, causando l'esito negativo del test del buffer z di alcuni pixel durante il rendering del volume dell'ombreggiatura. I valori lasciati nello stencil buffer corrispondono ai pixel presenti nell'ombreggiatura. Questi contenuti di stencil buffer rimanenti vengono usati come maschera, per eseguire la fusione alfa di un quad nero ampio e incomprenso nella scena. Con il buffer di stencil che funge da maschera, il risultato è quello di scurire i pixel che si trova nelle ombreggiature.

Ciò significa che la geometria dell'ombreggiatura viene disegnata due volte per ogni sorgente di luce, quindi esercitando pressione sulla velocità effettiva dei vertici della GPU. La funzionalità di stencil a due lati è stata progettata per attenuare questa situazione. In questo approccio sono disponibili due set di stato dello stencil (denominati di seguito), uno impostato per i triangoli frontale e l'altro per i triangoli rivolti all'indietro. In questo modo, viene disegnato un solo passaggio per ogni volume di ombreggiatura, per ogni luce.

Le modifiche dell'API sono limitate a un nuovo set di stati di rendering. Il nuovo stato di rendering D3DRS \_ Two \_ Sided \_ StencilMODE può essere impostato su **TRUE** o **FALSE.** È FALSE **per** impostazione predefinita, ovvero il comportamento corrente (DirectX 8). Quando questa proprietà è impostata su **TRUE** (funzionerà solo se È impostato D3DSTENCILCAPS TWOSIDED), gli stati di rendering seguenti verranno applicati solo ai triangoli frontale (in senso \_ orario).



| Stato di rendering        | Descrizione                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| D3DRS \_ STENCILFAIL  | D3DSTENCILOP da eseguire se il test di stencil ha esito negativo.                                                |
| D3DRS \_ STENCILZFAIL | D3DSTENCILOP da eseguire se il test di stencil ha esito positivo e il test z ha esito negativo.                              |
| D3DRS \_ STENCILPASS  | D3DSTENCILOP da eseguire se vengono superati sia lo stencil che i test z.                                     |
| D3DRS \_ STENCILFUNC  | D3DCMPFUNC fn. Test di stencil supera se ((& mask) stencilfn (stencil & mask)) è true. |



 

Un nuovo set di stati di rendering si applica ai triangoli rivolti verso il retro (in senso antiorario).



| Stato di rendering             | Descrizione                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| D3DRS \_ CCW \_ STENCILFAIL  | D3DSTENCILOP da eseguire se il test di stencil ha esito negativo.                                                      |
| D3DRS \_ CCW \_ STENCILZFAIL | D3DSTENCILOP da eseguire se il test di stencil ha esito positivo e il test z ha esito negativo.                                    |
| D3DRS \_ CCW \_ STENCILPASS  | D3DSTENCILOP da eseguire se vengono superati sia lo stencil che i test z.                                           |
| D3DRS \_ CCW \_ STENCILFUNC  | Funzione D3DCMPFUNC. Il test di stencil viene superato se ((& mask) stencilfn (stencil & mask)) è true. |



 

Gli stati di rendering degli stencil rimanenti si applicano sempre ai triangoli in senso orario e in senso antiorario.

D3DRS Two Sided StencilMODE viene ignorato per gli sprite di linee e punti, il che significa che il comportamento rimane invariato rispetto a \_ \_ \_ DirectX 8. Gli stati di rendering D3DRS \_ CCW \_ STENCIL vengono \* ignorati.

Un nuovo bit limite indica se il dispositivo supporta questa funzionalità. I driver che non supportano questa funzionalità dovrebbero ignorare questi nuovi stati di rendering. Tutti gli altri bit di estremità degli stencil si applicano a entrambe le modalità di memorizzazione nel buffer degli stencil. Poiché Two Sided Stencil implica la possibilità di disegnare con \_ \_ D3DCULLMODE NONE impostato, il limite corrispondente deve essere impostato dal driver se supporta questa nuova \_ modalità di stencil. Microsoft Windows Hardware Quality Labs (WHQL) deve applicare questa impostazione.

Nuovi stati di rendering:


```
D3DRS_Two_Sided_StencilMODE // BOOL (default is FALSE)
D3DRS_CCW_STENCILFAIL     // Same default as D3DRS_STENCILFAIL
D3DRS_CCW_STENCILZFAIL    // Same default as D3DRS_STENCILZFAIL
D3DRS_CCW_STENCILPASS     // Same default as D3DRS_STENCILPASS
D3DRS_CCW_STENCILFUNC     // Same default as D3DRS_STENCILFUNC
```



Nuovo limite:


```
D3DSTENCILCAPS_TWOSIDED // a flag on D3DCAPS9.StencilCaps
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tecniche di buffer di stencil](stencil-buffer-techniques.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
