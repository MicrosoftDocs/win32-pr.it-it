---
title: Finestre di dialogo Apri e Salva con nome
description: La finestra di dialogo Apri consente all'utente di specificare l'unità, la directory e il nome di un file o di un set di file da aprire.
ms.assetid: 5676ca9d-daca-40bf-8881-def2ff841c58
keywords:
- Libreria finestra di dialogo comune
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
ms.openlocfilehash: bc2977a5f91abde32a78c722a7a7c7b6b4a23ffd
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323878"
---
# <a name="open-and-save-as-dialog-boxes"></a>Finestre di dialogo Apri e Salva con nome

> [!NOTE]
> La funzione [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) è illustrata nell' [esempio di file in uso](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse).

\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)). È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]

La finestra di dialogo **Apri** consente all'utente di specificare l'unità, la directory e il nome di un file o di un set di file da aprire. Per creare e visualizzare una finestra di dialogo **aperta** , inizializzare una struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) e passare la struttura alla funzione [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) .

La finestra di dialogo **Salva con** nome consente all'utente di specificare l'unità, la directory e il nome di un file da salvare. Per creare e visualizzare una finestra di dialogo **Salva con nome** , inizializzare una struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) e passare la struttura alla funzione [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) .

Le finestre di dialogo **Apri** e **Salva con nome in** stile Explorer forniscono funzionalità dell'interfaccia utente simili a quelle di Esplora risorse. Tuttavia, il sistema continua a supportare le finestre di dialogo **Apri** e **Salva con nome** obsolete per le applicazioni che devono essere coerenti con l'interfaccia utente di tipo obsoleto.

Oltre alla differenza nell'aspetto, le finestre di dialogo di tipo Esplora risorse e obsolete differiscono per l'utilizzo di modelli personalizzati e di procedure hook per la personalizzazione delle finestre di dialogo. Tuttavia, le finestre di dialogo di tipo Esplora risorse e obsolete hanno lo stesso comportamento per la maggior parte delle operazioni di base, ad esempio la specifica di un filtro di nome file, la convalida dell'input dell'utente e il recupero del nome del file specificato dall'utente. Per ulteriori informazioni sulle finestre di dialogo di tipo Esplora risorse e obsolete, vedere la pagina relativa alla [personalizzazione della finestra di dialogo Apri e Salva con nome](#open-and-save-as-dialog-box-customization).

Nella figura seguente viene illustrata una tipica finestra di dialogo **Apri** in stile Esplora risorse.

![finestra di dialogo Apri file](images/opendialogboxxp.png)

Nella figura seguente viene illustrata una tipica finestra di dialogo **Salva con nome in** stile Esplora risorse.

![finestra di dialogo Salva file](images/saveasdialogboxxp.png)

Se l'utente specifica un nome di file e fa clic sul pulsante **OK** , [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) o [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) restituisce **true**. Il buffer a cui punta il membro **lpstrFile** della struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) contiene il percorso completo e il nome file specificati dall'utente.

Se l'utente annulla la finestra di dialogo **Apri** o **Salva con nome** o si verifica un errore, la funzione restituisce **false**. Per determinare la cause dell'errore, chiamare la funzione [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) per recuperare il valore di errore esteso. Se il buffer **lpstrFile** è troppo piccolo per ricevere il nome completo, **CommDlgExtendedError** restituisce **FNERR \_ BUFFERTOOSMALL** e i primi 2 byte del buffer a cui punta il membro **lpstrFile** vengono impostati su un valore integer che specifica le dimensioni necessarie per ricevere il nome completo.

In questa sezione vengono descritti gli argomenti seguenti.

