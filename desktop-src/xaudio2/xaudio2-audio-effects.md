---
description: Un effetto audio è un oggetto che accetta i dati audio in ingresso ed esegue un'operazione sui dati prima di passarlo. È possibile usare un effetto per eseguire un'ampia gamma di attività, tra cui l'aggiunta di riverbero a un flusso audio e il monitoraggio dei livelli di volume di picco.
ms.assetid: 8c3fa4ca-dcff-bd23-7220-7d0aeb6c6068
title: Effetti audio di XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886edb81718f772f7dec31f799b1612ca701c2327468ad554fe80a17c1f69ec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082855"
---
# <a name="xaudio2-audio-effects"></a>Effetti audio di XAudio2

Un effetto audio è un oggetto che accetta i dati audio in ingresso ed esegue un'operazione sui dati prima di passarlo. È possibile usare un effetto per eseguire un'ampia gamma di attività, tra cui l'aggiunta di riverbero a un flusso audio e il monitoraggio dei livelli di volume di picco.

## <a name="effect-chains"></a>Catene di effetti

Qualsiasi voce XAudio2 può ospitare una catena di effetti audio. È possibile usare una matrice di [**strutture XAUDIO2 \_ EFFECT \_ DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) per specificare le catene di effetti. Ogni descrittore contiene un puntatore a un oggetto effetto fornito dal client. Questi oggetti devono implementare le interfacce APO (Audio Processing Object). Per altre informazioni sul modello APO, vedere Panoramica di [XAPO.](xapo-overview.md)

Le catene di effetti possono essere modificate dinamicamente dal client (mentre il motore XAudio2 è in esecuzione), gli effetti possono essere abilitati o disabilitati singolarmente e i parametri degli effetti possono essere modificati, il tutto senza interruzioni dell'audio. Ogni volta che un aspetto del grafico degli effetti cambia, XAudio2 ottimizza nuovamente il grafico per evitare elaborazioni non necessarie. Vedere [**IXAudio2Voice::SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), [**IXAudio2Voice::EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)e [**IXAudio2Voice::SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters).

Dopo che un effetto è stato collegato a una voce XAudio2, XAudio2 assume il controllo dell'effetto e il client non deve effettuare altre chiamate. Il modo più semplice per garantire questa operazione è rilasciare tutti i puntatori all'effetto.

Gli effetti in una determinata catena di effetti della voce XAudio2 devono utilizzare e produrre audio a virgola mobile alla frequenza di campionamento di elaborazione di tale voce. L'unico aspetto del formato audio che possono modificare è il numero di canali (ad esempio, un effetto riverbero può convertire i dati mono in 5.1). Il client può usare il [**DESCRITTORE EFFETTO XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor).**Campo OutputChannels** per specificare il numero di canali che ogni effetto deve produrre. La catena di effetti ha esito negativo se uno degli effetti non soddisfa questi requisiti o se un effetto produce un numero di canali che l'effetto successivo non è in grado di gestire. Tutte le chiamate [**IXAudio2Voice::EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) o [**IXAudio2Voice::D isableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) che causano l'interruzione della catena di effetti a soddisfare questi requisiti avranno esito negativo.

Le interfacce APO usate in XAudio2 devono essere *distruttive.* Ciò significa che sovrascrivono sempre tutti i dati trovati nei buffer di output. In caso contrario, l'audio risultante potrebbe non essere corretto perché XAudio2 non garantisce che questi buffer siano stati inizializzati in precedenza con silenzio.

## <a name="xaudio2-built-in-effects"></a>Effetti predefiniti di XAudio2

La tabella seguente elenca il set di effetti audio predefiniti forniti da XAudio2 e i relativi metodi di creazione. 

| Effetto       | Metodo di creazione                                              |
|--------------|--------------------------------------------------------------|
| Riverbero       | [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)           |
| Contatore del volume | [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter) |



 

Per un esempio di creazione e uso di un'istanza di un effetto audio, vedere [Procedura: Creare una catena di effetti.](how-to--create-an-effect-chain.md)

## <a name="custom-effects-in-xaudio2"></a>Effetti personalizzati in XAudio2

[L'API XAPO](xapo-overview.md) fornisce un framework per la creazione di effetti audio personalizzati che è possibile usare in XAudio2. Per un esempio di creazione di un effetto personalizzato con XAPO, vedere [Procedura: Creare un effetto XAPO.](how-to--create-an-xapo.md)

## <a name="xapo-effect-library-xapofx"></a>Libreria degli effetti XAPO (XAPOFX)

[XAPOFX offre](xapofx-overview.md) una libreria aggiuntiva di XAPO e un meccanismo comune per crearli. Per un esempio dell'uso di XAPOFX con XAudio2, vedere [Procedura: Usare XAPOFX in XAudio2.](how-to--use-xapofx-in-xaudio2.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti audio](audio-effects.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> </dl>

 

 
