---
description: L'infrastruttura VSS richiede che i processi di scrittura siano in grado di funzionare sia come client COM che come server.
ms.assetid: 59bb7a86-e874-45ce-abd6-cafd18802c4d
title: Considerazioni sulla sicurezza per i writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601b981613636a571c204acdfac78ada778bb19b16a3d2677c4e56ff3ee099cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767681"
---
# <a name="security-considerations-for-writers"></a>Considerazioni sulla sicurezza per i writer

L'infrastruttura VSS richiede che i processi di scrittura siano in grado di funzionare sia come client COM che come server.

Quando agiscono come server, i writer VSS espongono le interfacce COM (ad esempio, i gestori eventi VSS, ad esempio [**CVssWriter::OnIdentify)**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)e ricevono chiamate COM in ingresso dai processi VSS (ad esempio, i richiedenti e il servizio VSS) o chiamate RPC da processi esterni a VSS, in genere quando questi processi generano eventi VSS (ad esempio, quando un richiedente chiama [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)). Pertanto, un VSS writer deve gestire in modo sicuro quali client COM sono in grado di effettuare chiamate COM in ingresso nel processo.

Analogamente, i writer VSS possono anche fungere da client COM, effettuando chiamate COM in uscita ai callback forniti dall'infrastruttura VSS o chiamate RPC a processi esterni a VSS. Questi callback forniti da un'applicazione di backup o dal servizio VSS consentono al writer di eseguire attività quali l'aggiornamento del documento dei componenti di backup tramite [**l'interfaccia IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) Pertanto, le impostazioni di sicurezza di VSS devono consentire ai writer di effettuare chiamate COM in uscita in altri processi vss.

Il meccanismo più semplice per la gestione dei problemi di sicurezza del writer prevede la selezione corretta dell'account utente con cui viene eseguito. Un writer deve in genere essere eseguito con un utente membro del gruppo Administrators o Backup Operators oppure deve essere eseguito come account di sistema locale.

Per impostazione predefinita, quando un writer funge da client COM, se non viene eseguito con questi account, qualsiasi chiamata COM eseguita viene automaticamente rifiutata con **E \_ ACCESSDENIED** senza neanche accedere all'implementazione del metodo COM.

## <a name="disabling-com-exception-handling"></a>Disabilitazione della gestione delle eccezioni COM

Quando si sviluppa un writer, impostare il flag delle opzioni globali DONOT HANDLE DELL'ECCEZIONE COMGLB \_ \_ per \_ disabilitare la gestione delle eccezioni COM. È importante eseguire questa operazione perché la gestione delle eccezioni COM può mascherare gli errori irreversibili in un'applicazione VSS. L'errore mascherato può lasciare il processo in uno stato instabile e imprevedibile, che può causare danneggiamenti e blocchi. Per altre informazioni su questo flag, vedere [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).

## <a name="setting-writer-default-com-access-check-permission"></a>Impostazione dell'autorizzazione di controllo di accesso COM predefinita del writer

I writer devono essere consapevoli del fatto che quando i processi fungono da server (ad esempio, per gestire gli eventi vss), devono consentire le chiamate in ingresso da altri partecipanti al servizio VsS, ad esempio i richiedenti o il servizio VSS.

Tuttavia, per impostazione predefinita, un processo consentirà solo ai client COM in esecuzione nella stessa sessione di accesso il SID SELF) o in esecuzione con l'account di sistema locale. Si tratta di un potenziale problema perché queste impostazioni predefinite non sono sufficienti per supportare l'infrastruttura vss. Ad esempio, i richiedenti possono essere eseguiti come account utente "Operatore di backup" che non si trova né nella stessa sessione di accesso del processo di scrittura né come account di sistema locale.

Per gestire questo tipo di problema, ogni processo server COM può esercitare un ulteriore controllo sul fatto che un client RPC o COM sia autorizzato a eseguire un metodo COM che il server (un writer in questo caso) implementa usando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare un'autorizzazione di controllo di accesso COM predefinita a livello di processo.

I writer possono eseguire in modo esplicito le operazioni seguenti:

