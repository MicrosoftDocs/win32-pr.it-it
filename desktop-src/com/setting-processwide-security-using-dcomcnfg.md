---
title: Impostazione della sicurezza Process-Wide tramite DCOMCNFG
description: Potrebbe essere necessario abilitare la protezione per una particolare applicazione se un'applicazione ha esigenze di sicurezza diverse da quelle richieste da altre applicazioni nel computer.
ms.assetid: 04a7f688-78a3-490a-bcfa-862824a05422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03174dd66e83a88724ff5d421d7b0dcb0c17699e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332780"
---
# <a name="setting-process-wide-security-using-dcomcnfg"></a>Impostazione della sicurezza Process-Wide tramite DCOMCNFG

Potrebbe essere necessario abilitare la protezione per una particolare applicazione se un'applicazione ha esigenze di sicurezza diverse da quelle richieste da altre applicazioni nel computer. Ad esempio, è possibile decidere di usare impostazioni a livello di sistema per le applicazioni che richiedono un livello di sicurezza basso, impostando un livello di sicurezza superiore per una particolare applicazione.

Tuttavia, le impostazioni di sicurezza nel registro di sistema che si applicano a una particolare applicazione non vengono utilizzate. Ad esempio, le impostazioni a livello di processo impostate nel registro di sistema utilizzando Dcomcnfg.exe verranno sostituite se un client chiama [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) per impostare la sicurezza per un particolare proxy di interfaccia. Analogamente, se un client o un server (o entrambi) chiama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare la sicurezza per un processo, le impostazioni nel registro di sistema verranno ignorate e verranno usati i parametri specificati in **CoInitializeSecurity** .

Quando si Abilita la sicurezza per un'applicazione, potrebbe essere necessario modificare diverse impostazioni. Sono inclusi il livello di autenticazione, il percorso, le autorizzazioni di avvio, le autorizzazioni di accesso e l'identità. Per le procedure dettagliate, vedere gli argomenti seguenti:

