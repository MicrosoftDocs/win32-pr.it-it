---
title: Mascheramento del registro di destinazione
description: La maschera specifica i componenti del registro di destinazione che verranno aggiornati con il risultato di un'istruzione . I registri di trama hanno un set di regole e i registri non di testo hanno un altro set di regole.
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1a8d45e847f7da785bd09b83e778d140cee68007add882066b508b38043550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119685"
---
# <a name="destination-register-masking"></a>Mascheramento del registro di destinazione

La maschera specifica i componenti del registro di destinazione che verranno aggiornati con il risultato di un'istruzione . I registri di trama hanno un set di regole e i registri non di testo hanno un altro set di regole.

-   dx9 \_ graphics \_ reference \_ asm vs \_ \_ registers \_ modifiers masking : \_ questa sezione contiene le regole per l'applicazione di maschere ai registri di destinazione.
-   Maschere \_ registro \_ trame: i registri trama hanno alcune regole univoche.

## <a name="destination-register-masking"></a>Mascheramento del registro di destinazione

Come illustrato nella tabella seguente, la maschera (dove sono uno dei registri [vertex shader vertex shader](dx9-graphics-reference-asm-vs-registers.md)validi) può essere applicata ai singoli componenti dei dati del vettore.



| Modificatore di componente | Descrizione      |
|--------------------|------------------|
| r.{x}{y}{z}{w}     | Maschera di destinazione |



 

-   In generale, specificare le maschere di scrittura del registro di destinazione è un buon stile di scrittura del codice. Semplifica la lettura e la manutenzione del codice.
-   Qualsiasi combinazione di componenti può essere specificata (inclusa nessuna) purché x preceda y, y precede z e z precede w.
-   I registri di output oPts e oFog devono usare una sola maschera.
-   Alcune istruzioni richiedono che il registro di destinazione usi una singola maschera di scrittura: exp, expp, log, logp, pow, rcp e rsq.
-   Nella versione 1.0 l'istruzione frc richiedeva una delle seguenti combinazioni di maschera: .x o .y o .xy. La versione 2.0 non ha alcuna restrizione della maschera.
-   sincos richiede una delle seguenti combinazioni di maschere: .x o .y o .xyz.
-   m3x2 richiede la maschera di scrittura .xy.
-   m3x3 e m4x3 richiedono la maschera di scrittura xyz.
-   m3x4 e m4x4 richiedono la maschera di scrittura xyz o la maschera di scrittura predefinita (xyzw).

## <a name="texture-register-masks"></a>Maschere registro trame

Le regole di convalida per l'uso dei modificatori nei registri delle coordinate di trama sono più rigide rispetto alle regole di convalida per altri registri.

-   Se si scrive oTn, devono essere scritti anche tutti i registri precedenti (oTn-1 ~ oT0).
-   La maschera di scrittura "combinata" per qualsiasi registro oT \# deve essere esattamente una delle seguenti:
    -   .x
    -   .xy
    -   .xyz
    -   .xyzw (che equivale a non usare modificatori di componente)

Ad esempio, un vertex shader può eseguire l'output nei registri di trama in istruzioni separate.


```
    oT1.y  
    oT0.y  
    oT2  
    oT0.xz  
    oT1.x
```



In caso contrario, le istruzioni possono essere combinate.


```
    oT0.xyz  
    oT1.xy  
    oT2.xyzw    
```



Queste restrizioni si applicano solo ai registri delle coordinate di trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori di registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




