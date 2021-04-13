---
description: I controlli padre possono essere estesi usando le impostazioni e le API di registrazione.
ms.assetid: f0fc1b11-6de4-48f6-afc9-f05c8812d2bd
title: Cenni preliminari sulle funzionalità di estensibilità dei controlli padre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fe150c5955881b8038cdca9a1e4562ee28093f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349106"
---
# <a name="parental-controls-extensibility-features-overview"></a>Cenni preliminari sulle funzionalità di estensibilità dei controlli padre

I controlli padre possono essere estesi usando le impostazioni e le API di registrazione.

-   [Registrazione-sfondo](/windows)
-   [Estendibilità della registrazione](#logging-extensibility)
-   [Aggiunta del collegamento di estendibilità dell'interfaccia utente generale del pannello controlli padre](#parental-controls-panel-general-ui-extensibility-link-addition)
-   [Sostituzione filtro contenuto Web](#web-content-filter-replacement)

## <a name="loggingbackground"></a>Registrazione-sfondo

Microsoft ha definito una serie di eventi standard per risolvere le attività comuni:

-   Sistema: controlla le impostazioni delle modifiche, le modifiche dell'account, la modifica dell'orologio di sistema e i tentativi di accesso non riusciti.
-   Utente:
    -   Limiti di sistema/tempo: Orari di accesso, disconnessione, tentativi di esecuzione dell'applicazione e durata dell'esecuzione dell'applicazione (vedere la nota).
    -   Restrizioni Web: siti Web visitati e bloccati, tentativi di download di file. I browser Web e le applicazioni simili al browser non devono registrarle, perché il filtro del contenuto Web esegue tale operazione. I filtri Web sostitutivi avrebbero la necessità di generare questi eventi.
    -   Giochi: giochi riprodotti e bloccati, fine del gioco (gli eventi insieme forniscono durata riprodotta).
    -   Consenti e blocca programmi specifici: Esegui tentativi, arresta, bloccati da restrizioni generali dell'applicazione.
    -   Messaggistica immediata: tentativo di avvio della conversione, tentativo di join della conversazione, uscita della conversazione, video/audio/gioco/servizio messaggi brevi/funzionalità di trasferimento di file/URL, tentativo di modifica dell'elenco contatti.
    -   Posta elettronica: ricevuta o ricezione bloccata, tentativo di invio, tentativo di modifica dell'elenco contatti.
    -   Supporti: contenuti multimediali riprodotti e tentativi.

Non tutti gli eventi precedenti sono idonei per l'uso da parte delle applicazioni. Le modifiche dell'account, la modifica dell'orologio di sistema e la registrazione degli eventi di accesso e disconnessione sono implementate solo dal sistema operativo e pertanto non vengono esposte pubblicamente.

> [!Note]  
> La strumentazione degli eventi di ingresso e uscita dell'applicazione è disponibile in Windows Vista ed è configurata dai controlli padre per la registrazione di questi dati.

 

## <a name="logging-extensibility"></a>Estendibilità della registrazione

Un evento personalizzato generico viene definito anche con 3 tag/valori disponibili, in modo che gli ISV non debbano in genere definire i propri in un manifesto. Log Viewer rileverà e visualizzerà le intestazioni e i valori dei tag se il numero di campi utilizzati (da 1 a 3) e le intestazioni per ogni campo vengono registrati tramite l'API WMI. Il Visualizzatore eventi generico può essere usato anche per visualizzare gli eventi personalizzati.

Se l'evento personalizzato generico non è adatto, un ISV può definirne uno proprio utilizzando un manifesto dell'applicazione e può registrare le intestazioni per un massimo di tre campi utilizzando la stessa API WMI.

Gli ISV possono scegliere di definire i propri eventi e di utilizzarli indipendentemente dal Visualizzatore di log tramite le API pubbliche di Windows. Questa operazione non ha il vantaggio di centralizzare il log completo.

## <a name="parental-controls-panel-general-ui-extensibility-link-addition"></a>Aggiunta del collegamento di estendibilità dell'interfaccia utente generale del pannello controlli padre

Un collegamento di estendibilità dell'interfaccia utente generica viene esposto tramite l'accesso alle impostazioni tramite WMI, creando un'istanza di estensione dal percorso della DLL delle risorse del nome e il percorso di ID, immagine (bitmap), il percorso dell'immagine di stato disabilitato (bitmap), il percorso e l'ID della DLL di risorse sottotitolo e le specifiche del percorso eseguibile. Dopo la registrazione, il collegamento verrà visualizzato nell'area altre impostazioni del pannello controlli padre e facendo clic su di esso verrà richiamato il file eseguibile specificato.

La stringa di percorso eseguibile può includere facoltativamente un token per il SID dell'utente corrente da sostituire prima della chiamata. In questo modo l'esecuzione del collegamento viene eseguita nel contesto dell'utente per cui è attualmente visualizzata la pagina Hub, se il file eseguibile deve conoscerlo.

## <a name="web-content-filter-replacement"></a>Sostituzione filtro contenuto Web

Come indicato nell'argomento, i [controlli parentali In-Box le restrizioni e le interfacce utente](parental-controls-in-box-restrictions-and-user-interfaces.md), il filtro contenuto Web incluso può essere sostituito con un filtro fornito dal fornitore. Questa operazione viene eseguita accedendo a impostazioni tramite WMI per impostare un GUID e un nome proprietario del filtro.

Il meccanismo di estendibilità dell'interfaccia utente generale viene usato per esporre un filtro di terze parti. Si tratta dello stesso meccanismo utilizzato per qualsiasi estensione che desidera visualizzare nella sezione altre impostazioni del pannello di controllo parentale di primo livello. Se si imposta lo stesso GUID e un percorso e un ID della DLL della risorsa nome appropriati nelle impostazioni di filtro a livello di sistema, il collegamento al filtro visualizzato in box verrà nascosto e la voce di terze parti verrà visualizzata nella parte superiore della sezione altre impostazioni. Il nome registrato per il filtro verrà visualizzato nella sezione Riepilogo.

Se si reimpostano le impostazioni GUID filtro e nome/percorso/ID, il filtro contenuto Web interno verrà ridefinito come filtro attivo e visualizzato di nuovo nella sezione impostazioni di Windows.

Si noti che i filtri di terze parti non sono limitati nelle tecnologie usate per inserire le comunicazioni di Windows. Un filtro deve semplicemente esporre le impostazioni utilizzando un collegamento di estendibilità e rispettare le impostazioni appropriate dei controlli padre.

 

 
