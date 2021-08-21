---
description: Il controllo genitori può essere esteso usando le IMPOSTAZIONI e le API di registrazione.
ms.assetid: f0fc1b11-6de4-48f6-afc9-f05c8812d2bd
title: Cenni preliminari sulle funzionalità di estendibilità di Controllo genitori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf609c08a4114d7d96ae600744879bda53ac483d90bcd25def3dd0d5f9e3c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971720"
---
# <a name="parental-controls-extensibility-features-overview"></a>Cenni preliminari sulle funzionalità di estendibilità di Controllo genitori

Il controllo genitori può essere esteso usando le IMPOSTAZIONI e le API di registrazione.

-   [Registrazione: in background](/windows)
-   [Estendibilità della registrazione](#logging-extensibility)
-   [Aggiunta del collegamento di estendibilità generale del pannello Controllo genitori](#parental-controls-panel-general-ui-extensibility-link-addition)
-   [Sostituzione filtro contenuto Web](#web-content-filter-replacement)

## <a name="loggingbackground"></a>Registrazione: in background

Microsoft ha definito una serie di eventi standard per affrontare le attività comuni:

-   Sistema: modifiche alle impostazioni di Controllo genitori, modifiche dell'account, modifica dell'orologio di sistema, tentativi di accesso non riusciti.
-   Utente:
    -   Limiti di sistema/ora: orari di accesso, disconnessione, tentativi di esecuzione dell'applicazione e durata dell'esecuzione dell'applicazione (vedere la nota).
    -   Restrizioni Web: siti Web visitati e bloccati, tentativi di download di file. Non è necessario che i Web browser e le applicazioni simili a browser registrino questi dati, come l'LSP filtro contenuto Web. I filtri Web sostitutivi devono generare questi eventi.
    -   Giochi: giochi giocati e bloccati, fine del gioco (gli eventi insieme forniscono la durata giocata).
    -   Consentire e bloccare programmi specifici: tentativo di esecuzione, arresto, blocco da restrizioni generali dell'applicazione.
    -   Messaggistica immediata: tentativo di avvio della conversione, tentativo di aggiunta alla conversazione, uscita conversazione, video/audio/gioco/servizio messaggi brevi/trasferimento file/funzionalità di scambio url, tentativo di modifica dell'elenco contatti.
    -   Posta elettronica: ricevuto o ricevuto bloccato, tentativo di invio, tentativo di modifica dell'elenco contatti.
    -   Elementi multimediali: contenuti multimediali riprodotti e tentati.

Non tutti gli eventi precedenti sono adatti per l'uso da parte delle applicazioni. Le modifiche dell'account, la modifica dell'orologio di sistema e la registrazione degli eventi di accesso e disconnessione vengono implementate solo dal sistema operativo e pertanto non vengono esposte pubblicamente.

> [!Note]  
> La strumentazione degli eventi di ingresso e uscita dell'applicazione è disponibile Windows Vista ed è configurata da Controllo genitori per registrare questi dati.

 

## <a name="logging-extensibility"></a>Estendibilità della registrazione

Un evento personalizzato generico viene definito anche con 3 tag/valori disponibili, quindi gli ISV in genere non dovranno definirne uno personalizzato in un manifesto. Log Viewer riconoscerà e visualizza le intestazioni e i valori dei tag se il numero di campi usati (da 1 a 3) e le intestazioni per ogni campo vengono registrati tramite l'API WMI. Il Visualizzatore eventi può essere usato anche per visualizzare eventi personalizzati.

Se l'evento personalizzato generico non è appropriato, un ISV può definirne uno personalizzato usando un manifesto dell'applicazione e può registrare intestazioni per un massimo di tre campi usando la stessa API WMI.

Gli ISV possono scegliere di definire i propri eventi e di utilizzarli indipendentemente dal Visualizzatore log tramite api Windows pubbliche. Questo non ha il vantaggio della centralizzazione completa dei log.

## <a name="parental-controls-panel-general-ui-extensibility-link-addition"></a>Aggiunta del collegamento di estendibilità generale del pannello Controllo genitori

Un collegamento di estendibilità dell'interfaccia utente per utilizzo generico viene esposto accedendo alle impostazioni tramite WMI, creando un'istanza di estensione dal percorso e dall'ID della DLL della risorsa nome, dal percorso immagine (bitmap), dal percorso dell'immagine di stato disabilitata (bitmap), dal percorso e dall'ID della DLL della risorsa sottotitolo e dalle specifiche del percorso eseguibile. Dopo la registrazione, il collegamento verrà visualizzato nell'area Altri Impostazioni del pannello Controllo genitori e facendo clic su di esso verrà richiamato l'eseguibile specificato.

La stringa del percorso eseguibile può includere facoltativamente un token per sostituire il SID dell'utente corrente prima della chiamata. In questo modo l'esecuzione del collegamento può funzionare nel contesto dell'utente per cui è attualmente visualizzata la pagina dell'hub, se l'eseguibile deve conoscere il SID.

## <a name="web-content-filter-replacement"></a>Sostituzione filtro contenuto Web

Come indicato nell'argomento Controllo [genitori](parental-controls-in-box-restrictions-and-user-interfaces.md)In-Box restrizioni e interfacce utente, il filtro contenuto Web predefinito può essere sostituito con un filtro fornito dal fornitore. Questa operazione viene eseguita accedendo alle impostazioni tramite WMI per impostare un GUID e un nome proprietario del filtro.

Il meccanismo generale di estendibilità dell'interfaccia utente viene usato per esporre un filtro di terze parti. Questo è lo stesso meccanismo usato per qualsiasi estensione che vuole essere visualizzata nella sezione Altri Impostazioni del riquadro di primo livello per i genitori Pannello di controllo. Se si impostano lo stesso GUID e un PERCORSO DLL della risorsa nome e un ID appropriati nelle impostazioni di filtro a livello di sistema, il collegamento al filtro visualizzato nella casella verrà nascosto e la voce di terze parti verrà visualizzata nella parte superiore della sezione More Impostazioni (Altre Impostazioni). Il nome registrato per il filtro verrà visualizzato nella sezione di riepilogo.

Se si reimpostano le impostazioni GUID e percorso/ID del nome del filtro, il filtro contenuto Web predefinito si ristabilirà come filtro attivo e verrà visualizzato di nuovo nella sezione Windows Impostazioni filtro.

Si noti che i filtri di terze parti non sono vincolati nelle tecnologie usate per collegare Windows comunicazioni. Un filtro deve semplicemente esporre le impostazioni usando un collegamento di estendibilità e rispettare le impostazioni appropriate di Controllo genitori.

 

 
