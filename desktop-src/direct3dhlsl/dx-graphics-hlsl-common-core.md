---
title: Common-Shader Core
description: Common-Shader Core
ms.assetid: f3cf2969-83a4-461f-8177-d336536194ba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c2d1851025cb051a21a997f5e3a4987d3b6309e148248b3ea55c6b9ca6ad31c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950481"
---
# <a name="common-shader-core"></a>Common-Shader Core

Nel modello shader 4 tutte le fasi dello shader implementano la stessa funzionalità di base usando un core di shader comune. Inoltre, ognuna delle tre fasi dello shader (vertice, geometria e pixel) offre funzionalità specifiche per ogni fase, ad esempio la possibilità di generare nuove primitive dalla fase geometry shader o di eliminare un pixel specifico nella fase pixel shader. Il diagramma seguente illustra il flusso dei dati attraverso una fase dello shader e la relazione tra il core dello shader comune e le risorse di memoria dello shader.

![diagramma del flusso di dati in una fase shader](images/d3d10-shader-unit.png)

-   **Dati di input:** un vertex shader riceve gli input dalla fase dell'assembler di input. I geometry shader e i pixel shader ricevono i rispettivi input dalla fase shader precedente. Gli input aggiuntivi includono [la semantica dei](dx-graphics-hlsl-semantics.md)valori di sistema, che possono essere utilizzati dalla prima unità nella pipeline a cui sono applicabili.
-   **Dati di** output: gli shader generano risultati di output da passare alla fase successiva nella pipeline. Per uno shader geometry, la quantità di dati restituiti da una singola chiamata può variare. Alcuni output vengono interpretati dal core dello shader comune (ad esempio la posizione del vertice e l'indice render-target-array), altri sono progettati per essere interpretati da un'applicazione.
-   **Codice shader:** gli shader possono leggere dalla memoria, eseguire operazioni a virgola mobile vettoriale e aritmetiche su interi o operazioni di controllo del flusso. Non esiste alcun limite al numero di istruzioni che possono essere implementate in uno shader.
-   **Campionatori:** i campionatori definiscono come campionare e filtrare le trame. A uno shader possono essere associati simultaneamente fino a 16 campionatori.
-   **Trame:** le trame possono essere filtrate usando campionatori o lette in base ai texel direttamente con la funzione intrinseca [di](dx-graphics-hlsl-to-load.md) caricamento.
-   **Buffer:** i buffer non vengono mai filtrati, ma possono essere letti dalla memoria in base all'elemento direttamente con la funzione intrinseca [di](dx-graphics-hlsl-to-load.md) caricamento. A uno shader possono essere associate simultaneamente fino a 128 risorse di trama e buffer (combinate).
-   **Buffer costanti:** i buffer costanti sono ottimizzati per le variabili costanti shader. A una fase shader possono essere associati simultaneamente fino a 16 buffer costanti. Sono progettati per un aggiornamento più frequente dalla CPU. pertanto hanno restrizioni aggiuntive per dimensioni, layout e accesso.


Differenze tra Direct3D 9 e Direct3D 10:

- In Direct3D 9 ogni unità shader aveva un singolo file di registro costante di piccole dimensioni per archiviare tutte le variabili di shader costanti. Per ospitare tutti gli shader con questo spazio costante limitato è necessario riciclare frequentemente le costanti da parte della CPU.
- In Direct3D 10 le costanti vengono archiviate in buffer non modificabili in memoria e vengono gestite come qualsiasi altra risorsa. Non esiste alcun limite al numero di buffer costanti che un'applicazione può creare. Organizzando le costanti in buffer in base alla frequenza di aggiornamento e utilizzo, la quantità di larghezza di banda necessaria per aggiornare le costanti per contenere tutti gli shader può essere notevolmente ridotta.



 

## <a name="integer-and-bitwise-support"></a>Supporto di interi e bit per bit

Il core dello shader comune fornisce un set completo di operazioni bit per bit e interi a 32 bit conformi a IEEE. Queste operazioni consentono una nuova classe di algoritmi negli esempi di hardware grafico, tra cui tecniche di compressione e compressione, FFT e controllo del flusso di programma dei campi di bit.

I **tipi di** dati int e **uint** in HLSL Direct3D 10 sono mappati a interi a 32 bit nell'hardware.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 10:<br/> In Direct3D 9 gli input del flusso contrassegnati come integer in HLSL sono stati interpretati come a virgola mobile. In Direct3D 10 gli input di flusso contrassegnati come integer vengono interpretati come integer a 32 bit.<br/> Inoltre, i valori booleani sono ora tutti bit impostati o tutti i bit non impostati. I dati convertiti in **bool** verranno interpretati come true se il valore non è uguale a 0,0f (sia lo zero positivo che quello negativo possono essere false) e false in caso contrario.<br/> |



 

## <a name="bitwise-operators"></a>Operatori bit per bit

Il nucleo comune dello shader supporta gli operatori bit per bit seguenti:



| Operatore  | Funzione          |
|-----------|-------------------|
| ~         | NOT logico       |
| <<  | Spostamento a sinistra        |
| >>  | Spostamento a destra       |
| &         | And logico       |
| \|        | Esegue un'operazione di Or logico.        |
| ^         | Xor logico       |
| <<= | Spostamento a sinistra uguale  |
| >>= | Right Shift Equal |
| &=        | Ed è uguale a         |
| \|=       | o uguale a          |
| ^=        | Xor Uguale         |



 

Gli operatori bit per bit vengono definiti per operare solo sui **tipi di** dati int e **uint.** Il tentativo di usare operatori bit per bit **su tipi di** dati float o **struct** restituirà un errore. Gli operatori bit per bit seguono la stessa precedenza di C rispetto ad altri operatori.

## <a name="binary-casts"></a>Cast binari

Il cast tra un integer e un tipo a virgola mobile convertirà il valore numerico in base alle regole di troncamento C. Il cast di un valore **da float** a **int** e di nuovo a un **tipo float** è una conversione persa che dipende dalla precisione del tipo di dati di destinazione. Ecco alcune delle funzioni di conversione: [**asfloat (DirectX HLSL),**](dx-graphics-hlsl-asfloat.md) [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL).**](dx-graphics-hlsl-asuint.md)

I cast binari possono essere eseguiti anche usando funzioni intrinseche HLSL. In questo modo il compilatore reinterpreta la rappresentazione di bit di un numero nel tipo di dati di destinazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





