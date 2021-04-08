---
title: Funzioni API Servizi Desktop remoto
description: Con Servizi Desktop remoto vengono utilizzate le funzioni seguenti.
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94a2168f5ad4501b9725b72923c98ea97cc707c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727978"
---
# <a name="remote-desktop-services-api-functions"></a>Funzioni API Servizi Desktop remoto

Con Servizi Desktop remoto vengono utilizzate le funzioni seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

Recupera la sessione di Servizi Desktop remoto associata a un processo specificato.

</dd> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dd>

Apre un handle per il server licenze Desktop remoto specificato.

</dd> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> <dd>

Chiude un handle aperto per un server licenze Desktop remoto.

</dd> <dt>

[**TLSGetServerCertificate**](tlsgetservercertificate.md)
</dt> <dd>

Restituisce il certificato del server licenze Desktop remoto.

</dd> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dd>

Inizia l'enumerazione tramite tutti i Key Pack installati in un server licenze Desktop remoto in base ai criteri di ricerca.

</dd> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> <dd>

Continua da una precedente chiamata alla funzione [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) e termina l'enumerazione.

</dd> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dd>

Continua da una precedente chiamata alla funzione [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) e restituisce il key pack successivo installato in un server licenze Desktop remoto corrispondente ai criteri di ricerca.

</dd> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dd>

Inizia l'enumerazione delle licenze rilasciate dal server licenze Desktop remoto in base ai criteri di ricerca.

</dd> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> <dd>

Continua da una precedente chiamata alla funzione [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) e termina l'enumerazione.

</dd> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dd>

Continua da una precedente chiamata alla funzione [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) e restituisce la licenza successiva installata in un server licenze Desktop remoto corrispondente ai criteri di ricerca.

</dd> <dt>

[**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

Chiude l'estremità client di un canale virtuale.

</dd> <dt>

[**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

Un punto di ingresso definito dall'applicazione per la DLL sul lato client di un'applicazione che usa Servizi Desktop remoto canali virtuali.

</dd> <dt>

[**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

Inizializza un accesso della DLL client ai canali virtuali Servizi Desktop remoto.

</dd> <dt>

[*VirtualChannelInitEvent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

Funzione di callback definita dall'applicazione che Servizi Desktop remoto chiama per notificare la DLL client degli eventi del canale virtuale.

</dd> <dt>

[**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

Apre l'estremità client di un canale virtuale.

</dd> <dt>

[*VirtualChannelOpenEvent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

Funzione di callback definita dall'applicazione che Servizi Desktop remoto chiama per notificare alla DLL del client gli eventi per un canale virtuale specifico.

</dd> <dt>

[**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

Invia i dati dall'estremità client di un canale virtuale a un'applicazione partner sul lato server.

</dd> <dt>

[**WTSCloseServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

Chiude un handle aperto per un server di host sessione Desktop remoto (host sessione Desktop remoto).

</dd> <dt>

[**WTSConnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

Connette una sessione di Servizi Desktop remoto a una sessione esistente nel computer locale.

</dd> <dt>

[**WTSCreateListener**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

Crea un nuovo listener di Servizi Desktop remoto o configura un listener esistente.

</dd> <dt>

[**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

Disconnette l'utente connesso dalla sessione di Servizi Desktop remoto specificata senza chiudere la sessione.

</dd> <dt>

[**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

Abilita o Disabilita le [sessioni figlio](child-sessions.md).

</dd> <dt>

[**WTSEnumerateListeners**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

Enumera tutti i listener di Servizi Desktop remoto in un server Host sessione Desktop remoto.

</dd> <dt>

[**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

Recupera le informazioni sui processi attivi in un server Host sessione Desktop remoto specificato.

</dd> <dt>

[**WTSEnumerateProcessesEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

Recupera le informazioni sui processi attivi nel server Host sessione Desktop remoto specificato o nel server Host di virtualizzazione Desktop remoto (host di virtualizzazione Desktop remoto).

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

Recupera un elenco di sessioni in un server Host sessione Desktop remoto o in un server host di virtualizzazione Desktop remoto specificato.

</dd> <dt>

[**WTSFreeMemory**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

Libera la memoria allocata da una funzione Servizi Desktop remoto.

</dd> <dt>

[**WTSFreeMemoryEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

Libera la memoria che contiene le strutture delle informazioni di [**sessione WTS o WTS \_ \_ \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) allocate da una funzione Servizi Desktop remoto. [**\_ \_ \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)

</dd> <dt>

[**WTSGetActiveConsoleSessionId**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

Recupera l'identificatore di sessione della sessione della console.

</dd> <dt>

[**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

Recupera l'identificatore della sessione figlio, se presente.

</dd> <dt>

[**WTSGetListenerSecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

Recupera il descrittore di sicurezza di un listener di Servizi Desktop remoto.

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

Apre un handle per il server Host sessione Desktop remoto o il server host di virtualizzazione Desktop remoto specificato.

</dd> <dt>

[**WTSQueryListenerConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

Recupera le informazioni di configurazione per un listener di Servizi Desktop remoto.

</dd> <dt>

[**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

Recupera le informazioni sulla sessione per la sessione specificata nel server Host sessione Desktop remoto specificato.

</dd> <dt>

[**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

Recupera le informazioni di configurazione per l'utente specificato nel controller di dominio o nel server Host sessione Desktop remoto specificati.

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

Visualizza una finestra di messaggio sul desktop client di una sessione di Servizi Desktop remoto specificata.

</dd> <dt>

[**WTSSetListenerSecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

Configura il descrittore di sicurezza di un listener di Servizi Desktop remoto.

</dd> <dt>

[**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

Modifica le informazioni di configurazione per l'utente specificato nel server Host sessione Desktop remoto o nel controller di dominio specificato.

</dd> <dt>

[**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

Arresta (e, facoltativamente, riavvia) il server Host sessione Desktop remoto specificato.

</dd> <dt>

[**WTSStartRemoteControlSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

Avvia il controllo remoto di un'altra sessione di Servizi Desktop remoto. È necessario chiamare questa funzione da una sessione remota.

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

Annulla la registrazione della finestra specificata in modo che non riceva ulteriori notifiche di modifica della sessione.

</dd> <dt>

[**WTSUnRegisterSessionNotificationEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex)
</dt> <dd>

Annulla la registrazione della finestra specificata in modo che non riceva ulteriori notifiche di modifica della sessione.

</dd> <dt>

[**WTSVirtualChannelClose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Chiude un handle di canale virtuale aperto.

</dd> <dt>

[**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)
</dt> <dd>

Apre un handle per la fine del server di un canale virtuale specificato.

</dd> <dt>

[**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

Crea un canale virtuale in modo analogo a [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Elimina tutti i dati di input in coda inviati dal client al server su un canale virtuale specificato.

</dd> <dt>

[**WTSVirtualChannelPurgeOutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Elimina tutti i dati di output in coda inviati dal server al client su un canale virtuale specificato.

</dd> <dt>

[**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

Restituisce informazioni su un canale virtuale specificato.

</dd> <dt>

[**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

Legge i dati dall'estremità server di un canale virtuale.

</dd> <dt>

[**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

Scrive i dati nell'entità finale del server di un canale virtuale.

</dd> <dt>

[**WTSWaitSystemEvent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

Attende un evento Servizi Desktop remoto prima di tornare al chiamante.

</dd> </dl>

 

 