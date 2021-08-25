---
description: Specifica le caratteristiche che un client può assegnare a un flusso audio durante l'inizializzazione del flusso.
ms.assetid: 7b2267c3-79f5-4ada-a7ce-78dd514f8487
title: AUDCLNT_STREAMFLAGS_XXX costanti (Audiosessiontypes.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84817607092c179286f47eb35ef51f5e0f82d44211bcd2345ca3d27ee06b0e13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407364"
---
# <a name="audclnt_streamflags_xxx-constants"></a>Costanti AUDCLNT \_ STREAMFLAGS \_ XXX

Specifica le caratteristiche che un client può assegnare a un flusso audio durante l'inizializzazione del flusso.



| Costante/valore                                                                                                                                                                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_STREAMFLAGS_CROSSPROCESS"></span><span id="audclnt_streamflags_crossprocess"></span><dl> <dt>**AUDCLNT \_ FLUSSOFLAGS \_ CROSSPROCESS**</dt> <dt>0x00010000</dt> </dl>                                       | Il flusso audio sarà un membro di una sessione audio multi-processo. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_LOOPBACK"></span><span id="audclnt_streamflags_loopback"></span><dl> <dt>**AUDCLNT \_ FLUSSOFLAGS \_ LOOPBACK**</dt> <dt>0x00020000</dt> </dl>                                                   | Il flusso audio funzionerà in modalità loopback. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                                                                                      |
| <span id="AUDCLNT_STREAMFLAGS_EVENTCALLBACK"></span><span id="audclnt_streamflags_eventcallback"></span><dl> <dt>**AUDCLNT \_ 0X00040000 STREAMFLAGS \_ EVENTCALLBACK**</dt> <dt></dt> </dl>                                    | L'elaborazione del buffer audio da parte del client sarà basata su eventi. Per altre informazioni, vedere la sezione Osservazioni. <br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_NOPERSIST"></span><span id="audclnt_streamflags_nopersist"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ NOPERSIST**</dt> <dt>0x00080000</dt> </dl>                                                | Le impostazioni di volume e disattivazione dell'audio per una sessione audio non verranno mantenute tra i riavvii dell'applicazione. Per altre informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                                           |
| <span id="AUDCLNT_STREAMFLAGS_RATEADJUST"></span><span id="audclnt_streamflags_rateadjust"></span><dl> <dt>**AUDCLNT \_ FLUSSOFLAGS \_ RATEADJUST**</dt> <dt>0x00100000</dt> </dl>                                             | Questa costante è una novità in Windows 7. La frequenza di campionamento del flusso viene regolata in base a una frequenza specificata da un'applicazione. Per altre informazioni, vedere la sezione Osservazioni. <br/>                                                                                                                                                                                 |
| <span id="AUDCLNT_STREAMFLAGS_AUTOCONVERTPCM"></span><span id="audclnt_streamflags_autoconvertpcm"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM**</dt> <dt>0x80000000</dt> </dl>                                 | Un channel matrixer e un convertitore di frequenza di campionamento vengono inseriti in base alle esigenze per eseguire la conversione tra il formato non compresso fornito in [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) e il formato di combinazione del motore audio.<br/>                                                                                                            |
| <span id="AUDCLNT_STREAMFLAGS_SRC_DEFAULT_QUALITY"></span><span id="audclnt_streamflags_src_default_quality"></span><dl> <dt>**AUDCLNT \_ QUALITÀ PREDEFINITA STREAMFLAGS \_ SRC \_ \_ 0x08000000**</dt> <dt></dt> </dl>                | Se usato con **AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM,** viene usato un convertitore di frequenza di campionamento con una qualità migliore rispetto alla conversione predefinita, ma con un costo delle prestazioni superiore. Questa opzione deve essere usata se l'audio è destinato a essere udito dagli esseri umani invece che in altri scenari, ad esempio la pompa del silenzio o il popolamento di un contatore.<br/> |



## <a name="remarks"></a>Commenti

Il [**metodo IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) e la struttura [**DIRECTX AUDIO ACTIVATION \_ \_ \_ PARAMS**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) usano le costanti AUDCLNT \_ STREAMFLAGS \_ XXX.

Il \_ flag CROSSPROCESS STREAMFLAGS AUDCLNT indica che la sessione audio per il flusso \_ è una sessione tra processi. Una sessione tra processi può accettare flussi da più di un processo. Se due applicazioni in due processi distinti chiamano **IAudioClient::Initialize** con GUID di sessione identici ed entrambe le applicazioni impostano il flag CROSSPROCESS AUDCLNT SHAREMODE, il motore audio assegna i flussi alla stessa sessione tra \_ \_ processi. Questo flag esegue l'override del comportamento predefinito, ovvero l'assegnazione del flusso a una sessione specifica del processo anziché a una sessione tra processi. Il bit del flag CROSSPROCESS AUDCLNT \_ STREAMFLAGS \_ non è compatibile con la modalità esclusiva. Per altre informazioni sulle sessioni tra processi, vedere [Sessioni audio.](audio-sessions.md)

Il flag AUDCLNT \_ STREAMFLAGS LOOPBACK abilita \_ la registrazione loopback. Nella registrazione loopback, il motore audio copia il flusso audio riprodotto da un dispositivo endpoint di rendering in un buffer dell'endpoint audio in modo che un client [WASAPI](wasapi.md) possa acquisire il flusso. Se questo flag è impostato, il **metodo IAudioClient::Initialize** tenta di aprire un buffer di acquisizione nel dispositivo di rendering. Questo flag è valido solo per un dispositivo di rendering e solo se la **chiamata Initialize** imposta il *parametro ShareMode* su AUDCLNT \_ SHAREMODE \_ SHARED. In caso **contrario, la chiamata a Initialize** avrà esito negativo. Se la chiamata ha esito positivo, il client può chiamare il metodo [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) per ottenere [**un'interfaccia IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) nel dispositivo di rendering. Per altre informazioni, vedere [Registrazione loopback.](loopback-recording.md)

