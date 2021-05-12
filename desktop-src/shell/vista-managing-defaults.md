---
description: Questo argomento fornisce ai fornitori di software indipendenti (ISV) una guida rapida ai passaggi necessari per registrare e gestire le impostazioni predefinite delle applicazioni in Windows Vista e versioni successive. Vengono forniti collegamenti ad articoli più approfonditi sull'argomento di ogni sezione.
ms.assetid: 649eb20d-07d3-4209-abff-45fc50f05631
title: Gestione delle applicazioni predefinite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc146858d197b96229edda49ac2e7249db51bf4c
ms.sourcegitcommit: 4d639170c06864e47ef66b2cfe6ca3d07cce0b02
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109812826"
---
# <a name="managing-default-applications"></a>Gestione delle applicazioni predefinite

La **funzionalità Set Program Access and Computer Defaults** (SPAD) è stata aggiunta a Windows XP e versioni successive di Windows per gestire le impostazioni predefinite per computer. Oltre a SPAD, Windows Vista ha introdotto il concetto di applicazioni predefinite per utente e l'elemento **Programmi** predefiniti in Pannello di controllo.

> [!IMPORTANT]
> Questo argomento non si applica a Windows 10. Il funzionamento delle associazioni di file predefinite è stato modificato in Windows 10. Per altre informazioni, vedere la sezione Modifiche al modo in cui Windows 10 **le app predefinite** in questo [post.](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)

 

Le impostazioni predefinite per utente sono specifiche di un singolo account utente nel sistema. Se sono presenti impostazioni predefinite per utente, hanno la precedenza sulle impostazioni predefinite per computer corrispondenti per tale account. A Windows 8, il sistema di estendibilità per le impostazioni predefinite del tipo di file e del protocollo è rigorosamente per utente e le impostazioni predefinite per computer vengono ignorate. SPAD è stato modificato anche in Windows 8 per impostare le impostazioni predefinite per utente.

