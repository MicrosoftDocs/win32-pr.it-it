---
description: Ripristino da un errore di Invalid-Device
ms.assetid: 1f5c3458-70ca-45ba-ac33-5c7b9f092320
title: Ripristino da un errore di Invalid-Device
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca20c32be46367f53a14ce26c39f980e3649b652
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127422"
---
# <a name="recovering-from-an-invalid-device-error"></a>Ripristino da un errore di Invalid-Device

Molti dei metodi in WASAPI restituiscono il codice di errore AUDCLNT \_ E \_ dispositivo \_ invalidato se il dispositivo dell'endpoint audio che l'applicazione client sta usando diventa non valido. Questo codice di errore indica che il dispositivo endpoint è stato scollegato o che l'hardware audio o le risorse hardware associate sono state riconfigurate, disabilitate, rimosse o rese non disponibili per l'utilizzo. Spesso l'applicazione può risolvere questo errore.

>[!NOTE]
> Per informazioni sul ripristino da errori di dispositivo non validi quando si usano le API ISAC (Spatial audio API), vedere [ripristino da un errore di Invalid-Device (audio spaziale)](recovering-from-an-invalid-device-error-spatial-sound.md)

La strategia che un'applicazione deve usare per eseguire il ripristino da \_ un \_ \_ errore invalidato del dispositivo AUDCLNT E dipende dalle tecniche seguenti utilizzate dall'applicazione per selezionare un dispositivo endpoint audio:

-   Selezionare sempre il dispositivo di acquisizione o il rendering audio predefinito.
-   Selezionare un dispositivo endpoint audio specifico.

Nel secondo caso, l'applicazione seleziona automaticamente un dispositivo specifico in base ai requisiti interni oppure consente all'utente di selezionare in modo esplicito un dispositivo da un elenco di dispositivi disponibili.

Un'applicazione che usa il dispositivo predefinito può tentare di eseguire il ripristino da \_ un \_ \_ errore invalidato del dispositivo AUDCLNT E come indicato di seguito:

1.  Rilasciare l'interfaccia [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) e tutte le altre interfacce WASAPI acquisite nel dispositivo.
2.  Chiamare il metodo [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) per ottenere il dispositivo audio predefinito corrente.
3.  Tentativo di attivare [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) sul dispositivo audio predefinito.

Seguendo i passaggi precedenti, l'applicazione tende a rispondere in modo appropriato, indipendentemente dalla cause dell' \_ \_ \_ errore invalidato del dispositivo AUDCLNT E. Se la riconfigurazione del dispositivo predefinito ha causato l'errore (ad esempio, se l'utente ha modificato il formato di flusso usato dal dispositivo), questi passaggi, se hanno esito positivo, consentono all'applicazione di continuare a usare lo stesso dispositivo. Se l'utente ha disabilitato o rimosso il dispositivo usato dall'applicazione e un altro dispositivo è disponibile per assumere il ruolo di dispositivo predefinito, l'applicazione può continuare usando il nuovo dispositivo predefinito. In entrambi i casi, l'applicazione si adatta automaticamente senza richiedere l'intervento dell'utente.

Un'applicazione che seleziona un dispositivo specifico può tentare di eseguire il ripristino dall' \_ \_ \_ errore invalidato del dispositivo AUDCLNT E come indicato di seguito:

1.  Rilasciare l'interfaccia [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) e tutte le altre interfacce WASAPI acquisite nel dispositivo.
2.  Tentativo di attivare un'interfaccia [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) sullo stesso dispositivo.
3.  Se il passaggio 2 ha esito negativo, l'applicazione può richiedere all'utente di selezionare un altro dispositivo.

Il passaggio 2 può avere esito positivo se il dispositivo utilizzato dall'applicazione è stato riconfigurato ma non disabilitato o rimosso. In caso di esito positivo, il passaggio 2 consente all'applicazione di continuare a usare automaticamente lo stesso dispositivo senza richiedere l'intervento dell'utente. Il passaggio 3 è appropriato se l'applicazione consente all'utente di selezionare in modo esplicito un altro dispositivo dopo che l'utente ha disabilitato o rimosso il dispositivo usato in precedenza.

Un'applicazione può determinare in modo più preciso la cause di un errore del dispositivo non valido eseguendo la registrazione per ricevere una notifica quando una sessione perde la connessione a un dispositivo. Per abilitare questa notifica, l'applicazione implementa un'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) e chiama il metodo [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) per registrare l'interfaccia. Quando un errore di dispositivo non valido causa la disconnessione della sessione, WASAPI chiama il metodo [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) nell'interfaccia registrata. Tramite questo metodo, WASAPI informa l'applicazione del motivo della disconnessione. In Windows Vista, la chiamata **OnSessionDisconnected** identifica i motivi seguenti:

-   L'utente ha rimosso il dispositivo dell'endpoint audio.
-   Il servizio audio Windows è stato arrestato.
-   Il formato di flusso preferito è stato modificato per il dispositivo a cui è connessa la sessione audio.
-   L'utente ha disconnesso la sessione Servizi terminal di Windows (WTS) in cui è in esecuzione la sessione audio. Per ulteriori informazioni sulle sessioni WTS, vedere la documentazione Windows SDK.
-   La sessione di WTS in cui è in esecuzione la sessione audio è stata disconnessa.
-   La sessione audio (modalità condivisa) è stata disconnessa per rendere disponibile il dispositivo dell'endpoint audio per una connessione in modalità esclusiva.

In risposta all'evento di disconnessione, WASAPI chiude tutti i flussi che appartengono alla sessione. Se un'applicazione tenta successivamente di accedere a un flusso chiuso tramite un metodo WASAPI, ad esempio [**IAudioClient:: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding), il metodo ha esito negativo e restituisce il codice di errore AUDCLNT \_ e il \_ dispositivo \_ invalidato.

Un ulteriore vantaggio della ricezione di notifiche tramite l'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) è che le notifiche arrivano in modo asincrono. Pertanto, anche quando il flusso non è in esecuzione, l'applicazione riceverà comunque una notifica tempestiva degli errori del dispositivo non validi che possono impedire l'esecuzione del flusso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei flussi](stream-management.md)
</dt> </dl>

 

 



