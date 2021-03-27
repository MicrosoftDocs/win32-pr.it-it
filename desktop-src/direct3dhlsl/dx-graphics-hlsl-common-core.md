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
ms.openlocfilehash: e27ebe7d908c473890ac5b851eac3e0bc840c859
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855722"
---
# <a name="common-shader-core"></a>Common-Shader Core

In Shader Model 4, tutte le fasi dello shader implementano la stessa funzionalità di base usando un core shader comune. Inoltre, ognuna delle tre fasi dello shader (vertice, geometria e pixel) offre funzionalità univoche per ogni fase, ad esempio la possibilità di generare nuove primitive dalla fase geometry shader o di rimuovere un pixel specifico nella fase pixel shader. Il diagramma seguente illustra il flusso dei dati attraverso una fase dello shader e la relazione tra il nucleo di shader comune e le risorse di memoria dello shader.

![diagramma del flusso di dati in una fase dello shader](images/d3d10-shader-unit.png)

-   **Dati di input**: un vertex shader riceve gli input dalla fase dell'assembler di input. la geometria e i pixel shader ricevono gli input dalla fase precedente dello shader. Gli input aggiuntivi includono la [semantica dei valori di sistema](dx-graphics-hlsl-semantics.md), che possono essere utilizzati dalla prima unità nella pipeline a cui sono applicabili.
-   **Dati di output**: gli shader generano i risultati di output da passare alla fase successiva nella pipeline. Per un geometry shader, la quantità di output di dati da una singola chiamata può variare. Alcuni output sono interpretati da Common-shader core, ad esempio la posizione del vertice e l'indice della matrice di destinazione di rendering, altri sono progettati per essere interpretati da un'applicazione.
-   **Codice shader**: gli shader possono leggere dalla memoria, eseguire operazioni aritmetiche a virgola mobile e numeri interi o operazioni di controllo di flusso. Non esiste alcun limite al numero di istruzioni che possono essere implementate in uno shader.
-   **Samplers**: i sampler definiscono le modalità di campionamento e filtro delle trame. È possibile associare un massimo di 16 campioni a uno shader simultaneamente.
-   **Trame**: è possibile filtrare le trame usando i sampler o leggere direttamente in base a Texel con la funzione intrinseca [Load](dx-graphics-hlsl-to-load.md) .
-   **Buffer**: i buffer non vengono mai filtrati, ma possono essere letti dalla memoria in base a ogni elemento direttamente con la funzione intrinseca [Load](dx-graphics-hlsl-to-load.md) . Fino a un massimo di 128, le risorse di trama e buffer (combinate) possono essere associate contemporaneamente a uno shader.
-   **Buffer costanti**: i buffer costanti sono ottimizzati per le variabili costanti dello shader. Fino a un massimo di 16 buffer costanti è possibile associare contemporaneamente una fase dello shader. Sono progettate per un aggiornamento più frequente dalla CPU; Pertanto, presentano restrizioni di dimensioni, layout e accesso aggiuntive.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 10:<br/> In Direct3D 9 ogni unità shader aveva un singolo file di registro costante di piccole dimensioni per archiviare tutte le variabili di shader costanti. Per ospitare tutti gli shader con questo spazio costante limitato è necessario riciclo frequente delle costanti da parte della CPU.<br/> In Direct3D 10, le costanti vengono archiviate in buffer non modificabili in memoria e vengono gestite come qualsiasi altra risorsa. Non esiste alcun limite al numero di buffer costanti che un'applicazione può creare. Organizzando le costanti in buffer in base alla frequenza di aggiornamento e utilizzo, la quantità di larghezza di banda necessaria per aggiornare le costanti per adattarsi a tutti gli shader può essere notevolmente ridotta.<br/> |



 

## <a name="integer-and-bitwise-support"></a>Supporto Integer e bit per bit

Common shader Core offre un set completo di operazioni bit per bit conformi a IEEE e a 32 bit. Queste operazioni abilitano una nuova classe di algoritmi negli esempi di hardware grafico sono le tecniche di compressione e compressione, FFT e il controllo del flusso del programma bit.

I tipi di dati **int** e **uint** in Direct3D 10 HLSL vengono mappati a interi a 32 bit nell'hardware.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 10:<br/> Negli input di flusso Direct3D 9 contrassegnati come Integer in HLSL sono stati interpretati come virgola mobile. In Direct3D 10, gli input di flusso contrassegnati come Integer vengono interpretati come Integer a 32 bit.<br/> Inoltre, i valori booleani sono ora tutti impostati su bit oppure tutti i bit non vengono impostati. I dati convertiti in **bool** verranno interpretati come true se il valore non è uguale a 0,0 f (il valore zero positivo e negativo possono essere false) e false in caso contrario.<br/> |



 

## <a name="bitwise-operators"></a>Operatori bit per bit

Common shader Core supporta gli operatori bit per bit seguenti:



| Operatore  | Funzione          |
|-----------|-------------------|
| ~         | Not logico       |
| <<  | Spostamento a sinistra        |
| >>  | Spostamento a destra       |
| &         | And logico       |
| \|        | Esegue un'operazione di Or logico.        |
| ^         | XOR logico       |
| <<= | Spostamento a sinistra uguale  |
| >>= | Spostamento a destra uguale |
| &=        | E uguale a         |
| \|=       | O uguale a          |
| ^=        | XOR uguale         |



 

Gli operatori bit per bit vengono definiti per operare solo sui tipi di dati **int** e **uint** . Il tentativo di utilizzare operatori bit per bit sui tipi di dati **float** o **struct** genererà un errore. Gli operatori bit per bit seguono la stessa precedenza di C rispetto ad altri operatori.

## <a name="binary-casts"></a>Cast binari

Eseguendo il cast tra un Integer e un tipo a virgola mobile, il valore numerico viene convertito dopo le regole di troncamento C. Il cast di un valore da un valore **float**, a un valore **int** e **viceversa è una** conversione con perdita di dati dipendente dalla precisione del tipo di dati di destinazione. Di seguito sono riportate alcune delle funzioni di conversione: [**AsFloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**AsInt (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).

I cast binari possono essere eseguiti anche usando funzioni intrinseche HLSL. In questo modo il compilatore reinterpreta la rappresentazione di bit di un numero nel tipo di dati di destinazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello Shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





