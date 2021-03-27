---
title: Formato effetto (Direct3D 11)
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: 'Altre informazioni su: formato effetto (Direct3D 11)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c08589fcb041591591d033b88e4fafe597e98520
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225628"
---
# <a name="effect-format-direct3d-11"></a>Formato effetto (Direct3D 11)

Un effetto (spesso archiviato in un file con estensione FX) dichiara lo stato della pipeline impostato da un effetto. Lo stato dell'effetto può essere suddiviso approssimativamente in tre categorie:

-   [Variabili](d3d11-effect-variable-syntax.md), generalmente dichiarate all'inizio di un effetto.
-   [Funzioni](d3d11-effect-function-syntax.md), che implementano il codice dello shader, o vengono usate come funzioni di supporto da altre funzioni.
-   [Tecniche](d3d11-effect-technique-syntax.md), che possono essere disposte in gruppi di effetti e implementare sequenze di rendering usando uno o più passaggi di effetto. Ogni sessione imposta uno o più [gruppi di stati](d3d11-effect-states.md) e chiama funzioni shader.

![diagramma delle categorie di dichiarazioni per gli effetti, incluse le variabili nella parte superiore, funzioni al centro e tecniche nella parte inferiore](images/d3d10-effect-intro.png)

Il diagramma precedente mostra le categorie dello stato dell'effetto.

La definizione del formato binario effetto si trova nel file binario \\ EffectBinaryFormat. h nel codice sorgente degli effetti.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                   | Descrizione                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Sintassi della variabile Effect](d3d11-effect-variable-syntax.md)<br/>   | Una variabile Effect viene dichiarata con la sintassi descritta in questa sezione.<br/>                                 |
| [Sintassi dell'annotazione](d3d11-effect-annotation-syntax.md)<br/>      | Un'annotazione è una parte di informazioni definita dall'utente, dichiarata con la sintassi descritta in questa sezione.<br/> |
| [Sintassi della funzione Effect](d3d11-effect-function-syntax.md)<br/>   | Una funzione Effect viene scritta in HLSL ed è dichiarata con la sintassi descritta in questa sezione.<br/>          |
| [Sintassi della tecnica degli effetti](d3d11-effect-technique-syntax.md)<br/> | Una tecnica degli effetti viene dichiarata con la sintassi descritta in questa sezione.<br/>                                |
| [Gruppi di stati effetti](d3d11-effect-states.md)<br/>               | Gli Stati degli effetti sono coppie nome-valore sotto forma di espressione.<br/>                                          |
| [Sintassi del gruppo di effetti](d3d11-effect-group-syntax.md)<br/>         | Un gruppo di effetti viene dichiarato con la sintassi descritta in questa sezione.<br/>                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento agli effetti 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





