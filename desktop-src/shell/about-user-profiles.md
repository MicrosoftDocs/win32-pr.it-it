---
description: Il sistema crea un profilo utente la prima volta che un utente accede a un computer. Al successivo accesso, il sistema carica il profilo dell'utente e altri componenti di sistema configurano l'ambiente dell'utente in base alle informazioni contenute nel profilo.
title: Informazioni sui profili utente
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 333f1861-91fe-4796-af13-dd300a5c6ec3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bafd5df7d59787104c2904b4e83c734deaf28708
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977418"
---
# <a name="about-user-profiles"></a>Informazioni sui profili utente

Il sistema crea un profilo utente la prima volta che un utente accede a un computer. Al successivo accesso, il sistema carica il profilo dell'utente e altri componenti di sistema configurano l'ambiente dell'utente in base alle informazioni contenute nel profilo.

## <a name="types-of-user-profiles"></a>Tipi di profili utente

-   [Profili utente locali](local-user-profiles.md). Viene creato un profilo utente locale la prima volta che un utente accede a un computer. Il profilo viene archiviato sul disco rigido locale del computer. Le modifiche apportate al profilo utente locale sono specifiche dell'utente e del computer in cui vengono apportate le modifiche.
-   [Profili utente mobili](roaming-user-profiles.md). Un profilo utente mobile è una copia del profilo locale che viene copiato e archiviato in una condivisione server. Questo profilo viene scaricato in qualsiasi computer a cui un utente accede in una rete. Le modifiche apportate a un profilo utente mobile vengono sincronizzate con la copia del server del profilo quando l'utente si disconnette. Il vantaggio dei profili utente mobili è che non è necessario che gli utenti creino un profilo in ogni computer utilizzato in una rete.
-   [Profili utente obbligatori](mandatory-user-profiles.md). Un profilo utente obbligatorio è un tipo di profilo che gli amministratori possono usare per specificare le impostazioni per gli utenti. Solo gli amministratori di sistema possono apportare modifiche ai profili utente obbligatori. Le modifiche apportate dagli utenti alle impostazioni desktop vengono perse quando l'utente si disconnette.
-   [Profili utente temporanei](temporary-user-profiles.md). Viene emesso un profilo temporaneo ogni volta che una condizione di errore impedisce il caricamento del profilo dell'utente. I profili temporanei vengono eliminati alla fine di ogni sessione e le modifiche apportate dall'utente alle impostazioni e ai file del desktop vengono perse quando l'utente si disconnette. I profili temporanei sono disponibili solo nei computer che eseguono Windows 2000 e versioni successive.

Un profilo utente è costituito dagli elementi seguenti:

-   Hive del registro di sistema. L'hive del registro di sistema è il file NTuser. dat. L'hive viene caricato dal sistema all'accesso dell'utente e viene mappato alla chiave del registro di sistema **\_ \_ dell'utente corrente di HKEY** . L'hive del registro di sistema dell'utente gestisce le preferenze e la configurazione basate sul Registro di sistema dell'utente.
-   Set di cartelle del profilo archiviate nel file system. I file del profilo utente vengono archiviati nella directory dei **profili** , in base a una cartella per ogni utente. La cartella del profilo utente è un contenitore per le applicazioni e altri componenti di sistema da popolare con le sottocartelle e i dati per utente, ad esempio documenti e file di configurazione. Esplora risorse utilizza ampiamente le cartelle del profilo utente per elementi quali il desktop dell'utente, il menu **Start** e la cartella **documenti** .

I profili utente offrono i vantaggi seguenti:

-   Quando l'utente accede a un computer, il sistema utilizza le stesse impostazioni in uso al momento dell'ultimo accesso dell'utente.
-   Quando si condivide un computer con altri utenti, ogni utente riceve il desktop personalizzato dopo l'accesso.
-   Le impostazioni nel profilo utente sono univoche per ogni utente. Non è possibile accedere alle impostazioni da altri utenti. Le modifiche apportate al profilo di un utente non influiscono sui profili di altri utenti o di altri utenti.

## <a name="user-profile-tiles-in-windows-7-and-later"></a>Riquadri del profilo utente in Windows 7 e versioni successive