-   [Impostazione del livello di autenticazione per un'applicazione](#setting-the-authentication-level-for-an-application)
-   [Impostazione del percorso di un'applicazione](#setting-the-location-for-an-application)
-   [Impostazione delle autorizzazioni di avvio per un'applicazione](#setting-launch-permissions-for-an-application)
-   [Impostazione delle autorizzazioni di accesso per un'applicazione](#setting-access-permissions-for-an-application)
-   [Impostazione dell'identità per un'applicazione](#setting-the-identity-for-an-application)
-   [Esplorazione del database utente](#browsing-the-user-database)
-   [ ApplicazioniDcomcnfg.exe e a 64 bit](#dcomcnfgexe-and-64-bit-applications)
-   [Argomenti correlati](#related-topics)

## <a name="setting-the-authentication-level-for-an-application"></a>Impostazione del livello di autenticazione per un'applicazione

Per abilitare la sicurezza per un'applicazione, è necessario impostare un livello di autenticazione diverso da nessuno. Il livello di autenticazione indica a COM la quantità di protezione necessaria per l'autenticazione e può variare dall'autenticazione del client alla prima chiamata al metodo per la crittografia completa degli Stati dei parametri.

**Per impostare il livello di autenticazione di un'applicazione**

1.  Nella pagina delle proprietà **applicazioni** in Dcomcnfg.exe selezionare l'applicazione e fare clic sul pulsante **Proprietà** (oppure fare doppio clic sull'applicazione selezionata).

2.  Nella pagina **generale** selezionare un livello di autenticazione diverso da **(nessuno)** nella casella di riepilogo **livello di autenticazione** .

3.  Se si intende impostare altre proprietà per l'applicazione, scegliere il pulsante **applica** per applicare il nuovo livello di autenticazione. Fare clic su **OK** se è stata completata l'impostazione delle proprietà per l'applicazione e si desidera applicare le modifiche.

## <a name="setting-the-location-for-an-application"></a>Impostazione del percorso di un'applicazione

Il percorso impostato per l'applicazione determina il computer in cui viene eseguita l'applicazione. È possibile scegliere di eseguire l'applicazione nel computer in cui si trovano i dati, nel computer utilizzato per impostare il percorso o in un computer specifico.

**Per impostare la posizione di un'applicazione**

1.  Con Dcomcnfg.exe in esecuzione, selezionare l'applicazione nella pagina **applicazioni** e scegliere il pulsante **Proprietà** (oppure fare doppio clic sull'applicazione selezionata).

2.  Nella pagina **percorso** selezionare una o più caselle di controllo che corrispondono ai percorsi in cui si desidera che l'applicazione venga eseguita. Se si seleziona più di una casella di controllo, COM utilizza il primo che si applica a. Se Dcomcnfg.exe è in esecuzione nel computer server, selezionare sempre **Esegui applicazione nel computer**.

3.  Se si intende impostare altre proprietà per l'applicazione, scegliere il pulsante **applica** per applicare la nuova posizione. Scegliere **OK** se si è terminato di impostare le proprietà per l'applicazione e si desidera applicare le modifiche.

## <a name="setting-launch-permissions-for-an-application"></a>Impostazione delle autorizzazioni di avvio per un'applicazione

Con Dcomcnfg.exe, è possibile impostare le autorizzazioni di avvio per controllare l'elenco di utenti a cui è stata concessa o negata l'autorizzazione per l'avvio di un server specifico. È possibile aggiungere utenti o gruppi all'elenco, specificando se l'autorizzazione di accesso viene concessa o negata. È anche possibile rimuovere gli utenti dall'elenco.

**Per impostare le autorizzazioni di avvio per un'applicazione**

1.  Con Dcomcnfg.exe in esecuzione, selezionare l'applicazione nella pagina **applicazioni** e scegliere il pulsante **Proprietà** (oppure fare doppio clic sull'applicazione selezionata).

2.  Nella pagina delle proprietà **sicurezza** , selezionare il pulsante di opzione **Usa autorizzazioni di avvio personalizzate** e scegliere il pulsante **modifica** nella stessa area.

3.  Per rimuovere utenti o gruppi, selezionare l'utente o il gruppo che si desidera rimuovere e scegliere il pulsante **Rimuovi** . L'utente o il gruppo selezionato non verrà più visualizzato nella casella di riepilogo. Al termine della rimozione di utenti e gruppi, scegliere **OK**.

4.  Se si desidera aggiungere utenti o gruppi, scegliere il pulsante **Aggiungi** .

5.  Se si conosce il nome utente completo che si desidera aggiungere, digitarlo nella casella di testo **Aggiungi nomi** . Se non si conosce il nome utente, è possibile esplorare il database utente per trovarlo. vedere l'esplorazione del database utente di seguito. Dopo aver individuato il nome utente, selezionare l'utente o il gruppo nella casella di riepilogo **nomi** e scegliere il pulsante **Aggiungi** .

6.  Nella casella **di riepilogo tipo di accesso** selezionare il tipo di accesso ( **Consenti** avvio o **Nega avvio**). Per aggiungere altri utenti che avranno il tipo di accesso selezionato, ripetere il passaggio 5. Al termine dell'aggiunta degli utenti per il tipo di accesso selezionato, scegliere il pulsante **OK** .

7.  Per aggiungere utenti che avranno un tipo di accesso diverso, ripetere i passaggi 5 e 6. In caso contrario, scegliere **OK** per applicare le modifiche.

## <a name="setting-access-permissions-for-an-application"></a>Impostazione delle autorizzazioni di accesso per un'applicazione

Con Dcomcnfg.exe, è possibile gestire l'elenco di utenti a cui è stato concesso o negato l'accesso ai metodi di un particolare server impostando le autorizzazioni di accesso. È possibile aggiungere utenti o gruppi all'elenco, specificando se l'autorizzazione di accesso viene concessa o negata. È anche possibile rimuovere gli utenti dall'elenco.

Quando si impostano le autorizzazioni di accesso, è necessario assicurarsi che il sistema sia incluso nell'elenco di utenti a cui è stato concesso l'accesso. Se sono state concesse le autorizzazioni di accesso a tutti, il sistema viene incluso in modo implicito.

Il processo di impostazione delle autorizzazioni di accesso per un'applicazione è simile all'impostazione delle autorizzazioni di avvio. I passaggi sono i seguenti.

**Per impostare le autorizzazioni di accesso per un'applicazione**

1.  Con Dcomcnfg.exe in esecuzione, selezionare l'applicazione nella pagina **applicazioni** e scegliere il pulsante **Proprietà** (oppure fare doppio clic sull'applicazione selezionata).

2.  Nella pagina delle proprietà **sicurezza** , selezionare il pulsante di opzione **Usa autorizzazioni di accesso personalizzate** e scegliere il pulsante **modifica** nella stessa area.

3.  Per rimuovere utenti o gruppi, selezionare l'utente o il gruppo che si desidera rimuovere e scegliere il pulsante **Rimuovi** . L'utente o il gruppo selezionato non verrà più visualizzato nella casella di riepilogo. Al termine della rimozione di utenti e gruppi, scegliere **OK**.

4.  Se si desidera aggiungere un utente o un gruppo, scegliere il pulsante **Aggiungi** .

5.  Se si conosce il nome utente completo che si desidera aggiungere, digitarlo nella casella di testo **Aggiungi nomi** . Se non si conosce il nome utente, è possibile esplorare il database utente per trovarlo. Dopo aver individuato il nome utente, selezionare l'utente o il gruppo nella casella di riepilogo **nomi** e scegliere il pulsante **Aggiungi** .

6.  Nella casella **di riepilogo tipo di accesso** selezionare il tipo di accesso ( **Consenti accesso** o **Nega accesso**). Per aggiungere altri utenti che avranno il tipo di accesso selezionato, ripetere il passaggio 5. Al termine dell'aggiunta degli utenti per il tipo di accesso selezionato, scegliere il pulsante **OK** .

7.  Per aggiungere utenti che avranno un tipo di accesso diverso, ripetere i passaggi 5 e 6. In caso contrario, scegliere **OK** per applicare le modifiche.

## <a name="setting-the-identity-for-an-application"></a>Impostazione dell'identità per un'applicazione

L'identità di un'applicazione è l'account usato per eseguire l'applicazione. L'identità può essere quella dell'utente attualmente connesso (utente interattivo), l'account utente del processo client che ha avviato il server, un utente specificato o un servizio. È possibile utilizzare Dcomcnfg.exe per scegliere una di queste identità per l'applicazione. Per informazioni su come decidere quale identità impostare per l'applicazione, vedere [identità dell'applicazione](application-identity.md).

**Per impostare l'identità per un'applicazione**

1.  Con Dcomcnfg.exe in esecuzione, selezionare l'applicazione nella pagina **applicazioni** e scegliere il pulsante **Proprietà** (oppure fare doppio clic sull'applicazione selezionata).

2.  Nella pagina delle proprietà **Identity** selezionare il pulsante di opzione per l'identità desiderata. Se si sceglie **questo utente**, è necessario digitare il nome utente, la password e la password confermata.

3.  Se si intende impostare altre proprietà per l'applicazione, scegliere il pulsante **applica** per applicare la nuova identità. Scegliere **OK** se si è terminato di impostare le proprietà per l'applicazione e si desidera applicare le modifiche.

## <a name="browsing-the-user-database"></a>Esplorazione del database utente

È possibile esplorare il database utente in Dcomcnfg.exe quando è necessario trovare il nome utente completo per un determinato utente. È ad esempio possibile esplorare il database utente per individuare un utente che si desidera aggiungere per le autorizzazioni di accesso o di avvio.

**Per esplorare il database utente**

1.  Nella casella di riepilogo **nome elenco** selezionare il dominio che contiene l'utente o il gruppo che si desidera aggiungere.

2.  Per visualizzare gli utenti che appartengono al dominio selezionato, scegliere il pulsante **Mostra utenti** .

3.  Per visualizzare i membri di un determinato gruppo, selezionare il gruppo nella casella di riepilogo **nomi** e scegliere il pulsante **Mostra membri** .

4.  Se non è possibile individuare l'utente o il gruppo che si desidera aggiungere, scegliere il pulsante **Cerca** per visualizzare la finestra di dialogo **Trova account** . Selezionare il dominio in cui si vuole eseguire la ricerca (oppure selezionare **Cerca tutto**), digitare il nome utente che si vuole cercare e scegliere il pulsante **Cerca** .

## <a name="dcomcnfgexe-and-64-bit-applications"></a>Applicazioni Dcomcnfg.exe e a 64 bit

Nei sistemi operativi x64 da Windows XP a Windows Server 2008, la versione a 64 bit di DCOMCNFG.EXE non configura correttamente le applicazioni DCOM a 32 bit per l'attivazione remota. Questo comportamento fa sì che i componenti che devono essere attivati in modalità remota vengano attivati in locale. Questo comportamento non si verifica in Windows 7 e Windows Server 2008 R2 e versioni successive.

La soluzione alternativa consiste nell'utilizzare la versione a 32 bit di DCOMCNFG. Eseguire la versione a 32 bit di mmc.exe e caricare la versione a 32 bit dello snap-in Servizi componenti usando la riga di comando seguente.

C: \\ Windows \\ SysWow64>**mmc comexp. msc/32**

La versione a 32 bit di Servizi componenti registra correttamente le applicazioni DCOM a 32 bit per l'attivazione remota.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza Process-Wide](setting-processwide-security.md)
</dt> </dl>

 

 




