---
title: Rendering di un effetto (Direct3D 11)
description: Un effetto può essere utilizzato per archiviare le informazioni o per eseguire il rendering utilizzando un gruppo di stato.
ms.assetid: 7af239de-812d-4295-b599-b9deb371b01b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c99aef9f83cdf286e86ca843e57315d9ab88619
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399266"
---
# <a name="rendering-an-effect-direct3d-11"></a>Rendering di un effetto (Direct3D 11)

Un effetto può essere utilizzato per archiviare le informazioni o per eseguire il rendering utilizzando un gruppo di stato. Ogni tecnica specifica un set di vertex shader, Hull shader, Domain shader, geometry shader, pixel shader, compute shader, stato dello shader, campionatore e stato della trama, stato di visualizzazione di accesso non ordinato e altro stato della pipeline. Quindi, dopo avere organizzato lo stato in un effetto, è possibile incapsulare l'effetto di rendering risultante da tale stato creando ed eseguendo il rendering dell'effetto.

Sono necessari alcuni passaggi per preparare un effetto per il rendering. Il primo sta eseguendo la compilazione, che controlla HLSL come il codice rispetto alla sintassi del linguaggio HLSL e alle regole del Framework effetti. È possibile compilare un effetto dall'applicazione usando le chiamate API oppure è possibile compilare un effetto offline usando l'utilità del compilatore Effect [fxc.exe](/windows/desktop/direct3dtools/fxc). Una volta che l'effetto è stato compilato correttamente, crearlo chiamando un set di API diverso (ma molto simile).

Dopo aver creato l'effetto, per utilizzarlo sono necessari due passaggi. In primo luogo, è necessario inizializzare i valori dello stato dell'effetto (i valori delle variabili dell'effetto) usando diversi metodi per impostare lo stato se non sono inizializzati in HLSL. Per alcune variabili questa operazione può essere eseguita una volta quando viene creato un effetto; altri devono essere aggiornati ogni volta che l'applicazione chiama il ciclo di rendering. Una volta impostate le variabili di effetto, si indica al runtime di eseguire il rendering dell'effetto applicando una tecnica. Questi argomenti sono descritti in dettaglio più avanti.

Naturalmente, esistono considerazioni sulle prestazioni per l'utilizzo di effetti. Queste considerazioni sono in gran parte identiche se non si utilizza un effetto. Come ridurre al minimo la quantità di modifiche di stato e organizzare le variabili in base alla frequenza di aggiornamento. Queste tattiche vengono usate per ridurre al minimo la quantità di dati che devono essere inviati dalla CPU alla GPU e quindi ridurre al minimo i potenziali problemi di sincronizzazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Compilazione di un effetto](d3d11-graphics-programming-guide-effects-compile.md)<br/>         | Dopo aver creato un effetto, il passaggio successivo consiste nel compilare il codice per verificare la presenza di problemi di sintassi.<br/>                                                                                                                                                                                                          |
| [Creazione di un effetto](d3d11-graphics-programming-guide-effects-create.md)<br/>           | Un effetto viene creato caricando il bytecode degli effetti compilati nel Framework degli effetti. A differenza degli effetti 10, è necessario compilare l'effetto prima di creare l'effetto. Gli effetti caricati in memoria possono essere creati chiamando [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).<br/>                 |
| [Imposta stato effetto](d3d11-graphics-programming-guide-effects-set-state.md)<br/>        | È necessario inizializzare alcune costanti di effetto. Una volta inizializzato, lo stato dell'effetto viene impostato sul dispositivo per l'intero ciclo di rendering. È necessario aggiornare altre variabili ogni volta che viene chiamato il ciclo di rendering. Di seguito è riportato il codice di base per l'impostazione delle variabili di effetto, per ognuno dei tipi di variabili.<br/> |
| [Applicare una tecnica](d3d11-graphics-programming-guide-effects-apply-technique.md)<br/> | Con le costanti, le trame e lo stato dello shader dichiarati e inizializzati, l'unica cosa che rimane da fare è impostare lo stato dell'effetto nel dispositivo.<br/>                                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