-   [Nomi di file e directory](#file-names-and-directories)
-   [Filtri](#filters)
-   [Convalida di file e directory](#file-and-directory-validation)
-   [Personalizzazione della finestra di dialogo Apri e Salva con nome](#open-and-save-as-dialog-box-customization)
-   [Routine hook di tipo Esplora risorse](#explorer-style-hook-procedures)
-   [Modelli personalizzati di tipo Esplora risorse](#explorer-style-custom-templates)
-   [Identificatori di controlli di tipo Esplora risorse](#explorer-style-control-identifiers)
-   [Personalizzazione delle finestre di dialogo Old-Style](#customizing-old-style-dialog-boxes)

## <a name="file-names-and-directories"></a>Nomi di file e directory

Le informazioni contenute in questa sezione sono valide per le finestre di dialogo **Apri** e **Salva con nome** di tipo Esplora risorse e obsolete.

Prima di chiamare le funzioni [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) o [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) , il membro **lpstrFile** della struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) deve puntare al buffer per ricevere il nome del file. Il membro **nMaxFile** deve specificare la dimensione, in caratteri, del buffer **lpstrFile** . Per una funzione ANSI si tratta del numero di byte, ma per una funzione Unicode corrisponde al numero di caratteri.

Se l'utente specifica un nome di file e fa clic sul pulsante **OK** , la finestra di dialogo Copia l'unità, la directory e il nome file selezionati nel buffer di **lpstrFile** . La funzione imposta anche i membri **nFileOffset** e **nFileExtension** sugli offset, in caratteri, dall'inizio del buffer al nome del file e all'estensione del nome file, rispettivamente.

Per recuperare solo il nome file e l'estensione, impostare il membro **lpstrFileTitle** in modo che punti a un buffer e impostare il membro **nMaxFileTitle** sulla dimensione, in caratteri, del buffer. In alternativa, è possibile passare il buffer **lpstrFile** in una chiamata alla funzione [**GetFileTitle**](/windows/desktop/api/Commdlg/nf-commdlg-getfiletitlea) per ottenere il nome visualizzato del file selezionato. Si noti, tuttavia, che il nome del file restituito da **GetFileTitle** include un'estensione solo se è la preferenza dell'utente per la visualizzazione dei nomi di file.

Nella finestra di dialogo viene utilizzata la directory corrente del processo chiamante come directory iniziale dalla quale visualizzare i file e le directory. Usare le funzioni [**GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) e [**SetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) per ottenere e modificare la directory corrente di un processo. Per specificare una directory iniziale diversa senza modificare la directory corrente, usare il membro **lpstrInitialDir** per specificare il nome di una directory. La finestra di dialogo modifica automaticamente la directory corrente quando l'utente seleziona un'unità o una directory diversa. Per impedire che la finestra di dialogo modifichi la directory corrente, impostare il flag **OFN \_ NOCHANGEDIR** . Questo flag non impedisce all'utente di modificare le directory per trovare un file.

Per specificare un'estensione del nome di file predefinita, usare il membro **lpstrDefExt** . Se l'utente specifica un nome di file che non dispone di un'estensione, la finestra di dialogo aggiunge l'estensione predefinita. Se si specifica un'estensione predefinita e l'utente specifica un nome file con un'estensione diversa, la finestra di dialogo Imposta il flag **OFN \_ EXTENSIONDIFFERENT**

Per consentire all'utente di selezionare più di un file da una directory, impostare il flag **OFN \_ ALLOWMULTISELECT** . Per la compatibilità con le applicazioni meno recenti, la finestra di dialogo selezione multipla predefinita utilizza l'interfaccia utente di tipo obsoleto. Per visualizzare una finestra di dialogo di selezione multipla in stile Esplora risorse, è necessario impostare anche il flag **OFN \_ Explorer** .

Se l'utente seleziona più di un file, il buffer a cui punta il membro **lpstrFile** restituisce il percorso della directory corrente seguito dai nomi file dei file selezionati. Il membro **nFileOffset** è l'offset del primo nome file e il membro **nFileExtension** non viene utilizzato. Nella tabella seguente viene descritta la differenza tra le finestre di dialogo di tipo Esplora risorse e quelle obsolete nella restituzione di più nomi di file.



| Stile della finestra di dialogo            | Descrizione                                                                                                                                                                                                               |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Finestre di dialogo di tipo Esplora risorse | Le stringhe di nomi di file e directory sono separate da **null** , con un carattere **null** aggiuntivo dopo l'ultimo nome file. Questo formato consente alle finestre di dialogo di tipo Esplora risorse di restituire nomi di file lunghi che includono spazi. |
| Finestre di dialogo obsolete      | Le stringhe di nomi di file e directory sono separate da spazi. Per i nomi di file con spazi, la funzione utilizza nomi di file brevi.                                                                                              |



 

È possibile utilizzare la funzione [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) per eseguire la conversione tra nomi di file lunghi e brevi.

Se si specifica **OFN \_ ALLOWMULTISELECT** e l'utente seleziona un solo file, la stringa **lpstrFile** non ha un separatore tra il percorso e il nome file.

## <a name="filters"></a>Filtri

Le informazioni contenute in questa sezione sono valide per le finestre di dialogo **Apri** e **Salva con nome** di tipo Esplora risorse.

È possibile specificare filtri per i nomi di file per aiutare l'utente a limitare i nomi di file visualizzati nella finestra di dialogo. Un filtro di nome file è costituito da una coppia di stringhe con terminazione null, una descrizione e un modello, uno concatenato all'altro. Nella finestra di dialogo viene visualizzata la descrizione per consentire all'utente di selezionare il filtro da utilizzare. e usa il modello per selezionare i file da visualizzare.

Per specificare i filtri, impostare il membro **lpstrFilter** della struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) in modo che punti a un buffer contenente una matrice di coppie di stringhe di filtro. L'ultima stringa della matrice deve essere seguita da un carattere null aggiuntivo.

Una stringa di modello può essere una combinazione di caratteri validi per il nome file e l'asterisco ( \* ). L'asterisco è un carattere jolly che rappresenta qualsiasi combinazione di caratteri di nomi file validi. Nella finestra di dialogo vengono visualizzati solo i file che corrispondono al modello. Per specificare più modelli per la stessa descrizione, è necessario utilizzare un punto e virgola (;) per separare i criteri. Si noti che i caratteri spazio nella stringa del modello possono produrre risultati imprevisti.

Il frammento di codice seguente specifica due filtri. Il filtro con la descrizione "Source" presenta due modelli. Se l'utente seleziona questo filtro, nella finestra di dialogo vengono visualizzati solo i file con estensione. C e. Estensioni CXX. Si noti che nel linguaggio di programmazione C una stringa racchiusa tra virgolette doppie è con terminazione null.


```
OPENFILENAME ofn;       // common dialog box structure

ofn.lpstrFilter = "Source\0*.C;*.CXX\0All\0*.*\0"
ofn.nFilterIndex = 1;
```



Il membro **nFilterIndex** della struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) specifica un indice che indica il filtro utilizzato inizialmente dalla finestra di dialogo. Il primo filtro nel buffer ha indice 1, il secondo 2 e così via. Se l'utente modifica il filtro durante l'utilizzo della finestra di dialogo, il membro **nFilterIndex** viene impostato sull'indice del filtro selezionato in fase di restituzione.

È possibile creare un filtro personalizzato impostando il membro **lpstrCustomFilter** sull'indirizzo di un buffer contenente un singolo filtro e impostando il membro **nMaxCustFilter** sulla dimensione del buffer, in caratteri o byte. La finestra di dialogo posiziona sempre il filtro personalizzato all'inizio dell'elenco di filtri e, in fase di restituzione, aggiorna sempre la parte del filtro con il modello del filtro selezionato dall'utente.

Per le finestre di dialogo di tipo Esplora risorse, è possibile che l'estensione predefinita venga modificata se l'utente seleziona un filtro diverso. Se l'utente seleziona un filtro il cui primo modello è nel formato \* .*xxx* , ovvero l'estensione non include un carattere jolly, la finestra di dialogo USA *xxx* come estensione predefinita. Questa situazione si verifica solo se è stata specificata un'estensione predefinita nel membro **lpstrDefExt** della struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . Se, ad esempio, l'utente seleziona "Source \\ 0" \* . C; \* . CXX \\ 0 "Filter, l'estensione predefinita cambia in" C ". Tuttavia, se il filtro è stato definito come "Source \\ 0" \* . C \* \\ 0 ", l'estensione predefinita non cambia perché l'estensione include un carattere jolly.

Il messaggio di notifica [**\_ INCLUDEITEM**](cdn-includeitem.md) della rete CDN fornisce un altro modo per filtrare i nomi visualizzati nella finestra di dialogo. Per utilizzare questo messaggio, fornire una procedura [**OFNHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) Hook e specificare il flag **OFN \_ ENABLEINCLUDENOTIFY** nella struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) quando si crea la finestra di dialogo. Ogni volta che l'utente apre una cartella, la finestra di dialogo Invia una notifica **\_ INCLUDEITEM** della rete CDN alla routine hook per ogni elemento nella cartella appena aperta. Il valore restituito della routine hook indica se nella finestra di dialogo deve essere visualizzato l'elemento nell'elenco di elementi della cartella.

## <a name="file-and-directory-validation"></a>Convalida di file e directory

Ad eccezione di quanto indicato, le informazioni contenute in questa sezione sono valide per le finestre di dialogo **Apri** e **Salva con nome** di tipo Esplora risorse e obsolete.

La finestra di dialogo convalida automaticamente i nomi di file digitati dall'utente per assicurarsi che i nomi contengano solo caratteri validi. Per eseguire l'override della convalida dei caratteri del nome file, impostare il flag **OFN \_ novalidate** .

Per forzare la finestra di dialogo per verificare che l'utente abbia specificato il nome di un file esistente, impostare il flag **OFN \_ FILEMUSTEXIST** . Per forzare la verifica dell'esistenza del percorso specificato, impostare il flag **OFN \_ PATHMUSTEXIST** . Se si imposta il flag **OFN \_ CREATEPROMPT** , la finestra di dialogo richiede all'utente l'autorizzazione per la creazione di un file inesistente. Se questo flag è impostato e l'utente sceglie di creare un nuovo file, la finestra di dialogo viene chiusa e la funzione restituisce il nome specificato. In caso contrario, la finestra di dialogo rimane aperta.

Quando si utilizza la finestra di dialogo **Salva con nome** , è possibile indirizzare la finestra di dialogo in modo da richiedere all'utente l'autorizzazione a sovrascrivere un file esistente impostando il flag **OFN \_ OVERWRITEPROMPT**

Per impostazione predefinita, nella finestra di dialogo viene creato un file di test di lunghezza zero per determinare se è possibile creare un nuovo file nella directory selezionata. Per evitare la creazione di questo file di test, impostare il flag **OFN \_ NOTESTFILECREATE** .

Se si abilita una routine hook, la finestra di dialogo Invia una notifica alla routine hook quando si verifica una violazione di condivisione di rete per il nome file specificato dall'utente. Se si imposta il flag **OFN \_ Explorer** , la finestra di dialogo Invia il messaggio [**\_ SHAREVIOLATION**](cdn-shareviolation.md) della rete CDN alla routine hook. Se non si imposta **OFN \_ Explorer**, la finestra di dialogo Invia il messaggio [**SHAREVISTRING**](sharevistring.md) registrato alla routine hook. Per impedire che la finestra di dialogo invii notifiche per violazioni di condivisione, impostare il flag **OFN \_ SHAREAWARE** .

Se l'utente seleziona la casella di controllo di sola lettura, la finestra di dialogo Imposta il flag di sola lettura **OFN \_** in caso di restituzione. Per nascondere la casella di controllo **Apri come sola lettura** , impostare il flag **OFN \_ HIDEREADONLY** . Per evitare che la finestra di dialogo restituisca i nomi dei file esistenti con l'attributo di sola lettura, impostare il flag **OFN \_ NOREADONLYRETURN** .

Per impedire alla finestra di dialogo di dereferenziare i file di collegamento, impostare il valore di **OFN \_ NODEREFERENCELINKS** . In questo caso, la finestra di dialogo restituisce il nome del file di collegamento anziché il nome del file a cui fa riferimento il file di collegamento.

## <a name="open-and-save-as-dialog-box-customization"></a>Personalizzazione della finestra di dialogo Apri e Salva con nome

È possibile personalizzare una finestra di dialogo **Apri** o **Salva con nome** fornendo una routine hook, un modello personalizzato o entrambi. Tuttavia, le versioni di tipo Esplora risorse e obsolete delle finestre di dialogo differiscono per l'utilizzo di modelli personalizzati e di procedure hook.

Per informazioni sulla personalizzazione di una finestra di dialogo di tipo Esplora risorse, vedere [procedure hook di tipo](#explorer-style-hook-procedures)Esplora risorse, [modelli personalizzati](#explorer-style-custom-templates)di tipo Esplora risorse e [identificatori di controllo](#explorer-style-control-identifiers)di tipo Esplora risorse. Per informazioni sulla personalizzazione di una finestra di dialogo di tipo obsoleto, vedere [personalizzazione delle finestre di dialogo Old-Style](#customizing-old-style-dialog-boxes).

Nella tabella seguente sono riepilogate le differenze tra i due stili.



| Personalizzazione                  | Descrizione                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Routine hook di tipo Esplora risorse  | La routine hook riceve i messaggi di notifica inviati dalla finestra di dialogo comune e i messaggi per i controlli aggiuntivi definiti specificando un modello di finestra di dialogo figlio. La routine hook non riceve messaggi per i controlli standard della finestra di dialogo predefinita. |
| Modello personalizzato di tipo Esplora risorse | Il sistema utilizza il modello personalizzato per creare una finestra di dialogo figlio. Il modello può definire controlli aggiuntivi e può specificare la posizione del cluster dei controlli standard. Il modello personalizzato non sostituisce il modello predefinito.                                          |
| Procedura hook obsoleta       | La routine hook riceve tutti i messaggi inviati alla finestra di dialogo, inclusi i messaggi per i controlli standard e gli eventuali controlli personalizzati. La routine hook riceve anche i messaggi registrati inviati dalla finestra di dialogo comune.                                                         |
| Modello personalizzato obsoleto      | Il modello personalizzato sostituisce il modello predefinito. Creare il modello personalizzato modificando il modello predefinito specificato nel file FileOpen. dlg.                                                                                                                                  |



 

Il titolo predefinito per le finestre di dialogo di tipo Esplora risorse e obsolete è "**Apri**" o "**Salva con nome**". Per modificare il titolo, specificare il nuovo titolo nel membro **lpstrTitle** della struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .

L'hive del registro di sistema **\_ \_ utente HKEY Current** User può contenere valori che personalizzano il contenuto delle finestre di dialogo **Apri** e **Salva con nome** di tipo Esplora risorse. Queste voci del registro di sistema influiscono solo sulle finestre di dialogo visualizzate per l'utente associato all'hive del registro di sistema.

Per nascondere le funzionalità delle finestre di dialogo **Apri** e **Salva con nome** in stile Esplora risorse, un amministratore può impostare i valori nella tabella seguente sotto questa sottochiave:

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
| **NoPlacesBar**  | 1     | Nasconde la barra dei punti.                    |
| **NoFileMRU**    | 1     | Nasconde l'elenco degli ultimi elementi usati (MRU). |
| **NoBackButton** | 1     | Nasconde il pulsante **indietro** .               |



 

Il contenuto della barra dei **punti** è determinato dal contenuto della sottochiave seguente:

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

Attualmente possono essere presenti solo cinque voci sotto questa chiave e l'indice di valore/nome è in base zero. I nomi delle voci devono essere Place0, Place1, Place2, Place3 e Place4. I valori delle voci possono essere **reg \_ DWORD**, **reg \_ sz** o **reg espandere i valori \_ \_ SZ** che identificano le posizioni da includere nella barra dei punti.



| Tipo di valore                         | Significato                                                                                                   |
|------------------------------------|-----------------------------------------------------------------------------------------------------------|
| **REG \_ DWORD**                     | Valore CSIDL che identifica una cartella. Per un elenco di valori CSIDL, vedere [**valori CSIDL**](../shell/csidl.md). |
| **Reg \_ SZ** o **reg \_ expand \_ SZ** | Stringa con terminazione null che specifica un percorso valido.                                                     |



 

## <a name="explorer-style-hook-procedures"></a>Procedure Hook Explorer-Style

È possibile personalizzare una finestra di dialogo **Apri** o **Salva con nome** di tipo Esplora risorse fornendo una procedura di hook, un modello personalizzato o entrambi. Se si fornisce una procedura di hook per una finestra di dialogo di tipo Esplora risorse, il sistema crea una finestra di dialogo che corrisponde a un elemento figlio della finestra di dialogo predefinita. La routine hook funge da routine della finestra di dialogo per la finestra di dialogo figlio. Questa finestra di dialogo figlio è basata sul modello personalizzato o su un modello predefinito se non ne viene specificato alcuno. Per ulteriori informazioni, vedere [modelli personalizzati di tipo Esplora risorse](#explorer-style-custom-templates).

Per abilitare una routine hook per una finestra di dialogo **Apri** o **Salva con nome** in stile esploratore, utilizzare la struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) quando si crea la finestra di dialogo. Impostare i **flag OFN \_ ENABLEHOOK** e **OFN \_ Explorer** nel membro **Flags** e specificare l'indirizzo di una routine hook [**OFNHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) nel membro **lpfnHook** . Se si specifica una stored procedure di hook e si omette il flag **OFN \_ Explorer** , è necessario usare una procedura di hook [**OFNHookProcOldStyle**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) e si otterrà l'interfaccia utente di tipo obsoleto. Per ulteriori informazioni, vedere [personalizzazione delle finestre di dialogo Old-Style](#customizing-old-style-dialog-boxes).

Una routine hook di tipo Esplora risorse riceve un'ampia gamma di messaggi mentre la finestra di dialogo è aperta. tra cui:

-   Il messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) e altri messaggi standard della finestra di dialogo, ad esempio il messaggio di colore del controllo [**WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md) .
-   Set di messaggi di notifica di notifica [**WM \_**](../controls/wm-notify.md) che indicano le azioni eseguite dall'utente o da altri eventi della finestra di dialogo.
-   Messaggi per tutti i controlli aggiuntivi definiti specificando un modello di finestra di dialogo figlio.

Inoltre, è disponibile un set di messaggi che è possibile inviare a una finestra di dialogo di tipo Esplora risorse per ottenere informazioni o controllare il comportamento e l'aspetto della finestra di dialogo.

Se si fornisce una procedura di hook per una finestra di dialogo di tipo Esplora risorse, la routine della finestra di dialogo predefinita crea una finestra di dialogo figlio quando la routine della finestra di dialogo predefinita elabora il proprio messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) . La routine hook funge da routine della finestra di dialogo per la finestra di dialogo figlio. A questo punto, la routine hook riceve il proprio messaggio **WM \_ INITDIALOG** con il parametro *lParam* impostato sull'indirizzo della struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) usata per inizializzare la finestra di dialogo. Quando la finestra di dialogo figlio completa l'elaborazione del proprio messaggio **WM \_ INITDIALOG** , la routine della finestra di dialogo predefinita sposta i controlli standard, se necessario, per creare spazio per tutti i controlli aggiuntivi della finestra di dialogo figlio. La routine della finestra di dialogo predefinita Invia quindi il messaggio di notifica [**\_ INITDONE**](cdn-initdone.md) della rete CDN alla routine hook.

La procedura di hook riceve i messaggi di notifica di notifica [**WM \_**](../controls/wm-notify.md) che indicano le azioni eseguite dall'utente nella finestra di dialogo. È possibile utilizzare alcuni di questi messaggi per controllare il comportamento della finestra di dialogo. Ad esempio, la routine hook riceve il [**messaggio \_ FILEOK**](cdn-fileok.md) della rete CDN quando l'utente sceglie un nome file e fa clic sul pulsante **OK** . In risposta a questo messaggio, la routine hook può utilizzare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per rifiutare il nome selezionato e forzare la finestra di dialogo in modo che rimanga aperta.

Il parametro *lParam* per ogni messaggio di [**\_ notifica WM**](../controls/wm-notify.md) è un puntatore a una struttura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) o [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) che definisce l'azione. Il membro del **codice** nell'intestazione di questa struttura contiene uno dei seguenti messaggi di notifica.



| Messaggio                                           | Significato                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FILEOK rete CDN \_**](cdn-fileok.md)                 | L'utente ha fatto clic sul pulsante **OK** ; la finestra di dialogo sta per essere chiusa.                                                                                                                                                                                                                          |
| [**FOLDERCHANGE rete CDN \_**](cdn-folderchange.md)     | L'utente ha aperto una nuova cartella o una nuova directory.                                                                                                                                                                                                                                                     |
| [**Guida della rete CDN \_**](cdn-help.md)                     | L'utente ha fatto clic sul pulsante della **Guida** .                                                                                                                                                                                                                                                          |
| [**INCLUDEITEM rete CDN \_**](cdn-includeitem.md)       | Determina se deve essere visualizzato un elemento. Quando l'utente apre una nuova cartella o una nuova directory, il sistema invia la notifica per ogni elemento nella cartella o nella directory. Questa notifica viene inviata dal sistema solo se è stato impostato il flag **OFN \_ ENABLEINCLUDENOTIFY** .                          |
| [**INITDONE rete CDN \_**](cdn-initdone.md)             | L'inizializzazione della finestra di dialogo del sistema è terminata e la finestra di dialogo ha terminato l'elaborazione del messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) . Inoltre, il sistema ha completato la disposizione dei controlli nella finestra di dialogo comune per fare spazio ai controlli della finestra di dialogo figlio (se presente). |
| [**SelChange rete CDN \_**](cdn-selchange.md)           | L'utente ha selezionato un nuovo file o una nuova cartella dall'elenco dei file.                                                                                                                                                                                                                                     |
| [**SHAREVIOLATION rete CDN \_**](cdn-shareviolation.md) | Nella finestra di dialogo comune è stata rilevata una violazione di condivisione sul file che sta per essere restituito.                                                                                                                                                                                                        |
| [**TYPECHANGE rete CDN \_**](cdn-typechange.md)         | L'utente ha selezionato un nuovo tipo di file dall'elenco dei tipi di file.                                                                                                                                                                                                                                 |



 

Questi messaggi di [**\_ notifica WM**](../controls/wm-notify.md) sostituiscono i messaggi registrati [**FILEOKSTRING**](fileokstring.md), [**LBSELCHSTRING**](lbselchstring.md), [**SHAREVISTRING**](sharevistring.md)e [**HELPMSGSTRING**](helpmsgstring.md) usati dalle versioni precedenti delle finestre di dialogo **Apri** e **Salva con nome** . Tuttavia, la routine hook riceve anche il messaggio sostituito dopo il messaggio **di \_ notifica WM** se l'elaborazione di **WM \_ Notify** non usa [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per impostare un valore **\_ MSGRESULT DWL** diverso da zero.

Per recuperare informazioni sullo stato della finestra di dialogo o controllare il comportamento e l'aspetto della finestra di dialogo, la procedura hook può inviare i messaggi seguenti alla finestra di dialogo.



| Messaggio                                             | Significato                                                                                                                                                                                                                  |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CDM \_ filePath**](cdm-getfilepath.md)         | Recupera il percorso e il nome del file selezionato.                                                                                                                                                                   |
| [**\_GETFOLDERIDLIST CDM**](cdm-getfolderidlist.md) | Recupera l'elenco di identificatori di elemento corrispondente alla cartella corrente aperta dalla finestra di dialogo. Per altre informazioni sugli elenchi di identificatori di elemento, vedere [Introduzione allo spazio dei nomi della shell](/windows/desktop/shell/namespace-intro). |
| [**\_GETFOLDERPATH CDM**](cdm-getfolderpath.md)     | Recupera il percorso della cartella o della directory corrente per la finestra di dialogo.                                                                                                                                                |
| [**CDM \_ GETspec**](cdm-getspec.md)                 | Recupera il nome file (senza includere il percorso) del file attualmente selezionato nella finestra di dialogo.                                                                                                                       |
| [**\_HIDECONTROL CDM**](cdm-hidecontrol.md)         | Nasconde il controllo specificato.                                                                                                                                                                                             |
| [**\_SETCONTROLTEXT CDM**](cdm-setcontroltext.md)   | Imposta il testo nel controllo specificato.                                                                                                                                                                                  |
| [**\_SETDEFEXT CDM**](cdm-setdefext.md)             | Imposta l'estensione predefinita per il nome di file per la finestra di dialogo.                                                                                                                                                                 |



 