-   Consentire a tutti i processi di accedere per chiamare nel processo di scrittura.

    Questa opzione può essere adeguata per molti writer e viene usata da altri server COM, ad esempio tutti i servizi Windows basati su SVCHOST usano già questa opzione, così come tutti i servizi COM+ per impostazione predefinita.

    Consentire a tutti i processi di eseguire chiamate COM in ingresso non è necessariamente un punto debole per la sicurezza. Un writer che funge da server COM, come tutti gli altri server COM, mantiene sempre la possibilità di autorizzare i client in ogni metodo COM implementato nel processo.

    Per consentire a tutti i processi l'accesso COM a un writer, è possibile passare un descrittore di sicurezza **NULL** come primo parametro di [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Si noti che **CoInitializeSecurity** deve essere chiamato al massimo una volta per l'intero processo. Per altre informazioni su **CoInitializeSecurity,** vedere la documentazione com.

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

    Quando si imposta in modo esplicito la sicurezza a livello COM di un writer con [**CoInitializeSecurity,**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)è necessario eseguire le operazioni seguenti:

    -   Impostare il livello di autenticazione almeno **su RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT**.

        Per una maggiore sicurezza, è consigliabile usare **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**.

    -   Impostare il livello di rappresentazione su **RPC C IMP LEVEL \_ \_ \_ \_ IDENTIFY** a meno che il processo di scrittura non deve consentire la rappresentazione per chiamate RPC o COM specifiche non correlate a VSS.

-   Consente solo ai processi specificati di accedere per chiamare nel processo di scrittura.

    Un server COM (ad esempio un writer) che chiama [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) con un descrittore di sicurezza non **NULL** può usare il descrittore per configurare se stesso per accettare chiamate in ingresso solo da utenti appartenenti a un set specifico di account.

    Un writer deve assicurarsi che i client COM in esecuzione con utenti validi siano autorizzati a chiamare nel processo. Un writer che specifica un descrittore di sicurezza nel primo parametro deve consentire agli utenti seguenti di eseguire chiamate in ingresso nel processo richiedente:

    -   Sistema locale
    -   Membri del gruppo Administrators locale
    -   Membri del gruppo Backup Operators locale
    -   Account con cui è in esecuzione il writer

## <a name="explicitly-controlling-user-account-access-to-a-writer"></a>Controllo esplicito dell'accesso dell'account utente a un writer

In alcuni casi, la limitazione dell'accesso a un writer ai processi in esecuzione come sistema locale o nei gruppi locali Administrators o Backup Operators locali può essere troppo restrittiva.

Ad esempio, un processo di scrittura (ad esempio un writer di terze parti non di sistema) potrebbe non dover essere in genere eseguito con un account amministratore o operatore di backup. Per motivi di sicurezza, è meglio non alzare di livello artificialmente i privilegi del processo per supportare VSS.

In questi casi, la chiave del Registro di sistema **\_ \_** \\  \\  \\  \\  \\ **VSS VssAccessControl** di HKEY LOCAL MACHINE SYSTEM CurrentControlSet Services deve essere modificata per indicare a VSS che un utente specificato è sicuro per eseguire un VSS writer.

In questa chiave è necessario creare una sottochiave con lo stesso nome dell'account a cui deve essere concesso o negato l'accesso. Questa sottochiave deve essere impostata su uno dei valori nella tabella seguente.

| Valore | Significato                                             |
|-------|-----------------------------------------------------|
| 0     | Negare all'utente l'accesso al writer e al richiedente.  |
| 1     | Concedere all'utente l'accesso al writer.               |
| 2     | Concedere all'utente l'accesso al richiedente.            |
| 3     | Concedere all'utente l'accesso al writer e al richiedente. |



 

L'esempio seguente concede l'accesso \\ all'account "MyDomain MyUser":

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

Questo meccanismo può essere usato anche per limitare in modo esplicito a un utente altrimenti consentito l'esecuzione di un VSS writer. L'esempio seguente limita l'accesso dall'account "ThatDomain \\ Administrator":

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

L'utente ThatDomain \\ Administrator non sarebbe in grado di eseguire un VSS writer.

 

 
