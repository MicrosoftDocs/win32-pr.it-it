---
description: Specifica le caratteristiche che un client può assegnare a un flusso audio durante l'inizializzazione del flusso.
ms.assetid: 7b2267c3-79f5-4ada-a7ce-78dd514f8487
title: Costanti AUDCLNT_STREAMFLAGS_XXX (Audiosessiontypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65faf887c35b4ce1110cecb7d7509eb3dfda1d57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126907"
---
# <a name="audclnt_streamflags_xxx-constants"></a>\_Costanti AUDCLNT STREAMFLAGS \_ xxx

Specifica le caratteristiche che un client può assegnare a un flusso audio durante l'inizializzazione del flusso.



| Costante/valore                                                                                                                                                                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_STREAMFLAGS_CROSSPROCESS"></span><span id="audclnt_streamflags_crossprocess"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ CROSSPROCESS**</dt> <dt>0x00010000</dt> </dl>                                       | Il flusso audio sarà un membro di una sessione audio tra processi. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_LOOPBACK"></span><span id="audclnt_streamflags_loopback"></span><dl> <dt>**AUDCLNT \_ 0x00020000 \_ loopback STREAMFLAGS**</dt> <dt></dt> </dl>                                                   | Il flusso audio funzionerà in modalità loopback. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                                                                                      |
| <span id="AUDCLNT_STREAMFLAGS_EVENTCALLBACK"></span><span id="audclnt_streamflags_eventcallback"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK**</dt> <dt>0x00040000</dt> </dl>                                    | L'elaborazione del buffer audio da parte del client sarà basata sugli eventi. Per altre informazioni, vedere la sezione Osservazioni. <br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_NOPERSIST"></span><span id="audclnt_streamflags_nopersist"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ nopermanente**</dt> <dt>0x00080000</dt> </dl>                                                | Le impostazioni volume e mute per una sessione audio non vengono mantenute tra i riavvii dell'applicazione. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                                           |
| <span id="AUDCLNT_STREAMFLAGS_RATEADJUST"></span><span id="audclnt_streamflags_rateadjust"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ RATEADJUST**</dt> <dt>0x00100000</dt> </dl>                                             | Questa costante è una novità di Windows 7. La frequenza di campionamento del flusso viene regolata in base a una velocità specificata da un'applicazione. Per altre informazioni, vedere la sezione Osservazioni. <br/>                                                                                                                                                                                 |
| <span id="AUDCLNT_STREAMFLAGS_AUTOCONVERTPCM"></span><span id="audclnt_streamflags_autoconvertpcm"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM**</dt> <dt>0x80000000</dt> </dl>                                 | Per eseguire la conversione tra il formato non compresso fornito in [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) e il formato di combinazione del motore audio, vengono inseriti una matrice di canali e un convertitore di frequenza di campionamento.<br/>                                                                                                            |
| <span id="AUDCLNT_STREAMFLAGS_SRC_DEFAULT_QUALITY"></span><span id="audclnt_streamflags_src_default_quality"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ src \_ default \_ Quality**</dt> <dt>0x08000000</dt> </dl>                | Se usato con **AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM**, viene usato un convertitore di frequenza di campionamento con una qualità migliore rispetto alla conversione predefinita, ma con un costo di prestazioni superiore. Questa operazione deve essere usata se l'audio è in definitiva destinato a essere sentito dagli utenti e non ad altri scenari, ad esempio il pompaggio del silenzio o il popolamento di un contatore.<br/> |



## <a name="remarks"></a>Commenti

Il metodo [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) e la struttura di [**\_ \_ \_ parametri di attivazione audio DirectX**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) usano le \_ costanti AUDCLNT STREAMFLAGS \_ xxx.

Il \_ flag AUDCLNT STREAMFLAGS \_ CROSSPROCESS indica che la sessione audio per il flusso è una sessione tra processi. Una sessione tra processi può accettare flussi da più di un processo. Se due applicazioni in due processi distinti chiamano **IAudioClient:: Initialize** con GUID di sessione identici e entrambe le applicazioni impostano il \_ flag AUDCLNT SHAREMODE \_ CROSSPROCESS, il motore audio assegna i flussi alla stessa sessione tra processi. Questo flag sostituisce il comportamento predefinito, ovvero l'assegnazione del flusso a una sessione specifica del processo anziché una sessione tra processi. Il \_ bit del flag AUDCLNT STREAMFLAGS CROSSPROCESS non \_ è compatibile con la modalità esclusiva. Per ulteriori informazioni sulle sessioni tra processi, vedere [sessioni audio](audio-sessions.md).

Il \_ flag di loopback AUDCLNT STREAMFLAGS Abilita la \_ registrazione loopback. Nella registrazione loopback il motore audio copia il flusso audio che viene riprodotto da un dispositivo dell'endpoint di rendering in un buffer dell'endpoint audio, in modo che un client [WASAPI](wasapi.md) possa acquisire il flusso. Se questo flag è impostato, il metodo **IAudioClient:: Initialize** tenta di aprire un buffer di acquisizione sul dispositivo di rendering. Questo flag è valido solo per un dispositivo di rendering e solo se la chiamata **Initialize** imposta il parametro *SHAREMODE* su AUDCLNT \_ SHAREMODE \_ Shared. In caso contrario, la chiamata **Initialize** avrà esito negativo. Se la chiamata ha esito positivo, il client può chiamare il metodo [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) per ottenere un'interfaccia [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) sul dispositivo di rendering. Per altre informazioni, vedere [registrazione di loopback](loopback-recording.md).

Il \_ flag AUDCLNT STREAMFLAGS \_ EVENTCALLBACK Abilita il buffering basato sugli eventi. Se un client imposta questo flag nella chiamata a **IAudioClient:: Initialize** che Inizializza un flusso, il client deve chiamare successivamente il metodo [**IAudioClient:: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) per fornire un handle di evento per il flusso. Dopo l'avvio del flusso, il motore audio segnalerà l'handle dell'evento per notificare al client ogni volta che un buffer diventa pronto per l'elaborazione da parte del client. WASAPI supporta il buffering basato sugli eventi per i buffer di rendering e di acquisizione. Entrambi i flussi in modalità condivisa e in modalità esclusiva possono utilizzare il buffer basato sugli eventi. Per un esempio di codice che usa il \_ flag AUDCLNT STREAMFLAGS \_ EVENTCALLBACK, vedere [flussi in modalità esclusiva](exclusive-mode-streams.md).

Il \_ flag AUDCLNT STREAMFLAGS \_ nopersistetion Disabilita la persistenza delle impostazioni volume e mute per una sessione che contiene flussi di rendering. Per impostazione predefinita, il livello di volume e lo stato di muting per una sessione di rendering sono persistenti tra i riavvii dell'applicazione. Il livello del volume e lo stato di muting per una sessione di acquisizione non sono mai permanenti. Per ulteriori informazioni sulla persistenza delle impostazioni del volume e del silenziamento della sessione, vedere [sessioni audio](audio-sessions.md).

Il \_ flag AUDCLNT STREAMFLAGS \_ RATEADJUST consente a un'applicazione di ottenere un riferimento all'interfaccia [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment) utilizzata per impostare la frequenza di campionamento per il flusso. Per ottenere un puntatore a questo interfaccia, un'applicazione deve inizializzare il client audio con questo flag e quindi chiamare [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) specificando l'identificatore **IID \_ IAudioClockAdjustment** . Per impostare la nuova frequenza di campionamento, chiamare [**IAudioClockAdjustment:: Sesamplerate**](/windows/desktop/api/audioclient/nf-audioclient-iaudioclockadjustment-setsamplerate). Questo flag è valido solo per un dispositivo di rendering. In caso contrario, la chiamata **GetService** non riesce con il codice di errore AUDCLNT \_ E il tipo di \_ \_ endpoint errato \_ . L'applicazione deve inoltre impostare il parametro *SHAREMODE* su AUDCLNT \_ SHAREMODE \_ Shared durante la chiamata di [**inizializzazione**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) . **Sesamplerate** ha esito negativo se il client audio non è in modalità condivisa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                                          |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Audiosessiontypes. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti audio Core](core-audio-constants.md)
</dt> <dt>

[**Interfaccia IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)
</dt> <dt>

[**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
</dt> <dt>

[**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)
</dt> <dt>

[**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle)
</dt> </dl>

 

 




