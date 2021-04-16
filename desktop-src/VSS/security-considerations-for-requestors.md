---
description: L'infrastruttura VSS richiede che i richiedenti VSS, ad esempio le applicazioni di backup, siano in grado di funzionare sia come client COM sia come server.
ms.assetid: b01145c6-76ba-4a81-bca6-59c4ca488dac
title: Considerazioni sulla sicurezza per i richiedenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e989793dbf5a5dd1fac3224cf6f06958564de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345011"
---
# <a name="security-considerations-for-requesters"></a>Considerazioni sulla sicurezza per i richiedenti

L'infrastruttura VSS richiede che i richiedenti VSS, ad esempio le applicazioni di backup, siano in grado di funzionare sia come client COM sia come server.

Quando funge da server, un richiedente espone un set di interfacce di callback COM che possono essere richiamate da processi esterni, ad esempio i writer o il servizio VSS. Pertanto, i richiedenti devono gestire in modo sicuro quali client COM sono in grado di effettuare chiamate COM in ingresso al proprio processo.

Analogamente, i richiedenti possono fungere da client COM per le API COM fornite da un VSS writer o dal servizio VSS. Le impostazioni di sicurezza specifiche del richiedente devono consentire le chiamate COM in uscita dal richiedente a questi altri processi.

Il meccanismo più semplice per la gestione dei problemi di sicurezza di un richiedente prevede una corretta selezione dell'account utente con cui viene eseguito.

Un richiedente deve essere in genere eseguito con un utente membro del gruppo Administrators o del gruppo Backup Operators oppure viene eseguito come account di sistema locale.

Per impostazione predefinita, quando un richiedente funge da client COM, se non viene eseguito con questi account, qualsiasi chiamata COM viene rifiutata automaticamente con **E \_ AccessDenied**, senza nemmeno ottenere l'implementazione del metodo com.

## <a name="disabling-com-exception-handling"></a>Disabilitazione della gestione delle eccezioni COM

Quando si sviluppa un richiedente, impostare il \_ \_ \_ flag di opzioni globali di gestione delle eccezioni com COMGLB per disabilitare la gestione delle eccezioni com. È importante eseguire questa operazione perché la gestione delle eccezioni COM può mascherare gli errori irreversibili in un'applicazione VSS. L'errore mascherato può lasciare il processo in uno stato instabile e imprevedibile, che può causare danneggiamenti e blocchi. Per ulteriori informazioni su questo flag, vedere [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).

## <a name="setting-requester-default-com-access-check-permission"></a>Impostazione dell'autorizzazione per il controllo dell'accesso COM predefinito del richiedente

I richiedenti devono tenere presente che quando il processo funge da server (ad esempio, consentendo ai writer di modificare il documento dei componenti di backup), devono consentire le chiamate in ingresso da altri partecipanti VSS, ad esempio i writer o il servizio VSS.

Tuttavia, per impostazione predefinita, un processo di Windows consentirà solo i client COM in esecuzione nella stessa sessione di accesso (SID SELF) o in esecuzione con l'account di sistema locale. Questo è un potenziale problema perché queste impostazioni predefinite non sono adeguate all'infrastruttura VSS. Ad esempio, i writer potrebbero essere eseguiti come account utente "Backup Operator" che non si trova nella stessa sessione di accesso del processo del richiedente o di un account di sistema locale.

Per gestire questo tipo di problema, ogni processo server COM può esercitare un ulteriore controllo sul fatto che un client RPC o COM sia autorizzato a eseguire un metodo COM implementato dal server (in questo caso un richiedente) utilizzando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare un'autorizzazione di controllo di accesso COM predefinita a livello di processo.

I richiedenti possono eseguire le operazioni seguenti in modo esplicito:

-   Consenti a tutti i processi l'accesso per chiamare il processo del richiedente.

    Questa opzione può essere adeguata per la maggior parte dei richiedenti e viene utilizzata da altri server COM. ad esempio, tutti i servizi Windows basati su SVCHOST utilizzano già questa opzione, così come tutti i servizi COM+ per impostazione predefinita.

    Consentire a tutti i processi di eseguire chiamate COM in ingresso non è necessariamente un punto debole per la sicurezza. Un richiedente che funge da server COM, come tutti gli altri server COM, mantiene sempre l'opzione per autorizzare i client su ogni metodo COM implementato nel processo.

    Si noti che i callback COM interni implementati da VSS sono protetti per impostazione predefinita.

    Per consentire a tutti i processi l'accesso COM a un richiedente, è possibile passare un descrittore di sicurezza **null** come primo parametro di [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Si noti che **CoInitializeSecurity** deve essere chiamato al massimo una volta per l'intero processo. Per ulteriori informazioni sulle chiamate **CoInitializeSecurity** , vedere la documentazione com o MSDN.

    Nell'esempio di codice seguente viene illustrato come un richiedente deve chiamare [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 8 e windows Server 2012 e versioni successive, in modo da essere compatibile con VSS per le condivisioni file Remote (RVSS):

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

    Quando si imposta in modo esplicito la sicurezza a livello COM di un richiedente con [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), è necessario eseguire le operazioni seguenti:

    -   Impostare il livello di autenticazione almeno sull' **\_ \_ \_ \_ \_ integrità PKT del livello auth C RPC**. Per una maggiore sicurezza, è consigliabile usare il **livello di autenticazione di RPC \_ C \_ \_ \_ PKT \_ privacy**.
    -   Impostare il livello di rappresentazione su **RPC \_ C \_ Imp \_ level \_ Impersonate**.
    -   Impostare le funzionalità di sicurezza mascheramento su **EOAC \_ static**. Per ulteriori informazioni sulla sicurezza del mascheramento, vedere [mascheramento](../com/cloaking.md).

    Nell'esempio di codice seguente viene illustrato come un richiedente deve chiamare [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 7 e windows Server 2008 R2 e versioni precedenti (oppure in Windows 8 e windows Server 2012 e versioni successive, se non è necessaria la compatibilità RVSS):

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

    Quando si imposta in modo esplicito la sicurezza a livello COM di un richiedente con [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), è necessario eseguire le operazioni seguenti:

    -   Impostare il livello di autenticazione su almeno **\_ \_ \_ \_ connessione a livello di autenticazione C RPC**. Per una maggiore sicurezza, è consigliabile usare il **livello di autenticazione di RPC \_ C \_ \_ \_ PKT \_ privacy**.
    -   Impostare il livello di rappresentazione sull' **Identificazione del \_ \_ \_ livello \_ Imp C di RPC** , a meno che il processo del richiedente non debba consentire la rappresentazione per chiamate RPC o com specifiche che non sono correlate a VSS.

-   Consenti solo ai processi specificati l'accesso per chiamare il processo del richiedente.

    Un server COM (ad esempio un richiedente) che chiama [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) con un descrittore di sicurezza non **null** come primo parametro può usare il descrittore per configurare se stesso in modo da accettare le chiamate in ingresso solo dagli utenti che appartengono a un set di account specifico.

    Un richiedente deve garantire che i client COM in esecuzione con utenti validi siano autorizzati a chiamare il processo. Un richiedente che specifica un descrittore di sicurezza nel primo parametro deve consentire agli utenti seguenti di eseguire chiamate in ingresso nel processo del richiedente:

    -   Sistema locale
    -   Servizio locale

        **Windows XP:** Questo valore non è supportato fino a Windows Server 2003.

    -   Servizio di rete

        **Windows XP:** Questo valore non è supportato fino a Windows Server 2003.

    -   Membri del gruppo Administrators locale
    -   Membri del gruppo Backup Operators locale
    -   Utenti speciali specificati nel percorso del registro di sistema, con "1" come \_ valore DWORD reg

## <a name="explicitly-controlling-user-account-access-to-a-requester"></a>Controllo esplicito dell'accesso degli account utente a un richiedente

Ci sono casi in cui la limitazione dell'accesso a un richiedente ai processi in esecuzione come sistema locale o ai gruppi Administrators locale o operatori di backup locale può essere troppo restrittiva.

Un processo del richiedente specificato, ad esempio, potrebbe non essere in genere necessario per l'esecuzione con un account amministratore o operatore di backup. Per motivi di sicurezza, è preferibile non innalzare di livello artificialmente i privilegi dei processi per supportare VSS.

In questi casi, è necessario modificare la chiave del registro di sistema **HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** per indicare a VSS che un utente specificato è sicuro per l'esecuzione di un richiedente VSS.

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
                  MyDomain\MyUser = 2<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

Questo meccanismo può essere usato anche per limitare in modo esplicito l'esecuzione di un richiedente VSS a un utente altrimenti consentito. Nell'esempio seguente viene limitato l'accesso dall'account "ThatDomain \\ Administrator":

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

L' \\ amministratore di ThatDomain utente non sarà in grado di eseguire un richiedente VSS.

## <a name="performing-a-file-backup-of-the-system-state"></a>Esecuzione di un backup di file dello stato del sistema

Se un richiedente esegue il backup dello stato del sistema eseguendo il backup di singoli file anziché usare un'immagine del volume per il backup, deve chiamare le funzioni [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) e [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) per enumerare i collegamenti reali nei file che si trovano nelle directory seguenti:

-   Windows \\ system32 \\ WDI \\ perftrack\\
-   Windows \\ WINSXS\\

È possibile accedere a tali directory solo da membri del gruppo Administrators. Per questo motivo, tale richiedente deve essere eseguito con l'account di sistema o con un account utente membro del gruppo Administrators.

**Windows XP e Windows Server 2003:** Le funzioni [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) e [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) non sono supportate fino a Windows Vista e Windows Server 2008.

 

 