In Windows 7 o versioni successive, a ogni profilo utente è associata un'immagine visualizzata come riquadro utente. Questi riquadri vengono visualizzati dagli utenti nell'elemento del pannello di controllo **account utente** e nella relativa sottopagina **Gestisci account** . Se si dispone dei diritti di accesso di amministratore, verranno visualizzati anche i file di immagine per gli account utente Guest predefiniti e predefiniti.

> [!Note]  
> È possibile accedere alla sottopagina **Gestisci** account tramite il collegamento **Gestisci un altro account** nell'elemento del pannello di controllo **account utente** .

 

-   % ProgramData% \\ \\ Immagini account utente Microsoft \\Guest.bmp
-   % ProgramData% \\ \\ Immagini account utente Microsoft \\User.bmp

L'immagine affiancata dell'utente viene archiviata nella \\ cartella temporanea locale% SystemDrive% Users \\ <username> \\ AppData \\ \\ come <username> . bmp. Qualsiasi barra ( \\ ) viene convertita in caratteri segno più (+). Ad esempio, l' \\ utente di dominio viene convertito in dominio + utente.

Il file di immagine viene visualizzato nella cartella **temporanea** dell'utente:

-   Dopo che l'utente ha completato la configurazione iniziale del sistema (OOBE).
-   Quando l'utente avvia per la prima volta l'elemento del pannello di controllo **degli account utente** .
-   Quando l'utente passa alla sottopagina **Gestisci account** dell'elemento del pannello di controllo **account utente** . Vengono inoltre visualizzati i riquadri per tutti gli altri utenti del computer.

Tali istanze sono le uniche volte in cui le immagini vengono create o aggiornate. Pertanto, quando si usa il percorso della cartella **temporanea** a livello di codice, è necessario tenere presenti alcune considerazioni:

1.  Non è garantito che il riquadro dell'utente sia presente. Se l'utente elimina il file con estensione bmp, ad esempio manualmente o tramite un'utilità che elimina i file temporanei, il riquadro utente non viene ricreato automaticamente fino a quando l'utente non avvia l'elemento del pannello di controllo degli **account utente** o la sottopagina **Gestisci account** .

2.  I riquadri utente per altri utenti del computer potrebbero non essere presenti nella cartella **temporanea** dell'utente attualmente connesso. Se, ad esempio, l'utente A crea l'utente B tramite l'elemento del pannello di controllo **account utente** , il riquadro dell'utente b viene creato nella cartella **temporanea** dell'utente a quando Windows invia l'utente a alla sottopagina **Gestisci account** . Poiché la struttura di directory non viene creata per l'utente B fino a quando non esegue l'accesso, la cartella **temporanea** dell'utente a è l'unica posizione in cui è archiviato il riquadro dell'utente b. Quando l'utente B esegue l'accesso, l'unica immagine archiviata nella cartella **temporanea** dell'utente b è la propria.

    1.  Per ottenere tutti i riquadri utente per gli utenti di un sistema, è possibile che le applicazioni debbano eseguire la ricerca nella directory **temporanea** di ogni utente.
    2.  Poiché l'elenco di controllo di accesso (ACL) di queste directory **temporanee** consente l'accesso a System, Administrator e l'utente corrente, le applicazioni devono elevare l'accesso ad altri utenti.

3.  Non è garantito che i riquadri di altri utenti siano aggiornati nelle cartelle **temporanee** . Se l'utente B aggiorna il riquadro utente, l'utente A non visualizzerà la modifica fino a quando l'utente A accede alla sottopagina **Gestisci account** . Di conseguenza, se le applicazioni usano la cartella **temporanea** dell'utente per ottenere il riquadro dell'utente B, le applicazioni possono ottenere un file di immagine non aggiornato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Profili utente locale](local-user-profiles.md)
</dt> <dt>

[Profili utente mobili](roaming-user-profiles.md)
</dt> <dt>

[Profili utente obbligatori](mandatory-user-profiles.md)
</dt> <dt>

[Profili utente temporanei](temporary-user-profiles.md)
</dt> <dt>

[Directory profili](profiles-directory.md)
</dt> <dt>

[Variabili di ambiente utente](user-environment-variables.md)
</dt> <dt>

[Cambio rapido utente](fast-user-switching.md)
</dt> </dl>

 

 



