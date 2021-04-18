---
description: L'infrastruttura VSS richiede che i processi writer siano in grado di funzionare sia come client COM sia come server.
ms.assetid: 59bb7a86-e874-45ce-abd6-cafd18802c4d
title: Considerazioni sulla sicurezza per i writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6f88243adbd62d928170a86ed57b91cbebe134
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310670"
---
# <a name="security-considerations-for-writers"></a>Considerazioni sulla sicurezza per i writer

L'infrastruttura VSS richiede che i processi writer siano in grado di funzionare sia come client COM sia come server.

Quando funge da server, i writer VSS espongono le interfacce COM (ad esempio, i gestori eventi VSS, ad esempio [**CVssWriter:: Onidentificate**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) e ricevono chiamate com in ingresso da processi VSS (come i richiedenti e il servizio VSS) o chiamate RPC da processi esterni a VSS, in genere quando questi processi generano eventi VSS (ad esempio, quando un richiedente chiama [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)). Pertanto, un VSS writer deve gestire in modo sicuro quali client COM sono in grado di effettuare chiamate COM in ingresso al suo processo.

Analogamente, i writer VSS possono fungere anche da client COM, effettuando chiamate COM in uscita a callback forniti dall'infrastruttura VSS o chiamate RPC a processi esterni a VSS. Questi callback forniti da un'applicazione di backup o dal servizio VSS consentono al writer di eseguire attività come l'aggiornamento del documento dei componenti di backup tramite l'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) . Pertanto, le impostazioni di sicurezza VSS devono consentire ai writer di eseguire chiamate COM in uscita in altri processi VSS.

Il meccanismo più semplice per la gestione dei problemi di sicurezza del writer riguarda la scelta corretta dell'account utente con cui viene eseguito. Un writer deve in genere essere eseguito con un utente membro del gruppo Administrators o del gruppo Backup Operators oppure deve essere eseguito come account di sistema locale.

Per impostazione predefinita, quando un writer funge da client COM, se non viene eseguito con questi account, qualsiasi chiamata COM che esegue viene rifiutata automaticamente con **E \_ AccessDenied** senza neanche dover ottenere l'implementazione del metodo com.

## <a name="disabling-com-exception-handling"></a>Disabilitazione della gestione delle eccezioni COM

Quando si sviluppa un writer, impostare il \_ \_ flag di opzioni globali di gestione delle eccezioni com COMGLB \_ per disabilitare la gestione delle eccezioni com. È importante eseguire questa operazione perché la gestione delle eccezioni COM può mascherare gli errori irreversibili in un'applicazione VSS. L'errore mascherato può lasciare il processo in uno stato instabile e imprevedibile, che può causare danneggiamenti e blocchi. Per ulteriori informazioni su questo flag, vedere [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).

## <a name="setting-writer-default-com-access-check-permission"></a>Impostazione dell'autorizzazione per il controllo dell'accesso COM predefinito del writer

È necessario tenere presente che quando i processi fungono da server, ad esempio per gestire gli eventi VSS, devono consentire le chiamate in ingresso da altri partecipanti VSS, ad esempio i richiedenti o il servizio VSS.

Tuttavia, per impostazione predefinita, un processo consentirà solo ai client COM che sono in esecuzione nella stessa sessione di accesso SID AUTONOMo o in esecuzione con l'account di sistema locale. Questo è un potenziale problema perché queste impostazioni predefinite non sono sufficienti per supportare l'infrastruttura VSS. Ad esempio, i richiedenti possono essere eseguiti come account utente "Backup Operator" che non si trova nella stessa sessione di accesso del processo di scrittura o di un account di sistema locale.

Per gestire questo tipo di problema, ogni processo server COM può esercitare un ulteriore controllo sul fatto che un client RPC o COM sia autorizzato a eseguire un metodo COM il server (in questo caso un writer) implementi utilizzando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare un'autorizzazione per il controllo dell'accesso COM predefinito a livello di processo.

I writer possono eseguire in modo esplicito le operazioni seguenti:

