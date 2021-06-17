---
description: Informazioni sul rendering di un effetto per Direct3D 10. Un effetto può essere usato per archiviare le informazioni o per eseguire il rendering usando un gruppo di stato.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Rendering di un effetto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79db595585c6587648fba12afa5fbb22ff33e845
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262573"
---
# <a name="rendering-an-effect-direct3d-10"></a>Rendering di un effetto (Direct3D 10)

Un effetto può essere usato per archiviare le informazioni o per eseguire il rendering usando un gruppo di stato. Ogni tecnica specifica vertex shader, geometry shader, pixel shader, stato dello shader, stato del campionatore e della trama e altro stato della pipeline. Quindi, dopo aver organizzato lo stato in un effetto, è possibile incapsulare l'effetto di rendering che risulta da tale stato creando ed esegue il rendering dell'effetto.

Esistono alcuni passaggi per preparare un effetto per il rendering. Il primo è la compilazione, che controlla il codice simile a HLSL rispetto alla sintassi del linguaggio HLSL e alle regole del framework degli effetti. È possibile compilare un effetto dall'applicazione usando le chiamate API oppure è possibile compilare un effetto offline usando l'utilità del compilatore di effetti. Dopo aver compilato correttamente l'effetto, crearlo chiamando un set di API diverso (ma molto simile).

Dopo aver creato l'effetto, esistono due passaggi rimanenti per usarlo. In primo luogo, è necessario inizializzare i valori dello stato dell'effetto (i valori delle variabili dell'effetto) usando diversi metodi per impostare lo stato. Per alcune variabili questa operazione può essere eseguita una sola volta quando viene creato un effetto. altri devono essere aggiornati ogni volta che l'applicazione chiama il ciclo di rendering. Dopo aver impostato le variabili di effetto, si indica al runtime di eseguire il rendering dell'effetto applicando una tecnica. Questi argomenti vengono tutti discussi in dettaglio più avanti.

-   [Compilare un effetto (Direct3D 10)](d3d10-graphics-programming-guide-effects-compile.md)
-   [Creare un effetto (Direct3D 10)](d3d10-graphics-programming-guide-effects-create.md)
-   [Impostare lo stato dell'effetto (Direct3D 10)](d3d10-graphics-programming-guide-effects-set-state.md)
-   [Applicare una tecnica (Direct3D 10)](d3d10-graphics-programming-guide-effects-apply-technique.md)

Naturalmente, esistono considerazioni sulle [prestazioni per l'uso](d3d10-graphics-programming-guide-effects-performance.md) degli effetti. Queste considerazioni sono in gran parte le stesse se non si usa un effetto. Ad esempio, riducendo al minimo la quantità di modifiche di stato o organizzando le variabili che devono essere aggiornate in base alla frequenza. Queste tattiche vengono usate per ridurre al minimo la quantità di dati che devono essere inviati dalla CPU alla GPU e quindi ridurre al minimo i potenziali problemi di sincronizzazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