-   Nei sistemi che eseguono versioni di Windows precedenti a Windows 8, un account utente appena creato riceve le impostazioni predefinite per ogni computer fino a quando non vengono stabilite le impostazioni predefinite per utente. In Windows Vista e versioni  successive, gli utenti possono usare l'elemento Programmi predefiniti Pannello di controllo per impostare o modificare le impostazioni predefinite per utente. Inoltre, quando un'applicazione viene eseguita per la prima volta, è possibile impostare le impostazioni predefinite per utente usando le linee guida riportate nella sezione [Application First Run and Defaults](#application-first-run-and-defaults) (Impostazioni predefinite e prima esecuzione dell'applicazione).
-   Nei sistemi che eseguono Windows 8, un account utente appena creato si basa sulle impostazioni predefinite per utente dall'inizio e l'impostazione di tali impostazioni predefinite alla prima esecuzione, come illustrato nella sezione Application [First Run and Defaults](#application-first-run-and-defaults) (Prima esecuzione dell'applicazione e impostazioni predefinite) non è più supportata.

Un'applicazione deve registrarsi sia con SPAD che con la funzionalità Programmi predefiniti per essere offerta come programma predefinito in Windows Vista e versioni successive.

Questo argomento fornisce ai fornitori di software indipendenti (ISV) una guida rapida ai passaggi necessari per registrare e gestire le impostazioni predefinite delle applicazioni in Windows Vista e versioni successive. Vengono forniti collegamenti ad articoli più dettagliati sull'argomento di ogni sezione.

-   [Elemento Programmi predefiniti in Pannello di controllo](#default-programs-item-in-control-panel)
-   [Impostare l'accesso ai programmi e le impostazioni predefinite del computer](#set-program-access-and-computer-defaults)
    -   [Impostazione dei valori predefiniti in SPAD](#setting-defaults-in-spad)
    -   [Nascondere l'accesso in SPAD](#hide-access-in-spad)
-   [Registrazione per i punti di ingresso dell'applicazione](#registering-for-application-entry-points)
    -   [Apri con](#open-with)
    -   [Menu Start e barra Avvio veloce avvio](#start-menu-and-quick-launch-bar)
-   [Installazione dell'applicazione e impostazioni predefinite](#application-installation-and-defaults)
-   [Aggiornamenti e impostazioni predefinite dell'applicazione](#application-upgrades-and-defaults)
-   [Application First Run and Defaults](#application-first-run-and-defaults)
-   [Verifica delle impostazioni predefinite e richiesta del consenso dell'utente](#verifying-defaults-and-asking-for-user-consent)
-   [Suggerimenti sulla compatibilità delle applicazioni](#application-compatibility-tips)
    -   [Evitare l'attivazione Per-User virtualizzazione](#avoid-triggering-per-user-virtualization)
    -   [Evitare avvisi o blocchi di AppCompat da Assistente compatibilità programmi](#avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant)
    -   [Supporto per le versioni precedenti del sistema operativo Windows](#support-for-previous-windows-operating-system-versions)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="default-programs-item-in-control-panel"></a>Elemento Programmi predefiniti in Pannello di controllo

**Programmi predefiniti** è una funzionalità introdotta in Windows Vista, accessibile direttamente dal menu **Start** e Pannello di controllo. Fornisce una nuova infrastruttura che funziona con privilegi utente standard (non elevati) ed è progettata per consentire a utenti e applicazioni di gestire le impostazioni predefinite per utente. Per gli utenti, Programmi predefiniti offre un modo unificato e facilmente accessibile per gestire impostazioni predefinite, associazioni di file e riproduzione automatica in tutte le applicazioni del sistema. Per le applicazioni, l'uso dell'ambito per utente fornito dalle API Programmi predefiniti offre i vantaggi seguenti:

-   **Nessuna elevazione dei privilegi**

    Un'applicazione non deve elevare i propri privilegi per richiedere i valori predefiniti.

-   **Buona cittadinanza**

    In un computer con più utenti ogni utente può selezionare applicazioni predefinite diverse.

-   **Gestione predefinita**

    Le API programmi predefinite offrono un meccanismo affidabile e coerente per il controllo automatico dello stato predefinito e il recupero delle impostazioni perse senza dover ricorrere alla scrittura diretta nel Registro di sistema. Tuttavia, a Windows 8, non è consigliabile che le applicazioni eseere query sullo stato predefinito perché un'applicazione non può più modificare le impostazioni predefinite. Tali modifiche possono essere apportate solo dall'utente.

Per consentire all'applicazione di gestire in modo efficace le impostazioni predefinite, è necessario registrare l'applicazione come programma predefinito potenziale. Per informazioni dettagliate sulla registrazione e sull'uso delle API Programmi predefiniti, vedere [Programmi predefiniti](default-programs.md).

Programmi predefiniti offre anche queste due funzionalità:

-   **Interfaccia utente delle impostazioni predefinite riutilizzabili**

    L'interfaccia utente di entrambe le impostazioni predefinite del programma **(** Impostare i programmi predefiniti ) e le associazioni di file ( Associare un tipo di file o un protocollo **a un programma**) può essere riutilizzata e chiamata dall'interno di un'applicazione. Ciò consente alle applicazioni di offrire un'esperienza utente standard per la gestione delle impostazioni predefinite e di non dover sviluppare un'interfaccia utente personalizzata o equivalente.

-   **Inclusione di URL e informazioni di marketing**

    Come parte della pagina **Imposta** i  programmi predefiniti dell'elemento Programmi predefiniti in Pannello di controllo, un'applicazione può fornire informazioni di marketing e un collegamento al sito Web del fornitore. Questo URL deriva dal certificato Authenticode con cui l'applicazione è stata firmata. Ciò impedisce l'uso improprio e la sostituzione non autorizzata di questo collegamento. Se un'applicazione ha un certificato Authenticode che include un URL incorporato, l'interfaccia utente di Windows visualizza tale URL incorporato. Gli ISV devono sfruttare questa funzionalità per indirizzare gli utenti al proprio sito Web per gli aggiornamenti e altri download.

## <a name="set-program-access-and-computer-defaults"></a>Impostare l'accesso ai programmi e le impostazioni predefinite del computer

**L'impostazione dell'accesso** ai programmi e delle impostazioni predefinite del computer consente agli amministratori di gestire le impostazioni predefinite a livello di computer ereditate da tutti i nuovi utenti del computer. Prima di Windows 8, SPAD consente anche agli amministratori di ripristinare le associazioni di file in caso di problemi quando i programmi vengono rimossi dal sistema. Tuttavia, a Windows 8, SPAD influisce solo sulle impostazioni predefinite specifiche dell'utente.

Per altre informazioni sulla registrazione di un'applicazione in SPAD, vedere Working [with Set Program Access and Computer Defaults (SPAD) e](cpl-setprogramaccess.md) [Registering Programs with Client Types](reg-middleware-apps.md). Le modifiche specifiche e le nuove raccomandazioni sono illustrate nelle sezioni seguenti.

### <a name="setting-defaults-in-spad"></a>Impostazione dei valori predefiniti in SPAD

Le impostazioni predefinite per utente sostituiscono le impostazioni predefinite per computer.

-   **Prima Windows 8:** le impostazioni predefinite impostate in SPAD (che sono per computer) non verranno visibili agli utenti se sono impostate le impostazioni predefinite per utente corrispondenti. Se un utente non ha impostato un valore predefinito per utente, il sistema usa il valore predefinito del computer corrispondente. I nuovi account utente in un computer ereditano inizialmente le impostazioni predefinite del computer. La prima volta che un utente esegue un'applicazione, l'applicazione deve richiedere all'utente di assegnare le impostazioni predefinite per utente. Vedere [Application First Run (Prima esecuzione dell'applicazione) e Defaults (Impostazioni predefinite).](#application-first-run-and-defaults)
-   **A Windows 8:** tutte le impostazioni predefinite sono per utente e qualsiasi impostazione predefinita per computer viene ignorata. Le applicazioni non possono più impostare scelte predefinite, quindi non possono illustrare all'utente l'assegnazione di tali impostazioni predefinite.

Quando un'applicazione pre-Windows 8 implementa **Imposta come** predefinito in SPAD, è necessario seguire queste linee guida:

-   Le applicazioni devono richiedere solo le impostazioni predefinite a livello di computer tramite SPAD.
-   Le applicazioni *non devono* richiedere impostazioni predefinite per utente tramite SPAD.

Quando un'Windows 8 implementa **Imposta** come predefinita in SPAD, deve registrare i relativi tipi di file e protocolli in [Programmi](default-programs.md)predefiniti , usando lo stesso nome dell'applicazione usato in SPAD. In questo modo una modifica in SPAD viene riflessa come modifica nella voce Programmi predefiniti corrispondente per l'utente corrente.

### <a name="hide-access-in-spad"></a>Nascondere l'accesso in SPAD

L'opzione nascondi accesso per ogni possibile impostazione predefinita in SPAD è accessibile in uno dei due modi seguenti:

-   Scegliere la **categoria di impostazioni predefinite non Microsoft,** che rimuove l'accesso a tutte le impostazioni predefinite di Microsoft.
-   Scegliere la **categoria Personalizzata** e deselezionare la casella di controllo **Abilita** accesso al programma.

In precedenza, l'esecuzione di una di queste azioni ha rimosso tutti i punti di ingresso per le applicazioni appropriate nel sistema. Linee guida specifiche per questa situazione, ad esempio, per rimuovere i collegamenti e le icone dalle posizioni seguenti:

-   Desktop
-   Menu Start
-   Avvio veloce barra (solo Windows Vista e versioni precedenti)
-   Area delle notifiche
-   Menu di scelta rapida
-   Banda attività cartella

I fornitori sono invitati a implementare queste linee guida nella funzione di callback Nascondi accesso dell'applicazione.

### <a name="alternate-hide-access-method-in-spad"></a>Metodo di accesso Nascondi alternativo in SPAD

Per alcune applicazioni legacy, un'implementazione completa di Nascondi accesso potrebbe non essere pratica. Un metodo alternativo che ottiene lo stesso effetto, ma non è facilmente reversibile dall'utente, è disinstallare l'applicazione. Di seguito viene illustrato il comportamento di esempio e il codice di esempio per implementare questa funzionalità.

L'esperienza utente consigliata per questa alternativa è la seguente:

-   Quando l'utente deseleziona la **casella Abilita l'accesso** a questo programma in SPAD, viene visualizzata l'interfaccia utente seguente.

    ![Finestra di dialogo vista su come nascondere l'accesso al programma](images/hideaccessvista.png)

-   Quando l'utente fa  clic **su OK,** viene visualizzato l'elemento Programmi e funzionalità Pannello di controllo in modo che l'utente possa disinstallare l'applicazione.
-   Gli utenti di Windows XP devono essere presentati con la finestra di dialogo seguente.

    ![finestra di dialogo di Windows XP su come nascondere l'accesso al programma](images/hideaccessxp.png)

-   Quando l'utente di Windows  XP fa clic su **OK,** viene visualizzato l'elemento Installazione applicazioni in Pannello di controllo in modo che l'utente possa disinstallare l'applicazione.

Il codice seguente fornisce un'implementazione riutilizzabile per la funzionalità Nascondi accesso, come descritto in precedenza. Può essere usato in Windows XP, Windows Vista e Windows 7.


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
-   Avvio veloce barra (solo Windows Vista e versioni precedenti)
-   Area delle notifiche
-   Menu di scelta rapida
-   Banda attività cartella

Questa sezione è incentrata su queste aree specifiche:

-   [Apri con](#open-with)
-   [Menu Start e barra Avvio veloce avvio](#start-menu-and-quick-launch-bar)

### <a name="open-with"></a>Apri con

Il menu **di scelta** rapida Apri con consente all'utente di selezionare un'applicazione in grado di gestire un tipo di file specifico. Anche **se l'opzione** Apri con può essere usata una sola volta per aprire un file con un'applicazione, può essere usata anche per impostare l'impostazione predefinita per tale estensione di file. Pertanto, un'applicazione deve sempre registrarsi **per Apri con** in modo che agli utenti sia presentata l'applicazione come scelta. Le applicazioni possono registrare sia i tipi di file che i protocolli **per l'apertura con**. Le applicazioni che registrano protocolli nel framework Programmi predefiniti vengono aggiunte automaticamente alle **opzioni Apri** con per i protocolli.

Per informazioni sulla registrazione per Apri **con**, vedere [Introduzione alle associazioni di file.](fa-intro.md)

### <a name="start-menu-and-quick-launch-bar"></a>Menu Start e barra Avvio veloce comandi

Per diventare più individuabili per l'utente, le applicazioni possono aggiungere collegamenti a varie posizioni in Windows. La posizione più comune in cui aggiungere un collegamento è il menu **Start.** In Windows Vista e versioni successive un'applicazione crea un collegamento nella cartella nascosta %ProgramData% Programmi del menu Start di Microsoft Windows da visualizzare nell'elenco dei programmi del menu Start per tutti \\ \\ gli \\ \\ utenti.  In genere, un'applicazione aggiunge una sottocartella che contiene il collegamento.

Per i programmi browser e di posta elettronica, il menu **Start** di Windows Vista presenta anche due collegamenti dedicati all'esterno dell'elenco dei programmi, in formato canonico **Internet** **e Posta elettronica.** Dopo la registrazione di un'applicazione per tali categorie, il framework Programmi predefiniti può gestire gli elementi avviati tramite tali collegamenti.

> [!Note]  
> I collegamenti **al** menu **Start** dedicato a **Internet** e posta elettronica non sono più presenti a partire da Windows 7.

 

Per aumentare ulteriormente l'individuabilità, le applicazioni possono anche aggiungere collegamenti al desktop e Avvio veloce barra. Le applicazioni devono chiedere all'utente l'autorizzazione (in genere durante l'installazione o alla prima esecuzione) prima di aggiungere un'icona al menu **Start,** al desktop o Avvio veloce barra.

> [!Note]  
> La Avvio veloce non è più disponibile a causa di Windows 7. L'alternativa di Windows 7 consiste nell'aggiungere l'applicazione alla barra delle applicazioni, ma l'aggiunta non può essere eseguita a livello di codice perché è strettamente una scelta dell'utente.

 

Per altre informazioni, vedere gli argomenti seguenti:

-   [Come registrare un browser Internet o un client di posta elettronica con il menu Start di Windows](start-menu-reg.md)
-   [Registrazione di programmi con tipi client](reg-middleware-apps.md)

## <a name="application-installation-and-defaults"></a>Installazione dell'applicazione e impostazioni predefinite

Le procedure di installazione delle applicazioni non sono state fondamentalmente modificate rispetto a Windows XP, ad eccezione di una nuova linea guida per i sistemi che eseguono versioni di Windows precedenti a Windows 8: prendere le impostazioni predefinite per ogni computer in fase di installazione, ma non impostare le impostazioni predefinite per utente fino a quando l'utente non esegue per la prima volta l'applicazione. Vedere [Application First Run and Defaults](#application-first-run-and-defaults)(Prima esecuzione dell'applicazione e impostazioni predefinite). Le applicazioni non devono impostare le impostazioni predefinite per utente durante l'installazione perché in alcune situazioni la persona che installa l'applicazione non è l'utente previsto. Al Windows 8, le impostazioni predefinite per computer non sono supportate e le applicazioni non possono modificare le impostazioni predefinite per utente.

Durante l'installazione, un'applicazione deve copiare i relativi file binari nel disco rigido e scrivere i relativi ProgID nel Registro di sistema. L'applicazione deve anche registrarsi per Programmi predefiniti e **Apri** con in questo momento per ogni associazione di file che è possibile gestire. L'applicazione può usare la **sottochiave OpenWithProgIds** per eseguire la registrazione con **Open With.**

Per altre informazioni, vedere gli argomenti seguenti:

-   [Programmi predefiniti](default-programs.md)
-   [Introduzione alle associazioni di file](fa-intro.md)

## <a name="application-upgrades-and-defaults"></a>Aggiornamenti e impostazioni predefinite dell'applicazione

Molte applicazioni hanno la possibilità di aggiornarsi nel tempo. Questa procedura di aggiornamento non deve modificare lo stato delle impostazioni predefinite per utente perché tale modifica sarebbe imprevista per l'utente. Tuttavia, è accettabile per un'applicazione controllare le associazioni di file a livello di computer e ripristinarle se sono state danneggiate.

## <a name="application-first-run-and-defaults"></a>Application First Run and Defaults

> [!Note]  
> Al Windows 8, il sistema gestisce questa procedura per conto di tutte le applicazioni. Le applicazioni stesse non possono più eseguire query e modificare le impostazioni predefinite. Solo l'utente può eseguire questa operazione. Pertanto, le applicazioni non devono tentare di eseguire una query per l'impostazione predefinita corrente o di modificare tale impostazione predefinita tramite qualsiasi meccanismo. Tuttavia, le applicazioni possono fornire un punto di ingresso ai programmi predefiniti nel Pannello di controllo chiamando il metodo [**LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) [**dell'interfaccia IApplicationAssociationRegistrationUI.**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

 

Con l'introduzione delle impostazioni predefinite per utente in Windows Vista, è importante che le applicazioni che contestano le estensioni di file più comuni ofnno un'esperienza utente comune per richiedere queste estensioni. Poiché queste impostazioni predefinite sono ora impostate nel contesto dell'utente, devono presentarsi come possibilità predefinita solo quando l'utente esegue il programma dopo l'installazione.

La linea guida per stabilire le impostazioni predefinite per utente è la seguente: quando un'applicazione viene eseguita per la prima volta per un utente specifico, tale applicazione deve richiedere preferenze utente per le impostazioni predefinite e le associazioni di file per se stessa.

L'interfaccia utente consigliata deve fornire due scelte chiare all'utente:

1.  Accettare tutte le impostazioni predefinite che l'applicazione vuole richiedere. Questa opzione può anche impostare altre proprietà predefinite dell'applicazione, ad esempio la privacy o le impostazioni di aggiornamento automatico. Questa opzione consente all'applicazione di richiedere tutte le impostazioni predefinite registrate.
2.  Personalizzare accettando o meno le selezioni predefinite e le impostazioni del programma singolarmente. Questa opzione presenta un'ulteriore interfaccia utente che consente all'utente di effettuare scelte granulari per le opzioni predefinite.

Per altre informazioni, vedere [Programmi predefiniti](default-programs.md).

## <a name="verifying-defaults-and-asking-for-user-consent"></a>Verifica delle impostazioni predefinite e richiesta del consenso dell'utente

> [!Note]  
> Questa operazione non è supportata a Windows 8.

 

Dopo la registrazione di un'applicazione con Programmi predefiniti in Windows Vista e versioni successive, alcune API diventano disponibili per l'applicazione. Ad esempio, un'applicazione potrebbe dover controllare se è il programma predefinito. [**L'interfaccia IApplicationAssociationRegistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) fornisce metodi a tale scopo.

Tutte le applicazioni che vogliono richiedere i valori predefiniti devono prima chiedere all'utente e non richiedere mai i valori predefiniti senza autorizzazione. All'utente deve essere chiesto se si vuole impostare l'applicazione come predefinita o lasciare l'impostazione predefinita corrente. Dovrebbe anche essere disponibile un'opzione per non rispondere a questa domanda dopo che l'utente ha scelto.

Per altre informazioni, vedere [Programmi predefiniti](default-programs.md).

## <a name="application-compatibility-tips"></a>Suggerimenti per la compatibilità delle applicazioni

In questa sezione vengono forniti alcuni suggerimenti sulla compatibilità delle applicazioni correlati all'esperienza Programmi predefiniti in Windows.

### <a name="avoid-triggering-per-user-virtualization"></a>Evitare l'attivazione Per-User virtualizzazione

Con l'ambiente di controllo dell'account utente, le applicazioni devono sempre essere eseguite con solo diritti utente standard per la migliore esperienza del cliente. Per motivi di sicurezza, alle applicazioni con un livello di privilegio utente standard viene impedito di scrivere in determinate parti del Registro di sistema e in determinati file di sistema. Windows Vista e versioni successive di Windows forniscono un livello di compatibilità delle applicazioni temporaneo (AppCompat) per consentire alle applicazioni di eseguire la transizione. I tentativi bloccati di scrittura nel Registro di sistema o nei file di sistema vengono "virtualizzati" in modo che l'applicazione continui a essere eseguita, ma le aree sensibili del sistema non vengono modificate. Tuttavia, le applicazioni non devono basarsi sulla tecnologia AppCompat come soluzione a lungo termine. Al contrario, le applicazioni devono usare i numerosi strumenti disponibili per verificare che possano essere eseguite correttamente con diritti utente standard. A tale scopo, potrebbe essere necessaria una riprogrammazione dell'applicazione, ma questa operazione deve essere eseguita nell'interesse della compatibilità a lungo termine.

### <a name="avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant"></a>Evitare avvisi o blocchi di AppCompat da Assistente compatibilità programmi

Program Compatibility Assistant (PCA) è disponibile in Windows Vista e versioni successive. Lo scopo è fornire un metodo automatizzato per migliorare il funzionamento dei programmi meno recenti con problemi di compatibilità. PcA monitora i programmi per i problemi noti. Se viene rilevato un problema, invia una notifica all'utente e offre di applicare soluzioni efficaci prima che l'utente eserciti nuovamente il programma. Per evitare la visualizzazione di questi avvisi o blocchi, gli ISV devono usare i numerosi strumenti disponibili per assicurarsi che le applicazioni siano compatibili con Windows Vista, Windows 7 e versioni successive.

### <a name="support-for-previous-windows-operating-system-versions"></a>Supporto per le versioni precedenti del sistema operativo Windows

L'infrastruttura Programmi predefiniti non è disponibile in alcun sistema operativo Windows prima di Windows Vista. Pertanto, quando le applicazioni passano alla nuova infrastruttura Programmi predefiniti, devono mantenere il codice predefinito dell'applicazione precedente per mantenere la compatibilità con le versioni precedenti di Windows. Un'applicazione deve eseguire un controllo della versione del sistema operativo come parte dell'installazione per determinare il codice predefinito dell'applicazione da eseguire.

Per supportare un aggiornamento da Windows XP a Windows Vista o versioni successive, le applicazioni devono aggiungere tutte le voci del Registro di sistema necessarie per i programmi predefiniti anche quando vengono installate in un computer che esegue Windows XP. La registrazione non avrà alcun effetto su un computer che esegue Windows XP, ma se il computer viene aggiornato in un secondo momento, l'applicazione sarà già registrata e sarà in grado di sfruttare i vantaggi del framework.

Per altre informazioni, vedere [**OSVERSIONINFO**](/windows/win32/api/winnt/ns-winnt-osversioninfoa).

## <a name="additional-resources"></a>Risorse aggiuntive

-   [Introduzione alle associazioni di file](fa-intro.md)
-   [Come registrare un browser Internet o un client di posta elettronica con il menu Start di Windows](start-menu-reg.md)
-   [Registrazione di un'applicazione in uno schema URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure consigliate per le associazioni di file](fa-best-practices.md)
</dt> <dt>

[Scenario di esempio di associazione file](fa-sample-scenarios.md)
</dt> <dt>

[Programmi predefiniti](default-programs.md)
</dt> <dt>

[Uso di Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