-   Consente l'accesso a tutti i processi per chiamare il processo del writer.

    Questa opzione può essere adeguata per molti writer e viene utilizzata da altri server COM. ad esempio, tutti i servizi Windows basati su SVCHOST utilizzano già questa opzione, così come tutti i servizi COM+ per impostazione predefinita.

    Consentire a tutti i processi di eseguire chiamate COM in ingresso non è necessariamente un punto debole per la sicurezza. Un writer che funge da server COM, come tutti gli altri server COM, mantiene sempre l'opzione di autorizzazione dei client su ogni metodo COM implementato nel processo.

    Per consentire a tutti i processi l'accesso COM a un writer, è possibile passare un descrittore di sicurezza **null** come primo parametro di [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Si noti che **CoInitializeSecurity** deve essere chiamato al massimo una volta per l'intero processo. Per ulteriori informazioni su **CoInitializeSecurity**, vedere la documentazione com.

    Di seguito è riportato un esempio di codice che include una chiamata a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity):

    ``` syntax
    // Initialize COM security.
    hr = CoInitializeSecurity(
           NULL,                          // PSECURITY_DESCRIPTOR          pSecDesc,
           -1,                            // LONG                          cAuthSvc,
           NULL,                          // SOLE_AUTHENTICATION_SERVICE  *asAuthSvc,
           NULL,                          // void                         *pReserved1,
           RPC_C_AUTHN_LEVEL_PKT_PRIVACY, // DWORD                         dwAuthnLevel,
           RPC_C_IMP_LEVEL_IDENTIFY,      // DWORD                         dwImpLevel,
           NULL,                          // void                         *pAuthList,
           EOAC_NONE,                     // DWORD                         dwCapabilities,
           NULL                           // void                         *pReserved3
        );
    ```

    Quando si imposta in modo esplicito la sicurezza a livello COM di un writer con [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), è necessario eseguire le operazioni seguenti:

    -   Impostare il livello di autenticazione su almeno **\_ \_ \_ \_ connessione a livello di autenticazione C RPC**.

        Per una maggiore sicurezza, è consigliabile usare il **livello di autenticazione di RPC \_ C \_ \_ \_ PKT \_ privacy**.

    -   Impostare il livello di rappresentazione sull' **Identificazione del \_ \_ \_ livello \_ Imp C di RPC** , a meno che il processo writer non debba consentire la rappresentazione per chiamate RPC o com specifiche non correlate a VSS.

-   Consenti solo ai processi specificati l'accesso per chiamare il processo del writer.

    Un server COM (ad esempio un writer) che chiama [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) con un descrittore di sicurezza non **null** può usare il descrittore per configurare se stesso in modo da accettare le chiamate in ingresso solo dagli utenti che appartengono a un set di account specifico.

    Un writer deve garantire che i client COM in esecuzione in utenti validi siano autorizzati a chiamare il processo. Un writer che specifica un descrittore di sicurezza nel primo parametro deve consentire agli utenti seguenti di eseguire chiamate in ingresso nel processo del richiedente:

    -   Sistema locale
    -   Membri del gruppo Administrators locale
    -   Membri del gruppo Backup Operators locale
    -   Account con cui è in esecuzione il writer

## <a name="explicitly-controlling-user-account-access-to-a-writer"></a>Controllo esplicito dell'accesso di un account utente a un writer

Ci sono casi in cui la limitazione dell'accesso a un writer ai processi in esecuzione come sistema locale o ai gruppi locali degli amministratori locali o degli operatori di backup locali può essere troppo restrittiva.

Ad esempio, un processo di scrittura (probabilmente un writer non di sistema di terze parti) potrebbe non essere in genere necessario per l'esecuzione con un account amministratore o operatore di backup. Per motivi di sicurezza, è preferibile non innalzare di livello artificialmente i privilegi del processo per supportare VSS.

In questi casi, è necessario modificare la chiave del registro di sistema **HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** per indicare a VSS che un utente specificato è sicuro per l'esecuzione di una VSS writer.

In questa chiave è necessario creare una sottochiave con lo stesso nome dell'account a cui viene concesso o negato l'accesso. Questa sottochiave deve essere impostata su uno dei valori indicati nella tabella seguente.

| Valore | Significato                                             |
|-------|-----------------------------------------------------|
| 0     | Negare all'utente l'accesso al writer e al richiedente.  |
| 1     | Concedere all'utente l'accesso al writer.               |
| 2     | Concedere all'utente l'accesso al richiedente.            |
| 3     | Concedere all'utente l'accesso al writer e al richiedente. |



 

Nell'esempio seguente viene concesso l'accesso all'account "dominio \\ utente":

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 1<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

Questo meccanismo può essere usato anche per limitare in modo esplicito l'esecuzione di un VSS writer da un utente altrimenti consentito. Nell'esempio seguente viene limitato l'accesso dall'account "ThatDomain \\ Administrator":

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  ThatDomain\Administrator = 0<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

L' \\ amministratore di ThatDomain utente non sarà in grado di eseguire un VSS writer.

 

 
