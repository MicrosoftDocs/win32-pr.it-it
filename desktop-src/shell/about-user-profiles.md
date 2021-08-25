---
description: Il sistema crea un profilo utente la prima volta che un utente accede a un computer. Agli accessi successivi, il sistema carica il profilo dell'utente e quindi altri componenti di sistema configurano l'ambiente dell'utente in base alle informazioni nel profilo.
title: Informazioni sui profili utente
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 333f1861-91fe-4796-af13-dd300a5c6ec3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f0463a38623baa427a6ddaf3ea19b47704b90e3ef36cf91dea2469e0cd2baa00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884771"
---
# <a name="about-user-profiles"></a>Informazioni sui profili utente

Il sistema crea un profilo utente la prima volta che un utente accede a un computer. Agli accessi successivi, il sistema carica il profilo dell'utente e quindi altri componenti di sistema configurano l'ambiente dell'utente in base alle informazioni nel profilo.

## <a name="types-of-user-profiles"></a>Tipi di profili utente

-   [Profili utente locali](local-user-profiles.md). Un profilo utente locale viene creato la prima volta che un utente accede a un computer. Il profilo viene archiviato nel disco rigido locale del computer. Le modifiche apportate al profilo utente locale sono specifiche dell'utente e del computer in cui vengono apportate le modifiche.
-   [Profili utente mobili](roaming-user-profiles.md). Un profilo utente mobile è una copia del profilo locale copiata e archiviata in una condivisione server. Questo profilo viene scaricato in qualsiasi computer a cui un utente accede in una rete. Le modifiche apportate a un profilo utente mobile vengono sincronizzate con la copia del server del profilo quando l'utente si disconnette. Il vantaggio dei profili utente mobili è che gli utenti non devono creare un profilo in ogni computer che usano in una rete.
-   [Profili utente obbligatori.](mandatory-user-profiles.md) Un profilo utente obbligatorio è un tipo di profilo che gli amministratori possono usare per specificare le impostazioni per gli utenti. Solo gli amministratori di sistema possono apportare modifiche ai profili utente obbligatori. Le modifiche apportate dagli utenti alle impostazioni del desktop vengono perse quando l'utente si disconnette.
-   [Profili utente temporanei](temporary-user-profiles.md). Viene generato un profilo temporaneo ogni volta che una condizione di errore impedisce il caricamento del profilo dell'utente. I profili temporanei vengono eliminati alla fine di ogni sessione e le modifiche apportate dall'utente alle impostazioni e ai file del desktop vengono perse quando l'utente si disconnette. I profili temporanei sono disponibili solo nei computer che eseguono Windows 2000 e versioni successive.

Un profilo utente è costituito dai seguenti elementi:

-   Hive del Registro di sistema. L'hive del Registro di sistema è il file NTuser.dat. L'hive viene caricato dal sistema all'accesso dell'utente ed è mappato alla **chiave HKEY \_ CURRENT USER \_ del** Registro di sistema. L'hive del Registro di sistema dell'utente mantiene le preferenze e la configurazione basate sul Registro di sistema dell'utente.
-   Set di cartelle del profilo archiviate nel file system. I file dei profili utente vengono archiviati nella directory **Profili,** in base a una cartella per utente. La cartella user-profile è un contenitore per le applicazioni e altri componenti di sistema da popolare con sottocartelle e dati per utente, ad esempio documenti e file di configurazione. Windows Explorer usa ampiamente le cartelle del profilo utente per elementi come il desktop dell'utente, il menu **Start** e la **cartella** Documenti.

I profili utente offrono i vantaggi seguenti:

-   Quando l'utente accede a un computer, il sistema usa le stesse impostazioni usate al momento dell'ultima disconnessione dell'utente.
-   Quando si condivide un computer con altri utenti, ogni utente riceve il desktop personalizzato dopo l'accesso.
-   Impostazioni nel profilo utente sono univoci per ogni utente. Non è possibile accedere alle impostazioni da altri utenti. Le modifiche apportate al profilo di un utente non influiscono su altri utenti o profili di altri utenti.

## <a name="user-profile-tiles-in-windows-7-and-later"></a>Riquadri del profilo utente in Windows 7 e versioni successive

