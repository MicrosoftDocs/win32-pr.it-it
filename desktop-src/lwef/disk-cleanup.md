---
title: Creazione di un gestore di pulizia del disco
description: Un axiom comprovato più volte nel mondo dei computer è che, indipendentemente dalle dimensioni della capacità di archiviazione del computer, alla fine si riempirà.
ms.assetid: f85e0db7-fbdb-452e-90c8-672f716b5692
keywords:
- gestori di pulizia del disco
- Pulizia disco
- DataDrivenCleaner
- registro, gestori di pulizia del disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ce7fc96e16cb27168e00196b65d48d378758a47594122cca978dc1a1f4de94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479895"
---
# <a name="creating-a-disk-cleanup-handler"></a>Creazione di un gestore di pulizia del disco

Un axiom comprovato più volte nel mondo dei computer è che, indipendentemente dalle dimensioni della capacità di archiviazione del computer, alla fine si riempirà. Anche se le dimensioni medie del disco rigido di un computer sono aumentate notevolmente nel tempo, anche le applicazioni sono aumentate di conseguenza, lasciando gli utenti alla ricerca di modi per creare più spazio libero su disco rigido. Lo spazio disponibile è inoltre ridotto dai numerosi file temporanei creati dalle applicazioni per motivi di backup o prestazioni. Quando lo spazio su disco diventa insufficiente, diventa necessario ridurre la quantità di spazio usata dalle applicazioni. Lo spazio su disco può essere liberato in diversi modi, tra cui:

-   Eliminazione di file.
-   Compressione di file.
-   Spostamento di file in un supporto di backup.
-   Trasferimento di file a un server remoto.

I file che sono candidati per la pulizia includono:

-   File di cui l'utente non avrà più bisogno.
-   File temporanei esistenti solo per motivi di prestazioni.
-   File che possono essere ripristinati, se necessario, da un CD di installazione.
-   File di dati che probabilmente sono stati sostituiti da versioni più recenti, ad esempio i file di backup precedenti.
-   File meno recenti che non sono stati usati da molto tempo.

L'eliminazione è particolarmente appropriata per i file che l'utente non avrà più bisogno, ad esempio i file che vengono temporaneamente memorizzati nella cache per motivi di prestazioni. L'eliminazione è appropriata anche per i file facilmente ripristinabili, ad esempio i file grafici che possono essere ricaricati da un CD di installazione. I file che l'utente potrebbe aver bisogno in un secondo momento o che sarebbe difficile ricostruire sono candidati migliori per la compressione o il backup.

Aspettarsi che un utente pulirà manualmente file system non è una buona soluzione. L'utente potrebbe non sapere dove si trovano molti dei file o come riconoscere quali possono essere rimossi in modo sicuro. Inoltre, esiste il rischio che l'utente possa eliminare i file essenziali.

In questo argomento vengono illustrati i facet seguenti dell'utilità Pulizia disco.

