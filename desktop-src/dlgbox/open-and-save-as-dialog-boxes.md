---
title: Finestre di dialogo Apri e Salva con nome
description: La finestra di dialogo Apri consente all'utente di specificare l'unità, la directory e il nome di un file o di un set di file da aprire.
ms.assetid: 5676ca9d-daca-40bf-8881-def2ff841c58
keywords:
- Libreria di finestre di dialogo comune
- finestre di dialogo comuni
- Finestra di dialogo Apri
- Salva con nome - finestra di dialogo
- personalizzazione della finestra di dialogo Apri
- personalizzazione della finestra di dialogo Salva con nome
- finestre di dialogo, Apri
- finestre di dialogo, Salva con nome
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 57f1986f950650840ff3acfc9ee19191088e0dcbe099fc4cb8b21690fa0646c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606303"
---
# <a name="open-and-save-as-dialog-boxes"></a>Finestre di dialogo Apri e Salva con nome

> [!NOTE]
> La [**funzione GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) è illustrata nell'esempio [file è in uso.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse)

\[A partire Windows Vista, le  **finestre** di dialogo comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](../shell/common-file-dialog.md). È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]

La **finestra** di dialogo Apri consente all'utente di specificare l'unità, la directory e il nome di un file o di un set di file da aprire. Per creare e visualizzare una **finestra** di dialogo Apri, inizializzare una struttura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) e passare la struttura [**alla funzione GetOpenFileName.**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)

La **finestra di dialogo** Salva con nome consente all'utente di specificare l'unità, la directory e il nome di un file da salvare. Per creare e visualizzare una **finestra di** dialogo Salva con nome, inizializzare una struttura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) e passare la struttura [**alla funzione GetSaveFileName.**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)

Le finestre di **dialogo** Apri e **Salva con** nome di tipo Esplora risorse offrono funzionalità dell'interfaccia utente simili Windows Explorer. Tuttavia, il sistema continua a  supportare le finestre di dialogo Apri e Salva con nome di tipo precedente per le applicazioni che devono essere coerenti con l'interfaccia utente di tipo precedente. 