## <a name="explorer-style-custom-templates"></a>Explorer-Style modelli personalizzati

Per definire ulteriori controlli per una finestra di dialogo **Apri** o **Salva con nome** in stile esploratore, utilizzare la struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) per specificare un modello per una finestra di dialogo figlio contenente i controlli aggiuntivi. Se il modello di finestra di dialogo figlio è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare il flag **OFN \_ ENABLETEMPLATE** nel membro **Flags** e usare i membri **HINSTANCE** e **lpTemplateName** della struttura per identificare il modulo e il nome della risorsa. Se il modello è già in memoria, impostare il flag **OFN \_ ENABLETEMPLATEHANDLE** e usare il membro **HINSTANCE** per identificare l'oggetto memoria che contiene il modello. Quando si specifica un modello di finestra di dialogo figlio per una finestra di dialogo di tipo Esplora risorse, è necessario impostare anche il flag **OFN \_ Explorer** . in caso contrario, il sistema presuppone che venga fornito un modello di sostituzione per una finestra di dialogo di tipo obsoleto. In genere, se si forniscono controlli aggiuntivi, è necessario fornire anche una [procedura di hook di tipo Esplora risorse](#explorer-style-hook-procedures) per elaborare i messaggi per i nuovi controlli.

È possibile creare un modello di finestra di dialogo figlio durante l'esecuzione di qualsiasi altro modello, ad eccezione del fatto che è necessario specificare gli stili **WS \_ child** e **WS \_ CLIPSIBLINGS** e specificare gli stili del **\_ controllo** DS **\_ 3DLOOK** e DS. Il sistema richiede lo stile **WS \_ child** perché il modello definisce una finestra di dialogo figlio della finestra di dialogo predefinita **Apri** o **Salva con nome** . Lo stile **WS \_ CLIPSIBLINGS** garantisce che la finestra di dialogo figlio non venga disegnata su nessuno dei controlli della finestra di dialogo predefinita. Lo stile **DS \_ 3DLOOK** garantisce che l'aspetto dei controlli nella finestra di dialogo figlio sia coerente con i controlli nella finestra di dialogo predefinita. Lo stile del **\_ controllo DS** garantisce che l'utente possa usare la scheda e altri tasti di spostamento per spostarsi tra tutti i controlli, predefiniti o personalizzati, nella finestra di dialogo personalizzata.

