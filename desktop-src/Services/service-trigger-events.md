---
description: Un servizio può registrarsi per l'avvio o l'arresto quando si verifica un evento trigger.
ms.assetid: ca02a3ae-b16a-4427-b6db-b935c9cf23b3
title: Eventi trigger del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdefd94b7896936f7ab4fc014647b08470611573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317674"
---
# <a name="service-trigger-events"></a>Eventi trigger del servizio

Un servizio può registrarsi per l'avvio o l'arresto quando si verifica un evento trigger. In questo modo si elimina la necessità di avviare i servizi all'avvio del sistema o per i servizi per eseguire il polling o attendere attivamente un evento. un servizio può essere avviato quando necessario, anziché iniziare automaticamente indipendentemente dal fatto che esista o meno lavoro da eseguire. Esempi di eventi trigger predefiniti includono l'arrivo di un dispositivo di una classe di interfaccia del dispositivo specificata o la disponibilità di una determinata porta del firewall. Un servizio può inoltre registrarsi per un evento trigger personalizzato generato da un provider [Event Tracing for Windows](../etw/event-tracing-portal.md) (ETW).

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Gli eventi di attivazione del servizio non sono supportati fino a Windows Server 2008 R2 e Windows 7.

Un trigger è costituito da un tipo di evento trigger, da un sottotipo di evento trigger, dall'azione da intraprendere in risposta all'evento trigger e (per determinati tipi di eventi trigger) uno o più elementi di dati specifici del trigger. Il sottotipo e gli elementi di dati specifici del trigger specificano insieme le condizioni per la notifica al servizio dell'evento. Il formato di un elemento dati dipende dal tipo di evento trigger. un elemento dati può essere costituito da dati binari, una stringa o una multistringa. Le stringhe devono essere Unicode; Le stringhe ANSI non sono supportate.

Per eseguire la registrazione per gli eventi trigger, il servizio chiama [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) con le **informazioni sul trigger di configurazione del servizio \_ \_ \_** e fornisce una struttura di [**\_ \_ informazioni sul trigger del servizio**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info) . La struttura di **\_ \_ informazioni del trigger del servizio** punta a una matrice di strutture di [**\_ trigger del servizio**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger) , ognuna delle quali specifica un trigger.

L'azione del trigger specificata viene eseguita se la condizione del trigger è true all'avvio del sistema o se la condizione del trigger diventa true mentre il sistema è in esecuzione. Se, ad esempio, un servizio viene registrato per l'avvio quando è disponibile un determinato dispositivo, il servizio viene avviato all'avvio del sistema se il dispositivo è già collegato al computer; il servizio viene avviato all'arrivo del dispositivo se l'utente si connette al dispositivo mentre il sistema è in esecuzione.

Se un trigger include elementi di dati specifici del trigger, l'azione trigger viene eseguita solo se l'elemento di dati che accompagna l'evento trigger corrisponde a uno degli elementi di dati specificati dal servizio con il trigger. La corrispondenza dei dati binari viene eseguita tramite il confronto bit per bit. La corrispondenza di stringa non fa distinzione tra maiuscole e minuscole. Se l'elemento dati è una multistringa, tutte le stringhe nella multistringa devono corrispondere.

Quando un servizio viene avviato in risposta a un evento trigger, il servizio riceve **l' \_ \_ \_ argomento avviato del trigger di servizio** come *argv* \[ 1 \] nella funzione di callback [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) . *Argv* \[ 0 \] è sempre il nome breve del servizio.

Un servizio che registra per essere avviato in risposta a un evento trigger potrebbe arrestarsi dopo un timeout di inattività quando il servizio non è in grado di eseguire operazioni. Un servizio che si arresta autonomamente deve essere preparato a gestire le richieste di controllo **\_ \_ TRIGGEREVENT di controllo del servizio** che arrivano mentre il servizio si arresta automaticamente. Gestione controllo servizi invia una richiesta di controllo del controllo del **\_ \_ TRIGGEREVENT** ogni volta che si verifica un nuovo evento trigger quando il servizio si trova nello stato in esecuzione. Per evitare la perdita di eventi trigger, il servizio deve restituire l' **errore di \_ arresto \_ in \_ corso** per qualsiasi richiesta di controllo **TRIGGEREVENT del \_ controllo \_ del servizio** che arriva durante la transizione del servizio dall'esecuzione a arrestata. In questo modo si indica a SCM di accodare gli eventi trigger e attendere che il servizio entri nello stato interrotto. SCM esegue quindi l'azione associata all'evento trigger in coda, ad esempio l'avvio del servizio.

Quando il servizio è pronto per gestire di nuovo gli eventi trigger, imposta il **servizio \_ Accept \_ TRIGGEREVENT** nella relativa maschera accettata dai controlli in una chiamata a [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus). Questa operazione viene in genere eseguita quando il servizio chiama **SetServiceStatus** con il **servizio \_ in esecuzione**. SCM rilascia quindi una richiesta **di \_ controllo \_ del servizio TRIGGEREVENT** per ogni evento trigger in coda finché la coda non è vuota.

Un servizio che dispone di servizi dipendenti in esecuzione non può essere arrestato in risposta a un evento trigger.

Le richieste trigger-Start e trigger-stop non sono garantite in condizioni di memoria insufficiente.

Utilizzare la funzione [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) per recuperare la configurazione dell'evento trigger di un servizio.

Lo strumento SC (sc.exe) può essere utilizzato per configurare o eseguire query sugli eventi trigger di un servizio al prompt dei comandi. Usare l'opzione **Triggerinfo** per configurare un servizio per l'avvio o l'arresto in risposta a un evento trigger. Usare l'opzione **qtriggerinfo** per eseguire una query sulla configurazione del trigger di un servizio.

Nell'esempio seguente viene eseguita una query sulla configurazione del trigger del servizio W32Time, che viene configurata per l'avvio quando il computer viene aggiunto a un dominio e si arresta quando il computer esce dal dominio.

``` syntax
C:\>sc qtriggerinfo w32time
[SC] QueryServiceConfig2 SUCCESS

SERVICE_NAME: w32time

        START SERVICE
          DOMAIN JOINED STATUS         : 1ce20aba-9851-4421-9430-1ddeb766e809 [DOMAIN JOINED]
        STOP SERVICE
          DOMAIN JOINED STATUS         : ddaf516e-58c2-4866-9574-c3b615d42ea1 [NOT DOMAIN JOINED]
```

Nell'esempio seguente viene eseguita una query sulla configurazione del trigger del servizio di input del tablet, configurato per l'avvio quando un dispositivo HID con il **GUID** {4d1e55b2-f16f-11CF-88cb-001111000030} e uno degli ID dispositivo HID specificati arriva.

``` syntax
C:\>sc qtriggerinfo tabletinputservice
[SC] QueryServiceConfig2 SUCCESS

SERVICE_NAME: tabletinputservice

        START SERVICE
          DEVICE INTERFACE ARRIVAL     : 4d1e55b2-f16f-11cf-88cb-001111000030 [INTERFACE CLASS GUID]
            DATA                       : HID_DEVICE_UP:000D_U:0001
            DATA                       : HID_DEVICE_UP:000D_U:0002
            DATA                       : HID_DEVICE_UP:000D_U:0003
            DATA                       : HID_DEVICE_UP:000D_U:0004
```

 

 
