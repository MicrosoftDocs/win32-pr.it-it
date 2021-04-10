---
description: Un effetto può essere utilizzato per archiviare le informazioni o per eseguire il rendering utilizzando un gruppo di stato.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Rendering di un effetto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfba9432412846e2dc634d6ab68be999b504e06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225577"
---
# <a name="rendering-an-effect-direct3d-10"></a>Rendering di un effetto (Direct3D 10)

Un effetto può essere utilizzato per archiviare le informazioni o per eseguire il rendering utilizzando un gruppo di stato. Ogni tecnica specifica i vertex shader, i geometry shader, i pixel shader, lo stato dello shader, il campionatore e lo stato della trama e altro stato della pipeline. Quindi, dopo avere organizzato lo stato in un effetto, è possibile incapsulare l'effetto di rendering risultante da tale stato creando ed eseguendo il rendering dell'effetto.

Sono necessari alcuni passaggi per preparare un effetto per il rendering. Il primo sta eseguendo la compilazione, che controlla HLSL come il codice rispetto alla sintassi del linguaggio HLSL e alle regole del Framework effetti. È possibile compilare un effetto dall'applicazione usando le chiamate API oppure è possibile compilare un effetto offline usando l'utilità del compilatore di effetti. Una volta che l'effetto è stato compilato correttamente, crearlo chiamando un set di API diverso (ma molto simile).

Dopo aver creato l'effetto, per utilizzarlo sono necessari due passaggi. In primo luogo, è necessario inizializzare i valori dello stato dell'effetto (i valori delle variabili dell'effetto) usando diversi metodi per impostare lo stato. Per alcune variabili questa operazione può essere eseguita una volta quando viene creato un effetto; altri devono essere aggiornati ogni volta che l'applicazione chiama il ciclo di rendering. Una volta impostate le variabili di effetto, si indica al runtime di eseguire il rendering dell'effetto applicando una tecnica. Questi argomenti sono descritti in dettaglio più avanti.

-   [Compilare un effetto (Direct3D 10)](d3d10-graphics-programming-guide-effects-compile.md)
-   [Creazione di un effetto (Direct3D 10)](d3d10-graphics-programming-guide-effects-create.md)
-   [Impostare lo stato dell'effetto (Direct3D 10)](d3d10-graphics-programming-guide-effects-set-state.md)
-   [Applicare una tecnica (Direct3D 10)](d3d10-graphics-programming-guide-effects-apply-technique.md)

Naturalmente, esistono [considerazioni sulle prestazioni](d3d10-graphics-programming-guide-effects-performance.md) per l'utilizzo di effetti. Queste considerazioni sono in gran parte identiche se non si utilizza un effetto. Come, ridurre al minimo la quantità di modifiche di stato o organizzare le variabili che devono essere aggiornate in base alla frequenza. Queste tattiche vengono usate per ridurre al minimo la quantità di dati che devono essere inviati dalla CPU alla GPU e quindi ridurre al minimo i potenziali problemi di sincronizzazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



