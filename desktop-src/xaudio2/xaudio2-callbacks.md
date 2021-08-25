---
description: XAudio2 può chiamare le funzioni fornite dal client per notificare in modo asincrono determinati eventi che si verificano nel thread di elaborazione audio.
ms.assetid: 4fbd4229-f7ac-33b3-b4b7-f09150a60598
title: Callback di XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3377bd029cc2e21971748eaca7309dd44390a5bd3420d772c45264dfdbd075c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054291"
---
# <a name="xaudio2-callbacks"></a>Callback di XAudio2

XAudio2 può chiamare le funzioni fornite dal client per notificare in modo asincrono determinati eventi che si verificano nel thread di elaborazione audio. Questi callback possono essere globali o specifici di una determinata voce di origine. Per ricevere callback globali del motore, il client deve fornire un'istanza di una classe che implementa [**l'interfaccia IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) durante l'inizializzazione di XAudio2. Per ricevere i callback vocali di origine, il client deve fornire un'istanza di una classe che implementa [**l'interfaccia IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) durante la creazione di voci di origine. Per altri dettagli, vedere **IXAudio2EngineCallback** e **IXAudio2VoiceCallback.**

È necessario implementare i callback con attenzione per evitare di causare interruzioni nell'audio. Ogni volta che è in esecuzione un callback, XAudio2 non può generare audio. Ritardi superiori a pochi millisecondi possono causare un problema audio. Anche i ritardi di questo tipo generano l'output del debugger. Ciò indica potenziali problemi di prestazioni. Come minimo, le funzioni di callback non devono eseguire le operazioni seguenti:

-   Accedere al disco rigido o ad altre risorse di archiviazione permanenti
-   Effettuare chiamate API costose o bloccante
-   Eseguire la sincronizzazione con altre parti del codice client
-   Richiedere un utilizzo significativo della CPU

Se la progettazione client richiede un callback per attivare azioni come quelle elencate in precedenza, il callback deve segnalare a un thread client diverso di eseguire le operazioni. È possibile eseguire questa operazione con un semplice meccanismo **SetEvent** o meccanismi più sofisticati, ad esempio una coda di comandi non bloccante utilizzata da un altro thread.

## <a name="ixaudio2enginecallback"></a>IXAudio2EngineCallback

La [**classe IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) contiene metodi che notificano al client quando si verificano determinati eventi nel motore XAudio2. Questi metodi devono essere implementati dal client XAudio2. XAudio2 chiama questi metodi tramite un puntatore a interfaccia fornito dal client usando il [**metodo IXAudio2::RegisterForCallbacks.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) Tutti questi metodi **restituiscono void** anziché **HRESULT.**

## <a name="ixaudio2voicecallback"></a>IXAudio2VoiceCallback

La [**classe IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) contiene metodi che notificano al client quando si verificano determinati eventi in una voce di origine XAudio2 specifica. XAudio2 chiama questi metodi tramite un puntatore a interfaccia fornito dal client in [**IXAudio2::CreateSourceVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) Come con [**IXAudio2EngineCallback,**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)questi metodi devono essere implementati dal client XAudio2 e restituire **void** anziché **un HRESULT.**

Come accennato in precedenza, è fondamentale che le implementazioni fornite dal client di questi callback restituiranno il più rapidamente possibile, preferibilmente entro un millisecondo. I callback vengono eseguiti nel thread di elaborazione audio e tutta l'elaborazione viene interrotta fino alla fine del callback. Un ritardo in un callback può facilmente causare un problema audio.

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

 

 
