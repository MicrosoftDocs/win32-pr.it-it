---
title: Limitazioni del controllo di flusso
description: Le istruzioni per il controllo di flusso pixel shader hanno limiti che influiscono sul numero di livelli di annidamento che è possibile includere nelle istruzioni. Esistono inoltre alcune limitazioni per l'implementazione del controllo di flusso per pixel con istruzioni per la sfumatura.
ms.assetid: 17a902cd-16a4-4065-9249-01f9b1f40506
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 34891e29a1bb27aead629db2cc7473c7d4329af5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856961"
---
# <a name="flow-control-limitations"></a>Limitazioni del controllo di flusso

Le istruzioni per il controllo di flusso pixel shader hanno limiti che influiscono sul numero di livelli di annidamento che è possibile includere nelle istruzioni. Esistono inoltre alcune limitazioni per l'implementazione del controllo di flusso per pixel con istruzioni per la sfumatura.

> [!Note]  
> Quando si usano i \* \_ \_ profili dello \_ shader HLSL a 4 0 di livello \_ 9 \_ , si usano in modo implicito i profili [Shader Model 2. x](dx-graphics-hlsl-sm2.md) per supportare l'hardware compatibile con Direct3D 9. I profili Shader Model 2. x supportano un comportamento di controllo di flusso più limitato rispetto ai profili [4. x](dx-graphics-hlsl-sm4.md) e successivi del modello shader.

 

