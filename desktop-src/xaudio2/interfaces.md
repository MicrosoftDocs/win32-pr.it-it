---
title: Interfacce XAudio2
description: Questa sezione contiene informazioni sulle interfacce fornite dall'API Microsoft XAudio2.
ms.assetid: 96691e00-9ed0-b31c-fbe9-4daaba0daf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d9f2c777a7b98c5cbc78a130c0a1431be5971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234063"
---
# <a name="xaudio2-interfaces"></a>Interfacce XAudio2

Questa sezione contiene informazioni sulle interfacce fornite dall'API Microsoft XAudio2.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                               | Descrizione                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)<br/>                             | IXAudio2 è l'interfaccia per l'oggetto [XAudio2](xaudio2-apis-portal.md) che gestisce tutti gli Stati del motore audio, il thread di elaborazione audio, il grafico vocale e così via. <br/>                                                                                                                                                |
| [**IXAudio2Voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice)<br/>                   | [**IXAudio2Voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice) rappresenta l'interfaccia di base da cui derivano [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice), [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) e [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) . I metodi elencati di seguito sono comuni a tutte le sottoclassi vocali.<br/> |
| [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)<br/>       | Usare una voce di origine per inviare i dati audio alla pipeline di elaborazione XAudio2.<br/>                                                                                                                                                                                                                                                   |
| [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)<br/>       | Una voce submix viene utilizzata principalmente per i miglioramenti delle prestazioni e l'elaborazione degli effetti. <br/>                                                                                                                                                                                                                                        |
| [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)<br/> | Viene usata una voce di mastering per rappresentare il dispositivo di output audio.<br/>                                                                                                                                                                                                                                                               |
| [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)<br/> | L'interfaccia IXAudio2EngineCallback contiene metodi che inviano una notifica al client quando si verificano determinati eventi nel motore [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .<br/>                                                                                                                                                                           |
| [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback)<br/>   | L'interfaccia [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) contiene metodi che inviano una notifica al client quando si verificano determinati eventi in un determinato [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice). <br/>                                                                                                                       |
| [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo)<br/>                                   | Interfaccia per un oggetto di elaborazione audio da utilizzare in una catena di effetti XAudio2.<br/>                                                                                                                                                                                                                                        |
| [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)<br/>               | Interfaccia facoltativa che consente a un XAPO di utilizzare parametri specifici dell'effetto.<br/>                                                                                                                                                                                                                                                  |
| [**IXAPOHrtfParameters**](/windows/win32/api/hrtfapoapi/nn-hrtfapoapi-ixapohrtfparameters)<br/>       | Interfaccia utilizzata per impostare i parametri che controllano la modalità di applicazione della funzione di trasferimento correlata alla testa (HRTF) a un suono.<br/>                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione](programming-reference.md)
</dt> <dt>

[Guida di riferimento alla programmazione](./programming-reference.md)
</dt> </dl>

 

 