Per fare spazio per i nuovi controlli, il sistema espande la finestra di dialogo predefinita in base alla larghezza e all'altezza della finestra di dialogo personalizzata. Per impostazione predefinita, tutti i controlli della finestra di dialogo personalizzata sono posizionati sotto i controlli della finestra di dialogo predefinita. Tuttavia, è possibile eseguire l'override di questo posizionamento predefinito includendo un controllo testo statico nel modello di finestra di dialogo personalizzato e assegnando il valore dell'identificatore di controllo **stc32**. (Questo valore è definito nel file di intestazione Dlgs. h). In questo caso, il sistema utilizza il controllo come punto di riferimento per determinare la posizione in cui posizionare i nuovi controlli. Tutti i nuovi controlli sopra e a sinistra del controllo **stc32** sono posizionati sulla stessa quantità sopra e a sinistra dei controlli nella finestra di dialogo predefinita. I nuovi controlli sotto e a destra del controllo **stc32** sono posizionati sotto e a destra dei controlli predefiniti. In generale, ogni nuovo controllo è posizionato in modo da avere la stessa posizione rispetto ai controlli predefiniti che aveva per il controllo **stc32** . Per fare spazio a questi nuovi controlli, il sistema aggiunge spazio a sinistra, a destra, in basso e all'inizio della finestra di dialogo predefinita in base alle esigenze.

