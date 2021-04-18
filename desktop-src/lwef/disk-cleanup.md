---
title: Creazione di un gestore pulitura disco
description: Un assioma collaudato nel mondo dei computer è che, a prescindere dalle dimensioni della capacità di archiviazione del computer, la compilazione verrà compilata.
ms.assetid: f85e0db7-fbdb-452e-90c8-672f716b5692
keywords:
- gestori pulitura disco
- Pulizia disco
- DataDrivenCleaner
- Register, gestori pulitura dischi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30584439ae2c38ae8a9b7106dae96f69eea5df37
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "106300584"
---
# <a name="creating-a-disk-cleanup-handler"></a>Creazione di un gestore pulitura disco

Un assioma collaudato nel mondo dei computer è che, a prescindere dalle dimensioni della capacità di archiviazione del computer, la compilazione verrà compilata. Anche se le dimensioni medie del disco rigido di un computer sono aumentate notevolmente nel tempo, le applicazioni sono aumentate di conseguenza, lasciando agli utenti la possibilità di creare più spazio disponibile su disco rigido. Lo spazio disponibile viene ridotto anche dai numerosi file temporanei creati dalle applicazioni per motivi di backup o prestazioni. Quando lo spazio su disco diventa basso, diventa necessario ridurre la quantità di spazio utilizzata dalle applicazioni. Lo spazio su disco può essere liberato utilizzando diversi mezzi, inclusi i seguenti:

-   Eliminazione di file.
-   Compressione di file.
-   Trasferimento di file in un supporto di backup.
-   Trasferimento di file in un server remoto.

I file che sono candidati validi per la pulizia includono:

-   File che l'utente non dovrà mai più utilizzare.
-   File temporanei che esistono solo per motivi di prestazioni.
-   File che possono essere ripristinati, se necessario, da un CD di installazione.
-   File di dati che potrebbero essere stati sostituiti da versioni più recenti, ad esempio file di backup obsoleti.
-   File meno recenti che non sono stati utilizzati da molto tempo.

L'eliminazione è particolarmente appropriata per i file che non saranno mai necessari all'utente, ad esempio file temporaneamente memorizzati nella cache per motivi di prestazioni. L'eliminazione è appropriata anche per i file facilmente ripristinabili, ad esempio i file di grafica che possono essere ricaricati da un CD di installazione. I file che l'utente potrebbe richiedere in un secondo momento o che sarebbero difficili da ricostruire sono candidati migliori per la compressione o il backup.

Se un utente deve pulire manualmente il file system non è una soluzione valida. L'utente potrebbe non sapere dove si trovano molti file o come riconoscere quelli che possono essere rimossi in modo sicuro. Inoltre, esiste il rischio che l'utente possa eliminare i file essenziali.

In questo argomento vengono descritti i facet seguenti dell'utilità Pulitura disco.

