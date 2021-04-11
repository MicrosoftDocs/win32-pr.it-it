---
description: XAudio2 può chiamare le funzioni fornite dal client per notificare in modo asincrono a determinati eventi che avvengono nel thread di elaborazione audio.
ms.assetid: 4fbd4229-f7ac-33b3-b4b7-f09150a60598
title: Callback di XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee191ad8c15d238a065c837c6fb192befbe7a51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349811"
---
# <a name="xaudio2-callbacks"></a>Callback di XAudio2

XAudio2 può chiamare le funzioni fornite dal client per notificare in modo asincrono a determinati eventi che avvengono nel thread di elaborazione audio. Questi callback possono essere globali o specifici di una determinata voce di origine. Per ricevere i callback del motore globale, il client deve fornire un'istanza di una classe che implementa l'interfaccia [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) durante l'inizializzazione di XAudio2. Per ricevere callback vocali di origine, il client deve fornire un'istanza di una classe che implementa l'interfaccia [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) durante la creazione di voci di origine. Per ulteriori informazioni, vedere **IXAudio2EngineCallback** e **IXAudio2VoiceCallback**.

È necessario implementare attentamente i callback per evitare di causare interruzioni nell'audio. Ogni volta che viene eseguito un callback, XAudio2 non può generare alcun audio. I ritardi di più di pochi millisecondi possono causare un problema audio. Anche i ritardi di questa natura generano l'output del debugger. Ciò indica i potenziali problemi di prestazioni. Come minimo, le funzioni di callback non devono eseguire le operazioni seguenti:

-   Accedere al disco rigido o ad altre archiviazioni permanenti
-   Eseguire chiamate API a costo elevato o di blocco
-   Sincronizzare con altre parti del codice client
-   Richiedi utilizzo CPU significativo

Se la progettazione client richiede un callback per attivare azioni come quelle elencate in precedenza, il callback deve segnalare a un thread client diverso di eseguire il lavoro. Questa operazione può essere eseguita con un semplice meccanismo **seevent** o con meccanismi più sofisticati come una coda di comandi non di blocco utilizzata da un altro thread.

## <a name="ixaudio2enginecallback"></a>IXAudio2EngineCallback

La classe [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) contiene metodi che inviano una notifica al client quando si verificano determinati eventi nel motore XAudio2. Questi metodi devono essere implementati dal client XAudio2. XAudio2 chiama questi metodi per mezzo di un puntatore a interfaccia fornito dal client usando il metodo [**IXAudio2:: RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) . Tutti questi metodi restituiscono **void** anziché un valore **HRESULT**.

## <a name="ixaudio2voicecallback"></a>IXAudio2VoiceCallback

La classe [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) contiene metodi che inviano una notifica al client quando si verificano determinati eventi in una specifica voce di origine XAudio2. XAudio2 chiama questi metodi per mezzo di un puntatore a interfaccia fornito dal client in [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice). Come per [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback), questi metodi devono essere implementati dal client XAudio2 e restituire **void** anziché un valore **HRESULT**.

Come indicato in precedenza, è fondamentale che le implementazioni fornite dal client di questi callback restituiscano il più rapidamente possibile, preferibilmente in un millisecondo. I callback vengono eseguiti nel thread di elaborazione audio e tutte le operazioni di elaborazione vengono interrotte fino a quando il callback non viene restituito. Un ritardo in un callback può causare facilmente un problema audio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Callback](callbacks.md)
</dt> <dt>

[Guida alla programmazione di XAudio2](programming-guide.md)
</dt> <dt>

[Procedura: Usare callback di voci di origine](how-to--use-source-voice-callbacks.md)
</dt> <dt>

[Procedura: Usare callback del motore](how-to--use-engine-callbacks.md)
</dt> <dt>

[Procedura: Trasmissione di un suono in un flusso da disco](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