Per elaborare tutti i messaggi destinati alla finestra di dialogo personalizzata, il sistema richiede che la routine di hook invii gli stessi messaggi di finestra alla procedura di hook come per qualsiasi altra routine della finestra di dialogo. Ad esempio, la routine hook riceve i messaggi di [**\_ comando WM**](/windows/desktop/menurc/wm-command) quando l'utente fa clic sui controlli Button nella finestra di dialogo personalizzata. La procedura di hook è responsabile dell'inizializzazione di questi controlli e del recupero dei valori dai controlli quando la finestra di dialogo viene chiusa. Si noti che quando la routine hook riceve il messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) , il sistema non ha ancora spostato i controlli nelle rispettive posizioni finali.

La routine della finestra di dialogo predefinita gestisce i messaggi per tutti i controlli della finestra di dialogo predefinita, ma la procedura hook riceve i messaggi di notifica per le azioni dell'utente su questi controlli, come descritto in [procedure hook di tipo Esplora risorse](#explorer-style-hook-procedures).

## <a name="explorer-style-control-identifiers"></a>Identificatori di controllo Explorer-Style

Windows Software Development Kit (SDK) fornisce il modello di finestra di dialogo predefinito per le finestre di dialogo obsolete, ma non include il modello predefinito per le finestre di dialogo di tipo Esplora. Ciò è dovuto al fatto che le finestre di dialogo di tipo Esplora risorse consentono di aggiungere controlli personalizzati, ma non supportano la modifica del modello per i controlli standard. In alcuni casi, tuttavia, potrebbe essere necessario individuare gli identificatori dei controlli utilizzati nei modelli predefiniti. Ad esempio, i messaggi [**CDM \_ HIDECONTROL**](cdm-hidecontrol.md) e [**CDM \_ SETCONTROLTEXT**](cdm-setcontroltext.md) richiedono un identificatore del controllo.