-   [Conteggi profondità istruzione pixel shader](#pixel-shader-instruction-depth-counts)
-   [Interazione del controllo di flusso Per-Pixel con sfumature dello schermo](#interaction-of-per-pixel-flow-control-with-screen-gradients)

## <a name="pixel-shader-instruction-depth-counts"></a>Conteggi profondità istruzione pixel shader

PS \_ 2 \_ 0 non supporta il controllo di flusso. Di seguito sono elencate le limitazioni per le altre versioni di pixel shader.

### <a name="instruction-depth-count-for-ps_2_x"></a>Conteggio profondità istruzioni per PS \_ 2 \_ x

Ogni istruzione viene conteggiata in base a uno o più limiti di profondità di nidificazione. Nella tabella seguente viene elencato il numero di profondità che ogni istruzione aggiunge o sottrae dalla profondità esistente.



| Istruzione                              | Annidamento statico                       | Annidamento dinamico                                                           | annidamento ciclo/Rep | annidamento delle chiamate |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [Se bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Se \_ comp-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [Se prede-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-PS](endif---ps.md)             | -1 ([se bool-PS](if-bool---ps.md)) | -1 ([se prede-PS](if-pred---ps.md) o [if \_ comp-PS](if-comp---ps.md)) | 0                | 0            |
| [Rep-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [Break-PS](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [Interrompi \_ comp-PS](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [Breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [chiamata a PS](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz prede-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [RET-PS](ret---ps.md)                 | 0                                    | -1 ([callnz Predator-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [setp \_ comp-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profondità di annidamento

Profondità di annidamento definisce il numero di istruzioni che possono essere chiamate dall'uno all'interno dell'altro. Ogni tipo di istruzione ha uno o più limiti di nidificazione, come indicato nella tabella seguente.



| Tipo di istruzione | Massimo                                                                                   |
|------------------|-------------------------------------------------------------------------------------------|
| Annidamento statico   | 24 if (D3DCAPS9. D3DPSHADERCAPS2 \_ 0. StaticFlowControlDepth > 0); 0 in caso contrario            |
| Annidamento dinamico  | da 0 a 24, vedere D3DCAPS9. D3DPSHADERCAPS2 \_ 0. DynamicFlowControlDepth                          |
| annidamento Rep      | da 0 a 4, vedere D3DCAPS9. D3DPSHADERCAPS2 \_ 0. StaticFlowControlDepth                            |
| annidamento delle chiamate     | da 0 a 4, vedere D3DCAPS9. D3DPSHADERCAPS2 \_ 0. StaticFlowControlDepth (indipendente dal limite Rep) |



 

### <a name="instruction-depth-count-for-ps_2_sw"></a>Conteggio profondità istruzioni per PS \_ 2 \_ SW

Ogni istruzione viene conteggiata in base a uno o più limiti di profondità di nidificazione. Questa tabella mostra il numero di profondità che ogni istruzione aggiunge o sottrae dalla profondità esistente.



| Istruzione                              | Annidamento statico                       | Annidamento dinamico                                                           | annidamento ciclo/Rep | annidamento delle chiamate |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [Se bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Se prede-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Se \_ comp-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-PS](endif---ps.md)             | -1 ([se bool-PS](if-bool---ps.md)) | -1 ([se prede-PS](if-pred---ps.md) o [if \_ comp-PS](if-comp---ps.md)) | 0                | 0            |
| [Rep-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [ciclo-PS](loop---ps.md)               | n/d                                  | n/d                                                                       | n/d              | n/d          |
| [endloop-PS](endloop---ps.md)         | n/d                                  | n/d                                                                       | n/d              | n/d          |
| [Break-PS](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [Interrompi \_ comp-PS](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [Breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [chiamata a PS](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz prede-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [RET-PS](ret---ps.md)                 | 0                                    | -1 ([callnz Predator-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [setp \_ comp-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profondità di annidamento

Profondità di annidamento definisce il numero di istruzioni che possono essere chiamate dall'interno. Ogni tipo di istruzione ha uno o più limiti di nidificazione, come indicato nella tabella seguente.



| Tipo di istruzione | Massimo |
|------------------|---------|
| Annidamento statico   | 24      |
| Annidamento dinamico  | 24      |
| annidamento Rep      | 4       |
| annidamento delle chiamate     | 4       |



 

### <a name="instruction-depth-count-for-ps_3_0"></a>Conteggio profondità istruzioni per PS \_ 3 \_ 0

Ogni istruzione viene conteggiata in base a uno o più limiti di profondità di nidificazione. Questa tabella mostra il numero di profondità che ogni istruzione aggiunge o sottrae dalla profondità esistente.



| Istruzione                              | Annidamento statico                       | Annidamento dinamico                                                           | annidamento ciclo/Rep | annidamento delle chiamate |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [Se bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Se prede-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Se \_ comp-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-PS](endif---ps.md)             | -1 ([se bool-PS](if-bool---ps.md)) | -1 ([se prede-PS](if-pred---ps.md) o [if \_ comp-PS](if-comp---ps.md)) | 0                | 0            |
| [Rep-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [ciclo-PS](loop---ps.md)               | 0                                    | 0                                                                         | 1                | 0            |
| [endloop-PS](endloop---ps.md)         | 0                                    | 0                                                                         | -1               | 0            |
| [Break-PS](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [Interrompi \_ comp-PS](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [Breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [chiamata a PS](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz prede-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [RET-PS](ret---ps.md)                 | 0                                    | -1 ([callnz Predator-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [setp \_ comp-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profondità di annidamento

Profondità di annidamento definisce il numero di istruzioni che possono essere chiamate dall'interno. Ogni tipo di istruzione ha uno o più limiti di nidificazione, come indicato nella tabella seguente.



| Tipo di istruzione | Massimo |
|------------------|---------|
| Annidamento statico   | 24      |
| Annidamento dinamico  | 24      |
| annidamento ciclo/Rep | 4       |
| annidamento delle chiamate     | 4       |



 

### <a name="instruction-depth-count-for-ps_3_sw"></a>Conteggio profondità istruzioni per PS \_ 3 \_ SW

Ogni istruzione viene conteggiata in base a uno o più limiti di profondità di nidificazione. Questa tabella mostra il numero di profondità che ogni istruzione aggiunge o sottrae dalla profondità esistente.



| Istruzione                              | Annidamento statico                       | Annidamento dinamico                                                           | annidamento ciclo/Rep | annidamento delle chiamate |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [Se bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Se prede-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Se \_ comp-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-PS](endif---ps.md)             | -1 ([se bool-PS](if-bool---ps.md)) | -1 ([se prede-PS](if-pred---ps.md) o [if \_ comp-PS](if-comp---ps.md)) | 0                | 0            |
| [Rep-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [ciclo-PS](loop---ps.md)               | 0                                    | 0                                                                         | 1                | 0            |
| [endloop-PS](endloop---ps.md)         | 0                                    | 0                                                                         | -1               | 0            |
| [Break-PS](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [Interrompi \_ comp-PS](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [Breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [chiamata a PS](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz prede-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [RET-PS](ret---ps.md)                 | 0                                    | -1 ([callnz Predator-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [setp \_ comp-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profondità di annidamento

Profondità di annidamento definisce il numero di istruzioni che possono essere chiamate dall'interno. Ogni tipo di istruzione ha uno o più limiti di nidificazione, come indicato nella tabella seguente.



| Tipo di istruzione | Massimo |
|------------------|---------|
| Annidamento statico   | 24      |
| Annidamento dinamico  | 24      |
| annidamento ciclo/Rep | 4       |
| annidamento delle chiamate     | 4       |



 

## <a name="interaction-of-per-pixel-flow-control-with-screen-gradients"></a>Interazione del controllo di flusso Per-Pixel con sfumature dello schermo

Il set di istruzioni pixel shader include diverse istruzioni che producono o utilizzano sfumature di quantità rispetto allo spazio dello schermo x e y. L'uso più comune per le sfumature consiste nel calcolare i calcoli del livello di dettaglio per il campionamento delle trame e, nel caso del filtro anisotropico, selezionando esempi lungo l'asse di anisotropia. In genere, le implementazioni hardware eseguono il pixel shader su più pixel simultaneamente, ad esempio una griglia 2x2, in modo che le sfumature di quantità calcolate nello shader possano essere ragionevolmente approssimate come Delta dei valori nello stesso punto di esecuzione in pixel adiacenti.

Quando il controllo di flusso è presente in uno shader, il risultato di un calcolo della sfumatura richiesto all'interno di un percorso di branch specificato è ambiguo quando i pixel adiacenti possono eseguire percorsi di controllo di flusso distinti. Pertanto, viene considerato non valido utilizzare qualsiasi operazione di pixel shader che richiede un calcolo di sfumatura in una posizione all'interno di un costrutto di controllo di flusso che può variare tra i pixel per una determinata primitiva che viene rasterizzata.

Tutte le istruzioni pixel shader vengono partizionate nelle operazioni consentite e in quelle non consentite all'interno del controllo di flusso:

-   Scenario A: operazioni non consentite all'interno del controllo di flusso che potrebbero variare tra i pixel in una primitiva. Sono incluse le operazioni elencate nella tabella seguente. 

    | Istruzione                                                                                                      | È consentito nel controllo di flusso quando:                       |
    |------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
    | [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md) e [texldp-PS](texldp---ps.md) | Per la coordinata di trama viene usato un registro temporaneo. |
    | [DSX-PS](dsx---ps.md) e [DSY-PS](dsy---ps.md)                                                            | Per l'operando viene usato un registro temporaneo.            |

    

     

-   Scenario B: operazioni consentite ovunque. Sono incluse le operazioni elencate nella tabella seguente. 

    | Istruzione                                                                                                      | È consentito ovunque nei casi seguenti:                                                                                             |
    |------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
    | [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md) e [texldp-PS](texldp---ps.md) | Per la coordinata di trama viene utilizzata una quantità di sola lettura (può variare per pixel, ad esempio coordinate di trama interpolate). |
    | [DSX-PS](dsx---ps.md) e [DSY-PS](dsy---ps.md)                                                            | Viene utilizzata una quantità di sola lettura per l'operando di input (può variare per pixel, ad esempio coordinate di trama interpolate).      |
    | [texldl-PS](texldl---ps.md)                                                                                   | L'utente fornisce il livello di dettaglio come argomento, quindi non sono presenti gradienti e pertanto non si verificano problemi con il controllo di flusso.       |
    | [texldd-PS](texldd---ps.md)                                                                                   | L'utente fornisce gradienti come argomenti di input, pertanto non è presente alcun problema con il controllo di flusso.                                 |

    

     

Queste restrizioni vengono applicate rigorosamente alla convalida dello shader. Gli scenari in cui si verifica una condizione di ramo simile a quello di un diramazione in modo coerente in una primitiva, anche se un operando nell'espressione della condizione è una quantità calcolata in pixel shader, comunque rientrano nello scenario A e non sono consentiti. In modo analogo, scenari in cui le sfumature sono richieste in una quantità calcolata shader x dall'interno del controllo di flusso dinamico, ma anche in cui sembra che x non venga modificato in nessuno dei rami, comunque rientrano nello scenario A e non sono consentiti.

Predicazione è incluso in queste restrizioni sul controllo di flusso, in modo che le implementazioni rimangano gratuite per l'interscambio dell'implementazione di istruzioni branch con istruzioni predicate.

L'utente può utilizzare le istruzioni degli scenari A e B insieme. Si supponga, ad esempio, che l'utente abbia bisogno di un campione di trama anisotropico data una coordinata di trama calcolata dello shader. Tuttavia, il carico di trama è necessario solo per i pixel che soddisfano alcune condizioni per pixel. Per soddisfare questi requisiti, l'utente può calcolare la coordinata di trama per tutti i pixel, al di fuori del controllo di flusso variabile per pixel, calcolando immediatamente le sfumature usando le istruzioni [DSX-PS](dsx---ps.md) e [DSY-PS](dsy---ps.md) . Quindi, all'interno di un blocco [bool](if-bool---ps.md)-PS / [endif-PS](endif---ps.md) per pixel, l'utente può usare [texldd-PS](texldd---ps.md) (Load di trama con gradienti forniti dall'utente), passando le sfumature precalcolate. Un altro modo per descrivere questo modello di utilizzo è che, mentre tutti i pixel della primitiva dovevano calcolare le coordinate di trama e essere interessati dal calcolo della sfumatura, solo i pixel che dovevano campionare una trama effettivamente lo facevano.

Indipendentemente da queste regole, l'onere è ancora presente all'utente per assicurarsi che prima di calcolare qualsiasi sfumatura (o eseguire un esempio di trama che calcola in modo implicito una sfumatura), il registro contenente i dati di origine deve essere stato inizializzato per tutti i percorsi di esecuzione in anticipo. L'inizializzazione dei registri temporanei non viene convalidata o applicata in generale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




