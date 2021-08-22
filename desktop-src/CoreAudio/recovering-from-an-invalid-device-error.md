---
description: Ripristino da un errore Invalid-Device errore
ms.assetid: 1f5c3458-70ca-45ba-ac33-5c7b9f092320
title: Ripristino da un errore Invalid-Device errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9f56972aeeae5cfb370a656a621c6b6e206f8caa115bec33203cab7eded3e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318561"
---
# <a name="recovering-from-an-invalid-device-error"></a>Ripristino da un errore Invalid-Device errore

Molti dei metodi in WASAPI restituiscono il codice di errore AUDCLNT E DEVICE INVALIDATED se il dispositivo endpoint audio in uso dall'applicazione \_ client non è più \_ \_ valido. Questo codice di errore indica che il dispositivo endpoint è stato scollegato o che l'hardware audio o le risorse hardware associate sono stati riconfigurati, disabilitati, rimossi o altrimenti resi non disponibili per l'uso. Spesso l'applicazione può eseguire il ripristino da questo errore.

>[!NOTE]
> Per informazioni sul ripristino da errori di dispositivo non validi quando si usano API audio spaziali (ISAC), vedere Ripristino da un errore di Invalid-Device [(audio spaziale)](recovering-from-an-invalid-device-error-spatial-sound.md)

La strategia che un'applicazione deve usare per il ripristino da un errore AUDCLNT E DEVICE INVALIDATED dipende dalla tecnica seguente che l'applicazione usa per selezionare un \_ \_ dispositivo endpoint \_ audio:

-   Selezionare sempre il dispositivo di acquisizione o rendering audio predefinito.
-   Selezionare un dispositivo endpoint audio specifico.

Nel secondo caso, l'applicazione seleziona automaticamente un dispositivo specifico in base ai requisiti interni o consente all'utente di selezionare in modo esplicito un dispositivo da un elenco di dispositivi disponibili.

Un'applicazione che usa il dispositivo predefinito può tentare di eseguire il ripristino da un errore AUDCLNT \_ E \_ DEVICE \_ INVALIDATED come indicato di seguito:

1.  Rilasciare [**l'interfaccia IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) e qualsiasi altra interfaccia WASAPI acquisita nel dispositivo.
2.  Chiamare il [**metodo IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) per ottenere il dispositivo audio predefinito corrente.
3.  Provare ad attivare [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) nel dispositivo audio predefinito.

Seguendo i passaggi precedenti, l'applicazione tende a rispondere in modo appropriato indipendentemente dalla causa dell'errore AUDCLNT \_ E \_ DEVICE \_ INVALIDATED. Se la riconfigurazione del dispositivo predefinito ha causato l'errore (ad esempio, se l'utente ha modificato il formato di flusso usato dal dispositivo), questi passaggi, se hanno esito positivo, consentono all'applicazione di continuare a usare lo stesso dispositivo. Se l'utente ha disabilitato o rimosso il dispositivo in uso dall'applicazione ed è disponibile un altro dispositivo per assumere il ruolo di dispositivo predefinito, l'applicazione può continuare a usare il nuovo dispositivo predefinito. In entrambi i casi, l'applicazione si adatta automaticamente senza richiedere l'intervento dell'utente.

Un'applicazione che seleziona un dispositivo specifico può tentare di eseguire il ripristino dall'errore AUDCLNT \_ E \_ DEVICE \_ INVALIDATED come indicato di seguito:

1.  Rilasciare [**l'interfaccia IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) e qualsiasi altra interfaccia WASAPI acquisita nel dispositivo.
2.  Provare ad attivare [**un'interfaccia IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) nello stesso dispositivo.
3.  Se il passaggio 2 ha esito negativo, l'applicazione può, come opzione, richiedere all'utente di selezionare un altro dispositivo.

Il passaggio 2 può avere esito positivo se il dispositivo usato dall'applicazione è stato riconfigurato ma non disabilitato o rimosso. In caso di esito positivo, il passaggio 2 consente all'applicazione di continuare automaticamente a usare lo stesso dispositivo senza richiedere l'intervento dell'utente. Il passaggio 3 è appropriato se l'applicazione consente all'utente di selezionare in modo esplicito un altro dispositivo dopo che l'utente ha disabilitato o rimosso il dispositivo usato in precedenza.

Un'applicazione può determinare più precisamente la causa di un errore del dispositivo non valido registrando per ricevere una notifica quando una sessione perde la connessione a un dispositivo. Per abilitare questa notifica, l'applicazione implementa [**un'interfaccia IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) e chiama il metodo [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) per registrare l'interfaccia. Quando un errore di dispositivo non valido causa la disconnessione della sessione, WASAPI chiama il metodo [**IAudioSessionEvents::OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) nell'interfaccia registrata. Tramite questo metodo, WASAPI informa l'applicazione del motivo della disconnessione. In Windows Vista la **chiamata OnSessionDisconnected** identifica i motivi seguenti:

-   L'utente ha rimosso il dispositivo endpoint audio.
-   Il Windows audio è stato arrestato.
-   Il formato di flusso preferito è stato modificato per il dispositivo a cui è connessa la sessione audio.
-   L'utente ha disconnesso la sessione Terminale Windows Services (WTS) in cui era in esecuzione la sessione audio. Per altre informazioni sulle sessioni WTS, vedere la documentazione Windows SDK.
-   La WTS sessione audio in cui era in esecuzione è stata disconnessa.
-   La sessione audio (modalità condivisa) è stata disconnessa per rendere disponibile il dispositivo endpoint audio per una connessione in modalità esclusiva.

In risposta all'evento di disconnessione, WASAPI chiude tutti i flussi che appartengono alla sessione. Se un'applicazione tenta successivamente di accedere a un flusso chiuso tramite un metodo WASAPI, ad esempio [**IAudioClient::GetCurrentPadding,**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)il metodo ha esito negativo e restituisce il codice di errore AUDCLNT \_ E DEVICE \_ \_ INVALIDATED.

Un altro vantaggio della ricezione di notifiche tramite [**l'interfaccia IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) è che le notifiche arrivano in modo asincrono. Pertanto, anche quando il flusso non è in esecuzione, l'applicazione riceverà comunque una notifica in tempo reale degli errori del dispositivo non valido che possono impedire l'esecuzione del flusso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei flussi](stream-management.md)
</dt> </dl>

 

 