La tabella seguente illustra gli identificatori dei controlli standard nelle finestre di dialogo **Apri** e **Salva con nome** di tipo Esplora risorse. Gli identificatori sono costanti definite in Dlgs. h e winuser. h.



| Identificatore di controllo | Descrizione del controllo                                                                                                                                                                                                                                                                        |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **chx1**           | Casella di controllo di sola lettura                                                                                                                                                                                                                                                                    |
| **cmb1**           | Casella combinata a discesa che Visualizza l'elenco di filtri per i tipi di file                                                                                                                                                                                                                            |
| **stc2**           | Etichetta per la casella combinata **cmb1**                                                                                                                                                                                                                                                           |
| **cmb2**           | Casella combinata a discesa che Visualizza l'unità o la cartella corrente e che consente all'utente di selezionare un'unità o una cartella da aprire                                                                                                                                                                |
| **stc4**           | Etichetta per la casella combinata **cmb2**                                                                                                                                                                                                                                                           |
| **cmb13**          | Casella combinata a discesa che Visualizza il nome del file corrente, consente all'utente di digitare il nome di un file da aprire e di selezionare un file aperto o salvato di recente. Si tratta di applicazioni precedenti compatibili con Esplora risorse senza modello di hook o di finestra di dialogo. Confrontare con **edt1**. |
| **edt1**           | Controllo di modifica che Visualizza il nome del file corrente oppure consente all'utente di digitare il nome del file da aprire. Confrontare con **CMB13**.                                                                                                                                                  |
| **STC3**           | Etichetta per la casella combinata **CMB13** e il controllo edt1 Edit                                                                                                                                                                                                                                |
| **lst1**           | Casella di riepilogo che Visualizza il contenuto dell'unità o della cartella corrente                                                                                                                                                                                                                         |
| **stc1**           | Etichetta per la casella di riepilogo **Lst1**                                                                                                                                                                                                                                                            |
| **IDOK**           | Pulsante di comando **OK** (pulsante di push)                                                                                                                                                                                                                                                    |
| **IDCANCEL**       | Pulsante di comando **Annulla** (pulsante di push)                                                                                                                                                                                                                                                |
| **pshHelp**        | Pulsante di comando della **Guida** (pulsante di push)                                                                                                                                                                                                                                                  |



 

