---
title: Servizi Desktop remoto funzioni API
description: Le funzioni seguenti vengono usate con Servizi Desktop remoto.
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5434f009d15bccc1db8279e576b71f079c8d73119a2d82bb8fd313dcc1837c47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000251"
---
# <a name="remote-desktop-services-api-functions"></a>Servizi Desktop remoto funzioni API

Le funzioni seguenti vengono usate con Servizi Desktop remoto.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

Recupera la Servizi Desktop remoto sessione associata a un processo specificato.

</dd> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dd>

Apre un handle per il server licenze Desktop remoto specificato.

</dd> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> <dd>

Chiude un handle aperto a un server Desktop remoto licenze.

</dd> <dt>

[**TLSGetServerCertificate**](tlsgetservercertificate.md)
</dt> <dd>

Restituisce il certificato del server Desktop remoto licenze.

</dd> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dd>

Inizia l'enumerazione tramite tutti i Key Pack installati in un server licenze Desktop remoto in base ai criteri di ricerca.

</dd> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> <dd>

Continua da una chiamata precedente alla [**funzione TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) e termina l'enumerazione.

</dd> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dd>

Continua da una chiamata precedente alla funzione [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) e restituisce il key pack successivo installato in un server licenze Desktop remoto che corrisponde ai criteri di ricerca.

</dd> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dd>

Inizia l'enumerazione delle licenze rilasciate dal server licenze Desktop remoto in base ai criteri di ricerca.

</dd> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> <dd>

Continua da una chiamata precedente alla [**funzione TLSLicenseEnumBegin**](tlslicenseenumbegin.md) e termina l'enumerazione.

</dd> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dd>

Continua da una chiamata precedente alla funzione [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) e restituisce la licenza successiva installata in un server licenze Desktop remoto che corrisponde ai criteri di ricerca.

</dd> <dt>

