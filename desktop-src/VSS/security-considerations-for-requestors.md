---
description: L'infrastruttura vss richiede che i richiedenti VSS, ad esempio le applicazioni di backup, siano in grado di funzionare sia come client COM che come server.
ms.assetid: b01145c6-76ba-4a81-bca6-59c4ca488dac
title: Considerazioni sulla sicurezza per i richiedenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d64a5c817a8c45951d56d3fa12e78a03d8bee9dd742f67755f949d1f90a0e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590952"
---
# <a name="security-considerations-for-requesters"></a>Considerazioni sulla sicurezza per i richiedenti

L'infrastruttura vss richiede che i richiedenti VSS, ad esempio le applicazioni di backup, siano in grado di funzionare sia come client COM che come server.

Quando funge da server, un richiedente espone un set di interfacce di callback COM che possono essere richiamate da processi esterni, ad esempio writer o il servizio VSS. Di conseguenza, i richiedenti devono gestire in modo sicuro i client COM in grado di effettuare chiamate COM in ingresso nel processo.

Analogamente, i richiedenti possono fungere da client COM per le API COM fornite da un VSS writer o dal servizio VSS. Le impostazioni di sicurezza specifiche del richiedente devono consentire le chiamate COM in uscita dal richiedente a questi altri processi.

Il meccanismo più semplice per la gestione dei problemi di sicurezza di un richiedente prevede la selezione corretta dell'account utente con cui viene eseguito.

Un richiedente deve in genere essere eseguito con un utente membro del gruppo Administrators o Backup Operators oppure come account di sistema locale.

Per impostazione predefinita, quando un richiedente funge da client COM, se non viene eseguito con questi account, qualsiasi chiamata COM viene rifiutata automaticamente con **E \_ ACCESSDENIED,** senza neanche accedere all'implementazione del metodo COM.

## <a name="disabling-com-exception-handling"></a>Disabilitazione della gestione delle eccezioni COM

Quando si sviluppa un richiedente, impostare il flag delle opzioni globali DONOT HANDLE DELL'ECCEZIONE COMGLB \_ \_ per \_ disabilitare la gestione delle eccezioni COM. È importante eseguire questa operazione perché la gestione delle eccezioni COM può mascherare gli errori irreversibili in un'applicazione VSS. L'errore mascherato può lasciare il processo in uno stato instabile e imprevedibile, che può causare danneggiamenti e blocchi. Per altre informazioni su questo flag, vedere [IGlobalOptions.](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions)

## <a name="setting-requester-default-com-access-check-permission"></a>Impostazione dell'autorizzazione di controllo dell'accesso COM predefinita del richiedente

I richiedenti devono essere consapevoli del fatto che quando il processo funge da server(ad esempio, consentendo ai writer di modificare il documento dei componenti di backup), devono consentire le chiamate in ingresso da altri partecipanti al Servizio Copia Backup, ad esempio writer o il servizio VSS.

Tuttavia, per impostazione predefinita, un processo Windows consente solo i client COM in esecuzione nella stessa sessione di accesso (SELF SID) o in esecuzione con l'account di sistema locale. Si tratta di un potenziale problema perché queste impostazioni predefinite non sono adeguate per l'infrastruttura del Servizio Copia Studio. Ad esempio, i writer potrebbero essere eseguiti come account utente "Operatore di backup" che non si trova nella stessa sessione di accesso del processo richiedente né come account di sistema locale.

Per gestire questo tipo di problema, ogni processo server COM può controllare ulteriormente se un client RPC o COM è autorizzato a eseguire un metodo COM implementato dal server (in questo caso un richiedente) usando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare un'autorizzazione di controllo dell'accesso COM predefinita a livello di processo.

I richiedenti possono eseguire in modo esplicito le operazioni seguenti:

-   Consentire a tutti i processi di accedere per chiamare il processo richiedente.

    Questa opzione può essere adeguata per la maggior parte dei richiedenti e viene usata da altri server COM, ad esempio tutti i servizi Windows basati su SVCHOST usano già questa opzione, così come tutti i servizi COM+ per impostazione predefinita.

    Consentire a tutti i processi di eseguire chiamate COM in ingresso non è necessariamente un punto debole per la sicurezza. Un richiedente che funge da server COM, come tutti gli altri server COM, mantiene sempre l'opzione per autorizzare i client in ogni metodo COM implementato nel processo.

    Si noti che i callback COM interni implementati da VSS sono protetti per impostazione predefinita.

    Per consentire a tutti i processi l'accesso COM a un richiedente, è possibile passare un descrittore di sicurezza **NULL** come primo parametro di [**CoInitializeSecurity.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) Si noti che **CoInitializeSecurity** deve essere chiamato al massimo una volta per l'intero processo. Per altre informazioni sulle chiamate **a CoInitializeSecurity,** vedere la documentazione COM o MSDN.

    L'esempio di codice seguente illustra come un richiedente deve chiamare [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 8 e Windows Server 2012 e versioni successive per essere compatibile con vss per le condivisioni file remote (RVSS):

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IMPERSONATE,   //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_STATIC,                   //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    Quando si imposta in modo esplicito la sicurezza a livello COM di un richiedente [**con CoInitializeSecurity,**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)è necessario eseguire le operazioni seguenti:

    -   Impostare il livello di autenticazione almeno su **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY**. Per una maggiore sicurezza, è consigliabile usare **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**.
    -   Impostare il livello di rappresentazione su **RPC C IMP LEVEL \_ \_ \_ \_ IMPERSONATE**.
    -   Impostare le funzionalità di sicurezza di cloaking su **EOAC \_ STATIC.** Per altre informazioni sulla clonazione della sicurezza, vedere [Cloaking](../com/cloaking.md).

    L'esempio di codice seguente illustra come un richiedente deve chiamare [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 7 e Windows Server 2008 R2 e versioni precedenti (o in Windows 8 e Windows Server 2012 e versioni successive, se non è necessaria la compatibilità RVSS):

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IDENTIFY,      //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_NONE,                     //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    Quando si imposta in modo esplicito la sicurezza a livello COM di un richiedente [**con CoInitializeSecurity,**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)è necessario eseguire le operazioni seguenti:

    -   Impostare il livello di autenticazione almeno **su RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT**. Per una maggiore sicurezza, è consigliabile usare **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**.
    -   Impostare il livello di rappresentazione su **RPC C IMP LEVEL \_ \_ \_ \_ IDENTIFY** a meno che il processo richiedente non deve consentire la rappresentazione per chiamate RPC o COM specifiche non correlate a VSS.

-   Consentire l'accesso solo ai processi specificati per la chiamata al processo richiedente.

    Un server COM( ad esempio un richiedente) che chiama [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) con un descrittore di sicurezza non **NULL** come primo parametro può usare il descrittore per configurare se stesso in modo da accettare le chiamate in ingresso solo da utenti appartenenti a un set specifico di account.

    Un richiedente deve assicurarsi che i client COM in esecuzione con utenti validi siano autorizzati a eseguire chiamate nel processo. Un richiedente che specifica un descrittore di sicurezza nel primo parametro deve consentire agli utenti seguenti di eseguire chiamate in ingresso nel processo richiedente:

    -   Sistema locale
    -   Servizio locale

        **Windows XP:** Questo valore non è supportato fino Windows Server 2003.

    -   Servizio di rete

        **Windows XP:** Questo valore non è supportato fino Windows Server 2003.

    -   Membri del gruppo Administrators locale
    -   Membri del gruppo Backup Operators locale
    -   Utenti speciali specificati nel percorso del Registro di sistema seguente, con "1" come valore \_ DWORD REG

## <a name="explicitly-controlling-user-account-access-to-a-requester"></a>Controllo esplicito dell'accesso dell'account utente a un richiedente

In alcuni casi la limitazione dell'accesso a un richiedente ai processi in esecuzione come sistema locale o nei gruppi Administrators o Backup Operators locali può essere troppo restrittiva.

Ad esempio, un processo del richiedente specificato potrebbe normalmente non dover essere eseguito con un account amministratore o operatore di backup. Per motivi di sicurezza, è meglio non alzare di livello artificialmente i privilegi dei processi per supportare vss.

In questi casi, la chiave del Registro di sistema **HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **VSSAccessControl** \\  deve essere modificata per indicare a VSS che un utente specificato è sicuro per eseguire un richiedente VSS.

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
                  MyDomain\MyUser = 2<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

Questo meccanismo può essere usato anche per limitare in modo esplicito a un utente altrimenti consentito l'esecuzione di un richiedente vss. L'esempio seguente limita l'accesso dall'account "ThatDomain \\ Administrator":

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

L'utente ThatDomain \\ Administrator non sarà in grado di eseguire un richiedente VSS.

## <a name="performing-a-file-backup-of-the-system-state"></a>Esecuzione di un backup di file dello stato del sistema

Se un richiedente esegue il backup dello stato del sistema tramite il backup di singoli file anziché usare un'immagine del volume per il backup, deve chiamare le funzioni [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) e [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) per enumerare i collegamenti rigidi nei file che si trovano nelle directory seguenti:

-   \\Windows system32 \\ WDI \\ perftrack\\
-   \\Windows Winsxs\\

È possibile accedere a queste directory solo dai membri del gruppo Administrators. Per questo motivo, tale richiedente deve essere eseguito con l'account di sistema o con un account utente membro del gruppo Administrators.

**Windows XP e Windows Server 2003:** Le [**funzioni FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) e [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) non sono supportate fino Windows Vista e Windows Server 2008.

 

 