-   [Utilità pulizia Windows disco](#the-windows-disk-cleanup-utility)
-   [Nozioni di base sull'implementazione](#implementation-basics)
    -   [Initialize/InitializeEx](#initializeinitializeex)
    -   [GetSpaceUsed](#getspaceused)
    -   [ShowProperties](#showproperties)
    -   [Ripulisci](#purge)
    -   [Disattivare](#deactivate)
-   [Registrazione di un gestore di pulizia del disco](#registering-a-disk-cleanup-handler)
    -   [Registrazione del CLSID di un gestore](#registering-a-handlers-clsid)
    -   [Registrazione di un gestore con Gestione pulizia disco: Generale](#registering-a-handler-with-the-disk-cleanup-manager-general)
    -   [Registrazione di un gestore con Gestione pulizia disco: Windows 2000 o versioni successive](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
    -   [Uso dell'oggetto DataDrivenCleaner](#using-the-datadrivencleaner-object)
    -   [Registrazione di esempio di un gestore di pulizia del disco](#example-registration-of-a-disk-cleanup-handler)

## <a name="the-windows-disk-cleanup-utility"></a>Utilità pulizia Windows disco

A partire da Windows 98, il sistema operativo Windows include Pulizia disco, un'utilità che rende molto più semplice per l'utente gestire lo spazio disponibile su disco rigido. L'utilità Pulizia disco è progettata per liberare più spazio su disco possibile e ridurre il rischio che l'utente elimini accidentalmente i file essenziali.

La pulizia del disco può essere avviata in tre modi.

-   L'utente può avviare la pulizia del disco facendo clic **su Avvia**. che punta a **Tutti i programmi**, **Accessori** e Strumenti **di sistema**; e quindi fare clic **su Pulizia disco**.
-   Il sistema notifica all'utente con una finestra di messaggio che lo spazio su disco inutilizzato ha raggiunto la modalità critica. La soglia della modalità critica per un'unità superiore a 2,25 gigabyte (GB) è di 200 megabyte (MB). Gli avvisi successivi vengono visualizzati a 80, 50 e 1 MB. All'utente viene data la possibilità di liberare spazio su disco manualmente o di avviare l'utilità Pulizia disco.
-   L'utente può fare in modo Windows guidata attività pianificata (nota come Manutenzione guidata nei sistemi meno recenti) eseguire automaticamente l'utilità Pulizia disco in orari pianificati.

La sfida di base insita nella pulizia del disco consiste nel liberare la maggior quantità possibile di spazio su disco senza eliminare i file essenziali. Poiché non esiste un modo standard per contrassegnare i file per la pulizia, nessuna singola applicazione può rilevare e pulire in modo affidabile tutti i file non necessari. L'utilità Pulizia disco risolve questo problema suddividendo  l'operazione di pulizia tra un singolo gestore di pulizia disco e una raccolta di gestori *di pulizia del disco*.

Quando si esegue l'utilità Pulizia disco, viene visualizzata la finestra di dialogo seguente. Se nel computer sono presenti più dischi o partizioni del disco, all'utente viene prima richiesto di scegliere un'unità prima che venga visualizzata questa finestra di dialogo.

![Screenshot della finestra di dialogo di pulizia](images/cleanup1.png)

Gestione pulizia disco fa parte del sistema operativo. Visualizza la finestra di dialogo illustrata nella figura precedente, gestisce l'input dell'utente e gestisce l'operazione di pulizia. La selezione e la pulizia effettive dei file non necessari vengono eseguite dai singoli gestori di pulizia del disco visualizzati nella casella di riepilogo di Gestione pulizia disco. L'utente ha la possibilità di abilitare o disabilitare singoli gestori selezionando o deselezionando la casella di controllo nell'interfaccia utente di Gestione pulizia disco.

Ogni gestore è responsabile di un set ben definito di file. Ad esempio, il gestore selezionato nell'illustrazione è responsabile della pulizia dei file di programma scaricati. Il gestore selezionato nell'illustrazione fornisce anche un **pulsante Visualizza** file. Facendo clic sul pulsante, l'utente può richiedere al gestore di visualizzare un'interfaccia utente in genere una finestra di Esplora Windows che consente all'utente di specificare quali file o classi di file pulire.

Sebbene Windows con una serie di gestori di pulizia del disco, non sono progettati per gestire i file prodotti da altre applicazioni. Al contrario, gestione pulizia disco è progettato per essere flessibile ed estendibile consentendo a qualsiasi sviluppatore di implementare e registrare il proprio gestore di pulizia del disco. Qualsiasi sviluppatore può estendere i servizi di pulizia del disco disponibili implementando e registrando un gestore di pulizia del disco.

Tutte le applicazioni che producono file temporanei possono e devono implementare e registrare un gestore di pulizia del disco. In questo modo gli utenti possono gestire i file temporanei dell'applicazione in modo pratico e affidabile. Quando si implementa il gestore , è possibile decidere quali file sono interessati e determinare come viene eseguita la pulizia effettiva.

## <a name="implementation-basics"></a>Nozioni di base sull'implementazione

I gestori di pulizia sono oggetti server Component Object Model (COM) in-process. Windows un oggetto gestore esistente denominato DataDrivenCleaner per l'uso. È anche possibile scegliere di implementare manualmente un gestore per una maggiore flessibilità. Questi oggetti consentono quindi di specificare come selezionare i file, liberare spazio su disco e, nel caso di un gestore implementato, visualizzare l'interfaccia utente facoltativa per un controllo più granulare. Questa sezione tratta la questione dell'implementazione di un gestore personalizzato. Per informazioni dettagliate sull'uso dell'oggetto DataDrivenCleaner, vedere [Uso dell'oggetto DataDrivenCleaner.](#using-the-datadrivencleaner-object)

Un gestore di pulizia del disco deve eseguire queste cinque attività di base.

-   Inizializzare l'oggetto gestore.
-   Analizzare il disco per determinare la quantità di spazio su disco che può essere liberata.
-   Visualizzare l'interfaccia utente per ottenere commenti e suggerimenti degli utenti sui file da pulire. Facoltativa
-   Eseguire la pulizia.
-   Spegni.

Per consentire a Gestione pulizia disco di gestire queste attività, un gestore deve esportare [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) per Windows 98 o [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) per Windows Millennium Edition (Windows Me), Windows 2000 e Windows XP. Poiché **IEmptyVolumeCache2** eredita da **IEmptyVolumeCache**, aggiungendo solo il metodo aggiuntivo **InitializeEx**, è necessario un lavoro aggiuntivo relativamente piccolo per implementare entrambi. A meno che il gestore non sia destinato a uno solo di questi sistemi operativi, deve esportare entrambe le interfacce.

Per esportare queste interfacce, è necessario implementare questi metodi corrispondenti alle cinque attività di base.

-   [Initialize/InitializeEx](#initializeinitializeex)
-   [GetSpaceUsed](#getspaceused)
-   [ShowProperties](#showproperties)
-   [Ripulisci](#purge)
-   [Disattivare](#deactivate)

### <a name="initializeinitializeex"></a>Initialize/InitializeEx

I due metodi di inizializzazione, che sono piuttosto simili, vengono chiamati quando viene eseguita l'utilità Pulizia disco. Il Windows di pulizia del disco 98 chiama il metodo [**IEmptyVolumeCache::Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) di un gestore. La gestione pulizia disco Windows Millennium Edition (Windows Me), Windows 2000 o Windows XP, tuttavia, prova prima a chiamare [**IEmptyVolumeCache2::InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) e usa **solo IEmptyVolumeCache::Initialize** se [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) non è esposto dal gestore. Gestione pulizia disco passa le informazioni al metodo , ad esempio la chiave del Registro di sistema del gestore e il volume del disco da pulire.

Entrambi i metodi possono restituire varie stringhe di visualizzazione e impostare uno o più flag. La differenza principale tra i due metodi è la modalità di gestione del testo visualizzato nel gestore pulizia disco. Le tre stringhe seguenti sono interessate.



| string       | Scopo                                                                            | Inizializzare                                                                           | InitializeEx                                                                                     |
|--------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Nome visualizzato | Nome del gestore visualizzato nella casella di riepilogo del gestore pulizia disco.               | Se *ppwszDisplayName* è **NULL,** il valore predefinito viene recuperato dal Registro di sistema. | In *ppwszDisplayName* non deve essere specificata una stringa localizzata correttamente. Non vengono usati valori del Registro di sistema. |
| Descrizione  | Testo descrittivo visualizzato sotto la casella di riepilogo quando viene selezionato il nome del gestore. | Se *ppwszDescription* è **NULL,** il valore predefinito viene recuperato dal Registro di sistema. | In *ppwszDescription* non deve essere specificata una stringa localizzata correttamente. Non vengono usati valori del Registro di sistema. |
| Testo pulsante  | Testo per il pulsante facoltativo che consente agli utenti di visualizzare l'interfaccia utente del gestore.        | Nessun parametro disponibile. Deve essere specificato nel Registro di sistema.                           | In *ppwszBtnText* non viene usato alcun valore del Registro di sistema.     |



 

Il *parametro pdwFlags* trovato in entrambi i metodi di inizializzazione riconosce lo stesso set di flag. Due di questi flag vengono passati al metodo dal gestore pulizia disco.

-   **EVCF \_ SETTINGSMODE**

    Se il gestore pulizia dischi viene eseguito in base a una pianificazione, imposta il flag **EVCF \_ SETTINGSMODE.** Se questo flag è impostato, gestione pulizia disco non chiama i [metodi GetSpaceUsed,](#getspaceused) [Purge](#purge)o [ShowProperties.](#showproperties) Il metodo [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) o [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) del gestore deve gestire tutte le attività normalmente eseguite da [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) ed [**Elimina**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge). Poiché non è possibile inviare commenti e suggerimenti agli utenti, è consigliabile toccare solo i file estremamente sicuri da pulire. È consigliabile ignorare il parametro *pcwszVolume* del metodo di inizializzazione e pulire i file non necessari indipendentemente dall'unità in cui sono presenti.

-   **EVCF \_ OUTOFDISKSPACE**

    Se il flag **\_ OUTOFDISKSPACE di EVCF** è impostato, l'unità disco dell'utente è a corto di spazio. Il gestore deve essere aggressivo nell'eliminazione dei file, anche se comporta una perdita di prestazioni. Tuttavia, il gestore ovviamente non deve eliminare i file che causerebbero l'errore di un'applicazione o la perdita di dati da parte dell'utente.

I flag rimanenti vengono impostati dal gestore di pulizia del disco e restituiti al gestore pulizia disco. Per altre informazioni, vedere le pagine di riferimento del metodo [**per IEmptyVolumeCache::Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) e [**IEmptyVolumeCache2::InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex).

-   EVCF \_ DONTSHOWIFZERO

    Visualizzare il gestore nella casella di riepilogo del gestore pulizia disco solo se il valore restituito da [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) indica che il gestore può liberare spazio su disco.

-   EVCF \_ ENABLEBYDEFAULT

    Specifica che il gestore è abilitato per impostazione predefinita. Verrà eseguito ogni volta che viene eseguita una pulizia del disco, a meno che l'utente non la disabilita deselezionando la relativa casella di controllo nell'elenco di gestori del gestore pulizia disco.

-   EVCF \_ ENABLEBYDEFAULT \_ AUTO

    Specifica che il gestore viene abilitato automaticamente per l'esecuzione durante le pulizioni pianificate.

-   EVCF \_ HASSETTINGS

    Impostare questo flag se il gestore ha un'interfaccia utente da visualizzare. In risposta, gestione pulizia disco visualizza un pulsante quando tale gestore viene selezionato nella casella di riepilogo. Se si fa clic sul pulsante, il gestore pulizia disco chiama [**ShowProperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties).

-   EVCF \_ REMOVEFROMLIST

    Eliminare il nome del gestore dall'elenco dei gestori disponibili dopo che il gestore è stato eseguito una sola volta. Vengono eliminate anche le informazioni del Registro di sistema del gestore.

### <a name="getspaceused"></a>GetSpaceUsed

Il gestore pulizia disco chiama questo metodo per determinare la quantità di spazio potenzialmente disponibile per un gestore di pulizia del disco. Gestione pulizia disco visualizza quindi tale valore a destra del nome del gestore nella casella di riepilogo. Questa operazione viene eseguita su tutti i gestori registrati con gestione pulizia disco quando il gestore viene avviato e prima che venga visualizzata l'interfaccia utente principale del manager. Quando viene chiamato [**GetSpaceUsed,**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) il gestore deve analizzare i file di cui è responsabile, determinare quali sono candidati per la pulizia e restituire la quantità di spazio su disco che può liberare.

Poiché l'analisi può essere un processo lungo, gestione pulizia disco usa il parametro *picb* di questo metodo per passare un puntatore a [**un'interfaccia IEmptyVolumeCacheCallBack.**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) Il gestore usa periodicamente l'interfaccia durante l'analisi per chiamare [**IEmptyVolumeCacheCallBack::ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress), che svolge due scopi.

-   Consente al gestore pulitura dischi di aggiornare un indicatore di stato, informando l'utente come procede l'analisi.
-   Notifica al gestore di arrestare l'analisi nel caso in cui sia stato fatto clic sul pulsante **Annulla** della finestra di stato. L'evento del pulsante non viene comunicato direttamente al gestore. al contrario, il gestore pulizia disco restituisce E ABORT alla successiva chiamata di \_ [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) [**AEmptyVolumeCacheCallBack::ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress).

### <a name="showproperties"></a>ShowProperties

Prima di avviare la pulizia, il gestore può visualizzare un'interfaccia utente in genere sotto forma di finestra di esplora Windows che consente all'utente di visualizzare un elenco di file o classi di file selezionati per la pulizia dal gestore. Se il gestore imposta il flag **\_ HASSETTINGS di EVCF** quando viene chiamato [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) o [**InitializeEx,**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) l'utente può richiedere l'interfaccia utente facendo clic sul pulsante visualizzato a tale scopo nel gestore pulizia disco. Il testo del pulsante varia da gestore a gestore, ma "Visualizza file", "Visualizza pagine" e "Opzioni" sono etichette comuni.

Quando si fa clic sul pulsante, il gestore della pulizia del disco chiama [**ShowProperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties) per richiedere al gestore di visualizzare l'interfaccia utente. L'interfaccia utente deve essere creata come figlio della finestra il cui handle viene passato nel parametro *hwnd del metodo* **ShowProperties.**

### <a name="purge"></a>Ripulisci

Il gestore della pulizia del disco chiama il metodo [**Purge del**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge) gestore per impostare la pulizia in movimento. Il parametro *picb del* metodo è un puntatore [**all'interfaccia IEmptyVolumeCacheCallBack**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) del gestore pulizia dischi. Come per il [**metodo GetSpaceUsed,**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) il gestore deve usare periodicamente l'interfaccia di callback per segnalare lo stato di avanzamento ed eseguire una query sul gestore pulizia disco se l'utente ha fatto clic su **Annulla.** Si noti tuttavia che il **metodo Purge** deve chiamare [**IEmptyVolumeCacheCallBack::P urgeProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-purgeprogress), non [**ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress).

### <a name="deactivate"></a>Disattivare

Il [**metodo Deactivate**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-deactivate) viene chiamato quando gestione pulizia disco si prepara all'arresto. Il gestore deve eseguire tutte le attività di pulizia necessarie e restituire . Se non si vuole eseguire di nuovo il gestore, impostare il flag **EVCF \_ REMOVEFROMLIST** nel parametro *pdwFlags del metodo di* inizializzazione. Se questo flag è impostato, gestione pulizia disco rimuove il gestore dal relativo elenco ed elimina le voci del Registro di sistema del gestore. È necessario aggiungere nuovamente le voci del Registro di sistema per eseguire nuovamente il gestore. Questo flag viene in genere usato per i gestori eseguiti una sola volta.

## <a name="registering-a-disk-cleanup-handler"></a>Registrazione di un gestore pulizia disco

Per aggiungere un gestore all'elenco del gestore pulizia disco, è necessario aggiungere determinate chiavi e valori al registro Windows disco.

-   [Registrazione del CLSID di un gestore](#registering-a-handlers-clsid)
-   [Registrazione di un gestore con Gestione pulizia disco: Generale](#registering-a-handler-with-the-disk-cleanup-manager-general)
-   [Registrazione di un gestore con Gestione pulizia disco: Windows 2000 o versioni successive](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
-   [Uso dell'oggetto DataDrivenCleaner](#using-the-datadrivencleaner-object)
-   [Registrazione di esempio di un gestore pulizia disco](#example-registration-of-a-disk-cleanup-handler)

### <a name="registering-a-handlers-clsid"></a>Registrazione del CLSID di un gestore

Come per tutti gli oggetti COM, il GUID e la DLL dell'oggetto gestore devono essere registrati nella chiave **CLSID** in **HKEY \_ CLASSES \_ ROOT**. È anche possibile registrare un'icona visualizzata accanto al nome del gestore nella casella di riepilogo del gestore pulizia disco, ma questa opzione è facoltativa. L'esempio seguente illustra le chiavi, i valori e i dati coinvolti.

```
HKEY_CLASSES_ROOT
   CLSID
      Handler's GUID
         DefaultIcon
            (Default) = Handler's Icon Path, Icon Index
         InprocServer32
            (Default) = Handler's DLL path
            ThreadingModel = Apartment
```

### <a name="registering-a-handler-with-the-disk-cleanup-manager-general"></a>Registrazione di un gestore con Gestione pulizia disco: Generale

Per completare la registrazione, un gestore deve aggiungere una chiave contenente le specifiche, come illustrato di seguito. Nella parte restante di questa sezione viene illustrato il contenuto di questa chiave.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     Handler's Key
```

In generale, il nome della chiave che contiene le specifiche di un gestore è denominato per il tipo di file gestito, ad esempio **File** di programma scaricati, ma questo non è un requisito. Nella tabella seguente sono elencati in dettaglio i possibili valori trovati in questa chiave.

> [!Note]  
> Solo il valore Predefinito che specifica l'identificatore di classe del gestore (CLSID) è obbligatorio, tutti gli altri valori sono facoltativi.

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Type</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Predefinito</td>
<td>REG_SZ</td>
<td>CLSID del gestore registrato in <strong>HKEY_CLASSES_ROOT</strong> \ <strong>CLSID</strong>.</td>
</tr>
<tr class="even">
<td>AdvancedButtonText</td>
<td>REG_SZ</td>
<td>Testo per il pulsante facoltativo su cui gli utenti possono fare clic per visualizzare l'interfaccia utente del gestore. Il & può essere posizionato prima di un carattere per assegnare un tasto di scelta rapida per il pulsante. Il valore AdvancedButtonText viene ignorato dai gestori che espongono <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx.</strong></a></td>
</tr>
<tr class="odd">
<td>CleanupString</td>
<td>REG_SZ</td>
<td>Riga di comando che specifica un file eseguibile e parametri facoltativi della riga di comando. Questa riga di comando viene eseguita al termine della pulizia del disco.</td>
</tr>
<tr class="even">
<td>CSIDL</td>
<td>REG_DWORD</td>
<td>Identificatore indipendente dal sistema per una cartella speciale da includere nella ricerca di file. Questo valore deve essere immesso come valore numerico, ad esempio, 0x0000001c anziché come CSIDL_LOCAL_APPDATA. Per un elenco dei valori possibili, vedere <a href="/windows/desktop/shell/csidl"><strong>CSIDL.</strong></a> È possibile usare un solo valore.<br/> Se si specifica il valore Folder, il percorso indicato dal valore CSIDL viene anteposto a queste informazioni per comporre un percorso di ricerca. Si consideri, ad esempio, lo scenario seguente.<br/>
<ul>
<li>Il valore CSIDL viene specificato come 0x0000000d (CSIDL_MYMUSIC)</li>
<li>La cartella My Musica si trova in C:\Documents and Impostazioni\<em>username</em>\My Musica</li>
<li>Il valore Folder contiene &quot; Jazz\Clubs&quot;</li>
</ul>
Il risultato di questo scenario è che il gestore di pulizia del disco esegue la ricerca nella cartella C:\Documents and Impostazioni\<em>username</em>\My Musica\Jazz\Più. Si noti che la barra che precede il valore Cartella viene aggiunta se non è presente.<br/></td>
</tr>
<tr class="odd">
<td>Descrizione</td>
<td>REG_SZ</td>
<td>Testo descrittivo visualizzato sotto la casella di riepilogo del gestore della pulizia del disco quando viene selezionato il nome del gestore. Qui è possibile spiegare cosa fa il gestore, quali file si preoccupa di se stesso ed eventuali altre informazioni utili all'utente. Se <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx</strong></a> non viene esposto dal gestore, questo testo può essere sottoposto a override tramite il metodo <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache::Initialize</strong></a> del gestore specificando una stringa alternativa nel parametro <em>ppwszDescription</em> quando viene chiamato il metodo .</td>
</tr>
<tr class="even">
<td>Visualizza</td>
<td>REG_SZ</td>
<td>Nome del gestore da visualizzare nella casella di riepilogo di Gestione pulizia disco. Se <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx</strong></a> non viene esposto dal gestore, questo testo può essere sottoposto a override tramite il metodo <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache::Initialize</strong></a> del gestore specificando una stringa alternativa nel parametro <em>ppwszDisplayName</em> quando viene chiamato il metodo .</td>
</tr>
<tr class="odd">
<td>FileList</td>
<td>REG_SZ o REG_MULTI_SZ</td>
<td>Elenco di file cercati e puliti da questo gestore. È possibile specificare caratteri jolly usando il carattere ? o * caratteri. Se il valore è di tipo REG_SZ, più estensioni vengono separate usando il | o : caratteri, senza spazi su entrambi i lati.<br/> Se il flag DDEVCF_REMOVEDIRS è impostato nel valore Flags, questi valori possono specificare i nomi di directory e i file.<br/></td>
</tr>
<tr class="even">
<td>Flags</td>
<td>REG_DWORD o REG_BINARY</td>
<td>Flag che controllano gli elementi della procedura di ricerca e pulizia. Uno o più dei valori seguenti.
<ul>
<li>DDEVCF_DOSUBDIRS (0x00000001). Cercare e rimuovere in modo ricorsivo.</li>
<li>DDEVCF_REMOVEAFTERCLEAN (0x00000002). Dopo che il gestore è stato eseguito una volta, rimuoverlo dal Registro di sistema.</li>
<li>DDEVCF_REMOVEREADONLY (0x00000004). Rimuovere i file che soddisfano i criteri di ricerca anche se sono di sola lettura.</li>
<li>DDEVCF_REMOVESYSTEM (0x00000008). Rimuovere i file che soddisfano i criteri di ricerca anche se sono file di sistema.</li>
<li>DDEVCF_REMOVEHIDDEN (0x00000010). Rimuovere i file che soddisfano i criteri di ricerca anche se sono file nascosti.</li>
<li>DDEVCF_DONTSHOWIFZERO (0x00000020). Non visualizzare questo gestore in Gestione pulizia disco se nessun file corrisponde ai criteri di ricerca.</li>
<li>DDEVCF_REMOVEDIRS (0x00000040). Trovare la corrispondenza tra il valore FileList e le directory e rimuovere le corrispondenze e tutte le relative sottodirectory.</li>
<li>DDEVCF_RUNIFOUTOFDISKSPACE (0x00000080). Eseguire questo gestore solo se lo spazio disponibile su disco è inferiore al valore critico, determinato dall'impostazione del flag EVCF_OUTOFDISKSPACE da parte di Gestione pulizia disco tramite <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache::Initialize</strong></a> o <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx</strong></a>.</li>
<li>DDEVCF_REMOVEPARENTDIR (0x00000100). Rimuovere la directory padre dei file specificati dopo l'esecuzione della pulitura.</li>
<li>DDEVCF_PRIVATE_LASTACCESS (0x10000000). Usare il valore LastAccess, se specificato, per verificare quali file devono essere puliti. Questo flag viene ignorato quando si usa <a href="#using-the-datadrivencleaner-object">DataDrivenCleaner</a> qualsiasi valore LastAccess specificato viene sempre usato.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Cartella</td>
<td>REG_SZ, REG_MULTI_SZ o REG_EXPAND_SZ</td>
<td>Cartella o cartelle specifiche in cui cercare gli elementi corrispondenti alle voci nel valore FileList. È possibile specificare caratteri jolly usando il carattere ? o * caratteri. Se il valore è di tipo REG_SZ, più nomi di cartella vengono separati usando il | senza spazi su entrambi i lati.<br/> Se è presente un valore CSIDL, è possibile specificare una sola cartella in questo valore. Il percorso indicato dal valore CSIDL viene anteposto al percorso della cartella per comporre un percorso di ricerca. Per un esempio, vedere la descrizione del valore CSIDL.<br/> Se questo valore è assente in Windows Vista Service Pack 1 (SP1) e versioni successive, il gestore di pulizia viene ignorato e restituisce S_FALSE durante l'inizializzazione.<br/> Se questo valore è assente nella versione originale di Windows Vista e versioni precedenti, viene usata la cartella radice del volume corrente. Il DDEVCF_DOSUBDIRS flag è necessario in questo caso per eseguire la ricerca nell'intera unità. Senza di essa, viene cercata solo la cartella radice stessa.<br/> È necessario specificare una o più unità. Può essere fornito tramite il valore CSIDL o tramite una REG_EXPAND_SZ stringa. A parte queste opzioni, tuttavia, l'unità in cui eseguire la ricerca deve essere specificata nel nome della cartella. Usare ?: per cercare la cartella nell'unità corrente.<br/></td>
</tr>
<tr class="even">
<td>IconPath</td>
<td>REG_SZ o REG_EXPAND_SZ</td>
<td>Percorso della risorsa da cui ottenere un'icona da usare in associazione al gestore.</td>
</tr>
<tr class="odd">
<td>LastAccess</td>
<td>REG_DWORD o REG_BINARY</td>
<td>Numero di giorni che devono trascorrere dall'ultimo accesso a un file o dalla creazione di una directory per il file o la directory da considerare per la pulizia.</td>
</tr>
<tr class="even">
<td>Priorità</td>
<td>REG_DWORD o REG_BINARY</td>
<td>Determina l'ordine di esecuzione del gestore rispetto ad altri gestori. Maggiore è il numero, più indietro nel processo viene eseguito il gestore. Nessun intervallo definito è accettabile.</td>
</tr>
<tr class="odd">
<td>Propertybag</td>
<td>REG_SZ</td>
<td>CLSID di una risorsa utilizzata per fornire il testo localizzato per il nome visualizzato, la descrizione e il testo del pulsante. Questa risorsa è utile nel caso in cui un gestore non implementi <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache"><strong>IEmptyVolumeCache</strong></a> e il gestore venga eseguito in Microsoft Windows NT o Windows XP.<br/> Gestione pulizia disco controlla innanzitutto se la routine di inizializzazione del gestore ha restituito tali stringhe, come nel caso dell'implementazione di <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2"><strong>IEmptyVolumeCache2.</strong></a> In caso contrario, il responsabile si trasforma in un contenitore di proprietà denominato in questo valore. Se non ne è stato specificato nessuno, recupera il testo dal Registro di sistema.<br/></td>
</tr>
<tr class="even">
<td>Flag di stato</td>
<td>REG_DWORD</td>
<td>Eseguendo il file eseguibile di Gestione pulizia disco Cleanmgr.exe riga di comando, è possibile dichiarare i profili di <em>pulizia</em>. Questi profili sono costituiti da un subset dei gestori disponibili e hanno un'etichetta numerica univoca. In questo modo è possibile automatizzare l'esecuzione di diversi set di gestori in momenti diversi.<br/> La riga di comando &quot;cleanmgr.exe /sageset:<strong>nnnn</strong>, dove &quot; <strong>nnnn</strong> è un'etichetta numerica univoca, visualizza un'interfaccia utente che consente di scegliere i gestori da includere nel profilo. Oltre a definire il profilo, il parametro sageset scrive anche un valore denominato StateFlags<strong>nnnn</strong>, dove <strong>nnnn</strong> è l'etichetta usata nel parametro , in tutte le sottochiavi in <strong>VolumeCaches</strong>. Esistono due valori di dati possibili per tali voci.
<ul>
<li>0: non eseguire questo gestore quando viene eseguito questo profilo.</li>
<li>2: includere questo gestore quando viene eseguito questo profilo.</li>
</ul>
<br/> Si supponga, ad esempio, che la riga &quot;cleanmgr.exe /sageset:1234 &quot; sia in esecuzione. Nell'interfaccia utente visualizzata l'utente sceglie <strong>File</strong>di programma scaricati, ma non file <strong>temporanei Internet.</strong> I valori seguenti vengono quindi scritti nel Registro di sistema.<br/>
<pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     Downloaded Program Files
                        StateFlags1234 = 0x00000002
                     Internet Cache Files
                        StateFlags1234 = 0x00000000</code></pre>
<br/> La riga di &quot; comandocleanmgr.exe /sagerun:<strong>nnnn</strong>, dove il valore di nnnn corrisponde all'etichetta dichiarata con il parametro &quot; sageset, <strong></strong> esegue tutti i gestori selezionati in tale profilo.<br/> Quando Pulizia disco viene eseguito normalmente, nel Registro di sistema viene scritto un valore StateFlags generico. Questo valore archivia semplicemente lo stato (selezionato o deselezionato) del gestore l'ultima volta che è stato presentato come opzione all'utente. Esistono due valori di dati possibili per tali voci.
<ul>
<li>0: il gestore non è stato selezionato.</li>
<li>1: il gestore è stato selezionato.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems"></a>Registrazione di un gestore con Gestione pulizia disco: Windows 2000 o versioni successive

La specifica del testo visualizzato nel Registro di sistema può rendere difficile la localizzazione del software. Per questo motivo, Windows 2000 e Windows XP supportano [**l'interfaccia IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) con il metodo di inizializzazione [**preferito InitializeEx.**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) In Windows 2000 o versioni successive viene sempre effettuato un tentativo di chiamare **IEmptyVolumeCache2::InitializeEx** prima di [**IEmptyVolumeCache::Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize). Il sistema usa **Initialize solo** per inizializzare un gestore **se IEmptyVolumeCache2** non è esposto.

Per quanto riguarda il Registro di sistema, l'unica differenza in Windows 2000 o versioni successive è che è possibile omettere i valori AdvancedButtonText, Display e Description quando [**IEmptyVolumeCache2::InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) viene esposto dal gestore. Questi valori, contenenti testo localizzato correttamente, vengono forniti al gestore della pulizia del disco quando chiama **InitializeEx.**

### <a name="using-the-datadrivencleaner-object"></a>Uso dell'oggetto DataDrivenCleaner

Un gestore di pulizia del disco di base, denominato DataDrivenCleaner, viene fornito dal sistema operativo. Per usare questo oggetto come gestore anziché implementarne uno personalizzato, usare il CLSID {C0E13E61-0CC6-11d1-BBB6-0060978B2AE6} come valore predefinito per la sottochiave del gestore in **VolumeCaches,** come descritto in Registrazione di un gestore con Gestione pulizia [disco: Generale.](#registering-a-handler-with-the-disk-cleanup-manager-general)

DataDrivenCleaner non espone [**IEmptyVolumeCache2,**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)quindi i valori display e description vengono forniti tramite il Registro di sistema. Quando si dichiarano queste stringhe, tenere presente che ciò potrebbe causare problemi di localizzazione. Il testo localizzato può essere fornito tramite il valore PropertyBag. Il valore AdvancedButtonText viene ignorato perché per questo gestore non è disponibile alcun pulsante per la visualizzazione dell'interfaccia utente.

### <a name="example-registration-of-a-disk-cleanup-handler"></a>Registrazione di esempio di un gestore di pulizia del disco

Di seguito viene illustrata una registrazione di esempio per un gestore di pulizia del disco implementato da The Telefono Company. Questo gestore implementa sia [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) che [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)e fornisce quindi i valori AdvancedButtonText, Description e Display nel caso in cui sia usato in un computer che esegue Windows 98. Il gestore combina i valori CSIDL e Folder per cercare i file nella directory C: Programmi La directory temporanea aziendale di Telefono e il \\ \\ flag \\ DDEVCF DOSUBDIRS è impostato in modo da eseguire la ricerca anche nelle relative \_ sottodirectory. Solo i file con estensioni tmp e tpc vengono considerati per la pulizia e il flag DDEVCF PRIVATE LASTACCESS è impostato in modo che da tali file siano considerati solo quelli a cui non è stato eseguito l'accesso per \_ \_ 14 o più giorni. Viene inoltre impostato il flag DDEVCF DONTSHOWIFZERO in modo che il gestore non venga visualizzato nell'elenco a meno che non siano stati trovati \_ candidati per la pulizia.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     The Phone Company Files
                        (Default) = {the CLSID GUID}
                        AdvancedButtonText = &View Files
                        CleanupString = c:\tpc.exe
                        CSIDL = 0x00000026
                        Description = Old temporary files.
                        Display = The Phone Company Files
                        FileList = *.tmp|*.tpc
                        Flags = 0x10000021
                        Folder = \The Phone Company\Temp
                        IconPath = c:\Program Files\The Phone Company\tpc.dll,2
                        LastAccess = 0x0000000e
                        Priority = 200
                        PropertyBag = {Property Bag CLSID GUID}
```

 

