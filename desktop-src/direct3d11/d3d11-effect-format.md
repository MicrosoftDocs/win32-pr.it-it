---
title: Formato effetto (Direct3D 11)
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: 'Altre informazioni su: Formato effetto (Direct3D 11)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7644e433f6c19df20cb2417659cf575e0613f93b0d53f6494ad6ee1422a55b9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792071"
---
# <a name="effect-format-direct3d-11"></a>Formato effetto (Direct3D 11)

Un effetto (che viene spesso archiviato in un file con estensione fx) dichiara lo stato della pipeline impostato da un effetto. Lo stato dell'effetto può essere suddiviso approssimativamente in tre categorie:

-   [Variabili](d3d11-effect-variable-syntax.md), che in genere vengono dichiarate all'inizio di un effetto.
-   [Funzioni](d3d11-effect-function-syntax.md), che implementano il codice shader o vengono usate come funzioni helper da altre funzioni.
-   [Tecniche ,](d3d11-effect-technique-syntax.md)che possono essere disposte in gruppi di effetti e implementano sequenze di rendering usando uno o più passaggi di effetto. Ogni passaggio imposta uno o più gruppi [di stati e](d3d11-effect-states.md) chiama le funzioni shader.

![diagramma delle categorie di dichiarazioni per gli effetti, incluse le variabili nella parte superiore, le funzioni al centro e le tecniche nella parte inferiore](images/d3d10-effect-intro.png)

Il diagramma precedente mostra le categorie di stato dell'effetto.

La definizione del formato binario degli effetti è disponibile in Binary \\ EffectBinaryFormat.h nel codice sorgente degli effetti.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                   | Descrizione                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Sintassi delle variabili effect](d3d11-effect-variable-syntax.md)<br/>   | Una variabile di effetto viene dichiarata con la sintassi descritta in questa sezione.<br/>                                 |
| [Sintassi delle annotazioni](d3d11-effect-annotation-syntax.md)<br/>      | Un'annotazione è un'informazione definita dall'utente, dichiarata con la sintassi descritta in questa sezione.<br/> |
| [Sintassi della funzione Effect](d3d11-effect-function-syntax.md)<br/>   | Una funzione di effetto è scritta in HLSL e viene dichiarata con la sintassi descritta in questa sezione.<br/>          |
| [Sintassi della tecnica degli effetti](d3d11-effect-technique-syntax.md)<br/> | Una tecnica di effetto viene dichiarata con la sintassi descritta in questa sezione.<br/>                                |
| [Gruppi di stati degli effetti](d3d11-effect-states.md)<br/>               | Gli stati dell'effetto sono coppie nome-valore sotto forma di espressione.<br/>                                          |
| [Sintassi dei gruppi di effetti](d3d11-effect-group-syntax.md)<br/>         | Un gruppo di effetti viene dichiarato con la sintassi descritta in questa sezione.<br/>                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su Effects 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





