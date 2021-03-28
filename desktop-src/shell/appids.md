---
description: Gli ID del modello utente dell'applicazione (AppUserModelIDs) vengono ampiamente utilizzati dalla barra delle applicazioni in sistemi Windows 7 e versioni successive per associare processi, file e finestre a una particolare applicazione.
ms.assetid: ebce2d99-6f20-4545-9f12-d79cd8d0828f
title: ID modello utente applicazione (AppUserModelIDs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b79f0bdd7fb5e6c4d5c41caa3cd6be3f4fb57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525416"
---
# <a name="application-user-model-ids-appusermodelids"></a>ID modello utente applicazione (AppUserModelIDs)

Gli ID del modello utente dell'applicazione (AppUserModelIDs) vengono ampiamente utilizzati dalla barra delle applicazioni in sistemi Windows 7 e versioni successive per associare processi, file e finestre a una particolare applicazione. In alcuni casi, è sufficiente basarsi sul AppUserModelID interno assegnato a un processo dal sistema. Tuttavia, un'applicazione che possiede più processi o un'applicazione in esecuzione in un processo host potrebbe dover identificarsi in modo esplicito in modo da poter raggruppare le finestre altrimenti diverse in un unico pulsante della barra delle applicazioni e controllare il contenuto della Jump List dell'applicazione.

-   [AppUserModelIDs definiti dall'applicazione e System-Defined](#application-defined-and-system-defined-appusermodelids)
-   [Come creare un Application-Defined AppUserModelID](#how-to-form-an-application-defined-appusermodelid)
-   [Dove assegnare un AppUserModelID](#where-to-assign-an-appusermodelid)
-   [Registrazione di un'applicazione come processo host](#registering-an-application-as-a-host-process)
-   [Elenchi di esclusione per il blocco della barra delle applicazioni e gli elenchi recenti/frequenti](#exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists)
-   [Argomenti correlati](#related-topics)

## <a name="application-defined-and-system-defined-appusermodelids"></a>Application-Defined e System-Defined AppUserModelIDs

Alcune applicazioni non dichiarano un AppUserModelID esplicito. Sono facoltativi. In tal caso, il sistema usa una serie di regole euristiche per assegnare un AppUserModelID interno. Tuttavia, esiste un vantaggio in termini di prestazioni nell'evitare questi calcoli e un AppUserModelID esplicito è l'unico modo per garantire un'esperienza utente esatta. È pertanto consigliabile impostare un ID esplicito. Le applicazioni non possono recuperare un AppUserModelID assegnato dal sistema.

Se un'applicazione usa un AppUserModelID esplicito, deve anche assegnare lo stesso AppUserModelID a tutti i processi, i collegamenti e le associazioni di file in esecuzione. Deve inoltre utilizzare tale AppUserModelID durante la personalizzazione della Jump List tramite [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)e in qualsiasi chiamata a [**funzione SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).

> [!Note]  
> Se le applicazioni non dispongono di un AppUserModelID esplicito, devono chiamare i metodi [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations), [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)e [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist) , nonché [**funzione SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) dall'interno dell'applicazione. Se questi metodi vengono chiamati da un altro processo, ad esempio un programma di installazione o una disinstallazione, il sistema non è in grado di generare il AppUserModelID corretto e tali chiamate non avranno alcun effetto.

 

Gli elementi seguenti descrivono scenari comuni che richiedono un AppUserModelID esplicito. Vengono inoltre segnalati i casi in cui devono essere utilizzati più AppUserModelIDs espliciti.

-   Un singolo file eseguibile con un'interfaccia utente con più modalità visualizzate all'utente come applicazioni separate deve assegnare AppUserModelIDs diversi a ogni modalità. Ad esempio, una parte di un'applicazione che gli utenti vedono come un'esperienza indipendente che è possibile aggiungere e avviare dalla barra delle applicazioni separatamente dal resto dell'applicazione deve avere la propria AppUserModelID, separata dall'esperienza principale.
-   Più collegamenti con argomenti diversi che portano tutti a ciò che l'utente vede come la stessa applicazione deve usare un AppUserModelID per tutti i tasti di scelta rapida. Windows Internet Explorer, ad esempio, dispone di scelte rapide diverse per le diverse modalità, ad esempio l'avvio senza componenti aggiuntivi, ma dovrebbero essere tutte visualizzate all'utente come una singola istanza di Internet Explorer.
-   Un eseguibile che funge da processo host e che esegue il contenuto di destinazione come un'applicazione deve essere [registrato come applicazione host](#registering-an-application-as-a-host-process), al termine del quale può assegnare AppUserModelIDs diversi a ogni esperienza percepita che ospita. In alternativa, il processo host può consentire al programma ospitato di impostare il relativo AppUserModelIDs. In entrambi i casi, il processo host deve tenere un record dell'origine del AppUserModelIDs, ovvero l'applicazione ospitata. In questo caso, non esiste un'esperienza utente primaria del processo host senza il contenuto di destinazione. Gli esempi sono le applicazioni remote di Windows (Rails), il runtime Java, RunDLL32.exe o DLLHost.exe.

    Nel caso di applicazioni ospitate esistenti, il sistema tenta di identificare le singole esperienze, ma le nuove applicazioni devono usare AppUserModelIDs esplicite per garantire l'esperienza utente desiderata.

-   I processi cooperativi o concatenati che fanno parte dell'utente fanno parte della stessa applicazione devono avere lo stesso AppUserModelID applicato a ogni processo. Gli esempi includono giochi con un processo di avvio (concatenato) e Microsoft Windows Media Player, che offre un'esperienza di installazione e di prima esecuzione in un processo e l'applicazione principale in esecuzione in un altro processo (cooperativa).
-   Un'estensione dello spazio dei nomi shell che funge da applicazione separata per più dell'esplorazione e la gestione del contenuto in Esplora risorse dovrebbe assegnare un AppUserModelID nelle proprietà della cartella. Un esempio è il pannello di controllo.
-   In un ambiente di virtualizzazione, ad esempio un Framework di distribuzione, l'ambiente di virtualizzazione deve assegnare AppUserModelIDs diversi a ogni applicazione gestita. In questi casi, un utilità di avvio dell'applicazione usa un processo intermediario per configurare l'ambiente e quindi passa l'operazione a un processo diverso per eseguire l'applicazione. Si noti che in questo modo il sistema non sarà in grado di correlare il processo di destinazione in esecuzione al collegamento, perché il collegamento punta al processo intermedio.

    Se un'applicazione dispone di più finestre, tasti di scelta rapida o processi, il AppUserModelID assegnato all'applicazione deve essere applicato anche a ognuna di queste parti dall'ambiente di virtualizzazione.

    Un esempio di questa situazione è il Framework ClickOnce, che assegna correttamente AppUserModelIDs per conto delle applicazioni gestite. Come in tutti questi ambienti, le applicazioni distribuite e gestite da ClickOnce non devono assegnare il AppUserModelIDs esplicito, perché in tal modo si verificherà un conflitto con il AppUserModelIDs assegnato da ClickOnce e causerà risultati imprevisti.

## <a name="how-to-form-an-application-defined-appusermodelid"></a>Come creare un Application-Defined AppUserModelID

Un'applicazione deve fornire il proprio AppUserModelID nel formato seguente. Non può contenere più di 128 caratteri e non può contenere spazi. Ogni sezione deve essere in un caso Pascal.

`CompanyName.ProductName.SubProduct.VersionInformation`

`CompanyName` e `ProductName` devono essere sempre usati, mentre le `SubProduct` `VersionInformation` parti e sono facoltative e dipendono dai requisiti dell'applicazione. `SubProduct` consente a un'applicazione principale costituita da più sottoapplicazioni di fornire un pulsante separato della barra delle applicazioni per ogni sottoapplicazione e le finestre associate. `VersionInformation` consente la coesistenza di due versioni di un'applicazione mentre vengono visualizzate come entità discrete. Se un'applicazione non è progettata per essere utilizzata in questo modo, è `VersionInformation` necessario omettere, in modo che una versione aggiornata possa utilizzare lo stesso AppUserModelID della versione sostituita.

## <a name="where-to-assign-an-appusermodelid"></a>Dove assegnare un AppUserModelID

Quando un'applicazione usa uno o più AppUserModelIDs espliciti, deve applicare tali AppUserModelIDs nei percorsi e nelle situazioni seguenti:

-   Nella proprietà [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) del file di collegamento dell'applicazione. Un collegamento (come un [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka), un \_ ShellLink CLSID o un file lnk) supporta le proprietà tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) e altri meccanismi di impostazione delle proprietà utilizzati in tutta la Shell. Questo consente alla barra delle applicazioni di identificare il collegamento appropriato per il PIN e garantisce che le finestre appartenenti al processo siano associate in modo appropriato al pulsante della barra delle applicazioni.
    > [!Note]  
    > Quando viene creato il collegamento, la proprietà [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) deve essere applicata a un tasto di scelta rapida. Quando si usa il Microsoft Windows Installer (MSI) per installare l'applicazione, la tabella [MsiShortcutProperty](../msi/msishortcutproperty-table.md) consente di applicare AppUserModelID al collegamento quando viene creato durante l'installazione.

     

-   Come proprietà di tutte le finestre in esecuzione dell'applicazione. Questo può essere impostato in uno dei due modi seguenti:

    1.  Se diverse finestre di proprietà di un processo richiedono un AppUserModelIDs diverso per controllare il raggruppamento della barra delle applicazioni, utilizzare [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)) per recuperare l'archivio delle proprietà della finestra e impostare AppUserModelID come proprietà della finestra.
    2.  Se tutte le finestre del processo utilizzano lo stesso AppUserModelID, impostare AppUserModelID sul processo, ma [**SetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid). Un'applicazione deve chiamare **SetCurrentProcessExplicitAppUserModelID** per impostare il relativo AppUserModelID durante la routine di avvio iniziale di un'applicazione prima che l'applicazione presenti un'interfaccia utente, effettui qualsiasi modifica delle Jump List o renda (o fa in modo che il sistema effettui qualsiasi chiamata a [**funzione SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)).

    Un AppUserModelID a livello di finestra esegue l'override di un AppUserModelID a livello di processo.

    Quando un'applicazione imposta un AppUserModelID esplicito a livello di finestra, l'applicazione può fornire le specifiche del comando di rilancio per il pulsante della relativa barra delle applicazioni. Per fornire tali informazioni, vengono utilizzate le proprietà seguenti:

    -   [System. AppUserModel. RelaunchCommand](../properties/props-system-appusermodel-relaunchcommand.md)
    -   [System. AppUserModel. RelaunchDisplayNameResource](../properties/props-system-appusermodel-relaunchdisplaynameresource.md)
    -   [System. AppUserModel. RelaunchIconResource](../properties/props-system-appusermodel-relaunchiconresource.md)

    > [!Note]  
    > Se esiste un collegamento per avviare l'applicazione, un'applicazione deve applicare AppUserModelID come proprietà del collegamento anziché usare le proprietà di rilancio. In tal caso, la riga di comando, l'icona e il testo del collegamento vengono usati per fornire le stesse informazioni delle proprietà di rilancio.

     

    Un AppUserModelID esplicito a livello di finestra può anche usare la proprietà [System. AppUserModel. PreventPinning](../properties/props-system-appusermodel-preventpinning.md) per specificare che non deve essere disponibile per l'aggiunta o il rilancio.

-   In una chiamata a Customize or Update ([**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)), Retrieve ([**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)) o Clear ([**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)) The Jump List dell'applicazione.
-   Nella registrazione dell'associazione di file (tramite il [ProgID](fa-progids.md)) se l'applicazione usa gli elenchi di destinazione **recenti** o **frequenti** generati automaticamente dal sistema. Le informazioni di associazione fanno riferimento a [**funzione SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Queste informazioni vengono usate anche quando si aggiungono destinazioni [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) a Jump List personalizzati tramite [**ICustomDestinationList:: AppendCategory**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory).
-   In qualsiasi chiamata eseguita direttamente dall'applicazione a [**funzione SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Se l'applicazione dipende dalla finestra di dialogo file comune per effettuare chiamate a **funzione SHAddToRecentDocs** per suo conto, tali chiamate possono dedurre il AppUserModelID esplicito solo se AppUserModelID è impostato per l'intero processo. Se l'applicazione imposta AppUserModelIDs nelle finestre anziché nel processo, l'applicazione deve eseguire tutte le chiamate a **funzione SHAddToRecentDocs** , con la relativa AppUserModelID esplicita, nonché impedire alla finestra di dialogo file comune di effettuare chiamate proprie. Questa operazione deve essere eseguita ogni volta che viene aperto un elemento, per assicurarsi che le sezioni **recenti** o **frequenti** della Jump List dell'applicazione siano accurate.

Gli elementi seguenti descrivono scenari comuni e dove applicare AppUserModelIDs espliciti in questi scenari.

-   Quando un singolo processo contiene più applicazioni, usare [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow) per recuperare l'archivio delle proprietà della finestra e impostare AppUserModelID come proprietà della finestra.
-   Quando un'applicazione usa più processi, applicare AppUserModelID a ogni processo. Se si usa lo stesso AppUserModelID in ogni processo, a seconda che si desideri visualizzare ogni processo come parte dell'applicazione principale o come entità singole.
-   Per separare determinate finestre da un set nello stesso processo, usare l'archivio delle proprietà della finestra per applicare un singolo AppUserModelID alle finestre che si vuole separare, quindi applicare un AppUserModelID diverso al processo. Qualsiasi finestra del processo che non è stata etichettata in modo esplicito con il AppUserModelID a livello di finestra eredita il AppUserModelID del processo.
-   Se un tipo di file è associato a un'applicazione, assegnare AppUserModelID nella registrazione [ProgID](fa-progids.md) del tipo di file. Se un singolo file eseguibile viene avviato in modalità diverse che vengono visualizzate all'utente come applicazioni distinte, è necessario un AppUserModelID separato per ogni modalità. In tal caso, è necessario che siano presenti più registrazioni ProgID per il tipo di file, ognuna con un AppUserModelID diverso.
-   Quando sono presenti più percorsi di collegamento da cui un utente può avviare un'applicazione (nel menu **Start** , sul desktop o altrove) recuperare l'archivio delle proprietà del collegamento per applicare un singolo AppUserModelID a tutti i collegamenti come proprietà di collegamento.
-   Quando viene eseguita una chiamata esplicita a [**funzione SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) da un'applicazione, usare AppUserModelID nella chiamata. Quando si usa la finestra di dialogo file comune per aprire o salvare i file, **funzione SHAddToRecentDocs** viene chiamato dalla finestra di dialogo per conto dell'applicazione. Tale chiamata può dedurre il AppUserModelID esplicito dal processo. Tuttavia, se un AppUserModelID esplicito viene applicato come proprietà della finestra, la finestra di dialogo file comune non è in grado di determinare il AppUserModelID corretto. In tal caso, l'applicazione deve chiamare in modo esplicito **funzione SHAddToRecentDocs** e fornire il AppUserModelID corretto. Inoltre, l'applicazione deve impedire alla finestra di dialogo file comune di chiamare **funzione SHAddToRecentDocs** per suo conto impostando il \_ flag Fos DONTADDTORECENT nel metodo **GetOptions** di [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) o [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog).

## <a name="registering-an-application-as-a-host-process"></a>Registrazione di un'applicazione come processo host

Un'applicazione può impostare la voce del registro di sistema IsHostApp per fare in modo che il processo dell'eseguibile venga considerato un processo host dalla barra delle applicazioni. Questa operazione influiscono sul raggruppamento e sulle voci predefinite della Jump List.

Nell'esempio seguente viene illustrata la voce del registro di sistema richiesta. Si noti che alla voce non viene assegnato un valore. la sua presenza è tutto ciò che è necessario. Si tratta di un \_ valore reg null.

```
HKEY_CLASSES_ROOT
   Applications
      example.exe
         IsHostApp
```

Se il processo stesso o il file di collegamento utilizzato per avviare il processo dispone di un AppUserModelID esplicito, l'elenco dei processi host viene ignorato e l'applicazione viene considerata come un'applicazione normale dalla barra delle applicazioni. Le finestre in esecuzione dell'applicazione sono raggruppate in un unico pulsante della barra delle applicazioni e l'applicazione può essere bloccata sulla barra delle applicazioni.

Se è noto solo il nome eseguibile del processo in esecuzione, senza un AppUserModelID esplicito e tale eseguibile si trova nell'elenco dei processi host, ogni istanza del processo viene considerata come un'entità separata per il raggruppamento della barra delle applicazioni. Il pulsante della barra delle applicazioni associato a un'istanza specifica del processo non visualizza un'opzione pin/Rimuovi o un'icona di avvio per una nuova istanza del processo. Il processo non è inoltre idoneo per l'inclusione nell'elenco dei menu **Start** (MFU) utilizzato più di frequente. Tuttavia, se il processo è stato avviato tramite un collegamento che contiene gli argomenti di avvio (in genere il contenuto di destinazione da ospitare come "applicazione"), il sistema è in grado di determinare l'identità e l'applicazione può essere bloccata e riavviata.

## <a name="exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists"></a>Elenchi di esclusione per il blocco della barra delle applicazioni e gli elenchi recenti/frequenti

Le applicazioni, i processi e le finestre possono scegliere di non essere disponibili per l'aggiunta alla barra delle applicazioni o per l'inclusione nell'elenco MFU del menu **Start** . Per eseguire questa operazione sono disponibili tre meccanismi:

1.  Aggiungere la voce NoStartPage alla registrazione dell'applicazione, come illustrato di seguito:

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    I dati associati alla voce NoStartPage vengono ignorati. È necessaria solo la presenza della voce. Pertanto, il tipo ideale per NoStartPage è REG \_ None.

    Si noti che qualsiasi uso di un AppUserModelID esplicito sostituisce la voce NoStartPage. Se un AppUserModelID esplicito viene applicato a un collegamento, a un processo o a una finestra, diventa aggiungibili e idoneo per l'elenco MFU del menu **Start** .

2.  Impostare la proprietà [System. AppUserModel. PreventPinning](../properties/props-system-appusermodel-preventpinning.md) in Windows e i collegamenti. Questa proprietà deve essere impostata su una finestra prima della [proprietà \_ \_ ID AppUserModel pkey](../properties/props-system-appusermodel-id.md) .
3.  Aggiungere un AppUserModelID esplicito come valore nella seguente sottochiave del registro di sistema, come illustrato di seguito:

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

    Ogni voce è un \_ valore reg null con il nome del AppUserModelID. Qualsiasi AppUserModelID trovato in questo elenco non è aggiungibili e non è idoneo per l'inclusione nell'elenco MFU del menu **Start** .

Tenere presente che alcuni file eseguibili, nonché collegamenti che contengono determinate stringhe nel nome, vengono automaticamente esclusi dal blocco e dall'inclusione nell'elenco MFU.

> [!Note]  
> Questa esclusione automatica può essere sottoposta a override applicando un AppUserModelID esplicito.

 

Se una delle stringhe seguenti, indipendentemente dalla distinzione tra maiuscole e minuscole, è inclusa nel nome del collegamento, il programma non è aggiungibili e non viene visualizzato nell'elenco degli elementi utilizzati più di frequente (non applicabile a Windows 10):

-   Documentazione
-   Help
-   Installazione
-   Altre informazioni
-   Leggi
-   Leggi prima
-   File Leggimi
-   Rimuovi
-   Configurazione
-   Supporto
-   Novità

L'elenco di programmi seguente non è aggiungibili e viene escluso dall'elenco degli elementi utilizzati più di frequente.

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

Gli elenchi precedenti vengono archiviati nei seguenti valori del registro di sistema.

> [!Note]  
> Questi elenchi non devono essere modificati dalle applicazioni. Usare uno dei metodi elenco di esclusione elencati in precedenza per la stessa esperienza.

 

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

[**ICustomDestinationList:: seappid**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-setappid)
</dt> <dt>

[**IApplicationDocumentLists:: seappid**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-setappid)
</dt> <dt>

[**IApplicationDestinations:: seappid**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-setappid)
</dt> <dt>

[**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> </dl>

 

 
