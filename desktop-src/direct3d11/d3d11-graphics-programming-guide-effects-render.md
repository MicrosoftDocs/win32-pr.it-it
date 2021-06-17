---
title: Rendering di un effetto (Direct3D 11)
description: Informazioni sul rendering di un effetto per Direct3D 11. Un effetto può essere usato per archiviare le informazioni o per eseguire il rendering usando un gruppo di stato.
ms.assetid: 7af239de-812d-4295-b599-b9deb371b01b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7def8f7bbfb9f2c7a5102eb8e02fc848155e4bde
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112261833"
---
# <a name="rendering-an-effect-direct3d-11"></a>Rendering di un effetto (Direct3D 11)

Un effetto può essere usato per archiviare le informazioni o per eseguire il rendering usando un gruppo di stato. Ogni tecnica specifica un set di vertex shader, hull shader, domain shader, geometry shader, pixel shader, compute shader, stato dello shader, campionatore e stato della trama, stato di visualizzazione di accesso non ordinato e altro stato della pipeline. Quindi, dopo aver organizzato lo stato in un effetto, è possibile incapsulare l'effetto di rendering che risulta da tale stato creando ed eseguendo il rendering dell'effetto.

Esistono alcuni passaggi per preparare un effetto per il rendering. Il primo è la compilazione, che controlla il codice HLSL come rispetto alla sintassi del linguaggio HLSL e alle regole del framework degli effetti. È possibile compilare un effetto dall'applicazione usando le chiamate API oppure è possibile compilare un effetto offline usando l'utilità del compilatore di [ effettifxc.exe](/windows/desktop/direct3dtools/fxc). Dopo aver compilato correttamente l'effetto, crearlo chiamando un set di API diverso (ma molto simile).

Dopo aver creato l'effetto, sono necessari due passaggi rimanenti per usarlo. Prima di tutto, è necessario inizializzare i valori dello stato dell'effetto (i valori delle variabili dell'effetto) usando diversi metodi per impostare lo stato se non vengono inizializzati in HLSL. Per alcune variabili questa operazione può essere eseguita una sola volta quando viene creato un effetto. altri devono essere aggiornati ogni volta che l'applicazione chiama il ciclo di rendering. Dopo aver impostato le variabili dell'effetto, si indica al runtime di eseguire il rendering dell'effetto applicando una tecnica. Questi argomenti sono tutti descritti in dettaglio più avanti.

Naturalmente, esistono considerazioni sulle prestazioni per l'uso degli effetti. Queste considerazioni sono in gran parte le stesse se non si usa un effetto. Come ridurre al minimo la quantità di modifiche dello stato e organizzare le variabili in base alla frequenza di aggiornamento. Queste tattiche vengono usate per ridurre al minimo la quantità di dati che devono essere inviati dalla CPU alla GPU e quindi ridurre al minimo i potenziali problemi di sincronizzazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Compilare un effetto](d3d11-graphics-programming-guide-effects-compile.md)<br/>         | Dopo aver creato un effetto, il passaggio successivo consiste nel compilare il codice per verificare la presenza di problemi di sintassi.<br/>                                                                                                                                                                                                          |
| [Creare un effetto](d3d11-graphics-programming-guide-effects-create.md)<br/>           | Un effetto viene creato caricando il bytecode dell'effetto compilato nel framework degli effetti. A differenza di Effects 10, l'effetto deve essere compilato prima di creare l'effetto. Gli effetti caricati in memoria possono essere creati chiamando [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).<br/>                 |
| [Impostare lo stato dell'effetto](d3d11-graphics-programming-guide-effects-set-state.md)<br/>        | Alcune costanti di effetto devono essere inizializzate. Dopo l'inizializzazione, lo stato dell'effetto viene impostato sul dispositivo per l'intero ciclo di rendering. È necessario aggiornare altre variabili ogni volta che viene chiamato il ciclo di rendering. Il codice di base per l'impostazione delle variabili di effetto è illustrato di seguito, per ognuno dei tipi di variabili.<br/> |
| [Applicare una tecnica](d3d11-graphics-programming-guide-effects-apply-technique.md)<br/> | Con le costanti, le trame e lo stato dello shader dichiarati e inizializzati, l'unica cosa da fare è impostare lo stato dell'effetto nel dispositivo.<br/>                                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

