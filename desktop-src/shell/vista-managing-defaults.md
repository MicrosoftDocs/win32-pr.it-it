---
description: In questo argomento vengono forniti fornitori di software indipendenti (ISV) con una guida rapida ai passaggi necessari per registrare e gestire le impostazioni predefinite dell'applicazione in Windows Vista e versioni successive. Sono disponibili collegamenti ad articoli più approfonditi sull'argomento di ogni sezione.
ms.assetid: 649eb20d-07d3-4209-abff-45fc50f05631
title: Gestione di applicazioni predefinite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de40d6c80aae4005fc015c08ef7bf2907289e795
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881538"
---
# <a name="managing-default-applications"></a>Gestione di applicazioni predefinite

La funzionalità **set Program Access and computer defaults** (SPAD) è stata aggiunta a Windows XP e versioni successive di Windows per gestire le impostazioni predefinite per computer. Oltre a SPAD, in Windows Vista è stato introdotto il concetto di applicazioni predefinite per utente e l'elemento **programmi predefiniti** nel pannello di controllo.

> [!IMPORTANT]
> Questo argomento non è applicabile a Windows 10. Il modo in cui le associazioni di file predefinite cambiano in Windows 10. Per ulteriori informazioni, vedere la sezione relativa alle **modifiche apportate al modo in cui Windows 10 gestisce le app predefinite** in [questo post](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

Le impostazioni predefinite per utente sono specifiche di un singolo account utente nel sistema. Se sono presenti impostazioni predefinite per utente, hanno la precedenza sui valori predefiniti per computer corrispondenti per tale account. A partire da Windows 8, il sistema di estendibilità per il tipo di file e le impostazioni predefinite del protocollo è rigorosamente per utente e i valori predefiniti per computer vengono ignorati. SPAD è stato modificato anche in Windows 8 per impostare le impostazioni predefinite per utente.

-   Nei sistemi che eseguono versioni di Windows precedenti a Windows 8, un account utente appena creato riceve i valori predefiniti per computer fino a quando non vengono stabilite le impostazioni predefinite per utente. In Windows Vista e versioni successive, gli utenti possono utilizzare l'elemento **programmi predefiniti** nel pannello di controllo per impostare o modificare le impostazioni predefinite per singolo utente. Inoltre, quando un'applicazione viene eseguita per la prima volta, è possibile impostare le impostazioni predefinite per utente utilizzando le linee guida seguenti nella sezione [prima esecuzione e impostazioni predefinite dell'applicazione](#application-first-run-and-defaults) .
-   Nei sistemi che eseguono Windows 8, un account utente appena creato si basa sulle impostazioni predefinite per singolo utente dall'inizio e l'impostazione di tali impostazioni predefinite alla prima esecuzione, come illustrato nella sezione relativa alla [prima esecuzione e le impostazioni predefinite dell'applicazione](#application-first-run-and-defaults) non sono più supportate.

Un'applicazione deve essere registrata sia con SPAD che con la funzionalità programmi predefiniti da offrire come programma predefinito in Windows Vista e versioni successive.

In questo argomento vengono forniti fornitori di software indipendenti (ISV) con una guida rapida ai passaggi necessari per registrare e gestire le impostazioni predefinite dell'applicazione in Windows Vista e versioni successive. Sono disponibili collegamenti ad articoli più approfonditi sull'argomento di ogni sezione.

-   [Elemento programmi predefiniti nel pannello di controllo](#default-programs-item-in-control-panel)
-   [Impostare l'accesso al programma e le impostazioni predefinite del computer](#set-program-access-and-computer-defaults)
    -   [Impostazione delle impostazioni predefinite in SPAD](#setting-defaults-in-spad)
    -   [Nascondi accesso in SPAD](#hide-access-in-spad)
-   [Registrazione per i punti di ingresso dell'applicazione](#registering-for-application-entry-points)
    -   [Apri con](#open-with)
    -   [Menu Start e barra avvio veloce](#start-menu-and-quick-launch-bar)
-   [Installazione e impostazioni predefinite dell'applicazione](#application-installation-and-defaults)
-   [Aggiornamenti e impostazioni predefinite dell'applicazione](#application-upgrades-and-defaults)
-   [Prima esecuzione e impostazioni predefinite dell'applicazione](#application-first-run-and-defaults)
-   [Verifica delle impostazioni predefinite e richiesta del consenso dell'utente](#verifying-defaults-and-asking-for-user-consent)
-   [Suggerimenti per la compatibilità delle applicazioni](#application-compatibility-tips)
    -   [Evitare di attivare la virtualizzazione Per-User](#avoid-triggering-per-user-virtualization)
    -   [Evitare gli avvisi o i blocchi di AppCompat da Program Compatibility Assistant](#avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant)
    -   [Supporto per le versioni precedenti del sistema operativo Windows](#support-for-previous-windows-operating-system-versions)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="default-programs-item-in-control-panel"></a>Elemento programmi predefiniti nel pannello di controllo

**Programmi predefiniti** è una funzionalità introdotta in Windows Vista, accessibile direttamente dal menu **Start** e dal pannello di controllo. Fornisce una nuova infrastruttura che funziona con privilegi utente standard (non elevati) ed è progettata per consentire a utenti e applicazioni di gestire le impostazioni predefinite per singolo utente. Per gli utenti, i programmi predefiniti offrono un modo unificato e facilmente accessibile per gestire i valori predefiniti, le associazioni di file e le impostazioni AutoPlay in tutte le applicazioni del sistema. Per le applicazioni, l'utilizzo dell'ambito per utente fornito dalle API dei programmi predefiniti offre i vantaggi seguenti:

-   **Nessuna elevazione**

    Un'applicazione non deve elevare i propri privilegi ai valori predefiniti delle attestazioni.

-   **Cittadinanza corretta**

    In un computer con più utenti, ogni utente può selezionare applicazioni predefinite diverse.

-   **Gestione predefinita**

    Le API dei programmi predefiniti offrono un meccanismo affidabile e coerente per controllare automaticamente lo stato predefinito e recuperare le impostazioni perse senza ricorrere alla scrittura diretta nel registro di sistema. Tuttavia, a partire da Windows 8, non è consigliabile che le applicazioni eseguano lo stato predefinito perché un'applicazione non può più modificare le impostazioni predefinite. tali modifiche possono essere apportate solo dall'utente.

Per consentire all'applicazione di gestire i valori predefiniti in modo efficiente, è necessario registrare l'applicazione come un potenziale programma predefinito. Per informazioni dettagliate sulla registrazione e sull'uso delle API dei programmi predefiniti, vedere [programmi predefiniti](default-programs.md).

I programmi predefiniti forniscono anche queste due funzionalità:

-   **Interfaccia utente delle impostazioni predefinite riutilizzabili**

    L'interfaccia utente di entrambe le impostazioni predefinite del programma (impostazione dei **programmi predefiniti**) e delle associazioni di file (**associare un tipo di file o un protocollo a un programma**) può essere riutilizzata e chiamata dall'interno di un'applicazione. Ciò consente alle applicazioni di offrire un'esperienza utente standard per la gestione delle impostazioni predefinite e di risparmiare agli ISV la necessità di sviluppare un'interfaccia utente personalizzata o equivalente.

-   **Inclusione di informazioni di URL e marketing**

    Nell'ambito della pagina **Imposta programmi predefiniti** dell'elemento **programmi predefiniti** nel pannello di controllo, un'applicazione può fornire informazioni di marketing e un collegamento al sito Web del fornitore. Questo URL è derivato dal certificato Authenticode con cui l'applicazione è stata firmata. In questo modo si evita l'utilizzo improprio e la sostituzione non autorizzata di questo collegamento. Se un'applicazione dispone di un certificato Authenticode che include un URL incorporato, l'interfaccia utente di Windows Visualizza l'URL incorporato. Gli ISV devono avvalersi di questa funzionalità per indirizzare gli utenti al proprio sito Web per gli aggiornamenti e altri download.

## <a name="set-program-access-and-computer-defaults"></a>Impostare l'accesso al programma e le impostazioni predefinite del computer

**Imposta accesso programma e impostazioni predefinite computer** (SPAD) consente agli amministratori di gestire le impostazioni predefinite a livello di computer ereditate da tutti i nuovi utenti del computer. Prima di Windows 8, SPAD consentiva anche agli amministratori di ripristinare le associazioni di file qualora venissero interrotti quando i programmi venivano rimossi dal sistema. Tuttavia, a partire da Windows 8, SPAD influiscono solo sui valori predefiniti specifici dell'utente.

Per ulteriori informazioni sulla registrazione di un'applicazione in SPAD, vedere [utilizzo di set Program Access e computer Defaults (SPAD)](cpl-setprogramaccess.md) e [registrazione di programmi con i tipi di client](reg-middleware-apps.md). Le sezioni seguenti illustrano le modifiche specifiche e le nuove raccomandazioni.

### <a name="setting-defaults-in-spad"></a>Impostazione delle impostazioni predefinite in SPAD

Le impostazioni predefinite per utente eseguono l'override delle impostazioni predefinite per computer.

-   **Prima di Windows 8**: le impostazioni predefinite impostate in SPAD (che sono per computer) non verranno visualizzate dagli utenti se sono impostate le impostazioni predefinite per utente corrispondenti. Se un utente non ha impostato un valore predefinito per utente, il sistema utilizza l'impostazione predefinita del computer corrispondente. I nuovi account utente in un computer ereditano inizialmente le impostazioni predefinite del computer. La prima volta che un utente esegue un'applicazione, l'applicazione deve richiedere all'utente di assegnare le impostazioni predefinite per singolo utente. Vedere la [prima esecuzione e le impostazioni predefinite dell'applicazione](#application-first-run-and-defaults).
-   A **partire da Windows 8**: tutte le impostazioni predefinite sono per utente e tutte le impostazioni predefinite per computer vengono ignorate. Le applicazioni non possono più impostare le scelte predefinite, quindi non possono passare l'utente tramite l'assegnazione di tali impostazioni predefinite.

Quando un'applicazione precedente a Windows 8 implementa **set come predefinito** in SPAD, è necessario seguire queste linee guida:

-   Le applicazioni devono richiedere solo le impostazioni predefinite a livello di computer tramite SPAD.
-   Le applicazioni *non* devono richiedere le impostazioni predefinite per utente tramite SPAD.

Quando un'applicazione Windows 8 implementa **set come predefinito** in SPAD, è necessario che registri i tipi di file e i protocolli nei [programmi predefiniti](default-programs.md), usando lo stesso nome dell'applicazione usato in SPAD. Ciò consente a una modifica in SPAD di riflettere come una modifica nella voce dei programmi predefiniti corrispondente per l'utente corrente.

### <a name="hide-access-in-spad"></a>Nascondi accesso in SPAD

È possibile accedere all'opzione Nascondi accesso per ogni possibile impostazione predefinita in SPAD in uno dei due modi seguenti:

-   Scegliere la categoria delle impostazioni predefinite **non Microsoft** , che consente di rimuovere l'accesso a tutte le impostazioni predefinite di Microsoft.
-   Scegliere la categoria **personalizzata** e deselezionare la casella **di controllo Abilita accesso al programma** .

In precedenza, una di queste azioni rimuoveva tutti i punti di ingresso alle applicazioni appropriate nel sistema. Linee guida specifiche per questa situazione dicono di rimuovere i tasti di scelta rapida e le icone dalle posizioni seguenti:

-   Desktop
-   Menu Start
-   Barra avvio veloce (solo Windows Vista e versioni precedenti)
-   Area delle notifiche
-   Menu di scelta rapida
-   Gruppo di attività cartella

I fornitori sono invitati a implementare queste linee guida nella funzione di callback Nascondi accesso dell'applicazione.

### <a name="alternate-hide-access-method-in-spad"></a>Metodo di accesso Hide alternativo in SPAD

Per alcune applicazioni legacy, un'implementazione completa di Hide Access potrebbe non essere pratica. Un metodo alternativo che ottiene lo stesso effetto, ma non è facilmente reversibile dall'utente, consiste nel disinstallare l'applicazione. Di seguito viene illustrato il comportamento di esempio e il codice di esempio per implementarlo.

L'esperienza utente consigliata per questa alternativa è la seguente:

-   Quando l'utente cancella la casella **Abilita l'accesso a questo programma** in SPAD, viene visualizzata l'interfaccia utente seguente.

    ![finestra di dialogo Vista su come nascondere l'accesso al programma](images/hideaccessvista.png)

-   Quando l'utente fa clic su **OK**, viene visualizzato l'elemento **programmi e funzionalità** nel pannello di controllo in modo che l'utente possa disinstallare l'applicazione.
-   Gli utenti di Windows XP devono essere presentati con la finestra di dialogo seguente.

    ![finestra di dialogo di Windows XP su come nascondere l'accesso al programma](images/hideaccessxp.png)

-   Quando l'utente di Windows XP fa clic su **OK**, viene visualizzata l'opzione **Installazione applicazioni** nel pannello di controllo in modo che l'utente possa disinstallare l'applicazione.

Il codice seguente fornisce un'implementazione riutilizzabile per la funzionalità Nascondi accesso, come descritto in precedenza. Può essere utilizzato in Windows XP, Windows Vista e Windows 7.


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



## <a name="registering-for-application-entry-points"></a>Registrazione per i punti di ingresso dell'applicazione

Un'applicazione può avere molti punti di ingresso all'interno del sistema operativo. Di seguito sono riportati i percorsi consigliati per i punti di ingresso:

-   Desktop
-   Menu Start
-   Barra avvio veloce (solo Windows Vista e versioni precedenti)
-   Area delle notifiche
-   Menu di scelta rapida
-   Gruppo di attività cartella

Questa sezione è incentrata su queste aree specifiche:

-   [Apri con](#open-with)
-   [Menu Start e barra avvio veloce](#start-menu-and-quick-launch-bar)

### <a name="open-with"></a>Apri con

Il menu di scelta rapida **Apri con** consente all'utente di selezionare un'applicazione in grado di gestire un tipo di file specifico. Quando è **aperto con** può essere usato per aprire un file con un'applicazione una sola volta, può anche essere usato per impostare il valore predefinito per l'estensione di file. Pertanto, un'applicazione deve sempre registrarsi per **aprirlo in** modo che gli utenti vengano presentati con tale applicazione come scelta. Le applicazioni possono registrare sia i tipi di file che i protocolli per **Apri con**. Le applicazioni che registrano i protocolli nel Framework dei programmi predefiniti vengono aggiunte automaticamente alle opzioni **Apri con** per i protocolli.

Per informazioni sulla registrazione per **Apri con**, vedere [Introduzione alle associazioni di file](fa-intro.md).

### <a name="start-menu-and-quick-launch-bar"></a>Menu Start e barra avvio veloce

Per diventare più individuabili per l'utente, le applicazioni possono aggiungere collegamenti a diverse posizioni in Windows. La posizione più comune per aggiungere un collegamento è il menu **Start** . In Windows Vista e versioni successive, un'applicazione crea un collegamento nella cartella nascosta% ProgramData% \\ Microsoft \\ Windows \\ Start menu \\ Programs da visualizzare nell'elenco di programmi del menu **Start** per tutti gli utenti. In genere, un'applicazione aggiunge una sottocartella che contiene il collegamento.

Per i programmi browser e di posta elettronica, il menu **Start** di Windows Vista presenta anche due collegamenti dedicati all'esterno dell'elenco di programmi, con intitolato **Internet** e **posta elettronica**. Dopo che un'applicazione è stata registrata per tali categorie, il Framework dei programmi predefinito può gestire gli elementi avviati tramite tali collegamenti.

> [!Note]  
> I collegamenti del menu **Start** dedicato a **Internet** e alla **posta elettronica** non sono più presenti in Windows 7.

 

Per incrementare ulteriormente l'individuabilità, le applicazioni possono anche aggiungere collegamenti al desktop e alla barra di avvio veloce. Prima di aggiungere un'icona al menu **Start** , al desktop o alla barra di avvio veloce, le applicazioni devono chiedere all'utente l'autorizzazione (in genere durante l'installazione o alla prima esecuzione).

> [!Note]  
> La barra avvio veloce non è più disponibile a partire da Windows 7. L'alternativa di Windows 7 prevede che l'applicazione sia stata aggiunta alla barra delle applicazioni, ma non può essere eseguita a livello di codice poiché è esclusivamente una scelta utente.

 

Per altre informazioni, vedere gli argomenti seguenti:

-   [Come registrare un browser Internet o un client di posta elettronica con il menu Start di Windows](start-menu-reg.md)
-   [Registrazione di programmi con tipi di client](reg-middleware-apps.md)

## <a name="application-installation-and-defaults"></a>Installazione e impostazioni predefinite dell'applicazione

Le procedure di installazione dell'applicazione non sono state modificate in maniera sostanziale rispetto a Windows XP, fatta eccezione per le nuove linee guida per i sistemi in cui sono in esecuzione versioni di Windows precedenti a Windows 8: è necessario impostare i valori predefiniti per computer al momento dell'installazione, ma non impostare le impostazioni predefinite per utente fino a quando l'utente non esegue prima l'applicazione. (Vedere la [prima esecuzione dell'applicazione e le impostazioni predefinite](#application-first-run-and-defaults)). Le applicazioni non devono impostare le impostazioni predefinite per utente durante l'installazione, perché in alcuni casi la persona che installa l'applicazione non è l'utente previsto. A partire da Windows 8, i valori predefiniti per computer non sono supportati e le applicazioni non possono modificare le impostazioni predefinite per utente.

Durante l'installazione, un'applicazione deve copiare i file binari nel disco rigido e scrivere i relativi ProgID nel registro di sistema. L'applicazione deve inoltre registrarsi per i programmi predefiniti e **aprirla con** in questo momento per ogni associazione di file che è un candidato a gestire. L'applicazione può usare la sottochiave **OpenWithProgids** per eseguire la registrazione con **Open con**.

Per altre informazioni, vedere gli argomenti seguenti:

-   [Programmi predefiniti](default-programs.md)
-   [Introduzione alle associazioni di file](fa-intro.md)

## <a name="application-upgrades-and-defaults"></a>Aggiornamenti e impostazioni predefinite dell'applicazione

Molte applicazioni hanno la possibilità di eseguire l'aggiornamento nel tempo. Questa procedura di aggiornamento non deve modificare lo stato delle impostazioni predefinite per singolo utente, perché la modifica sarebbe imprevista per l'utente. Tuttavia, è accettabile che un'applicazione verifichi le associazioni di file a livello di computer e le ripristini se sono state danneggiate.

## <a name="application-first-run-and-defaults"></a>Prima esecuzione e impostazioni predefinite dell'applicazione

> [!Note]  
> A partire da Windows 8, il sistema gestisce questa procedura per conto di tutte le applicazioni. Le applicazioni non possono più eseguire query e modificare le impostazioni predefinite. Questa operazione può essere eseguita solo dall'utente. Pertanto, le applicazioni non devono tentare di eseguire una query per l'impostazione predefinita corrente o modificare il valore predefinito tramite qualsiasi meccanismo. Tuttavia, le applicazioni possono fornire un punto di ingresso ai programmi predefiniti nel pannello di controllo chiamando il metodo [**LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) dell'interfaccia [**IApplicationAssociationRegistrationUI**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui) .

 

Con l'introduzione delle impostazioni predefinite per utente in Windows Vista, è importante che le applicazioni che si contendono le estensioni di file più diffuse forniscano tutte un'esperienza utente comune per richiedere queste estensioni. Poiché queste impostazioni predefinite sono ora impostate nel contesto dell'utente, devono presentarsi come una possibilità predefinita solo quando l'utente esegue il programma dopo l'installazione.

Le linee guida per la definizione delle impostazioni predefinite per utente sono le seguenti: quando un'applicazione viene eseguita per la prima volta per un utente specifico, l'applicazione deve richiedere le preferenze utente per le impostazioni predefinite e le associazioni di file.

L'interfaccia utente consigliata deve fornire due opzioni chiare all'utente:

1.  Accettare tutti i valori predefiniti che l'applicazione desidera richiedere. Questa opzione può anche impostare altre proprietà predefinite dell'applicazione, ad esempio la privacy o le impostazioni di aggiornamento automatico. Questa opzione consente all'applicazione di richiedere tutte le impostazioni predefinite registrate.
2.  Personalizzare accettando o non accettando singolarmente le selezioni predefinite e le impostazioni del programma. Questa opzione presenta un'ulteriore interfaccia utente che consente all'utente di eseguire scelte granulari per le opzioni predefinite.

Per ulteriori informazioni, vedere [programmi predefiniti](default-programs.md).

## <a name="verifying-defaults-and-asking-for-user-consent"></a>Verifica delle impostazioni predefinite e richiesta del consenso dell'utente

> [!Note]  
> Questa operazione non è supportata a partire da Windows 8.

 

Dopo che un'applicazione è stata registrata con i programmi predefiniti in Windows Vista e versioni successive, alcune API diventano disponibili per l'applicazione. Ad esempio, un'applicazione potrebbe dover controllare se si tratta del programma predefinito. L'interfaccia [**IApplicationAssociationRegistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) fornisce i metodi per eseguire questa operazione.

Qualsiasi applicazione che desidera richiedere le impostazioni predefinite deve prima chiedere all'utente e non richiedere le impostazioni predefinite senza autorizzazione. All'utente deve essere richiesto se desidera che l'applicazione venga impostata come predefinita o lasci l'impostazione predefinita corrente. Dovrebbe inoltre essere presente un'opzione in modo da non dover più porre questa domanda dopo che l'utente ha scelto.

Per ulteriori informazioni, vedere [programmi predefiniti](default-programs.md).

## <a name="application-compatibility-tips"></a>Suggerimenti per la compatibilità delle applicazioni

In questa sezione vengono forniti alcuni suggerimenti per la compatibilità delle applicazioni correlati all'esperienza dei programmi predefiniti di Windows.

### <a name="avoid-triggering-per-user-virtualization"></a>Evitare di attivare la virtualizzazione Per-User

Con l'ambiente controllo dell'account utente, le applicazioni devono essere sempre eseguite con diritti utente standard per la migliore esperienza con i clienti. Per motivi di sicurezza, le applicazioni con un livello di privilegi utente standard sono bloccate dalla scrittura in determinate parti del registro di sistema e in alcuni file di sistema. Windows Vista e le versioni successive di Windows forniscono un livello di compatibilità delle applicazioni temporanee (AppCompat) per aiutare le applicazioni a eseguire la transizione. I tentativi bloccati di scrivere nel registro di sistema o nei file di sistema sono "virtualizzati" in modo che l'applicazione continui a essere eseguita, ma le aree sensibili del sistema non vengono modificate. Tuttavia, le applicazioni non devono basarsi sulla tecnologia AppCompat come soluzione a lungo termine. Al contrario, le applicazioni devono utilizzare i numerosi strumenti disponibili per verificare che possano essere eseguiti correttamente con diritti utente standard. Per eseguire questa operazione, potrebbe essere necessaria una riprogrammazione dell'applicazione, che tuttavia deve essere eseguita per la compatibilità a lungo termine.

### <a name="avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant"></a>Evitare gli avvisi o i blocchi di AppCompat da Program Compatibility Assistant

Il programma Compatibility Assistant (PCA) viene fornito in Windows Vista e versioni successive. Lo scopo è quello di fornire un metodo automatizzato per garantire un funzionamento ottimale dei programmi meno recenti con problemi di compatibilità. La PCA monitora i programmi per i problemi noti. Se viene rilevato un problema, viene inviata una notifica all'utente del problema e viene offerta l'applicazione di soluzioni valide prima che l'utente esegua nuovamente il programma. Per evitare di visualizzare questi avvisi o blocchi, gli ISV devono utilizzare i numerosi strumenti disponibili per garantire la compatibilità delle applicazioni con Windows Vista, Windows 7 e versioni successive.

### <a name="support-for-previous-windows-operating-system-versions"></a>Supporto per le versioni precedenti del sistema operativo Windows

L'infrastruttura dei programmi predefinita non è disponibile in alcun sistema operativo Windows prima di Windows Vista. Pertanto, quando le applicazioni passano alla nuova infrastruttura dei programmi predefiniti, devono mantenere il codice predefinito dell'applicazione precedente per mantenere la compatibilità con le versioni precedenti di Windows. Un'applicazione deve eseguire un controllo della versione del sistema operativo come parte dell'installazione per determinare quale applicazione-impostazione predefinita del codice da eseguire.

Per supportare un aggiornamento da Windows XP a Windows Vista o versione successiva, le applicazioni devono aggiungere tutte le voci del registro di sistema necessarie per i programmi predefiniti anche durante l'installazione di in un computer che esegue Windows XP. La registrazione non avrà alcun effetto su un computer che esegue Windows XP, ma se il computer viene aggiornato in un secondo momento, l'applicazione sarà già registrata e potrà sfruttare i vantaggi offerti dal Framework.

Per ulteriori informazioni, vedere [**osVersionInfo**](/windows/win32/api/winnt/ns-winnt-osversioninfoa).

## <a name="additional-resources"></a>Risorse aggiuntive

-   [Introduzione alle associazioni di file](fa-intro.md)
-   [Come registrare un browser Internet o un client di posta elettronica con il menu Start di Windows](start-menu-reg.md)
-   [Registrazione di un'applicazione in uno schema URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure consigliate per le associazioni di file](fa-best-practices.md)
</dt> <dt>

[Scenario di esempio di associazione di file](fa-sample-scenarios.md)
</dt> <dt>

[Programmi predefiniti](default-programs.md)
</dt> <dt>

[Utilizzo di set Program Access e computer Defaults (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
