---
title: Impostazione Process-Wide sicurezza tramite DCOMCNFG
description: È possibile abilitare la sicurezza per una determinata applicazione se un'applicazione ha esigenze di sicurezza diverse da quelle richieste da altre applicazioni nel computer.
ms.assetid: 04a7f688-78a3-490a-bcfa-862824a05422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ace37c685748983d36b8a1e27a406fb8a81034d82ab793e77c4def960dfa2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309106"
---
# <a name="setting-process-wide-security-using-dcomcnfg"></a>Impostazione Process-Wide sicurezza tramite DCOMCNFG

È possibile abilitare la sicurezza per una determinata applicazione se un'applicazione ha esigenze di sicurezza diverse da quelle richieste da altre applicazioni nel computer. Ad esempio, è possibile decidere di usare impostazioni a livello di sistema per le applicazioni che richiedono un livello basso di sicurezza, impostando un livello di sicurezza superiore per una determinata applicazione.

Tuttavia, le impostazioni di sicurezza nel Registro di sistema che si applicano a una determinata applicazione talvolta non vengono usate. Ad esempio, le impostazioni a livello di processo impostate nel Registro di sistema usando Dcomcnfg.exe verranno sostituite se un client chiama [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) per impostare la sicurezza per un proxy di interfaccia specifico. Analogamente, se un client o un server (o entrambi) chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare la sicurezza per un processo, le impostazioni nel Registro di sistema verranno ignorate e verranno usati i parametri specificati in **CoInitializeSecurity.**

Quando si abilita la sicurezza per un'applicazione, potrebbe essere necessario modificare diverse impostazioni. tra cui il livello di autenticazione, la posizione, le autorizzazioni di avvio, le autorizzazioni di accesso e l'identità. Per le procedure dettagliate, vedere quanto segue:

