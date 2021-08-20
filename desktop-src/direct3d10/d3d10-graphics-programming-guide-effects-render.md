---
description: Informazioni sul rendering di un effetto per Direct3D 10. Un effetto può essere usato per archiviare le informazioni o per eseguire il rendering usando un gruppo di stato.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Rendering di un effetto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fcee8c4f0056359416133bbfc852259843b15391a422c3cf12bdeff7c25157
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101531"
---
# <a name="rendering-an-effect-direct3d-10"></a>Rendering di un effetto (Direct3D 10)

Un effetto può essere usato per archiviare le informazioni o per eseguire il rendering usando un gruppo di stato. Ogni tecnica specifica vertex shader, geometry shader, pixel shader, stato dello shader, campionamento e stato della trama e altro stato della pipeline. Quindi, dopo aver organizzato lo stato in un effetto, è possibile incapsulare l'effetto di rendering che risulta da tale stato creando ed eseguendo il rendering dell'effetto.

Esistono alcuni passaggi per preparare un effetto per il rendering. Il primo è la compilazione, che controlla il codice HLSL come rispetto alla sintassi del linguaggio HLSL e alle regole del framework degli effetti. È possibile compilare un effetto dall'applicazione usando le chiamate API oppure è possibile compilare un effetto offline usando l'utilità del compilatore di effetti. Dopo aver compilato correttamente l'effetto, crearlo chiamando un set di API diverso (ma molto simile).

Dopo aver creato l'effetto, sono disponibili due passaggi rimanenti per usarlo. Prima di tutto, è necessario inizializzare i valori dello stato dell'effetto (i valori delle variabili dell'effetto) usando diversi metodi per l'impostazione dello stato. Per alcune variabili questa operazione può essere eseguita una sola volta quando viene creato un effetto. altri devono essere aggiornati ogni volta che l'applicazione chiama il ciclo di rendering. Dopo aver impostato le variabili dell'effetto, si indica al runtime di eseguire il rendering dell'effetto applicando una tecnica. Questi argomenti sono tutti descritti in dettaglio più avanti.

-   [Compilare un effetto (Direct3D 10)](d3d10-graphics-programming-guide-effects-compile.md)
-   [Creare un effetto (Direct3D 10)](d3d10-graphics-programming-guide-effects-create.md)
-   [Impostare lo stato dell'effetto (Direct3D 10)](d3d10-graphics-programming-guide-effects-set-state.md)
-   [Applicare una tecnica (Direct3D 10)](d3d10-graphics-programming-guide-effects-apply-technique.md)

Naturalmente, esistono considerazioni [sulle prestazioni per](d3d10-graphics-programming-guide-effects-performance.md) l'uso degli effetti. Queste considerazioni sono in gran parte le stesse se non si usa un effetto. Ad esempio, riducendo al minimo la quantità di modifiche dello stato o organizzando le variabili che devono essere aggiornate in base alla frequenza. Queste tattiche vengono usate per ridurre al minimo la quantità di dati che devono essere inviati dalla CPU alla GPU e quindi ridurre al minimo i potenziali problemi di sincronizzazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



