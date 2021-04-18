---
description: Un effetto audio è un oggetto che accetta i dati audio in ingresso ed esegue alcune operazioni sui dati prima di passarli. È possibile usare un effetto per eseguire un'ampia gamma di attività, tra cui l'aggiunta di un riverbero a un flusso audio e il monitoraggio dei livelli di picco del volume.
ms.assetid: 8c3fa4ca-dcff-bd23-7220-7d0aeb6c6068
title: Effetti audio di XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8de87a65ea4321b5e8d73a837f79a3e56e8e3a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307938"
---
# <a name="xaudio2-audio-effects"></a>Effetti audio di XAudio2

Un effetto audio è un oggetto che accetta i dati audio in ingresso ed esegue alcune operazioni sui dati prima di passarli. È possibile usare un effetto per eseguire un'ampia gamma di attività, tra cui l'aggiunta di un riverbero a un flusso audio e il monitoraggio dei livelli di picco del volume.

## <a name="effect-chains"></a>Catene di effetti

Qualsiasi voce XAudio2 può ospitare una catena di effetti audio. È possibile usare una matrice di strutture del [**\_ \_ descrittore dell'effetto XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) per specificare le catene di effetti. Ogni descrittore contiene un puntatore a un oggetto effetto fornito dal client. Questi oggetti devono implementare le interfacce APO (Audio Processing Object). Per ulteriori informazioni sul modello APO, vedere [Panoramica di XAPO](xapo-overview.md) .

Le catene di effetti possono essere modificate dal client in modo dinamico (mentre il motore XAudio2 è in esecuzione), gli effetti possono essere abilitati o disabilitati singolarmente ed è possibile modificare i parametri degli effetti, senza interruzioni dell'audio. Ogni volta che viene modificato un aspetto del grafico effetti, XAudio2 ottimizza nuovamente il grafo per evitare l'elaborazione non necessaria. Vedere [**IXAudio2Voice:: SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), [**IXAudio2Voice:: EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)e [**IXAudio2Voice:: SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters).

Dopo che un effetto è stato associato a una voce XAudio2, XAudio2 prende il controllo dell'effetto e il client non deve effettuare altre chiamate. Il modo più semplice per garantire questo problema consiste nel rilasciare tutti i puntatori all'effetto.

Gli effetti di una determinata catena di effetti della voce XAudio2 devono usare e produrre audio a virgola mobile alla frequenza di campionamento di elaborazione di tale voce. L'unico aspetto del formato audio che può cambiare è il numero di canali (ad esempio, un effetto di riverbero può convertire i dati mono in 5,1). Il client può usare il [**\_ \_ descrittore dell'effetto XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor).**Campo OutputChannels** per specificare il numero di canali che ogni effetto deve produrre. La catena di effetti ha esito negativo se uno degli effetti non è in grado di soddisfare questi requisiti o se un effetto produce un numero di canali che non possono essere gestiti dall'effetto successivo. Tutte le chiamate a [**IXAudio2Voice:: EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) o [**IXAudio2Voice::D isableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) che comportano l'arresto della catena di effetti che soddisfano questi requisiti avranno esito negativo.

Le interfacce APO usate in XAudio2 devono essere *distruttive*. Ciò significa che sovrascriveranno sempre tutti i dati trovati nei buffer di output. In caso contrario, l'audio risultante potrebbe non essere corretto perché XAudio2 non garantisce che questi buffer siano stati inizializzati in precedenza con il silenzio.

## <a name="xaudio2-built-in-effects"></a>Effetti predefiniti di XAudio2

La tabella seguente elenca il set di effetti audio predefiniti forniti da XAudio2 e i relativi metodi di creazione. 

| Effetto       | Metodo di creazione                                              |
|--------------|--------------------------------------------------------------|
| Riverbero       | [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)           |
| Misuratore volume | [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter) |



 

Per un esempio di creazione e uso di un'istanza di un effetto audio, vedere [procedura: creare una catena di effetti](how-to--create-an-effect-chain.md).

## <a name="custom-effects-in-xaudio2"></a>Effetti personalizzati in XAudio2

L'API [XAPO](xapo-overview.md) fornisce un Framework per la creazione di effetti audio personalizzati che è possibile usare in XAudio2. Per un esempio di creazione di un effetto personalizzato con XAPO, vedere [procedura: creare un XAPO](how-to--create-an-xapo.md).

## <a name="xapo-effect-library-xapofx"></a>Libreria effetti XAPO (XAPOFX)

[XAPOFX](xapofx-overview.md) fornisce una libreria aggiuntiva di XAPOs e un meccanismo comune per crearli. Per un esempio dell'uso di XAPOFX con XAudio2, vedere [procedura: Usare XAPOFX in XAudio2](how-to--use-xapofx-in-xaudio2.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti audio](audio-effects.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> </dl>

 

 