Il flag AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK abilita il buffering basato su eventi. Se un client imposta questo flag nella chiamata a **IAudioClient::Initialize** che inizializza un flusso, il client deve chiamare successivamente il metodo [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) per fornire un handle di evento per il flusso. Dopo l'avvio del flusso, il motore audio segnalerà l'handle di evento per notificare al client ogni volta che un buffer diventa pronto per l'elaborazione da parte del client. WASAPI supporta la memorizzazione nel buffer basata su eventi sia per i buffer di rendering che per i buffer di acquisizione. Sia i flussi in modalità condivisa che i flussi in modalità esclusiva possono usare la memorizzazione nel buffer basata su eventi. Per un esempio di codice che usa il flag EVENTCALLBACK AUDCLNT \_ STREAMFLAGS, vedere \_ [Exclusive-Mode Flussi](exclusive-mode-streams.md).

Il flag AUDCLNT \_ STREAMFLAGS NOPERSIST disabilita la persistenza delle impostazioni del volume e dell'audio per una sessione che \_ contiene flussi di rendering. Per impostazione predefinita, il livello del volume e lo stato di muting per una sessione di rendering sono persistenti tra i riavvii dell'applicazione. Il livello del volume e lo stato di muting per una sessione di acquisizione non sono mai persistenti. Per altre informazioni sulla persistenza delle impostazioni relative al volume e all'audio della sessione, vedere [Sessioni audio.](audio-sessions.md)

Il flag AUDCLNT STREAMFLAGS RATEADJUST consente a un'applicazione di ottenere un riferimento \_ \_ [**all'interfaccia IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment) usata per impostare la frequenza di campionamento per il flusso. Per ottenere un puntatore a questo interace, un'applicazione deve inizializzare il client audio con questo flag e quindi chiamare [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) specificando **l'identificatore \_ IAudioClockAdjustment IID.** Per impostare la nuova frequenza di campionamento, chiamare [**IAudioClockAdjustment::SetSampleRate**](/windows/desktop/api/audioclient/nf-audioclient-iaudioclockadjustment-setsamplerate). Questo flag è valido solo per un dispositivo di rendering. In caso contrario, **la chiamata a GetService** ha esito negativo con il codice di errore AUDCLNT \_ E WRONG ENDPOINT \_ \_ \_ TYPE. L'applicazione deve anche impostare il *parametro ShareMode* su AUDCLNT \_ SHAREMODE \_ SHARED durante la chiamata [**a Initialize.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) **SetSampleRate ha** esito negativo se il client audio non è in modalità condivisa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop vista \[ \| app UWP\]<br/>                                          |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 \[ \| app UWP\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Audiosessiontypes.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti audio principali](core-audio-constants.md)
</dt> <dt>

[**Interfaccia IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)
</dt> <dt>

[**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
</dt> <dt>

[**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)
</dt> <dt>

[**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle)
</dt> </dl>

 

 




