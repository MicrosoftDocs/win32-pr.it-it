---
description: Gli ID modello utente applicazione (AppUserModelID) vengono ampiamente usati dalla barra delle applicazioni nei sistemi Windows 7 e versioni successive per associare processi, file e finestre a una particolare applicazione.
ms.assetid: ebce2d99-6f20-4545-9f12-d79cd8d0828f
title: ID modello utente applicazione (AppUserModelIDs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd0835af241a36e4d9c95237890cb63790f7fe9031476dfa8ec21254266ffd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351471"
---
# <a name="application-user-model-ids-appusermodelids"></a>ID modello utente applicazione (AppUserModelIDs)

Gli ID modello utente applicazione (AppUserModelID) vengono ampiamente usati dalla barra delle applicazioni nei sistemi Windows 7 e versioni successive per associare processi, file e finestre a una particolare applicazione. In alcuni casi, è sufficiente fare affidamento sull'AppUserModelID interno assegnato a un processo dal sistema. Tuttavia, un'applicazione proprietaria di più processi o un'applicazione in esecuzione in un processo host potrebbe dover identificarsi in modo esplicito in modo che possa raggruppare le finestre altrimenti diverse sotto un singolo pulsante della barra delle applicazioni e controllare il contenuto del Jump List dell'applicazione.

-   [Definito dall'applicazione e System-Defined AppUserModelIDs](#application-defined-and-system-defined-appusermodelids)
-   [Come formare un Application-Defined AppUserModelID](#how-to-form-an-application-defined-appusermodelid)
-   [Dove assegnare un AppUserModelID](#where-to-assign-an-appusermodelid)
-   [Registrazione di un'applicazione come processo host](#registering-an-application-as-a-host-process)
-   [Elenchi di esclusione per l'aggiunta alla barra delle applicazioni e gli elenchi recenti/frequenti](#exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists)
-   [Argomenti correlati](#related-topics)

## <a name="application-defined-and-system-defined-appusermodelids"></a>Application-Defined e System-Defined AppUserModelID

Alcune applicazioni non dichiarano un AppUserModelID esplicito. Sono facoltativi. In tal caso, il sistema usa una serie di euristica per assegnare un AppUserModelID interno. Tuttavia, esiste un vantaggio in termini di prestazioni nell'evitare questi calcoli e un AppUserModelID esplicito è l'unico modo per garantire un'esperienza utente esatta. È pertanto consigliabile impostare un ID esplicito. Le applicazioni non possono recuperare un AppUserModelID assegnato dal sistema.

Se un'applicazione usa un AppUserModelID esplicito, deve anche assegnare lo stesso AppUserModelID a tutte le finestre o processi in esecuzione, i collegamenti e le associazioni di file. Deve anche usare tale AppUserModelID quando si personalizza il Jump List [**tramite ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)e in qualsiasi chiamata a [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).

> [!Note]  
> Se le applicazioni non hanno un AppUserModelID esplicito, devono chiamare i metodi [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations), [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)e [**ICustomDestinationList,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist) nonché [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) dall'interno dell'applicazione. Se questi metodi vengono chiamati da un altro processo, ad esempio un programma di installazione o un programma di disinstallazione, il sistema non può generare l'AppUserModelID corretto e tali chiamate non avranno alcun effetto.

 

Gli elementi seguenti descrivono scenari comuni che richiedono un AppUserModelID esplicito. Fanno anche riferimento ai casi in cui devono essere usati più AppUserModelID espliciti.

-   Un singolo file eseguibile con un'interfaccia utente con più modalità che vengono visualizzate all'utente come applicazioni separate deve assegnare appUserModelID diversi a ogni modalità. Ad esempio, una parte di un'applicazione che gli utenti vedono come un'esperienza indipendente che possono aggiungere e avviare dalla barra delle applicazioni separatamente dal resto dell'applicazione deve avere un proprio AppUserModelID, separato dall'esperienza principale.
-   Più tasti di scelta rapida con argomenti diversi che portano a ciò che l'utente vede come la stessa applicazione devono usare un AppUserModelID per tutti i collegamenti. Ad esempio, Windows Internet Explorer diversi tasti di scelta rapida per diverse modalità ,ad esempio l'avvio senza componenti aggiuntivi, ma devono essere tutti visualizzati all'utente come una singola Internet Explorer istanza.
-   Un eseguibile che funge da processo host ed esegue il contenuto di destinazione come applicazione deve essere registrato come applicazione [host,](#registering-an-application-as-a-host-process)dopo di che può assegnare appusermodelID diversi a ogni esperienza percepita ospitata. In alternativa, il processo host può consentire al programma ospitato di impostare i relativi AppUserModelID. In entrambi i casi, il processo host deve mantenere un record dell'origine di AppUserModelIDs, se stesso o dell'applicazione ospitata. In questo caso, non esiste un'esperienza utente primaria del processo host senza il contenuto di destinazione. Ad esempio Windows applicazioni remote integrate localmente (RAIL), java runtime, RunDLL32.exe o DLLHost.exe.

    Nel caso di applicazioni ospitate esistenti, il sistema tenta di identificare singole esperienze, ma le nuove applicazioni devono usare AppUserModelID espliciti per garantire l'esperienza utente prevista.

-   Ai processi cooperativi o concatenati che fanno parte della stessa applicazione deve essere applicato lo stesso AppUserModelID a ogni processo. Ad esempio, i giochi con un processo di avvio (concatenato) e Microsoft Windows Media Player, con un'esperienza di prima esecuzione/configurazione in esecuzione in un processo e l'applicazione principale in esecuzione in un altro processo (cooperativo).
-   Un'estensione dello spazio dei nomi Shell che funge da applicazione separata per più dell'esplorazione e della gestione del contenuto in Windows Explorer deve assegnare un AppUserModelID nelle proprietà della cartella. Un esempio è il Pannello di controllo.
-   In un ambiente di virtualizzazione, ad esempio un framework di distribuzione, l'ambiente di virtualizzazione deve assegnare appUserModelID diversi a ogni applicazione che gestisce. In questi casi, un'utilità di avvio delle applicazioni usa un processo intermedio per configurare l'ambiente e quindi trasla l'operazione a un processo diverso per eseguire l'applicazione. Si noti che in questo modo il sistema non riesce a correlare il processo di destinazione in esecuzione al collegamento perché il collegamento punta al processo intermedio.

    Se un'applicazione ha più finestre, collegamenti o processi, l'AppUserModelID assegnato dall'applicazione deve essere applicato anche a ognuna di queste parti dall'ambiente di virtualizzazione.

    Un esempio di questa situazione è il framework ClickOnce, che assegna correttamente Gli ID AppUserModel per conto delle applicazioni gestite. Come in tutti questi ambienti, le applicazioni distribuite e gestite da ClickOnce non devono assegnare appUserModelID esplicite, perché in questo modo saranno in conflitto con gli AppUserModelID assegnati da ClickOnce e genereranno risultati imprevisti.

## <a name="how-to-form-an-application-defined-appusermodelid"></a>Come formare un Application-Defined AppUserModelID

Un'applicazione deve fornire il relativo AppUserModelID nel formato seguente. Non può contenere più di 128 caratteri e non può contenere spazi. Ogni sezione deve essere con distinzione tra maiuscole e minuscole.

`CompanyName.ProductName.SubProduct.VersionInformation`

`CompanyName` e devono essere sempre usati, mentre le parti `ProductName` e sono `SubProduct` `VersionInformation` facoltative e dipendono dai requisiti dell'applicazione. `SubProduct` consente a un'applicazione principale costituita da diverse sottoapplicazioni di fornire un pulsante della barra delle applicazioni separato per ogni sottoapplicazione e le finestre associate. `VersionInformation` consente a due versioni di un'applicazione di coesistere mentre vengono viste come entità discrete. Se un'applicazione non deve essere usata in questo modo, deve essere omesso in modo che una versione aggiornata possa usare lo stesso AppUserModelID della versione `VersionInformation` sostituita.

## <a name="where-to-assign-an-appusermodelid"></a>Dove assegnare un AppUserModelID

Quando un'applicazione usa uno o più AppUserModelID espliciti, deve applicare tali AppUserModelID nei percorsi e nelle situazioni seguenti:

-   Nella proprietà [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) proprietà del file di collegamento dell'applicazione. Un collegamento (come [**IShellLink,**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka)CLSID ShellLink o un file con estensione lnk) supporta le proprietà tramite \_ [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) e altri meccanismi di impostazione delle proprietà usati in Shell. Ciò consente alla barra delle applicazioni di identificare il collegamento appropriato da aggiungere e garantisce che le finestre appartenenti al processo siano associate in modo appropriato al pulsante della barra delle applicazioni.
    > [!Note]  
    > La [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) proprietà deve essere applicata a un collegamento quando viene creato il collegamento. Quando si usa il programma di installazione di Microsoft Windows (MSI) per installare l'applicazione, la tabella [MsiShortcutProperty](../msi/msishortcutproperty-table.md) consente di applicare AppUserModelID al collegamento quando viene creato durante l'installazione.

     

-   Come proprietà di una delle finestre in esecuzione dell'applicazione. Questa impostazione può essere impostata in uno dei due modi seguenti:

    1.  Se finestre diverse di proprietà di un processo richiedono appUserModelID diversi per controllare il raggruppamento della barra delle applicazioni, usare [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)) per recuperare l'archivio delle proprietà della finestra e impostare AppUserModelID come proprietà della finestra.
    2.  Se tutte le finestre nel processo usano lo stesso AppUserModelID, impostare AppUserModelID nel processo, anche se [**SetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid). Un'applicazione deve chiamare **SetCurrentProcessExplicitAppUserModelID** per impostare il relativo AppUserModelID durante la routine di avvio iniziale di un'applicazione prima che l'applicazione presenti un'interfaccia utente, apportare modifiche alle jump list o a effettuare (o fa sì che il sistema ese) qualsiasi chiamata a [**SHAddToRecentDocs.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)

    Un AppUserModelID a livello di finestra esegue l'override di un AppUserModelID a livello di processo.

    Quando un'applicazione imposta un AppUserModelID esplicito a livello di finestra, l'applicazione può fornire le specifiche del relativo comando di riavvio per il pulsante della barra delle applicazioni. Per fornire queste informazioni, vengono usate le proprietà seguenti:

    -   [System.AppUserModel.RelaunchCommand](../properties/props-system-appusermodel-relaunchcommand.md)
    -   [System.AppUserModel.RelaunchDisplayNameResource](../properties/props-system-appusermodel-relaunchdisplaynameresource.md)
    -   [System.AppUserModel.RelaunchIconResource](../properties/props-system-appusermodel-relaunchiconresource.md)

    > [!Note]  
    > Se esiste un collegamento per avviare l'applicazione, un'applicazione deve applicare AppUserModelID come proprietà del collegamento anziché usare le proprietà di riavvio. In tal caso, la riga di comando, l'icona e il testo del collegamento vengono usati per fornire le stesse informazioni delle proprietà di riavvio.

     

    Un AppUserModelID esplicito a livello di finestra può anche usare la proprietà [System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) per specificare che non deve essere disponibile per l'aggiunta o il riavvio.

-   In una chiamata per personalizzare o aggiornare ([**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)), recuperare ([**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)) o cancellare ([**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)) l'Jump List.
-   Nella registrazione dell'associazione di file (tramite [il relativo ProgID](fa-progids.md)) se l'applicazione usa gli elenchi di destinazione **Recenti** **o Frequenti** generati automaticamente dal sistema. A queste informazioni di associazione viene fatto riferimento [**da SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Queste informazioni vengono usate anche quando si aggiungono [**destinazioni IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) a jump list personalizzate tramite [**ICustomDestinationList::AppendCategory**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory).
-   In qualsiasi chiamata l'applicazione effettua direttamente [**a SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Se l'applicazione dipende dalla finestra di dialogo file comune per effettuare chiamate a **SHAddToRecentDocs** per suo conto, tali chiamate possono dedurre l'appUserModelID esplicito solo se AppUserModelID è impostato per l'intero processo. Se l'applicazione imposta AppUserModelIDs nelle finestre anziché nel processo, l'applicazione deve eseguire tutte le chiamate a **SHAddToRecentDocs** stesso, con il relativo AppUserModelID esplicito, nonché impedire alla finestra di dialogo di file comune di effettuare chiamate proprie. Questa operazione deve essere eseguita ogni volta  che  un elemento viene aperto, per assicurarsi che le sezioni Recenti o Frequenti del Jump List dell'applicazione siano accurate.

Gli elementi seguenti descrivono scenari comuni e dove applicare appUserModelID espliciti in tali scenari.

-   Quando un singolo processo contiene più applicazioni, usare [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow) per recuperare l'archivio delle proprietà della finestra e impostare AppUserModelID come proprietà della finestra.
-   Quando un'applicazione usa più processi, applicare AppUserModelID a ogni processo. L'uso dello stesso AppUserModelID in ogni processo dipende dal fatto che ogni processo venga visualizzato come parte dell'applicazione principale o come singole entità.
-   Per separare determinate finestre da un set nello stesso processo, usare l'archivio delle proprietà della finestra per applicare un singolo AppUserModelID alle finestre da separare e quindi applicare un AppUserModelID diverso al processo. Qualsiasi finestra del processo che non è stata etichettata in modo esplicito con AppUserModelID a livello di finestra eredita appUserModelID del processo.
-   Se un tipo di file è associato a un'applicazione, assegnare AppUserModelID nella registrazione [ProgID](fa-progids.md) del tipo di file. Se un singolo file eseguibile viene avviato in modalità diverse che vengono visualizzate all'utente come applicazioni distinte, è necessario un AppUserModelID separato per ogni modalità. In tal caso, devono essere presenti più registrazioni ProgID per il tipo di file, ognuna con un AppUserModelID diverso.
-   Quando sono presenti più percorsi di collegamento da cui un utente può avviare un'applicazione (nel menu **Start,** sul desktop o altrove) recuperare l'archivio delle proprietà del collegamento per applicare un singolo AppUserModelID a tutti i collegamenti come proprietà di collegamento.
-   Quando un'applicazione esegue una chiamata esplicita a [**SHAddToRecentDocs,**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) usare AppUserModelID nella chiamata. Quando la finestra di dialogo file comune viene usata per aprire o salvare i file, **SHAddToRecentDocs** viene chiamato dalla finestra di dialogo per conto dell'applicazione. Tale chiamata può dedurre l'appUserModelID esplicito dal processo. Tuttavia, se un AppUserModelID esplicito viene applicato come proprietà della finestra, la finestra di dialogo del file comune non è in grado di determinare l'AppUserModelID corretto. In tal caso, l'applicazione stessa deve chiamare in modo **esplicito SHAddToRecentDocs** e fornire l'AppUserModelID corretto. Inoltre, l'applicazione deve impedire al dialogo di file comune di chiamare **SHAddToRecentDocs** per suo conto impostando il flag DONTADDTORECENT fos nel \_ metodo **GetOptions** di [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) o [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog).

## <a name="registering-an-application-as-a-host-process"></a>Registrazione di un'applicazione come processo host

Un'applicazione può impostare la voce del Registro di sistema IsHostApp in modo che il processo dell'eseguibile sia considerato un processo host dalla barra delle applicazioni. Ciò influisce sul raggruppamento e sulle Jump List predefinite.

Nell'esempio seguente viene illustrata la voce del Registro di sistema richiesta. Si noti che alla voce non è assegnato un valore. la sua presenza è tutto ciò che è necessario. Si tratta di un valore \_ REG NULL.

```
HKEY_CLASSES_ROOT
   Applications
      example.exe
         IsHostApp
```

Se il processo stesso o il file di collegamento usato per avviare il processo ha un AppUserModelID esplicito, l'elenco di processi host viene ignorato e l'applicazione viene considerata come una normale applicazione dalla barra delle applicazioni. Le finestre in esecuzione dell'applicazione sono raggruppate sotto un singolo pulsante della barra delle applicazioni e l'applicazione può essere aggiunta alla barra delle applicazioni.

Se è noto solo il nome eseguibile del processo in esecuzione, senza un AppUserModelID esplicito e tale eseguibile è presente nell'elenco di processi host, ogni istanza del processo viene considerata come un'entità separata per il raggruppamento della barra delle applicazioni. Il pulsante della barra delle applicazioni associato a un'istanza specifica del processo non visualizza un'opzione di aggiunta/sblocco o un'icona di avvio per una nuova istanza del processo. Il processo non è inoltre idoneo per l'inclusione nell'elenco MFU (Most Frequently Used) del menu **Start.** Tuttavia, se il processo è stato avviato tramite un collegamento che contiene argomenti di avvio (in genere il contenuto di destinazione da ospitare come "applicazione"), il sistema può determinare l'identità e l'applicazione può essere bloccata e avviata di nuovo.

## <a name="exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists"></a>Elenchi di esclusione per l'aggiunta alla barra delle applicazioni e gli elenchi recenti/frequenti

Applicazioni, processi e finestre possono scegliere di non essere più disponibili per l'aggiunta alla barra delle applicazioni o per l'inclusione nell'elenco MFU del menu **Start.** A tale scopo, sono disponibili tre meccanismi:

1.  Aggiungere la voce NoStartPage alla registrazione dell'applicazione, come illustrato di seguito:

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    I dati associati alla voce NoStartPage vengono ignorati. È necessaria solo la presenza della voce . Pertanto, il tipo ideale per NoStartPage è REG \_ NONE.

    Si noti che qualsiasi uso di un AppUserModelID esplicito esegue l'override della voce NoStartPage. Se un AppUserModelID esplicito viene applicato a un collegamento, un processo o una finestra, diventa pinnable e idoneo per l'elenco MFU del menu **Start.**

2.  Impostare la [proprietà System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) nelle finestre e nei collegamenti. Questa proprietà deve essere impostata in una finestra prima della [proprietà PKEY \_ AppUserModel \_ ID.](../properties/props-system-appusermodel-id.md)
3.  Aggiungere un AppUserModelID esplicito come valore nella sottochiave del Registro di sistema seguente, come illustrato di seguito:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    Ogni voce è un valore \_ REG NULL con il nome di AppUserModelID. Qualsiasi AppUserModelID trovato in questo elenco non è aggiungibile e non è idoneo per l'inclusione nell'elenco MFU del menu **Start.**

Tenere presente che alcuni file eseguibili e collegamenti che contengono determinate stringhe nel nome vengono automaticamente esclusi dall'aggiunta e dall'inclusione nell'elenco MFU.

> [!Note]  
> Questa esclusione automatica può essere sostituita applicando un AppUserModelID esplicito.

 

Se una delle stringhe seguenti, indipendentemente dalla distinzione tra maiuscole e minuscole, viene inclusa nel nome del collegamento, il programma non è bloccabile e non viene visualizzato nell'elenco degli elementi usati più di frequente (non applicabile a Windows 10):

-   Documentazione
-   Help
-   Installazione
-   Altre informazioni
-   Leggimi
-   Read First
-   File Leggimi
-   Rimuovi
-   Eseguire la configurazione
-   Supporto
-   Novità

L'elenco seguente di programmi non è aggiungibile e viene escluso dall'elenco dei programmi usati più di frequente.

-   Applaunch.exe
-   Control.exe
-   Dfsvc.exe
-   Dllhost.exe
-   Guestmodemsg.exe
-   Hh.exe
-   Install.exe
-   Isuninst.exe
-   Lnkstub.exe
-   Mmc.exe
-   Mshta.exe
-   Msiexec.exe
-   Msoobe.exe
-   Rundll32.exe
-   Setup.exe
-   St5unst.exe
-   Unwise.exe
-   Unwise32.exe
-   Werfault.exe
-   Winhlp32.exe
-   Wlrmdr.exe
-   Wuapp.exe

Gli elenchi precedenti sono archiviati nei valori del Registro di sistema seguenti.

> [!Note]  
> Questi elenchi non devono essere modificati dalle applicazioni. Usare uno dei metodi dell'elenco di esclusione elencati in precedenza per la stessa esperienza.

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**SetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid)
</dt> <dt>

[**GetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid)
</dt> <dt>

[Estensioni della barra delle applicazioni](taskbar-extensions.md)
</dt> <dt>

[**ICustomDestinationList::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-setappid)
</dt> <dt>

[**IApplicationDocumentLists::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-setappid)
</dt> <dt>

[**IApplicationDestinations::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-setappid)
</dt> <dt>

[**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> </dl>

 

 