Oltre alla differenza di aspetto, le finestre di dialogo di tipo Esplora risorse e stile precedente differiscono per l'uso di modelli personalizzati e procedure hook per la personalizzazione delle finestre di dialogo. Tuttavia, le finestre di dialogo stile Esplora risorse e stile precedente hanno lo stesso comportamento per la maggior parte delle operazioni di base, ad esempio la specifica di un filtro di nome file, la convalida dell'input dell'utente e il recupero del nome file specificato dall'utente. Per altre informazioni sulle finestre di dialogo di tipo Esplora risorse e stile precedente, vedere Personalizzazione della finestra di dialogo Apri [e salva con nome](#open-and-save-as-dialog-box-customization).

Nella figura seguente viene illustrata una tipica finestra di dialogo **Apri di** tipo Esplora risorse.

![Finestra di dialogo Apri file](images/opendialogboxxp.png)

La figura seguente mostra una tipica finestra di dialogo **Salva** con nome di tipo Esplora risorse.

![Finestra di dialogo Salva file](images/saveasdialogboxxp.png)

Se l'utente specifica un nome file e fa clic sul pulsante **OK,** [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) o [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) restituisce **TRUE.** Il buffer a cui punta il **membro lpstrFile** della struttura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) contiene il percorso completo e il nome file specificati dall'utente.

Se l'utente annulla  la **finestra di dialogo** Apri o Salva con nome o si verifica un errore, la funzione restituisce **FALSE.** Per determinare la causa dell'errore, chiamare la [**funzione CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) per recuperare il valore di errore esteso. Se il buffer **lpstrFile** è troppo piccolo per ricevere il nome completo, **CommDlgExtendedError** restituisce **FNERR \_ BUFFERTOOSMALL** e i primi 2 byte del buffer a cui punta il membro **lpstrFile** sono impostati su un valore intero che specifica le dimensioni necessarie per ricevere il nome completo.

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Nomi di file e directory](#file-names-and-directories)
-   [Filtri](#filters)
-   [Convalida di file e directory](#file-and-directory-validation)
-   [Personalizzazione della finestra di dialogo Apri e salva con nome](#open-and-save-as-dialog-box-customization)
-   [Routine hook di tipo Explorer](#explorer-style-hook-procedures)
-   [Modelli personalizzati in stile Esplora risorse](#explorer-style-custom-templates)
-   [Identificatori di controllo in stile Esplora risorse](#explorer-style-control-identifiers)
-   [Personalizzazione di Old-Style finestre di dialogo](#customizing-old-style-dialog-boxes)

## <a name="file-names-and-directories"></a>Nomi di file e directory

Le informazioni contenute in questa sezione si  applicano sia alle finestre di dialogo Apri e **Salva con nome** di tipo Esplora risorse che alle finestre di dialogo stile precedente.

Prima di chiamare le funzioni [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) o [**GetSaveFileName,**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) il membro **lpstrFile** della struttura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) deve puntare al buffer per ricevere il nome del file. Il **membro nMaxFile** deve specificare le dimensioni, in caratteri, del buffer **lpstrFile.** Per una funzione ANSI si tratta del numero di byte, ma per una funzione Unicode si tratta del numero di caratteri.

Se l'utente specifica un nome file e fa clic sul pulsante **OK,** la finestra di dialogo copia l'unità, la directory e il nome file selezionati nel buffer **lpstrFile.** La funzione imposta anche i membri **nFileOffset** e **nFileExtension** rispettivamente per gli offset, in caratteri, dall'inizio del buffer al nome del file e all'estensione del nome file.

Per recuperare solo il nome file e l'estensione, impostare il membro **lpstrFileTitle** in modo che punti a un buffer e impostare il membro **nMaxFileTitle** sulla dimensione, in caratteri, del buffer. In alternativa, è possibile passare il buffer **lpstrFile** in una chiamata alla [**funzione GetFileTitle**](/windows/desktop/api/Commdlg/nf-commdlg-getfiletitlea) per ottenere il nome visualizzato del file selezionato. Si noti, tuttavia, che il nome file restituito da **GetFileTitle** include un'estensione solo se questa è la preferenza dell'utente per la visualizzazione dei nomi di file.

Nella finestra di dialogo viene utilizzata la directory corrente per il processo chiamante come directory iniziale da cui visualizzare file e directory. Usare le [**funzioni GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) [**e SetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) per ottenere e modificare la directory corrente di un processo. Per specificare una directory iniziale diversa senza modificare la directory corrente, usare il membro **lpstrInitialDir** per specificare il nome di una directory. La finestra di dialogo modifica automaticamente la directory corrente quando l'utente seleziona un'unità o una directory diversa. Per impedire alla finestra di dialogo di modificare la directory corrente, impostare il flag **OFN \_ NOCHANGEDIR.** Questo flag non impedisce all'utente di modificare le directory per trovare un file.

Per specificare un'estensione di file predefinita, usare il **membro lpstrDefExt** . Se l'utente specifica un nome di file senza estensione, nella finestra di dialogo viene aggiunta l'estensione predefinita. Se si specifica un'estensione predefinita e l'utente specifica un nome file con un'estensione diversa, nella finestra di dialogo viene impostato il flag **\_ OFN EXTENSIONDIFFERENT.**

Per consentire all'utente di selezionare più file da una directory, impostare il flag **\_ OFN ALLOWMULTISELECT.** Per garantire la compatibilità con le applicazioni meno recenti, la finestra di dialogo di selezione multipla predefinita usa l'interfaccia utente di tipo precedente. Per visualizzare una finestra di dialogo di selezione multipla in stile Esplora risorse, è necessario impostare anche il flag **OFN \_ EXPLORER.**

Se l'utente seleziona più di un file, il buffer a cui punta il membro **lpstrFile** restituisce il percorso della directory corrente seguito dai nomi dei file selezionati. Il **membro nFileOffset** è l'offset del nome del primo file e il **membro nFileExtension** non viene usato. Nella tabella seguente viene descritta la differenza tra le finestre di dialogo di tipo Esplora risorse e le finestre di dialogo di tipo precedente per la restituzione di più nomi di file.



| Stile della finestra di dialogo            | Descrizione                                                                                                                                                                                                               |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Finestre di dialogo in stile Esplora risorse | Le stringhe di directory e nome file **sono separate da NULL,** con un carattere **NULL** aggiuntivo dopo l'ultimo nome file. Questo formato consente alle finestre di dialogo in stile Esplora risorse di restituire nomi di file lunghi che includono spazi. |
| Finestre di dialogo in stile precedente      | Le stringhe di directory e nome file sono separate da spazi. Per i nomi di file con spazi, la funzione usa nomi di file brevi.                                                                                              |



 

È possibile usare la [**funzione FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) per eseguire la conversione tra nomi di file lunghi e brevi.

Se si specifica **OFN \_ ALLOWMULTISELECT** e l'utente seleziona un solo file, la stringa **lpstrFile** non include un separatore tra il percorso e il nome del file.

## <a name="filters"></a>Filtri

Le informazioni contenute in questa sezione si  applicano alle finestre di dialogo Apri e **Salva** con nome in stile Esplora risorse e stile precedente.

È possibile specificare filtri per i nomi di file che consentono all'utente di limitare i nomi di file visualizzati nella finestra di dialogo. Un filtro di nome file è costituito da una coppia di stringhe con terminazione Null, una descrizione e un modello, una concatenata all'altra. Nella finestra di dialogo viene visualizzata la descrizione per consentire all'utente di scegliere il filtro da usare. e usa il modello per selezionare i file da visualizzare.

Per specificare i filtri, impostare il membro **lpstrFilter** della struttura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) in modo che punti a un buffer che contiene una matrice di coppie di stringhe di filtro. L'ultima stringa nella matrice deve essere seguita da un carattere Null aggiuntivo.

Una stringa di criteri può essere una combinazione di caratteri validi per il nome file e l'asterisco ( \* ). L'asterisco è un carattere jolly che rappresenta qualsiasi combinazione di caratteri validi del nome file. Nella finestra di dialogo vengono visualizzati solo i file che corrispondono al modello. Per specificare più criteri per la stessa descrizione, è necessario usare un punto e virgola (;) per separare i modelli. Si noti che gli spazi nella stringa del criterio possono produrre risultati imprevisti.

Nel frammento di codice seguente vengono specificati due filtri. Il filtro con la descrizione "Source" ha due modelli. Se l'utente seleziona questo filtro, nella finestra di dialogo vengono visualizzati solo i file con . C e . Estensioni CXX. Si noti che nel linguaggio di programmazione C una stringa racchiusa tra virgolette doppie ha terminazione Null.


```
OPENFILENAME ofn;       // common dialog box structure

ofn.lpstrFilter = "Source\0*.C;*.CXX\0All\0*.*\0"
ofn.nFilterIndex = 1;
```



Il **membro nFilterIndex** della struttura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) specifica un indice che indica quale filtro viene inizialmente utilizzato dalla finestra di dialogo. Il primo filtro nel buffer include l'indice 1, il secondo 2 e così via. Se l'utente modifica il filtro durante l'uso della finestra di dialogo, il membro **nFilterIndex** viene impostato sull'indice del filtro selezionato al ritorno.

È possibile creare un filtro personalizzato impostando il membro **lpstrCustomFilter** sull'indirizzo di un buffer che contiene un singolo filtro e impostando il membro **nMaxCustFilter** sulla dimensione del buffer, in caratteri o byte. La finestra di dialogo inserisce sempre il filtro personalizzato all'inizio dell'elenco di filtri e, al ritorno, aggiorna sempre la parte del criterio del filtro con il criterio del filtro selezionato dall'utente.

Per le finestre di dialogo di tipo Esplora risorse, l'estensione predefinita può cambiare se l'utente seleziona un filtro diverso. Se l'utente seleziona un filtro il cui primo modello è nel formato \* .*xxx* (ovvero l'estensione non include un carattere jolly), la finestra di dialogo usa *xxx* come estensione predefinita. Questo errore si verifica solo se è stata specificata un'estensione predefinita nel membro **lpstrDefExt** della [**struttura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) Ad esempio, se l'utente seleziona "Origine \\ 0 \* . C; \* . filtro CXX \\ 0", l'estensione predefinita viene modificata in "C". Tuttavia, se il filtro è stato definito come "Source \\ 0 \* . C \* \\ 0", l'estensione predefinita non cambia perché l'estensione include un carattere jolly.

Il [**rete CDN di notifica \_ INCLUDEITEM**](cdn-includeitem.md) offre un altro modo per filtrare i nomi visualizzati nella finestra di dialogo. Per usare questo messaggio, specificare una routine hook [**OFNHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) e specificare il flag **OFN \_ ENABLEINCLUDENOTIFY** nella struttura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) quando si crea la finestra di dialogo. Ogni volta che l'utente apre una cartella, la finestra di dialogo invia una notifica **\_ includeITEM rete CDN** alla procedura hook per ogni elemento nella cartella appena aperta. Il valore restituito della routine hook indica se nella finestra di dialogo deve essere visualizzato l'elemento nell'elenco di elementi della cartella.

## <a name="file-and-directory-validation"></a>Convalida di file e directory

Fatta eccezione per quanto specificato, le informazioni contenute in  questa sezione si applicano sia alle finestre di dialogo Apri e **Salva con** nome di tipo Esplora risorse che alle finestre di dialogo di tipo Precedente.

La finestra di dialogo convalida automaticamente i nomi di file digitati dall'utente per garantire che i nomi contengano solo caratteri validi. Per eseguire l'override della convalida dei caratteri del nome file, impostare il flag **\_ OFN NOVALIDATE.**

Per forzare la finestra di dialogo per verificare che l'utente ha specificato il nome di un file esistente, impostare il flag **\_ OFN FILEMUSTEXIST.** Per forzare la verifica dell'esistenza del percorso specificato, impostare il flag **\_ OFN PATHMUSTEXIST.** Se si imposta il flag **OFN \_ CREATEPROMPT,** la finestra di dialogo richiede all'utente l'autorizzazione per creare un file inesistente. Se questo flag è impostato e l'utente sceglie di creare un nuovo file, la finestra di dialogo viene chiusa e la funzione restituisce il nome specificato. In caso contrario, la finestra di dialogo rimane aperta.

Quando si usa la **finestra** di dialogo Salva con nome , è possibile indirizzare la finestra di dialogo per richiedere all'utente l'autorizzazione per sovrascrivere un file esistente impostando il flag **OFN \_ OVERWRITEPROMPT.**

Per impostazione predefinita, la finestra di dialogo crea un file di test di lunghezza zero per determinare se è possibile creare un nuovo file nella directory selezionata. Per impedire la creazione di questo file di test, impostare il flag **OFN \_ NOTESTFILECREATE.**

Se si abilita una routine hook, la finestra di dialogo invia una notifica alla procedura hook quando si verifica una violazione della condivisione di rete per il nome file specificato dall'utente. Se si imposta il flag **OFN \_ EXPLORER,** la finestra di dialogo [**invia il messaggio rete CDN \_ SHAREVIOLATION**](cdn-shareviolation.md) alla procedura hook. Se non si imposta **OFN \_ EXPLORER,** la finestra di dialogo invia il messaggio registrato [**SHAREVISTRING**](sharevistring.md) alla procedura hook. Per impedire alla finestra di dialogo di inviare notifiche per violazioni di condivisione, impostare il flag **\_ SHAREAWARE OFN.**

Se l'utente seleziona la casella di controllo di sola lettura, la finestra di dialogo imposta il flag **OFN \_ READONLY** al ritorno. Per nascondere la **casella di controllo Apri** come sola lettura, impostare il flag **\_ OFN HIDEREADONLY.** Per impedire alla finestra di dialogo di restituire nomi di file esistenti con l'attributo di sola lettura, impostare il flag **OFN \_ NOREADONLYRETURN.**

Per impedire alla finestra di dialogo di dereferenziare i file di collegamento, impostare il **valore OFN \_ NODEREFERENCELINKS.** In questo caso, la finestra di dialogo restituisce il nome del file di collegamento anziché il nome del file a cui fa riferimento il file di collegamento.

## <a name="open-and-save-as-dialog-box-customization"></a>Personalizzazione della finestra di dialogo Apri e salva con nome

È possibile personalizzare una **finestra di** dialogo Apri o **Salva** con nome fornendo una procedura hook, un modello personalizzato o entrambi. Tuttavia, le versioni in stile Esplora risorse e le versioni precedenti delle finestre di dialogo differiscono per l'uso di modelli personalizzati e routine hook.

Per informazioni sulla personalizzazione di una finestra di dialogo di tipo Explorer, vedere Routine hook in stile [Explorer,](#explorer-style-hook-procedures)Modelli personalizzati in stile [Explorer](#explorer-style-custom-templates)e Identificatori di controllo in stile [Esplora risorse.](#explorer-style-control-identifiers) Per informazioni sulla personalizzazione di una finestra di dialogo di tipo precedente, vedere Personalizzazione Old-Style [finestre di dialogo.](#customizing-old-style-dialog-boxes)

Nella tabella seguente vengono riepilogate le differenze tra i due stili.



| Personalizzazione                  | Descrizione                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Procedura hook di tipo Explorer  | La procedura hook riceve messaggi di notifica inviati dalla finestra di dialogo comune e messaggi per tutti i controlli aggiuntivi definiti specificando un modello di finestra di dialogo figlio. La routine hook non riceve messaggi per i controlli standard della finestra di dialogo predefinita. |
| Modello personalizzato in stile Esplora risorse | Il sistema usa il modello personalizzato per creare una finestra di dialogo figlio. Il modello può definire controlli aggiuntivi e può specificare la posizione del cluster di controlli standard. Il modello personalizzato non sostituisce il modello predefinito.                                          |
| Procedura hook precedente       | La routine hook riceve tutti i messaggi inviati alla finestra di dialogo, inclusi i messaggi per i controlli standard ed eventuali controlli personalizzati. La routine hook riceve anche i messaggi registrati inviati dalla finestra di dialogo comune.                                                         |
| Modello personalizzato in stile precedente      | Il modello personalizzato sostituisce il modello predefinito. Creare il modello personalizzato modificando il modello predefinito specificato nel file Fileopen.dlg.                                                                                                                                  |



 

Il titolo predefinito per entrambe le finestre di dialogo di tipo Esplora risorse e precedente è "**Apri**" o **"Salva con nome".** Per modificare il titolo, specificare il nuovo titolo nel membro **lpstrTitle** della [**struttura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)

L'hive del Registro di sistema **HKEY CURRENT \_ \_ USER** di un  utente può contenere valori che personalizzano il contenuto delle finestre di dialogo Apri e **Salva con** nome in stile Esplora risorse. Queste voci del Registro di sistema influiscono solo sulle finestre di dialogo visualizzate per l'utente associato all'hive del Registro di sistema.

Per nascondere le funzionalità  delle finestre di dialogo Apri e **Salva** con nome in stile Esplora risorse, un amministratore può impostare i valori nella tabella seguente in questa sottochiave:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Comdlg32
```



| Nome del valore       | Valore | Significato                                  |
|------------------|-------|------------------------------------------|
| **NoPlacesBar**  | 1     | Nasconde la barra dei luoghi.                    |
| **NoFileMRU**    | 1     | Nasconde l'elenco degli elementi usati più di recente. |
| **NoBackButton** | 1     | Nasconde il **pulsante** Indietro.               |



 

Il contenuto della **barra Posizioni** è determinato dal contenuto della sottochiave seguente:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Comdlg32
                     Placesbar
```

Attualmente, in questa chiave possono essere presenti solo cinque voci e l'indice di valore/nome è in base zero. I nomi delle voci devono essere Place0, Place1, Place2, Place3 e Place4. I valori delle voci possono essere **REG \_ DWORD,** **REG \_ SZ** o **REG EXPAND \_ \_ SZ** che identificano le posizioni da includere nella barra delle posizioni.



| Tipo di valore                         | Significato                                                                                                   |
|------------------------------------|-----------------------------------------------------------------------------------------------------------|
| **REG \_ DWORD**                     | Valore CSIDL che identifica una cartella. Per un elenco di valori CSIDL, vedere [**Valori CSIDL.**](../shell/csidl.md) |
| **REG \_ SZ** o **REG \_ EXPAND \_ SZ** | Stringa con terminazione Null che specifica un percorso valido.                                                     |



 

## <a name="explorer-style-hook-procedures"></a>Explorer-Style hook

È possibile personalizzare una finestra di dialogo **Apri** o **Salva** con nome di tipo Esplora risorse fornendo una procedura hook, un modello personalizzato o entrambi. Se si specifica una routine hook per una finestra di dialogo di tipo Esplora risorse, il sistema crea una finestra di dialogo figlio della finestra di dialogo predefinita. La routine hook funge da routine di dialogo per la finestra di dialogo figlio. Questa finestra di dialogo figlio è basata sul modello personalizzato o su un modello predefinito se non ne viene specificato nessuno. Per altre informazioni, vedere [Modelli personalizzati in stile Esplora risorse.](#explorer-style-custom-templates)

Per abilitare una routine hook  per una finestra di dialogo Apri o **Salva** con nome di tipo Esplora risorse, utilizzare la struttura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) quando si crea la finestra di dialogo. Impostare i flag **OFN \_ ENABLEHOOK** e **OFN \_ EXPLORER** nel membro **Flags** e specificare l'indirizzo di una procedura hook [**OFNHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) nel membro **lpfnHook.** Se si specifica una routine hook e si omette il flag **OFN \_ EXPLORER,** è necessario usare una routine hook [**OFNHookProcOldStyle**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) per ottenere l'interfaccia utente di tipo precedente. Per altre informazioni, vedere [Personalizzazione Old-Style di dialogo.](#customizing-old-style-dialog-boxes)

Una routine hook di tipo Esplora risorse riceve diversi messaggi mentre la finestra di dialogo è aperta. tra cui:

-   Messaggio [**WM \_ INITDIALOG e**](wm-initdialog.md) altri messaggi di finestra di dialogo standard, ad esempio il messaggio di colore del controllo WM [**\_ CTLCOLORDLG.**](wm-ctlcolordlg.md)
-   Set di messaggi [**di \_ notifica WM NOTIFY**](../controls/wm-notify.md) che indicano le azioni eseguite dall'utente o da altri eventi della finestra di dialogo.
-   Messaggi per tutti i controlli aggiuntivi definiti specificando un modello di finestra di dialogo figlio.

È inoltre disponibile un set di messaggi che è possibile inviare a una finestra di dialogo di tipo Esplora risorse per ottenere informazioni o per controllare il comportamento e l'aspetto della finestra di dialogo.

Se si specifica una routine hook per una finestra di dialogo di tipo Esplora risorse, la routine della finestra di dialogo predefinita crea una finestra di dialogo figlio quando la routine predefinita della finestra di dialogo elabora il messaggio [**WM \_ INITDIALOG.**](wm-initdialog.md) La routine hook funge da routine di dialogo per la finestra di dialogo figlio. A questo momento, la routine hook riceve il proprio messaggio **WM \_ INITDIALOG** con il parametro *lParam* impostato sull'indirizzo della struttura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) usata per inizializzare la finestra di dialogo. Al termine dell'elaborazione del messaggio **\_ WM INITDIALOG** da parte della finestra di dialogo figlio, la procedura predefinita sposta i controlli standard, se necessario, per fare spazio a eventuali controlli aggiuntivi della finestra di dialogo figlio. La procedura di dialogo predefinita invia quindi [**il rete CDN di notifica \_ INITDONE**](cdn-initdone.md) alla procedura hook.

La procedura hook riceve messaggi [**di \_ notifica WM NOTIFY**](../controls/wm-notify.md) che indicano le azioni eseguite dall'utente nella finestra di dialogo. È possibile utilizzare alcuni di questi messaggi per controllare il comportamento della finestra di dialogo. Ad esempio, la procedura hook riceve il messaggio [**rete CDN \_ FILEOK**](cdn-fileok.md) quando l'utente sceglie un nome di file e fa clic sul **pulsante OK.** In risposta a questo messaggio, la procedura hook può usare la [**funzione SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per rifiutare il nome selezionato e forzare la finestra di dialogo a rimanere aperta.

Il *parametro lParam* per ogni [**messaggio WM \_ NOTIFY**](../controls/wm-notify.md) è un puntatore a una [**struttura OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) o [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) che definisce l'azione. Il **membro** di codice nell'intestazione di questa struttura contiene uno dei messaggi di notifica seguenti.



| Messaggio                                           | Significato                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_rete CDN FILEOK**](cdn-fileok.md)                 | L'utente ha fatto clic **sul pulsante OK.** la finestra di dialogo sta per essere chiusa.                                                                                                                                                                                                                          |
| [**\_rete CDN FOLDERCHANGE**](cdn-folderchange.md)     | L'utente ha aperto una nuova cartella o una nuova directory.                                                                                                                                                                                                                                                     |
| [**\_rete CDN Guida**](cdn-help.md)                     | L'utente ha fatto clic **sul pulsante ?** .                                                                                                                                                                                                                                                          |
| [**\_rete CDN INCLUDEITEM**](cdn-includeitem.md)       | Determina se un elemento deve essere visualizzato. Quando l'utente apre una nuova cartella o directory, il sistema invia questa notifica per ogni elemento nella cartella o nella directory. Il sistema invia questa notifica solo se è stato impostato il flag **\_ OFN ENABLEINCLUDENOTIFY.**                          |
| [**\_rete CDN INITDONE**](cdn-initdone.md)             | Il sistema ha completato l'inizializzazione della finestra di dialogo e la finestra di dialogo ha terminato l'elaborazione del [**messaggio WM \_ INITDIALOG.**](wm-initdialog.md) Inoltre, il sistema ha completato la disposizione dei controlli nella finestra di dialogo comune per fare spazio ai controlli della finestra di dialogo figlio (se presente). |
| [**\_rete CDN Selchange**](cdn-selchange.md)           | L'utente ha selezionato un nuovo file o una nuova cartella dall'elenco di file.                                                                                                                                                                                                                                     |
| [**\_rete CDN SHAREVIOLATION**](cdn-shareviolation.md) | Nella finestra di dialogo comune è stata rilevata una violazione di condivisione nel file che sta per essere restituito.                                                                                                                                                                                                        |
| [**\_rete CDN TYPECHANGE**](cdn-typechange.md)         | L'utente ha selezionato un nuovo tipo di file dall'elenco dei tipi di file.                                                                                                                                                                                                                                 |



 

Questi [**messaggi WM \_ NOTIFY**](../controls/wm-notify.md) soppiattono i  messaggi registrati [**FILEOKSTRING,**](fileokstring.md) [**LBSELCHSTRING,**](lbselchstring.md) [**SHAREVISTRING**](sharevistring.md)  [**e HELPMSGSTRING**](helpmsgstring.md) usati dalle versioni precedenti delle finestre di dialogo Apri e Salva con nome. Tuttavia, la routine hook riceve anche il messaggio sostituito dopo il messaggio **WM \_ NOTIFY** se l'elaborazione **WM \_ NOTIFY** non usa [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per impostare un valore **\_ MSGRESULT DWL** diverso da zero.

Per recuperare informazioni sullo stato della finestra di dialogo o per controllare il comportamento e l'aspetto della finestra di dialogo, la procedura hook può inviare i messaggi seguenti alla finestra di dialogo.



| Messaggio                                             | Significato                                                                                                                                                                                                                  |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CDM \_ GETFILEPATH**](cdm-getfilepath.md)         | Recupera il percorso e il nome del file selezionato.                                                                                                                                                                   |
| [**CDM \_ GETFOLDERIDLIST**](cdm-getfolderidlist.md) | Recupera l'elenco di identificatori di elemento corrispondente alla cartella corrente aperta nella finestra di dialogo. Per altre informazioni sugli elenchi di identificatori di elemento, vedere [Introduzione allo spazio dei nomi shell](/windows/desktop/shell/namespace-intro). |
| [**CDM \_ GETFOLDERPATH**](cdm-getfolderpath.md)     | Recupera il percorso della cartella o della directory corrente per la finestra di dialogo.                                                                                                                                                |
| [**GETSPEC di CDM \_**](cdm-getspec.md)                 | Recupera il nome file (senza includere il percorso) del file attualmente selezionato nella finestra di dialogo.                                                                                                                       |
| [**HIDECONTROL DI CDM \_**](cdm-hidecontrol.md)         | Nasconde il controllo specificato.                                                                                                                                                                                             |
| [**CDM \_ SETCONTROLTEXT**](cdm-setcontroltext.md)   | Imposta il testo nel controllo specificato.                                                                                                                                                                                  |
| [**CDM \_ SETDEFEXT**](cdm-setdefext.md)             | Imposta l'estensione di file predefinita per la finestra di dialogo.                                                                                                                                                                 |



 

## <a name="explorer-style-custom-templates"></a>Explorer-Style modelli personalizzati

Per definire controlli aggiuntivi per  una  finestra di dialogo Apri o Salva con nome in stile Esplora risorse, usare la struttura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) per specificare un modello per una finestra di dialogo figlio contenente i controlli aggiuntivi. Se il modello di dialogo figlio è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare il flag **\_ OFN ENABLETEMPLATE** nel membro **Flags** e usare i membri **hInstance** e **lpTemplateName** della struttura per identificare il modulo e il nome della risorsa. Se il modello è già in memoria, impostare il flag **OFN \_ ENABLETEMPLATEHANDLE** e usare il membro **hInstance** per identificare l'oggetto di memoria che contiene il modello. Quando si fornisce un modello di finestra di dialogo figlio per una finestra di dialogo in stile Esplora risorse, è necessario impostare anche il flag **OFN \_ EXPLORER.** In caso contrario, il sistema presuppone che si fornirà un modello sostitutivo per una finestra di dialogo di stile precedente. In genere, se si forniscono controlli aggiuntivi, è necessario fornire anche una procedura hook di tipo [Esplora](#explorer-style-hook-procedures) risorse per elaborare i messaggi per i nuovi controlli.

È possibile creare il modello di finestra di dialogo figlio come qualsiasi altro modello, ad eccezione del fatto che è necessario specificare gli stili **WS \_ CHILD** e **WS \_ CLIPSIBLINGS** e specificare gli stili **DS \_ 3DLOOK** e **DS \_ CONTROL.** Il sistema richiede lo **stile WS \_ CHILD** perché il modello definisce una finestra di dialogo figlio della finestra di dialogo predefinita **Apri** o **Salva** con nome. Lo **stile \_ WS CLIPSIBLINGS** garantisce che la finestra di dialogo figlio non dipinga alcun controllo nella finestra di dialogo predefinita. Lo **stile \_ DS 3DLOOK** assicura che l'aspetto dei controlli nella finestra di dialogo figlio sia coerente con i controlli nella finestra di dialogo predefinita. Lo **stile DS \_ CONTROL** garantisce che l'utente possa usare TAB e altri tasti di spostamento per spostarsi tra tutti i controlli, predefiniti o personalizzati, nella finestra di dialogo personalizzata.

Per fare spazio ai nuovi controlli, il sistema espande la finestra di dialogo predefinita in base alla larghezza e all'altezza della finestra di dialogo personalizzata. Per impostazione predefinita, tutti i controlli della finestra di dialogo personalizzata sono posizionati sotto i controlli nella finestra di dialogo predefinita. È tuttavia possibile eseguire l'override di questo posizionamento predefinito includendo un controllo di testo statico nel modello di finestra di dialogo personalizzato e assegnando il valore dell'identificatore di controllo **stc32**. Questo valore è definito nel file di intestazione Dlgs.h. In questo caso, il sistema usa il controllo come punto di riferimento per determinare dove posizionare i nuovi controlli. Tutti i nuovi controlli sopra e a sinistra del controllo **stc32** vengono posizionati nella stessa quantità sopra e a sinistra dei controlli nella finestra di dialogo predefinita. I nuovi controlli sotto e a destra del **controllo stc32** sono posizionati sotto e a destra dei controlli predefiniti. In generale, ogni nuovo controllo viene posizionato in modo che abbia la stessa posizione rispetto ai controlli predefiniti rispetto al **controllo stc32.** Per fare spazio a questi nuovi controlli, il sistema aggiunge spazio a sinistra, a destra, in basso e nella parte superiore della finestra di dialogo predefinita in base alle esigenze.

Il sistema richiede la procedura hook per elaborare tutti i messaggi destinati alla finestra di dialogo personalizzata e quindi invia gli stessi messaggi della finestra alla routine hook di qualsiasi altra routine della finestra di dialogo. Ad esempio, la routine hook riceve messaggi [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) quando l'utente fa clic sui controlli pulsante nella finestra di dialogo personalizzata. La procedura hook è responsabile dell'inizializzazione di questi controlli e del recupero di valori dai controlli quando la finestra di dialogo viene chiusa. Si noti che quando la routine hook riceve il [**messaggio WM \_ INITDIALOG,**](wm-initdialog.md) il sistema non ha ancora spostato i controlli nelle posizioni finali.

La procedura predefinita della finestra di dialogo gestisce i messaggi per tutti i controlli nella finestra di dialogo predefinita, ma la procedura hook riceve i messaggi di notifica per le azioni dell'utente su questi controlli, come descritto in Procedure [hook](#explorer-style-hook-procedures)in stile Esplora risorse .

## <a name="explorer-style-control-identifiers"></a>Explorer-Style identificatori di controllo

Il Windows Software Development Kit (SDK) fornisce il modello di finestra di dialogo predefinito per le finestre di dialogo di stile precedente, ma non include il modello predefinito per le finestre di dialogo in stile Esplora risorse. Ciò è dovuto al fatto che le finestre di dialogo in stile Esplora risorse consentono di aggiungere controlli personalizzati, ma non supportano la modifica del modello per i controlli standard. In alcuni casi, tuttavia, potrebbe essere necessario conoscere gli identificatori di controllo usati nei modelli predefiniti. Ad esempio, i [**messaggi CDM \_ HIDECONTROL**](cdm-hidecontrol.md) e [**CDM \_ SETCONTROLTEXT**](cdm-setcontroltext.md) richiedono un identificatore di controllo.

Nella tabella seguente vengono illustrati gli identificatori dei  controlli standard nelle finestre di dialogo Apri e **Salva con** nome in stile Esplora risorse. Gli identificatori sono costanti definite in Dlgs.h e Winuser.h.



| Identificatore di controllo | Descrizione del controllo                                                                                                                                                                                                                                                                        |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **chx1**           | Casella di controllo di sola lettura                                                                                                                                                                                                                                                                    |
| **cmb1**           | Casella combinata a discesa che visualizza l'elenco di filtri per i tipi di file                                                                                                                                                                                                                            |
| **stc2**           | Etichetta per la **casella combinata cmb1**                                                                                                                                                                                                                                                           |
| **cmb2**           | Casella combinata a discesa che visualizza l'unità o la cartella corrente e che consente all'utente di selezionare un'unità o una cartella da aprire                                                                                                                                                                |
| **stc4**           | Etichetta per la **casella combinata cmb2**                                                                                                                                                                                                                                                           |
| **cmb13**          | Casella combinata a discesa che visualizza il nome del file corrente, consente all'utente di digitare il nome di un file da aprire e selezionare un file aperto o salvato di recente. Questo è per le applicazioni precedenti compatibili con Esplora risorse senza hook o modello di finestra di dialogo. Confrontare con **edt1**. |
| **edt1**           | Controllo di modifica che visualizza il nome del file corrente o consente all'utente di digitare il nome del file da aprire. Confrontare con **cmb13**.                                                                                                                                                  |
| **stc3**           | Etichetta per la casella **combinata cmb13** e il controllo di modifica edt1                                                                                                                                                                                                                                |
| **lst1**           | Casella di riepilogo che visualizza il contenuto dell'unità o della cartella corrente                                                                                                                                                                                                                         |
| **stc1**           | Etichetta per la casella **di riepilogo lst1**                                                                                                                                                                                                                                                            |
| **IDOK**           | Pulsante di comando **OK** (pulsante di invio)                                                                                                                                                                                                                                                    |
| **IDCANCEL**       | Pulsante **di** comando Annulla (pulsante di invio)                                                                                                                                                                                                                                                |
| **pshHelp**        | Pulsante **di** comando Guida (pulsante di invio)                                                                                                                                                                                                                                                  |



 

## <a name="customizing-old-style-dialog-boxes"></a>Personalizzazione di Old-Style finestre di dialogo

È possibile personalizzare una  vecchia  finestra di dialogo Apri o Salva con nome fornendo una routine hook [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) che riceve messaggi o notifiche destinati alla procedura predefinita della finestra di dialogo. È anche possibile fornire un modello personalizzato da usare al posto del modello predefinito. Le procedure hook e i modelli usati con le finestre di dialogo di stile precedente sono simili a quelli usati con le altre finestre di dialogo comuni. Per altre informazioni, vedere [Procedure hook per finestre di dialogo comuni](customizing-common-dialog-boxes.md) e modelli [personalizzati.](customizing-common-dialog-boxes.md)

Per abilitare una procedura hook  per  una finestra di dialogo Apri o Salva con nome di vecchio stile, usare la struttura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) quando si crea la finestra di dialogo. Impostare il flag **\_ OFN ENABLEHOOK** nel membro **Flags** e specificare l'indirizzo di una routine hook [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) nel membro **lpfnHook.** La routine della finestra di dialogo invia un messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) alla routine hook con il *parametro Param* impostato sull'indirizzo della struttura **OPENFILENAME** utilizzata per inizializzare la finestra di dialogo.

È possibile usare la [**struttura OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) per  specificare  un modello personalizzato per la finestra di dialogo Apri o Salva con nome da usare al posto del modello predefinito. Se il modello personalizzato è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare il flag **\_ OFN ENABLETEMPLATE** nel membro **Flags** e usare i membri **hInstance** e **lpTemplateName** della struttura per identificare il modulo e il nome della risorsa. Se il modello personalizzato è già in memoria, impostare il flag **OFN \_ ENABLETEMPLATEHANDLE** e usare il membro **hInstance** per identificare l'oggetto memoria che contiene il modello. Creare il modello personalizzato modificando il modello predefinito specificato nel file Fileopen.dlg. Gli identificatori di controllo usati nei modelli predefiniti della finestra di dialogo Trova e sostituisci sono definiti nel file Dlgs.h.

Per impostazione predefinita, le [**funzioni GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) e [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) visualizzano le finestre di dialogo in stile Esplora risorse. Se si vuole visualizzare una finestra di dialogo di stile precedente, è necessario fornire una routine hook [**OFNHookProcOldStyle**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) e assicurarsi che il flag **OFN \_ EXPLORER** non sia impostato nel membro **Flags** della struttura [**OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)

Se si imposta il flag **OFN \_ EXPLORER,** il sistema considera una routine hook o un modello personalizzato come una personalizzazione di tipo Esplora risorse. Per informazioni sulla personalizzazione di una finestra di dialogo in stile Esplora risorse, vedere [Modelli personalizzati in stile Esplora risorse](#explorer-style-custom-templates).

## <a name="see-also"></a>Vedi anche

* [Esempio di file in uso](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse)