---
title: Mascheramento del registro di destinazione
description: La maschera specifica quali componenti del registro di destinazione verranno aggiornati con il risultato di un'istruzione. I registri di trama includono un set di regole e registri non di trama hanno un altro set di regole.
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ce15f75f424cb7796ef7db7a8b89bd5bcbfa9cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396406"
---
# <a name="destination-register-masking"></a>Mascheramento del registro di destinazione

La maschera specifica quali componenti del registro di destinazione verranno aggiornati con il risultato di un'istruzione. I registri di trama includono un set di regole e registri non di trama hanno un altro set di regole.

-   Guida \_ di \_ riferimento \_ alla grafica di DX9 ASM e \_ \_ registri \_ modificatori \_ -questa sezione contiene le regole per l'applicazione delle maschere ai registri di destinazione.
-   \_Maschere registro trama \_ : i registri di trama hanno alcune regole univoche.

## <a name="destination-register-masking"></a>Mascheramento del registro di destinazione

Come illustrato nella tabella seguente, la maschera (dove è uno dei [registri](dx9-graphics-reference-asm-vs-registers.md)di vertex shader di vertex shader validi) può essere applicata ai singoli componenti dei dati vettoriali.



| Modificatore Component | Descrizione      |
|--------------------|------------------|
| r. {x} {y} {z} {w}     | Maschera di destinazione |



 

-   In generale, specificare le maschere di scrittura del registro di destinazione è uno stile di codifica valido. Semplifica la lettura e la gestione del codice.
-   È possibile specificare qualsiasi combinazione di componenti (incluso None) a condizione che x preceda y, y preceda z e z preceda w.
-   I registri di output opz e oFog devono usare solo una maschera.
-   Per alcune istruzioni è necessario che il registro di destinazione usi una singola maschera di scrittura: EXP, EXPP, log, LogP, POW, RCP e rsq.
-   Nella versione 1,0, l'istruzione FRC richiede una delle combinazioni di maschere seguenti:. x o. y o. XY. La versione 2,0 non presenta alcuna restrizione mask.
-   SinCos richiede una delle combinazioni di maschere seguenti:. x o. y o. xyz.
-   M3X2 richiede la maschera di scrittura. XY.
-   M3X3 e m4x3 richiedono la maschera di scrittura. xyz.
-   M3x4 e M4x4 richiedono la maschera di scrittura. xyz o la maschera di scrittura predefinita (xyzw).

## <a name="texture-register-masks"></a>Maschere registro trama

Le regole di convalida per l'utilizzo di modificatori sui registri delle coordinate di trama sono più strette rispetto alle regole di convalida per altri registri.

-   Se viene scritto oTn, è necessario scrivere anche tutti i registri precedenti (oTn-1 ~ oT0).
-   La maschera di scrittura "combinata" per qualsiasi \# Registro OT deve essere esattamente una delle seguenti:
    -   .x
    -   . XY
    -   . xyz
    -   . xyzw (che equivale a non usare alcun modificatore di componente)

Ad esempio, un vertex shader può restituire i registri di trama in istruzioni separate.


```
    oT1.y  
    oT0.y  
    oT2  
    oT0.xz  
    oT1.x
```



In alternativa, le istruzioni possono essere combinate.


```
    oT0.xyz  
    oT1.xy  
    oT2.xyzw    
```



Queste restrizioni si applicano solo ai registri delle coordinate di trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro vertex shader](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