In Windows 7 o versioni successive, a ogni profilo utente è associata un'immagine presentata come riquadro utente. Questi riquadri vengono visualizzati agli utenti **nella pagina Pannello di controllo** utente e nella relativa pagina **secondaria** Gestisci account. I file di immagine per gli account Utente predefinito e Guest predefinito vengono visualizzati anche qui se si hanno diritti di accesso di amministratore.

> [!Note]  
> È **possibile accedere alla** pagina secondaria Gestisci account tramite il collegamento Gestisci un altro **account** nell'elemento Pannello di controllo utente. 

 

-   %ProgramData% \\ Immagini \\ dell'account utente Microsoft \\Guest.bmp
-   %ProgramData% \\ Immagini \\ dell'account utente Microsoft \\User.bmp

L'immagine del riquadro dell'utente viene archiviata nella cartella %SystemDrive% \\ Users \\ <username> \\ AppData \\ Local Temp come \\ <username>.bmp. Tutti i caratteri barra ( \\ ) vengono convertiti in caratteri di segno più (+). Ad esempio, DOMAIN \\ user viene convertito in DOMAIN+user.

Il file di immagine viene visualizzato nella cartella **Temp dell'utente:**

-   Dopo che l'utente ha completato la configurazione iniziale del sistema(OOBE).
-   Quando l'utente avvia per la **prima volta l'Pannello di controllo** utente.
-   Quando l'utente passa alla **pagina secondaria Gestisci account** dell'elemento **Pannello di controllo** utente. Vengono inoltre visualizzati i riquadri per tutti gli altri utenti nel computer.

Queste istanze sono le uniche volte in cui le immagini vengono create o aggiornate. Di conseguenza, quando si usa il percorso  della cartella Temp a livello di codice è necessario tenere presenti diverse avvertenze:

1.  Non è garantito che il riquadro dell'utente sia presente. Se l'utente elimina il file .bmp, ad esempio manualmente o tramite un'utilità che elimina i file temporanei,  il riquadro utente  non viene ricreato automaticamente fino a quando l'utente non avvia l'elemento Pannello di controllo Account utente o la pagina secondaria Gestisci account.

2.  I riquadri utente per altri utenti nel computer potrebbero non essere presenti nella cartella Temp dell'utente **attualmente** connesso. Ad esempio, se l'utente A crea l'utente B tramite l'elemento **Pannello di controllo** Account  utente, il riquadro dell'utente B  viene creato nella cartella Temporanea dell'utente A quando Windows invia l'utente A alla pagina secondaria Gestisci account. Poiché la struttura di directory non viene creata per l'utente B fino a quando non esegue l'accesso, la cartella **Temp** dell'utente A è l'unico percorso in cui è archiviato il riquadro dell'utente B. Quando l'utente B esegue l'accesso, l'unica immagine archiviata nella cartella **Temp** dell'utente B è la propria.

    1.  Per ottenere tutti i riquadri utente per gli utenti in un sistema, le applicazioni potrebbero dover eseguire ricerche nella directory **Temp di ogni** utente.
    2.  Poiché l'elenco di controllo di  accesso (ACL) di queste directory temporanee consente l'accesso a SYSTEM, Administrator e all'utente corrente, le applicazioni devono elevare i privilegi di accesso per altri utenti.

3.  Non è garantito che i riquadri di altri utenti siano aggiornati nelle **cartelle** temporanee. Se l'utente B aggiorna il riquadro utente, l'utente A non visualizza la modifica fino a quando l'utente A non accede alla **pagina secondaria** Gestisci account. Pertanto, se le applicazioni usano la cartella **Temp** dell'utente A per ottenere il riquadro dell'utente B, tali applicazioni possono ottenere un file di immagine non aggiornato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Profili utente locali](local-user-profiles.md)
</dt> <dt>

[Profili utente mobili](roaming-user-profiles.md)
</dt> <dt>

[Profili utente obbligatori](mandatory-user-profiles.md)
</dt> <dt>

[Profili utente temporanei](temporary-user-profiles.md)
</dt> <dt>

[Directory dei profili](profiles-directory.md)
</dt> <dt>

[Variabili di ambiente utente](user-environment-variables.md)
</dt> <dt>

[Cambio rapido utente](fast-user-switching.md)
</dt> </dl>

 

 