-   [Impostazione del livello di autenticazione per un'applicazione](#setting-the-authentication-level-for-an-application)
-   [Impostazione del percorso di un'applicazione](#setting-the-location-for-an-application)
-   [Impostazione delle autorizzazioni di avvio per un'applicazione](#setting-launch-permissions-for-an-application)
-   [Impostazione delle autorizzazioni di accesso per un'applicazione](#setting-access-permissions-for-an-application)
-   [Impostazione dell'identità per un'applicazione](#setting-the-identity-for-an-application)
-   [Esplorazione del database utente](#browsing-the-user-database)
-   [Dcomcnfg.exe applicazioni a 64 bit](#dcomcnfgexe-and-64-bit-applications)
-   [Argomenti correlati](#related-topics)

## <a name="setting-the-authentication-level-for-an-application"></a>Impostazione del livello di autenticazione per un'applicazione

Per abilitare la sicurezza per un'applicazione, è necessario impostare un livello di autenticazione diverso da Nessuno. Il livello di autenticazione indica a COM la quantità di protezione dell'autenticazione necessaria e può variare dall'autenticazione del client alla prima chiamata al metodo alla crittografia completa degli stati dei parametri.

**Per impostare il livello di autenticazione di un'applicazione**

1.  Nella pagina **delle proprietà** Applicazioni in Dcomcnfg.exe selezionare l'applicazione e fare clic sul pulsante **Proprietà** oppure fare doppio clic sull'applicazione selezionata.

2.  Nella pagina **Generale** selezionare un livello di autenticazione diverso **da (Nessuno)** dalla **casella di riepilogo Livello di** autenticazione .

3.  Se si impostano altre proprietà per questa applicazione, scegliere il **pulsante Applica** per applicare il nuovo livello di autenticazione. Fare **clic su OK** se è stata completata l'impostazione delle proprietà per questa applicazione e si desidera applicare le modifiche.

## <a name="setting-the-location-for-an-application"></a>Impostazione del percorso di un'applicazione

Il percorso impostato per l'applicazione determina il computer in cui verrà eseguita l'applicazione. È possibile scegliere di eseguire l'applicazione nel computer in cui si trovano i dati, nel computer utilizzato per impostare il percorso o in un computer specificato.

**Per impostare il percorso di un'applicazione**

1.  Con Dcomcnfg.exe in esecuzione, selezionare l'applicazione **nella**  pagina Applicazioni e scegliere il pulsante Proprietà oppure fare doppio clic sull'applicazione selezionata.

2.  Nella pagina **Percorso** selezionare una o più caselle di controllo corrispondenti alle posizioni in cui si vuole eseguire l'applicazione. Se si seleziona più di una casella di controllo, COM usa la prima casella di controllo applicabile. Se Dcomcnfg.exe in esecuzione nel computer server, selezionare sempre **Esegui applicazione in questo computer**.

3.  Se si impostano altre proprietà per questa applicazione, scegliere il **pulsante** Applica per applicare la nuova posizione. Scegliere **OK** se è stata completata l'impostazione delle proprietà per questa applicazione e si desidera applicare le modifiche.

## <a name="setting-launch-permissions-for-an-application"></a>Impostazione delle autorizzazioni di avvio per un'applicazione

Con Dcomcnfg.exe, è possibile impostare le autorizzazioni di avvio per controllare l'elenco di utenti a cui viene concessa o negata l'autorizzazione per avviare un server specifico. È possibile aggiungere utenti o gruppi all'elenco, specificando se l'autorizzazione di accesso viene concessa o negata. È anche possibile rimuovere gli utenti dall'elenco.

**Per impostare le autorizzazioni di avvio per un'applicazione**

1.  Con Dcomcnfg.exe in esecuzione, selezionare l'applicazione **nella**  pagina Applicazioni e scegliere il pulsante Proprietà oppure fare doppio clic sull'applicazione selezionata.

2.  Nella pagina **delle proprietà** Sicurezza selezionare il pulsante di opzione Usa autorizzazioni **di** avvio personalizzate e scegliere il **pulsante** Modifica nella stessa area.

3.  Per rimuovere utenti o gruppi, selezionare l'utente o il gruppo da rimuovere e scegliere il **pulsante** Rimuovi. L'utente o il gruppo selezionato non verrà più visualizzato nella casella di riepilogo. Al termine della rimozione di utenti e gruppi, scegliere **OK.**

4.  Per aggiungere utenti o gruppi, scegliere il **pulsante** Aggiungi.

5.  Se si conosce il nome utente completo da aggiungere, digitarlo nella **casella di testo Aggiungi** nomi. Se non si conosce il nome utente, è possibile esplorare il database utente per trovarlo (vedere Esplorazione del database utente più avanti). Dopo aver individuato il nome utente, selezionare l'utente o il gruppo dalla casella **di** riepilogo Nomi e scegliere il **pulsante** Aggiungi.

6.  Nella casella **di riepilogo Tipo di** accesso selezionare il tipo di accesso **(Consenti avvio** o Nega **avvio**). Per aggiungere altri utenti che avranno il tipo di accesso selezionato, ripetere il passaggio 5. Al termine dell'aggiunta di utenti per il tipo di accesso selezionato, scegliere **il pulsante OK.**

7.  Per aggiungere utenti con un tipo di accesso diverso, ripetere i passaggi 5 e 6. In caso contrario, **scegliere OK** per applicare le modifiche.

## <a name="setting-access-permissions-for-an-application"></a>Impostazione delle autorizzazioni di accesso per un'applicazione

Con Dcomcnfg.exe, è possibile gestire l'elenco di utenti a cui viene concesso o negato l'accesso ai metodi di un determinato server impostando le autorizzazioni di accesso. È possibile aggiungere utenti o gruppi all'elenco, specificando se l'autorizzazione di accesso viene concessa o negata. È anche possibile rimuovere gli utenti dall'elenco.

Quando si impostano le autorizzazioni di accesso, è necessario assicurarsi che SYSTEM sia incluso nell'elenco degli utenti a cui viene concesso l'accesso. Se sono state concesse autorizzazioni di accesso a Everyone, SYSTEM viene incluso in modo implicito.

Il processo di impostazione delle autorizzazioni di accesso per un'applicazione è simile all'impostazione delle autorizzazioni di avvio. I passaggi sono i seguenti.

**Per impostare le autorizzazioni di accesso per un'applicazione**

1.  Con Dcomcnfg.exe in esecuzione, selezionare l'applicazione **nella**  pagina Applicazioni e scegliere il pulsante Proprietà oppure fare doppio clic sull'applicazione selezionata.

2.  Nella pagina **delle proprietà** Sicurezza selezionare il **pulsante** di opzione Usa autorizzazioni di accesso personalizzate e scegliere il **pulsante** Modifica nella stessa area.

3.  Per rimuovere utenti o gruppi, selezionare l'utente o il gruppo da rimuovere e scegliere il **pulsante** Rimuovi. L'utente o il gruppo selezionato non verrà più visualizzato nella casella di riepilogo. Al termine della rimozione di utenti e gruppi, scegliere **OK.**

4.  Se si vuole aggiungere un utente o un gruppo, scegliere il **pulsante** Aggiungi.

5.  Se si conosce il nome utente completo da aggiungere, digitarlo nella **casella di testo Aggiungi** nomi. Se non si conosce il nome utente, è possibile esplorare il database utente per trovarlo. Dopo aver individuato il nome utente, selezionare l'utente o il gruppo dalla casella **di** riepilogo Nomi e scegliere il **pulsante** Aggiungi.

6.  Nella casella **di riepilogo Tipo di** accesso selezionare il tipo di accesso **(Consenti accesso** o Nega **accesso**). Per aggiungere altri utenti che avranno il tipo di accesso selezionato, ripetere il passaggio 5. Al termine dell'aggiunta di utenti per il tipo di accesso selezionato, scegliere **il pulsante OK.**

7.  Per aggiungere utenti con un tipo di accesso diverso, ripetere i passaggi 5 e 6. In caso contrario, **scegliere OK** per applicare le modifiche.

## <a name="setting-the-identity-for-an-application"></a>Impostazione dell'identità per un'applicazione

L'identità di un'applicazione è l'account usato per eseguire l'applicazione. L'identità può essere quella dell'utente attualmente connesso (utente interattivo), dell'account utente del processo client che ha avviato il server, di un utente specificato o di un servizio. È possibile usare Dcomcnfg.exe scegliere una di queste identità per l'applicazione. Per informazioni sulla scelta dell'identità da impostare per l'applicazione, vedere [Identità dell'applicazione](application-identity.md).

**Per impostare l'identità per un'applicazione**

1.  Con Dcomcnfg.exe in esecuzione, selezionare l'applicazione **nella**  pagina Applicazioni e scegliere il pulsante Proprietà oppure fare doppio clic sull'applicazione selezionata.

2.  Nella pagina **delle proprietà** Identità selezionare il pulsante di opzione per l'identità desiderata. Se si sceglie **Questo utente,** è necessario digitare il nome utente, la password e la password confermata.

3.  Se si impostano altre proprietà per questa applicazione, scegliere il **pulsante Applica** per applicare la nuova identità. Scegliere **OK** se è stata completata l'impostazione delle proprietà per questa applicazione e si desidera applicare le modifiche.

## <a name="browsing-the-user-database"></a>Esplorazione del database utente

È possibile esplorare il database utente in Dcomcnfg.exe quando è necessario trovare il nome utente completo per un determinato utente. Ad esempio, è possibile esplorare il database utente per individuare un utente che si vuole aggiungere per le autorizzazioni di accesso o avvio.

**Per esplorare il database utente**

1.  Nella casella **di riepilogo Elenca nomi da** selezionare il dominio contenente l'utente o il gruppo da aggiungere.

2.  Per visualizzare gli utenti che appartengono al dominio selezionato, scegliere il **pulsante Mostra** utenti.

3.  Per visualizzare i membri di un gruppo specifico, selezionare il gruppo nella casella **di** riepilogo Nomi e scegliere **il pulsante Mostra** membri.

4.  Se non è possibile individuare l'utente o il gruppo da aggiungere, scegliere il **pulsante** Cerca per visualizzare la finestra **di** dialogo Trova account. Selezionare il dominio in cui si vuole eseguire la ricerca oppure selezionare Cerca **tutto,** digitare il nome utente da cercare e scegliere il **pulsante** Cerca.

## <a name="dcomcnfgexe-and-64-bit-applications"></a>Dcomcnfg.exe applicazioni a 64 bit

Nei sistemi operativi x64 da Windows XP a Windows Server 2008, la versione a 64 bit di DCOMCNFG.EXE non configura correttamente le applicazioni DCOM a 32 bit per l'attivazione remota. Questo comportamento fa sì che i componenti che devono essere attivati in modalità remota vengano attivati in locale. Questo comportamento non si verifica in Windows 7 e Windows Server 2008 R2 e versioni successive.

La soluzione alternativa consiste nell'usare la versione a 32 bit di DCOMCNFG. Eseguire la versione a 32 bit di mmc.exe e caricare la versione a 32 bit dello snap-in Servizi componenti usando la riga di comando seguente.

C: \\ WINDOWS \\ SysWOW64>**mmc comexp.msc /32**

La versione a 32 bit di Servizi componenti registra correttamente le applicazioni DCOM a 32 bit per l'attivazione remota.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della Process-Wide sicurezza](setting-processwide-security.md)
</dt> </dl>

 

 