## <a name="customizing-old-style-dialog-boxes"></a>Personalizzazione delle finestre di dialogo Old-Style

È possibile personalizzare una finestra di dialogo **Apri** o **Salva con nome** obsoleta specificando una procedura di hook [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) che riceve i messaggi o le notifiche destinate alla routine predefinita della finestra di dialogo. È anche possibile fornire un modello personalizzato da usare al posto del modello predefinito. Le procedure e i modelli Hook utilizzati con le finestre di dialogo obsolete sono simili a quelli utilizzati con le altre finestre di dialogo comuni. Per altre informazioni, vedere [procedure hook per finestre di dialogo comuni](customizing-common-dialog-boxes.md) e [modelli personalizzati](customizing-common-dialog-boxes.md).

Per abilitare una routine hook per una finestra di dialogo **Apri** o **Salva con nome** obsoleta, utilizzare la struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) quando si crea la finestra di dialogo. Impostare il **flag OFN \_ ENABLEHOOK** nel membro **Flags** e specificare l'indirizzo di una routine hook [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) nel membro **lpfnHook** . La routine della finestra di dialogo Invia un messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) alla routine hook con il parametro *param* impostato sull'indirizzo della struttura **OpenFileName** utilizzata per inizializzare la finestra di dialogo.

È possibile utilizzare la struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) per specificare un modello personalizzato per la finestra di dialogo **Apri** o **Salva con nome** da utilizzare al posto del modello predefinito. Se il modello personalizzato è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare il flag **OFN \_ ENABLETEMPLATE** nel membro **Flags** e usare i membri **HINSTANCE** e **lpTemplateName** della struttura per identificare il modulo e il nome della risorsa. Se il modello personalizzato è già in memoria, impostare il flag **OFN \_ ENABLETEMPLATEHANDLE** e usare il membro **HINSTANCE** per identificare l'oggetto memoria che contiene il modello. Creare il modello personalizzato modificando il modello predefinito specificato nel file FileOpen. dlg. Gli identificatori di controllo utilizzati nei modelli di finestra di dialogo Trova e Sostituisci predefiniti sono definiti nel file Dlgs. h.

Per impostazione predefinita, le funzioni [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) e [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) visualizzano le finestre di dialogo di tipo Esplora risorse. Se si desidera visualizzare una finestra di dialogo obsoleta, è necessario fornire una procedura di hook [**OFNHookProcOldStyle**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) e assicurarsi che il flag **OFN \_ Explorer** non sia impostato nel membro **Flags** della struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .

Se si imposta il flag **OFN \_ Explorer** , il sistema considera una procedura di hook o un modello personalizzato come personalizzazione di tipo Esplora risorse. Per informazioni sulla personalizzazione di una finestra di dialogo di tipo Esplora risorse, vedere [modelli personalizzati di tipo Esplora risorse](#explorer-style-custom-templates).

## <a name="see-also"></a>Vedi anche

* [Esempio di file in uso](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse)