-   [Utilità pulizia dischi di Windows](#the-windows-disk-cleanup-utility)
-   [Nozioni fondamentali sull'implementazione](#implementation-basics)
    -   [Initialize/InitializeEx](#initializeinitializeex)
    -   [GetSpaceUsed](#getspaceused)
    -   [ShowProperties](#showproperties)
    -   [Ripulisci](#purge)
    -   [Disattivare](#deactivate)
-   [Registrazione di un gestore pulitura disco](#registering-a-disk-cleanup-handler)
    -   [Registrazione del CLSID di un gestore](#registering-a-handlers-clsid)
    -   [Registrazione di un gestore con Gestione pulitura disco: generale](#registering-a-handler-with-the-disk-cleanup-manager-general)
    -   [Registrazione di un gestore con Gestione pulitura disco: sistemi Windows 2000 o versioni successive](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
    -   [Utilizzo dell'oggetto DataDrivenCleaner](#using-the-datadrivencleaner-object)
    -   [Registrazione di esempio di un gestore di pulitura del disco](#example-registration-of-a-disk-cleanup-handler)

## <a name="the-windows-disk-cleanup-utility"></a>Utilità pulizia dischi di Windows

A partire da Windows 98, il sistema operativo Windows include la pulizia dei dischi, un'utilità che rende molto più semplice per l'utente gestire lo spazio disponibile su disco rigido. L'utilità Pulitura disco è progettata per liberare lo spazio su disco possibile e ridurre il rischio che l'utente elimini accidentalmente i file essenziali.

È possibile avviare la pulizia del disco in tre modi.

-   L'utente può avviare la pulizia del disco facendo clic sul pulsante **Start**; puntare a **tutti i programmi**, **Accessori** e **strumenti di sistema**; e quindi fare clic su **Pulitura disco**.
-   Il sistema notifica all'utente una finestra di messaggio in cui lo spazio su disco inutilizzato ha raggiunto la modalità critica. La soglia della modalità critica per un'unità di dimensioni superiori a 2,25 gigabyte (GB) è 200 megabyte (MB). Gli avvisi successivi sono assegnati a 80, 50 e 1 MB. L'utente ha la possibilità di liberare spazio su disco manualmente o di avviare l'utilità di pulitura del disco.
-   L'utente può avere la creazione guidata attività pianificata di Windows (nota come manutenzione guidata nei sistemi meno recenti) eseguire automaticamente l'utilità di pulitura del disco in orari pianificati.

La sfida di base inerente alla pulizia dei dischi è liberare il maggior spazio su disco possibile senza eliminare i file essenziali. Poiché non esiste un modo standard per contrassegnare i file per la pulizia, nessuna singola applicazione può rilevare e pulire in modo affidabile tutti i file non essenziali. L'utilità pulizia dischi risolve questo problema suddividendo l'operazione di pulizia tra un singolo *gestore pulizia dischi* e una raccolta di *gestori di pulitura disco*.

Quando viene eseguita l'utilità Pulitura disco, l'utente Visualizza la finestra di dialogo seguente. Se nel computer è presente più di una partizione disco o disco, all'utente viene prima richiesta la scelta di un'unità prima che venga visualizzata la finestra di dialogo.

![screenshot della finestra di dialogo Pulisci](images/cleanup1.png)

Gestione pulizia dischi fa parte del sistema operativo. Viene visualizzata la finestra di dialogo illustrata nella figura precedente, viene gestito l'input dell'utente e viene gestita l'operazione di pulizia. La selezione e la pulizia effettive dei file non necessari vengono eseguite dai singoli gestori di pulitura del disco visualizzati nella casella di riepilogo di gestione pulizia dischi. L'utente ha la possibilità di abilitare o disabilitare i singoli gestori selezionando o deselezionando la casella di controllo nell'interfaccia utente di gestione pulizia dischi.

Ogni gestore è responsabile di un set di file ben definito. Il gestore selezionato nell'illustrazione, ad esempio, è responsabile della pulizia dei file di programma scaricati. Il gestore selezionato nell'illustrazione fornisce anche un pulsante **Visualizza file** . Facendo clic sul pulsante, l'utente può richiedere al gestore di visualizzare un'interfaccia utente in genere una finestra di Esplora risorse che consente all'utente di specificare i file o le classi di file da pulire.

Sebbene Windows sia dotato di un numero di gestori di pulitura del disco, non è progettato per gestire i file prodotti da altre applicazioni. Il gestore pulitura disco è invece progettato per essere flessibile ed estendibile, consentendo a tutti gli sviluppatori di implementare e registrare il proprio gestore pulitura dischi. Tutti gli sviluppatori possono estendere i servizi di pulizia dischi disponibili implementando e registrando un gestore pulitura disco.

Tutte le applicazioni che producono file temporanei possono e devono implementare e registrare un gestore pulitura disco. In questo modo si offre agli utenti un modo pratico e affidabile per gestire i file temporanei dell'applicazione. Quando si implementa il gestore, è possibile decidere quali file sono interessati e determinare il modo in cui viene eseguita la pulizia effettiva.

## <a name="implementation-basics"></a>Nozioni fondamentali sull'implementazione

I gestori di pulitura sono oggetti del server Component Object Model (COM) in-process. Windows fornisce un oggetto gestore esistente denominato DataDrivenCleaner per l'utilizzo. È anche possibile scegliere di implementare un gestore per maggiore flessibilità. Questi oggetti consentono quindi di specificare come selezionare i file, liberare spazio su disco e, nel caso di un gestore implementato, visualizzare l'interfaccia utente facoltativa per un controllo più granulare. In questa sezione viene illustrata l'implementazione di un gestore personalizzato. Per informazioni dettagliate sull'uso dell'oggetto DataDrivenCleaner, vedere [using the DataDrivenCleaner Object](#using-the-datadrivencleaner-object).

Un gestore pulitura dischi deve eseguire queste cinque attività di base.

-   Inizializzare l'oggetto gestore.
-   Eseguire la scansione del disco per determinare la quantità di spazio su disco che è possibile liberare.
-   Consente di visualizzare l'interfaccia utente per ottenere i commenti e i suggerimenti degli utenti sui file da pulire. Facoltativa
-   Eseguire la pulizia.
-   Spegni.

Per consentire a gestione pulizia dischi di gestire queste attività, è necessario che un gestore esporti [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) per Windows 98 o [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) per Windows Millennium Edition (Windows Me), Windows 2000 e Windows XP. Poiché **IEmptyVolumeCache2** eredita da **IEmptyVolumeCache**, aggiungendo solo il metodo aggiuntivo **InitializeEx**, è necessario un lavoro aggiuntivo relativamente piccolo per implementare entrambi. A meno che il gestore non sia destinato solo a uno di questi sistemi operativi, deve esportare entrambe le interfacce.

Per esportare queste interfacce, è necessario implementare questi metodi corrispondenti alle cinque attività di base.

-   [Initialize/InitializeEx](#initializeinitializeex)
-   [GetSpaceUsed](#getspaceused)
-   [ShowProperties](#showproperties)
-   [Ripulisci](#purge)
-   [Disattivare](#deactivate)

### <a name="initializeinitializeex"></a>Initialize/InitializeEx

I due metodi di inizializzazione, che sono molto simili, vengono chiamati quando viene eseguita l'utilità di pulitura del disco. Gestione pulizia disco di Windows 98 chiama il metodo [**IEmptyVolumeCache:: Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) di un gestore. Windows Millennium Edition (Windows Me), Windows 2000 o Windows XP Disk Cleanup Manager, tuttavia, tenta prima di tutto di chiamare [**IEmptyVolumeCache2:: InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) e USA **IEmptyVolumeCache:: Initialize** solo se [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) non è esposto dal gestore. Gestione pulizia dischi passa informazioni al metodo, ad esempio la chiave del registro di sistema del gestore e il volume del disco da pulire.

Entrambi i metodi possono restituire varie stringhe di visualizzazione e impostare uno o più flag. La differenza principale tra i due metodi è il modo in cui viene gestito il testo visualizzato in Gestione pulitura disco. Le tre stringhe seguenti sono interessate.



| string       | Scopo                                                                            | Inizializzare                                                                           | InitializeEx                                                                                     |
|--------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Nome visualizzato | Nome del gestore visualizzato nella casella di riepilogo di gestione pulizia dischi.               | Se *ppwszDisplayName* è **null**, il valore predefinito viene recuperato dal registro di sistema. | È necessario specificare una stringa localizzata correttamente in *ppwszDisplayName* . non viene usato alcun valore del registro di sistema. |
| Descrizione  | Testo descrittivo visualizzato sotto la casella di riepilogo quando viene selezionato il nome del gestore. | Se *ppwszDescription* è **null**, il valore predefinito viene recuperato dal registro di sistema. | È necessario specificare una stringa localizzata correttamente in *ppwszDescription* . non viene usato alcun valore del registro di sistema. |
| Testo pulsante  | Testo per il pulsante facoltativo che consente agli utenti di visualizzare l'interfaccia utente del gestore.        | Nessun parametro disponibile. Deve essere specificato nel registro di sistema.                           | È necessario specificare una stringa localizzata correttamente in *ppwszBtnText* . non viene usato alcun valore del registro di sistema.     |



 

Il parametro *pdwFlags* trovato in entrambi i metodi di inizializzazione riconosce lo stesso set di flag. Due di questi flag vengono passati al metodo da Gestione pulitura disco.

-   **\_SETTINGSMODE EVCF**

    Se il gestore pulitura disco viene eseguito in base a una pianificazione, imposta il flag **\_ SETTINGSMODE di EVCF** . Se questo flag è impostato, Gestione pulitura disco non chiama i metodi [GetSpaceUsed](#getspaceused), [Purge](#purge)o [showProperties](#showproperties) . Il metodo [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) o [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) del gestore deve gestire tutte le attività normalmente eseguite da [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) ed [**Purge**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge). Poiché non è possibile inviare commenti e suggerimenti degli utenti, è necessario toccare solo i file estremamente sicuri da pulire. È consigliabile ignorare il parametro *pcwszVolume* del metodo di inizializzazione e pulire i file non necessari indipendentemente dall'unità in cui si trovano.

-   **\_OUTOFDISKSPACE EVCF**

    Se viene impostato il flag **EVCF \_ OUTOFDISKSPACE** , l'unità disco dell'utente è insufficiente. Il gestore deve essere aggressivo per eliminare i file, anche se comporta una perdita di prestazioni. Tuttavia, il gestore non deve ovviamente eliminare i file che potrebbero causare un errore dell'applicazione o la perdita dei dati da parte dell'utente.

I flag rimanenti vengono impostati dal gestore pulitura disco e restituiti al gestore pulitura disco. Per ulteriori informazioni, vedere le pagine di riferimento del metodo per [**IEmptyVolumeCache:: Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) e [**IEmptyVolumeCache2:: InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex).

-   \_DONTSHOWIFZERO EVCF

    Visualizza il gestore nella casella di riepilogo di gestione pulizia dischi solo se il valore restituito da [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) indica che il gestore può liberare spazio su disco.

-   \_ENABLEBYDEFAULT EVCF

    Specifica che il gestore è abilitato per impostazione predefinita. Viene eseguito ogni volta che viene eseguita una pulizia del disco, a meno che l'utente non lo Disabilita deselezionando la relativa casella di controllo nell'elenco dei gestori di Gestione pulitura disco.

-   EVCF \_ ENABLEBYDEFAULT \_ auto

    Specifica che il gestore viene abilitato automaticamente per l'esecuzione durante le pulizie pianificate.

-   \_HASSETTINGS EVCF

    Impostare questo flag se il gestore dispone di un'interfaccia utente da visualizzare. In risposta, Gestione pulitura disco Visualizza un pulsante quando tale gestore è selezionato nella casella di riepilogo. Se si fa clic su tale pulsante, il gestore pulitura disco chiama [**showProperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties).

-   \_REMOVEFROMLIST EVCF

    Eliminare il nome del gestore dall'elenco dei gestori disponibili dopo che il gestore è stato eseguito una sola volta. Vengono eliminate anche le informazioni del registro di sistema del gestore.

### <a name="getspaceused"></a>GetSpaceUsed

Il gestore pulitura disco chiama questo metodo per determinare la quantità di spazio che un gestore pulitura dischi può potenzialmente liberare. Il gestore pulitura disco Visualizza quindi il valore a destra del nome del gestore nella casella di riepilogo. Questa operazione viene eseguita su tutti i gestori registrati con Gestione pulitura disco quando viene avviato il gestore e prima che venga visualizzata l'interfaccia utente principale del Manager. Quando viene chiamato [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) , il gestore deve eseguire la scansione dei file di cui è responsabile, determinare quali sono i candidati per la pulizia e restituire la quantità di spazio su disco che può liberare.

Poiché l'analisi può essere un processo lungo, Gestione pulitura dischi usa il parametro *picB* del metodo per passare un puntatore a un'interfaccia [**IEmptyVolumeCacheCallBack**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) . Il gestore utilizza l'interfaccia periodicamente durante l'analisi per chiamare [**IEmptyVolumeCacheCallBack:: ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress), che svolge due finalità.

-   Consente a gestione pulizia disco di aggiornare un indicatore di stato, indicando all'utente la modalità di avanzamento dell'analisi.
-   Notifica al gestore di arrestare l'analisi nel caso in cui venga fatto clic sul pulsante **Annulla** della finestra di stato. Questo evento Button non viene comunicato direttamente al gestore; al contrario, la gestione pulizia disco restituisce E \_ Abort la volta successiva che [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) chiama [**IEmptyVolumeCacheCallBack:: ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress).

### <a name="showproperties"></a>ShowProperties

Prima di avviare la pulizia, il gestore può visualizzare un'interfaccia utente in genere sotto forma di finestra di Esplora risorse che consente all'utente di visualizzare un elenco di file o classi di file selezionati per la pulizia da parte del gestore. Se il gestore imposta il flag **EVCF \_ HASSETTINGS** quando viene chiamato [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) o [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) , l'utente può richiedere l'interfaccia utente facendo clic sul pulsante visualizzato a tale scopo in Gestione pulitura disco. Il testo del pulsante varia dal gestore al gestore, ma "Visualizza file", "Visualizza pagine" e "Opzioni" sono etichette comuni.

Quando si fa clic sul pulsante, Gestione pulitura disco chiama [**showProperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties) per richiedere al gestore di visualizzare l'interfaccia utente. L'interfaccia utente deve essere creata come figlio della finestra il cui handle viene passato nel parametro *HWND* del metodo **showProperties** .

### <a name="purge"></a>Ripulisci

Il gestore pulitura disco chiama il metodo di [**ripulitura**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge) del gestore per impostare la pulizia in movimento. Il parametro *picB* del metodo è un puntatore all'interfaccia [**IEmptyVolumeCacheCallBack**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) di Gestione pulitura disco. Come per il metodo [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) , è necessario che il gestore usi periodicamente l'interfaccia di callback per segnalare lo stato di avanzamento ed eseguire una query su Gestione pulitura disco se l'utente ha fatto clic su **Annulla**. Si noti tuttavia che il metodo **Purge** deve chiamare [**IEmptyVolumeCacheCallBack::P Urgeprogress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-purgeprogress), non [**ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress).

### <a name="deactivate"></a>Disattivare

Il metodo [**Deactivate**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-deactivate) viene chiamato quando Gestione pulitura disco sta preparando l'arresto. Il gestore deve eseguire tutte le attività di pulizia necessarie e restituire. Se non si desidera che il gestore venga nuovamente eseguito, impostare il flag **EVCF \_ REMOVEFROMLIST** nel parametro *pdwFlags* del metodo di inizializzazione. Se questo flag è impostato, Gestione pulitura disco rimuove il gestore dall'elenco ed Elimina le voci del registro di sistema del gestore. Per eseguire nuovamente il gestore, è necessario aggiungere nuovamente le voci del registro di sistema. Questo flag viene in genere usato per i gestori che vengono eseguiti una sola volta.

## <a name="registering-a-disk-cleanup-handler"></a>Registrazione di un gestore pulitura disco

Per aggiungere un gestore all'elenco di Gestione pulitura disco, è necessario aggiungere alcune chiavi e valori al registro di sistema di Windows.

-   [Registrazione del CLSID di un gestore](#registering-a-handlers-clsid)
-   [Registrazione di un gestore con Gestione pulitura disco: generale](#registering-a-handler-with-the-disk-cleanup-manager-general)
-   [Registrazione di un gestore con Gestione pulitura disco: sistemi Windows 2000 o versioni successive](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
-   [Utilizzo dell'oggetto DataDrivenCleaner](#using-the-datadrivencleaner-object)
-   [Registrazione di esempio di un gestore di pulitura del disco](#example-registration-of-a-disk-cleanup-handler)

### <a name="registering-a-handlers-clsid"></a>Registrazione del CLSID di un gestore

Come per tutti gli oggetti COM, il GUID e la DLL dell'oggetto gestore devono essere registrati nella chiave **CLSID** della **\_ \_ radice delle classi HKEY**. È anche possibile registrare un'icona visualizzata accanto al nome del gestore nella casella di riepilogo di Gestione pulitura disco, ma questo è facoltativo. Nell'esempio seguente vengono illustrate le chiavi, i valori e i dati necessari.

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

### <a name="registering-a-handler-with-the-disk-cleanup-manager-general"></a>Registrazione di un gestore con Gestione pulitura disco: generale

Per completare la registrazione, un gestore deve aggiungere una chiave che contiene le proprie specifiche, come illustrato di seguito. Nella parte restante di questa sezione viene illustrato il contenuto di questa chiave.

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

In generale, il nome della chiave che contiene i particolari di un gestore è denominato per il tipo di file che gestisce, ad esempio **i file di programma scaricati**, ma questo non è un requisito. La tabella seguente illustra in dettaglio i possibili valori trovati in questa chiave.

> [!Note]  
> Solo il valore predefinito che specifica l'identificatore di classe (CLSID) del gestore è obbligatorio tutti gli altri valori sono facoltativi.

 



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
<td>Il CLSID del gestore è registrato nel <strong>HKEY_CLASSES_ROOT</strong> \ <strong>CLSID</strong>.</td>
</tr>
<tr class="even">
<td>AdvancedButtonText</td>
<td>REG_SZ</td>
<td>Testo per il pulsante facoltativo su cui gli utenti possono fare clic per visualizzare l'interfaccia utente del gestore. Il carattere & può essere inserito prima di un carattere per assegnare una scelta rapida da tastiera per il pulsante. Il valore AdvancedButtonText viene ignorato dai gestori che espongono <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2:: InitializeEx</strong></a>.</td>
</tr>
<tr class="odd">
<td>CleanupString</td>
<td>REG_SZ</td>
<td>Riga di comando che specifica un file eseguibile e i parametri facoltativi della riga di comando. Questa riga di comando viene eseguita al completamento della pulizia del disco.</td>
</tr>
<tr class="even">
<td>CSIDL</td>
<td>REG_DWORD</td>
<td>Identificatore indipendente dal sistema per una cartella speciale da includere nella ricerca di file. Questo valore deve essere immesso come valore numerico per instance, 0X0000001C anziché CSIDL_LOCAL_APPDATA. Per un elenco di valori possibili, vedere <a href="/windows/desktop/shell/csidl"><strong>CSIDL</strong></a>. È possibile utilizzare solo un singolo valore.<br/> Se viene specificato il valore della cartella, il percorso indicato dal valore CSIDL viene anteposto a tali informazioni per comporre un percorso di ricerca. Si consideri, ad esempio, lo scenario seguente.<br/>
<ul>
<li>Il valore CSIDL è specificato come 0x0000000D (CSIDL_MYMUSIC)</li>
<li>La cartella Music si trova in C:\Documents and Settings \<em>username</em>\My Music</li>
<li>Il valore della cartella contiene &quot; Jazz\Singers&quot;</li>
</ul>
Il risultato di tale scenario è che il gestore pulitura dischi esegue la ricerca nella cartella C:\Documents and Settings \<em>username</em>\My Music\Jazz\Singers Si noti che la barra che precede il valore della cartella viene aggiunta se non è presente.<br/></td>
</tr>
<tr class="odd">
<td>Descrizione</td>
<td>REG_SZ</td>
<td>Testo descrittivo visualizzato sotto la casella di riepilogo di Gestione pulitura disco quando viene selezionato il nome del gestore. Qui è possibile illustrare il funzionamento del gestore, i file con cui si riferisce e qualsiasi altra informazione elucidatory all'utente. Se <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2:: InitializeEx</strong></a> non è esposto dal gestore, è possibile eseguire l'override di questo testo tramite il metodo <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache:: Initialize</strong></a> del gestore specificando una stringa alternativa nel parametro <em>ppwszDescription</em> quando viene chiamato il metodo.</td>
</tr>
<tr class="even">
<td>Visualizza</td>
<td>REG_SZ</td>
<td>Nome del gestore da visualizzare nella casella di riepilogo di gestione pulizia dischi. Se <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2:: InitializeEx</strong></a> non è esposto dal gestore, è possibile eseguire l'override di questo testo tramite il metodo <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache:: Initialize</strong></a> del gestore specificando una stringa alternativa nel parametro <em>ppwszDisplayName</em> quando viene chiamato il metodo.</td>
</tr>
<tr class="odd">
<td>FileList</td>
<td>REG_SZ o REG_MULTI_SZ</td>
<td>Elenco di file ricercati e puliti da questo gestore. È possibile specificare caratteri jolly usando? o * caratteri. Se il valore è di tipo REG_SZ, più estensioni sono separate usando | o: caratteri, senza spazi su entrambi i lati.<br/> Se il flag DDEVCF_REMOVEDIRS è impostato nel valore dei flag, questi valori possono specificare i nomi di directory e i file.<br/></td>
</tr>
<tr class="even">
<td>Flags</td>
<td>REG_DWORD o REG_BINARY</td>
<td>Flag che controllano gli elementi della procedura di ricerca e di pulizia. Uno o più dei valori seguenti.
<ul>
<li>DDEVCF_DOSUBDIRS (0x00000001). Eseguire ricerche e rimuovere in modo ricorsivo.</li>
<li>DDEVCF_REMOVEAFTERCLEAN (0x00000002). Quando il gestore viene eseguito una volta, rimuoverlo dal registro di sistema.</li>
<li>DDEVCF_REMOVEREADONLY (0x00000004). Rimuovere i file che soddisfano i criteri di ricerca anche se sono di sola lettura.</li>
<li>DDEVCF_REMOVESYSTEM (0x00000008). Rimuovere i file che soddisfano i criteri di ricerca anche se sono file di sistema.</li>
<li>DDEVCF_REMOVEHIDDEN (0x00000010). Rimuovere i file che soddisfano i criteri di ricerca anche se si tratta di file nascosti.</li>
<li>DDEVCF_DONTSHOWIFZERO (0x00000020). Non visualizzare questo gestore in Gestione pulitura disco se nessun file corrisponde ai criteri di ricerca.</li>
<li>DDEVCF_REMOVEDIRS (0x00000040). Trovare la corrispondenza con il valore di fileelenchi per le directory e rimuovere le corrispondenze e tutte le relative sottodirectory.</li>
<li>DDEVCF_RUNIFOUTOFDISKSPACE (0x00000080). Eseguire questo gestore solo se lo spazio disponibile su disco è sceso al di sotto del valore critico, determinato da Gestione pulizia dischi che imposta il flag di EVCF_OUTOFDISKSPACE tramite <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache:: Initialize</strong></a> o <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2:: InitializeEx</strong></a>.</li>
<li>DDEVCF_REMOVEPARENTDIR (0x00000100). Rimuovere la directory padre dei file specificati dopo l'esecuzione del pulisci.</li>
<li>DDEVCF_PRIVATE_LASTACCESS (0x10000000). Usare il valore LastAccess, se specificato, per verificare i file da pulire. Questo flag viene ignorato quando si usa <a href="#using-the-datadrivencleaner-object">DataDrivenCleaner</a> , viene sempre usato il valore LastAccess fornito.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Cartella</td>
<td>REG_SZ, REG_MULTI_SZ o REG_EXPAND_SZ</td>
<td>Cartella o cartelle specifiche in cui cercare gli elementi corrispondenti alle voci nel valore di fileitem. È possibile specificare caratteri jolly usando? o * caratteri. Se il valore è di tipo REG_SZ, più nomi di cartella vengono separati con | carattere senza spazi su entrambi i lati.<br/> Se è presente un valore CSIDL, in questo valore è possibile specificare una sola cartella. Il percorso indicato dal valore CSIDL è anteposto al percorso della cartella per comporre un percorso di ricerca. Per un esempio, vedere la descrizione del valore CSIDL.<br/> Se questo valore è assente in Windows Vista Service Pack 1 (SP1) e versioni successive, il gestore pulitura viene ignorato e restituisce S_FALSE all'inizializzazione.<br/> Se questo valore è assente nella versione originale di Windows Vista e versioni precedenti, viene utilizzata la cartella radice del volume corrente. In tal caso, è necessario il flag DDEVCF_DOSUBDIRS per eseguire la ricerca nell'intera unità. Senza di esso, viene eseguita la ricerca solo nella cartella radice.<br/> È necessario specificare un'unità o unità. Questa operazione può essere fornita tramite il valore CSIDL o tramite una stringa REG_EXPAND_SZ. Escludendo tali opzioni, tuttavia, l'unità in cui eseguire la ricerca deve essere specificata nel nome della cartella. Usare?: per eseguire la ricerca nella cartella dell'unità corrente.<br/></td>
</tr>
<tr class="even">
<td>IconPath</td>
<td>REG_SZ o REG_EXPAND_SZ</td>
<td>Percorso della risorsa da cui ottenere un'icona da usare in associazione al gestore.</td>
</tr>
<tr class="odd">
<td>LastAccess</td>
<td>REG_DWORD o REG_BINARY</td>
<td>Il numero di giorni che devono essere trascorsi dopo l'ultimo accesso al file o la creazione di una directory per il file o la directory da considerare per la pulizia.</td>
</tr>
<tr class="even">
<td>Priorità</td>
<td>REG_DWORD o REG_BINARY</td>
<td>Determina l'ordine di esecuzione del gestore rispetto ad altri gestori. Maggiore è il numero, precedente nel processo eseguito dal gestore. Nessun intervallo definito è accettabile.</td>
</tr>
<tr class="odd">
<td>PropertyBag</td>
<td>REG_SZ</td>
<td>CLSID di una risorsa utilizzata per fornire il testo localizzato per il nome visualizzato, la descrizione e il testo del pulsante. Questa risorsa è utile nei casi in cui un gestore non implementa <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache"><strong>IEmptyVolumeCache</strong></a> e il gestore viene eseguito in Microsoft Windows NT o Windows XP.<br/> Gestione pulitura disco controlla prima di tutto se la routine di inizializzazione del gestore ha restituito tali stringhe, come avviene quando viene implementato <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2"><strong>IEmptyVolumeCache2</strong></a> . In caso contrario, il gestore si rivolge a un contenitore di proprietà denominato in questo valore. Se non è stato specificato alcun valore, viene recuperato il testo dal registro di sistema.<br/></td>
</tr>
<tr class="even">
<td>StateFlags</td>
<td>REG_DWORD</td>
<td>Eseguendo il file eseguibile di gestione pulizia dischi Cleanmgr.exe dalla riga di comando, è possibile dichiarare i <em>profili</em>di pulizia. Questi profili sono composti da un subset dei gestori disponibili a cui viene assegnata un'etichetta numerica univoca. In questo modo è possibile automatizzare l'esecuzione di diversi set di gestori in momenti diversi.<br/> La riga di comando &quot;cleanmgr.exe/sageset:<strong>nnnn</strong> &quot; , dove <strong>nnnn</strong> è un'etichetta numerica UNIVOCa, Visualizza un'interfaccia utente che consente di scegliere i gestori da includere nel profilo. Così come per la definizione del profilo, il parametro sageset scrive anche un valore denominato StateFlags<strong>nnnn</strong>, dove <strong>nnnn</strong> è l'etichetta usata nel parametro, a tutte le sottochiavi in <strong>VolumeCaches</strong>. Per tali voci sono possibili due valori di dati.
<ul>
<li>0: non eseguire questo gestore quando il profilo viene eseguito.</li>
<li>2: includere questo gestore quando viene eseguito questo profilo.</li>
</ul>
<br/> Si supponga, ad esempio, che la riga di comando &quot;cleanmgr.exe/sageset: 1234 &quot; venga eseguita. Nell'interfaccia utente visualizzata, l'utente sceglie i file di <strong>programma scaricati</strong>, ma non sceglie <strong>i file temporanei di Internet</strong>. I valori seguenti vengono quindi scritti nel registro di sistema.<br/>
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
<br/> La riga &quot; di comandocleanmgr.exe/sagerun:<strong>nnnn</strong> &quot; , in cui il valore di <strong>nnnn</strong> corrisponde all'etichetta dichiarata con il parametro sageset, esegue tutti i gestori selezionati in quel profilo.<br/> Un valore StateFlags generico viene scritto nel registro di sistema quando la pulizia del disco viene eseguita normalmente. Questo valore archivia semplicemente lo stato (selezionato o non selezionato) del gestore nell'ultima volta in cui è stato presentato come opzione per l'utente. Per tali voci sono possibili due valori di dati.
<ul>
<li>0: il gestore non è stato selezionato.</li>
<li>1: il gestore è stato selezionato.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems"></a>Registrazione di un gestore con Gestione pulitura disco: sistemi Windows 2000 o versioni successive

La specifica del testo visualizzato nel registro di sistema può rendere difficile la localizzazione del software. Per questo motivo, Windows 2000 e Windows XP supportano l'interfaccia [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) con il metodo di inizializzazione preferito [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex). In Windows 2000 o versioni successive viene sempre eseguito un tentativo di chiamare **IEmptyVolumeCache2:: InitializeEx** prima di [**IEmptyVolumeCache:: Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize). Il sistema usa solo **Initialize** per inizializzare un gestore se **IEmptyVolumeCache2** non è esposto.

Per quanto riguarda il registro di sistema, l'unica differenza in Windows 2000 o versioni successive è la possibilità di omettere i valori AdvancedButtonText, display e Description quando [**IEmptyVolumeCache2:: InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) viene esposto dal gestore. Tali valori, che contengono testo localizzato correttamente, vengono forniti al gestore pulitura disco quando chiama **InitializeEx**.

### <a name="using-the-datadrivencleaner-object"></a>Utilizzo dell'oggetto DataDrivenCleaner

Un gestore pulitura disco di base, denominato DataDrivenCleaner, viene fornito dal sistema operativo. Per usare questo oggetto come gestore anziché implementare il proprio, usare il CLSID {C0E13E61-0CC6-11d1-BBB6-0060978B2AE6} come valore predefinito per la sottochiave del gestore in **VolumeCaches** come descritto in registrazione di [un gestore con Gestione pulitura disco: generale](#registering-a-handler-with-the-disk-cleanup-manager-general).

DataDrivenCleaner non espone [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2), quindi i valori di visualizzazione e descrizione vengono forniti tramite il registro di sistema. Quando si dichiarano tali stringhe, tenere presente che ciò potrebbe causare problemi di localizzazione. Il testo localizzato può essere fornito tramite il valore PropertyBag. Il valore di AdvancedButtonText viene ignorato poiché non è disponibile alcuna interfaccia utente e pertanto non è disponibile alcun pulsante per visualizzarlo, è disponibile per questo gestore.

### <a name="example-registration-of-a-disk-cleanup-handler"></a>Registrazione di esempio di un gestore di pulitura del disco

Di seguito viene illustrata una registrazione di esempio per un gestore di pulitura dischi implementato dall'azienda telefonica. Questo gestore implementa sia [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) che [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2), quindi fornisce AdvancedButtonText, descrizione e valori di visualizzazione nel caso in cui venga usato in un computer che esegue Windows 98. Il gestore combina i valori CSIDL e Folder per cercare i file nella directory C: \\ Program Files \\ The Phone Company \\ Temp e il flag DDEVCF DOSUBDIRS, in \_ modo che venga eseguita la ricerca nelle sottodirectory. Solo i file con estensione tmp e TPC sono considerati per la pulizia e il \_ flag LASTACCESS privato DDEVCF \_ è impostato in modo da escludere tali file, solo quelli a cui non è stato eseguito l'accesso per 14 giorni o più. \_Viene inoltre impostato il flag DDEVCF DONTSHOWIFZERO, in modo che il gestore non venga visualizzato nell'elenco a meno che non siano stati trovati candidati di pulizia.

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

 