[**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

Chiude l'estremità client di un canale virtuale.

</dd> <dt>

[**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

Punto di ingresso definito dall'applicazione per la DLL lato client di un'applicazione che usa Servizi Desktop remoto canali virtuali.

</dd> <dt>

[**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

Inizializza l'accesso di una DLL client Servizi Desktop remoto canali virtuali.

</dd> <dt>

[*VirtualChannelInitEvent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

Funzione di callback definita dall'applicazione che Servizi Desktop remoto per notificare alla DLL client gli eventi del canale virtuale.

</dd> <dt>

[**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

Apre l'estremità client di un canale virtuale.

</dd> <dt>

[*VirtualChannelOpenEvent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

Funzione di callback definita dall'applicazione che Servizi Desktop remoto per notificare alla DLL client gli eventi per un canale virtuale specifico.

</dd> <dt>

[**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

Invia dati dall'estremità client di un canale virtuale a un'applicazione partner sul lato server.

</dd> <dt>

[**WTSCloseServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

Chiude un handle aperto a un Desktop remoto host sessione Desktop remoto.

</dd> <dt>

[**WTSConnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

Connette una Servizi Desktop remoto sessione a una sessione esistente nel computer locale.

</dd> <dt>

[**WTSCreateListener**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

Crea un nuovo listener Servizi Desktop remoto o configura un listener esistente.

</dd> <dt>

[**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

Disconnette l'utente connesso dal Servizi Desktop remoto sessione senza chiudere la sessione.

</dd> <dt>

[**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

Abilita o disabilita le [sessioni figlio.](child-sessions.md)

</dd> <dt>

[**WTSEnumerateListeners**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

Enumera tutti i listener Servizi Desktop remoto in un server Host sessione Desktop remoto.

</dd> <dt>

[**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

Recupera informazioni sui processi attivi in un server Host sessione Desktop remoto specificato.

</dd> <dt>

[**WTSEnumerateProcessesEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

Recupera informazioni sui processi attivi nel server Host sessione Desktop remoto o nel server Host Desktop remoto di virtualizzazione Desktop remoto specificato.

</dd> <dt>

[**WTSEnumerateServers**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateserversa)
</dt> <dd>

Restituisce un elenco di tutti i server Host sessione Desktop remoto all'interno del dominio specificato.

</dd> <dt>

[**WTSEnumerateSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)
</dt> <dd>

Recupera un elenco di sessioni in un server Host sessione Desktop remoto.

</dd> <dt>

[**WTSEnumerateSessionsEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa)
</dt> <dd>

Recupera un elenco di sessioni in un server Host sessione Desktop remoto o in un server Host di virtualizzazione Desktop remoto specificato.

</dd> <dt>

[**WTSFreeMemory**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

Libera la memoria allocata da una Servizi Desktop remoto funzione.

</dd> <dt>

[**WTSFreeMemoryEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

Libera memoria che contiene le [**WTS \_ PROCESS INFO \_ \_ EX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) o WTS [**SESSION INFO \_ \_ \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) allocate da una Servizi Desktop remoto funzione.

</dd> <dt>

[**WTSGetActiveConsoleSessionId**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

Recupera l'identificatore di sessione della sessione della console.

</dd> <dt>

[**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

Recupera l'identificatore di sessione figlio, se presente.

</dd> <dt>

[**WTSGetListenerSecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

Recupera il descrittore di sicurezza di Servizi Desktop remoto listener.

</dd> <dt>

[**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
</dt> <dd>

Determina se le sessioni figlio sono abilitate.

</dd> <dt>

[**WTSLogoffSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)
</dt> <dd>

Disconnette una sessione di Servizi Desktop remoto specificata.

</dd> <dt>

[**WTSOpenServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera)
</dt> <dd>

Apre un handle per il server Host sessione Desktop remoto specificato.

</dd> <dt>

[**WTSOpenServerEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenserverexa)
</dt> <dd>

Apre un handle per il server Host sessione Desktop remoto o il server Host di virtualizzazione Desktop remoto specificato.

</dd> <dt>

[**WTSQueryListenerConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

Recupera le informazioni di configurazione per Servizi Desktop remoto listener.

</dd> <dt>

[**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

Recupera le informazioni di sessione per la sessione specificata nel server Host sessione Desktop remoto specificato.

</dd> <dt>

[**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

Recupera le informazioni di configurazione per l'utente specificato nel controller di dominio specificato o nel server Host sessione Desktop remoto.

</dd> <dt>

[**WTSQueryUserToken**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryusertoken)
</dt> <dd>

Ottiene il token di accesso primario dell'utente connesso specificato dall'ID sessione.

</dd> <dt>

[**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dd>

Registra la finestra specificata per ricevere le notifiche di modifica della sessione.

</dd> <dt>

[**WTSRegisterSessionNotificationEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex)
</dt> <dd>

Registra la finestra specificata per ricevere le notifiche di modifica della sessione.

</dd> <dt>

[**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)
</dt> <dd>

Visualizza una finestra di messaggio sul desktop client di una sessione Servizi Desktop remoto specificata.

</dd> <dt>

[**WTSSetListenerSecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

Configura il descrittore di sicurezza di un listener Servizi Desktop remoto sicurezza.

</dd> <dt>

[**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

Modifica le informazioni di configurazione per l'utente specificato nel controller di dominio specificato o nel server Host sessione Desktop remoto.

</dd> <dt>

[**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

Arresta (e facoltativamente riavvia) il server Host sessione Desktop remoto specificato.

</dd> <dt>

[**WTSStartRemoteControlSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

Avvia il controllo remoto di un'altra Servizi Desktop remoto sessione. È necessario chiamare questa funzione da una sessione remota.

</dd> <dt>

[**WTSStopRemoteControlSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession)
</dt> <dd>

Arresta una sessione di controllo remoto.

</dd> <dt>

[**WTSTerminateProcess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)
</dt> <dd>

Termina il processo specificato nel server Host sessione Desktop remoto specificato.

</dd> <dt>

[**WTSUnRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> <dd>

Annulla la registrazione della finestra specificata in modo che non riceva altre notifiche di modifica della sessione.

</dd> <dt>

[**WTSUnRegisterSessionNotificationEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex)
</dt> <dd>

Annulla la registrazione della finestra specificata in modo che non riceva altre notifiche di modifica della sessione.

</dd> <dt>

[**WTSVirtualChannelClose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Chiude un handle di canale virtuale aperto.

</dd> <dt>

[**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)
</dt> <dd>

Apre un handle all'estremità server di un canale virtuale specificato.

</dd> <dt>

[**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

Crea un canale virtuale in modo simile a [**WTSVirtualChannelOpen.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Elimina tutti i dati di input in coda inviati dal client al server in un canale virtuale specificato.

</dd> <dt>

[**WTSVirtualChannelPurgeOutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Elimina tutti i dati di output in coda inviati dal server al client in un canale virtuale specificato.

</dd> <dt>

[**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

Restituisce informazioni su un canale virtuale specificato.

</dd> <dt>

[**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

Legge i dati dall'estremità del server di un canale virtuale.

</dd> <dt>

[**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

Scrive i dati sul server finale di un canale virtuale.

</dd> <dt>

[**WTSWaitSystemEvent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

Attende un evento Servizi Desktop remoto prima di tornare al chiamante.

</dd> </dl>

 

 