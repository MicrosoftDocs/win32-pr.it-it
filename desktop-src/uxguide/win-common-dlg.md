---
title: Finestre di dialogo comuni
description: Le finestre di dialogo comuni di Microsoft Windows sono costituite dalle finestre di dialogo Apri file, Salva file, Apri cartella, trova e Sostituisci, stampa, Imposta pagina, carattere e colore.
ms.assetid: 3f9fb0c9-bc1a-48c4-b021-99f155f8ea9e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 336cb368fa25bf68313e2bf336de68845a87e663
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104401819"
---
# <a name="common-dialogs"></a>Finestre di dialogo comuni

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Le finestre di dialogo comuni di Microsoft Windows sono costituite dalle finestre di dialogo Apri file, Salva file, Apri cartella, trova e Sostituisci, stampa, Imposta pagina, carattere e colore.

## <a name="open-file"></a>Apri file

![screenshot della finestra di dialogo Apri ](images/win-common-dlg-image1.png)

Il file aperto è ottimizzato per trovare rapidamente gli elementi da usare con un programma.

## <a name="save-file"></a>Salva file

![screenshot della finestra di dialogo Salva con nome ](images/win-common-dlg-image2.png)

Salva file chiude il ciclo salvando un file con i relativi metadati.

## <a name="open-folder"></a>Apri cartella

![screenshot della finestra di dialogo Cerca file/cartelle ](images/win-common-dlg-image3.png)

Apri cartella è specifico per la scelta delle cartelle.

## <a name="find-and-replace"></a>Trova e sostituisci

![cattura di schermata delle finestre di dialogo Trova e Sostituisci ](images/win-common-dlg-image4.png)

Trova consente agli utenti di cercare stringhe di testo, mentre la versione di sostituzione consente facoltativamente agli utenti di sostituire le corrispondenze con un'altra stringa.

## <a name="print"></a>Stampa

![screenshot della finestra di dialogo Stampa ](images/win-common-dlg-image5.png)

Print consente agli utenti di selezionare gli elementi da stampare, il numero di copie da stampare e la sequenza delle regole di confronto, oltre alla possibilità di scegliere e configurare stampanti.

## <a name="page-setup"></a>Impostazioni di pagina

![screenshot della finestra di dialogo Imposta pagina ](images/win-common-dlg-image6.png)

La configurazione della pagina consente agli utenti di selezionare il formato della carta e l'origine, l'orientamento della pagina e i margini.

## <a name="font"></a>Carattere

![screenshot della finestra di dialogo tipo di carattere ](images/win-common-dlg-image7.png)

Tipo di carattere consente di visualizzare i tipi di carattere e le dimensioni punti dei tipi di carattere installati disponibili.

## <a name="color"></a>Colore

![screenshot della finestra di dialogo Modifica colori ](images/win-common-dlg-image8.png)

Il colore consente agli utenti di selezionare un colore tramite un set predefinito di colori o scegliendo un colore "personalizzato".

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Utilizzando le finestre di dialogo comuni, è possibile offrire agli utenti un'esperienza coerente in diversi programmi. Utilizzando le finestre di dialogo comuni, è anche possibile offrire agli utenti un'esperienza efficace e piacevole.

Per migliorare significativamente l'esperienza degli utenti con queste finestre di dialogo, è possibile scegliere le impostazioni predefinite più appropriate per:

-   Valori di input (esempi: cartelle predefinite, nomi file predefiniti).
-   Opzioni selezionate (esempi: stampante selezionata, opzioni di stampa).
-   Viste (esempi: visualizzazione di immagini nella visualizzazione anteprima, visualizzazione di immagini senza nomi di file, ordinamento per data, larghezze delle colonne).
-   Presentazione (esempi: dimensioni della finestra, posizione e contenuto).

È necessario determinare le impostazioni predefinite iniziali e le impostazioni predefinite successive. I valori predefiniti iniziali sono determinati dal programma e in base all'utilizzo previsto dell'utente di destinazione, mentre le impostazioni predefinite successive si basano sull'utilizzo effettivo. L'utilizzo passato è l'indicatore migliore dell'utilizzo futuro.

Le impostazioni predefinite del programma sono efficienti? Consente di monitorare il numero di passaggi necessari agli utenti per eseguire le attività più comuni. Se gli utenti devono ripetere gli stessi passaggi potenzialmente inutili ogni volta che eseguono un'attività, è possibile migliorare i valori predefiniti.

**Se si esegue una sola operazione...**

Offrire agli utenti un'esperienza efficace e gradevole selezionando i valori predefiniti iniziali e successivi appropriati.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

**Sì! Usare le finestre di dialogo comuni per un'esperienza utente coerente. Non crearne di personalizzati.** È particolarmente difficile creare interfacce utente personalizzate che consentono di esplorare lo spazio dei nomi in modo corretto e sicuro. Si noti che, se necessario, è possibile personalizzare le finestre di dialogo comuni.

Per Windows Vista, il file aperto e il file di salvataggio hanno una nuova architettura estendibile che semplifica l'esposizione di funzionalità aggiuntive. Questo meccanismo è sufficientemente flessibile per soddisfare i requisiti minimi dei principali fornitori di software indipendenti (ISV), ma non deve essere suddiviso nelle versioni successive di Windows.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   Quando appropriato, fornire alternative dirette o non [modali](glossary.md) . Consenti agli utenti di:
    -   Aprire i file trascinandoli sul programma.
    -   Salvare i file usando il nome e il percorso correnti con un comando Save.
    -   Trovare l'occorrenza successiva di una stringa usando il tasto F3.
    -   Stampare una copia di un intero documento sulla stampante predefinita con un comando di stampa.
    -   Modificare i tipi di carattere e gli attributi del carattere utilizzando una barra degli strumenti o una finestra tavolo
    -   Modificare i colori utilizzando una barra degli strumenti o una finestra della tavolozza.
-   Usare i comandi seguenti per visualizzare le finestre di dialogo comuni (fornite insieme alle [chiavi di accesso](glossary.md)preferite):



|                              |                                               |
|------------------------------|-----------------------------------------------|
| **Finestra di dialogo comune**<br/> | **Comando**<br/>                        |
| Apri file<br/>         | Apri...<br/>                            |
| Salva file<br/>         | Salva con nome...<br/>                         |
| Apri cartella<br/>       | Apri cartella... in alternativa, scegliere cartella...<br/> |
| Trova e sostituisci<br/>  | Trova... o Sostituisci...<br/>              |
| Stampa<br/>             | Stampa...<br/>                           |
| Imposta pagina<br/>        | Imposta pagina...<br/>                      |
| Carattere<br/>              | Tipo di carattere... in alternativa, scegliere carattere...<br/>          |
| Colore<br/>             | Colore... in alternativa, scegliere colore...<br/>        |



 

-   È possibile usare comandi più specifici, in base alle esigenze. Esempio: per esportare un file, usare il comando Esporta file anziché Salva con nome.
-   Impostare il titolo della finestra di dialogo in modo che corrisponda al comando che lo ha avviato. Esempio: se Save file viene avviato da un comando export file, rinominare la finestra di dialogo per esportare il file.

### <a name="open-file"></a>Apri file

-   Per la cartella predefinita iniziale, utilizzare una cartella specializzata (immagini, musica, video) in base alle esigenze, in caso contrario utilizzare documenti.
-   Per le cartelle predefinite successive, usare l'ultima cartella aperta dall'utente tramite il programma.
-   Quando si aprono file di foto, per impostazione predefinita non è necessario visualizzare i nomi file Le foto vengono in genere identificate dalle anteprime e i nomi in genere non sono significativi.

### <a name="save-file"></a>Salva file

-   Per la cartella iniziale predefinita (se un nuovo file viene salvato per la prima volta), usare la cartella specializzata (immagini, musica, video) in base alle esigenze, altrimenti usare i documenti.
-   Per i file temporanei, usare la cartella temporanea dell'utente corrente. Scegliere i nomi file univoci, ma univoci. Esempio: usare File0001. tmp anziché ~ DF1A92. tmp.
    -   **Sviluppatori:** È possibile ottenere la cartella temporanea dell'utente corrente usando la funzione API GetTempPath.
-   Per il nome file predefinito iniziale, usare un nome predefinito univoco basato su:
    -   Contenuto del file, se noto. Esempio: prime parole in un documento.
    -   Modello scelto dall'utente. Esempio: se il file precedente è denominato "Hawaii 1.jpg", scegliere "Hawaii 2.jpg" come file successivo.
    -   Modello generico basato sul tipo di file. Esempio: "Photo1.jpg".
-   Per le impostazioni predefinite successive, se il file esiste già, usare la cartella e il nome del file corrente.
-   Quando si salva un file, conservarne la data di creazione. Se il programma salva i file creando un file temporaneo, Elimina l'originale e Rinomina il file temporaneo con il nome del file originale, assicurarsi di copiare la data di creazione dal file originale.
-   Usare Save file se l'utente seleziona il comando Save senza specificare un nome file.

### <a name="file-types-lists"></a>Elenchi di tipi di file

**Nota:** Gli elenchi dei tipi di file vengono utilizzati da Apri file e Salva file per determinare i tipi di file visualizzati e l'estensione di file predefinita.

-   Se l'elenco dei tipi di file è breve (cinque o meno), ordinare l'elenco in base alla probabilità di utilizzo. Se l'elenco è lungo (sei o più), usare un ordine alfabetico per facilitare la ricerca dei tipi.
-   Per Salva file, includere tutte le varianti delle estensioni di file supportate, anche se non comuni, e inserire prima di tutto l'estensione più comune. La logica di gestione dei file esamina questo elenco per determinare se l'utente ha fornito un'estensione di file supportata. Esempio: se un elenco di tipi di file JPEG include solo i file con estensione jpg e JPEG, il file test. jpe potrebbe essere salvato come test.jpe.jpg.
-   Per Salva file, il tipo di file predefinito iniziale è il più probabile scelto dall'utente di destinazione. Il valore predefinito successivo è il tipo corrente del file.
-   Per file aperto, il tipo di file predefinito iniziale è il più probabile scelto dall'utente di destinazione. Il valore predefinito successivo deve essere l'ultimo tipo di file utilizzato.
-   Per file aperto, includere una voce "tutti i file" come primo elemento se gli utenti possono aprire qualsiasi tipo di file o potrebbe dover visualizzare contemporaneamente tutti i file in una cartella. Si consiglia di fornire altri filtri meta, ad esempio "tutte le immagini", "tutti i brani musicali" e "tutti i video". Posizionarli immediatamente dopo "tutti i file".
-   Usare il formato "nome del tipo di file ( \* . EXT1; \* . EXT2). " Il nome del tipo di file deve essere il nome del tipo di file registrato, che è possibile visualizzare nell'elemento del pannello di controllo Opzioni cartella. Esempio: "documento HTML ( \* . htm; \* . HTML). "
    -   **Eccezione:** Per i metadati, rimuovere l'elenco di estensioni di file per evitare confusione. Esempi: "tutti i file", "tutte le immagini", "tutti i brani musicali" e "tutti i video".
-   Usare le [maiuscole](glossary.md) e minuscole per i nomi dei tipi di file e minuscole per le estensioni dei tipi di file.

### <a name="open-folder"></a>Apri cartella

-   **Per i nuovi programmi, usare la finestra di dialogo Apri file nella modalità "Seleziona cartelle".** Questa operazione richiede Windows Vista o versioni successive, pertanto utilizzare la finestra di dialogo Apri cartella per i programmi eseguiti nelle versioni precedenti di Windows.
    -   **Sviluppatori:** È possibile usare la finestra di dialogo Apri file nella modalità "pick Folders" usando il \_ flag Fos PICKFOLDERS.

### <a name="font"></a>Carattere

-   Se necessario, è possibile filtrare l'elenco dei tipi di carattere in modo da visualizzare solo i tipi di carattere disponibili per il programma.

### <a name="persistence"></a>Persistenza

-   Provare a rendere persistenti i valori seguenti per l'uso come impostazioni predefinite successive:
    -   Valori di input (esempi: cartelle predefinite, nomi file predefiniti).
    -   Opzioni selezionate (esempi: stampante selezionata, opzioni di stampa).
    -   Viste (esempi: visualizzazione di immagini nella visualizzazione anteprima, visualizzazione di immagini senza nomi di file, ordinamento per data, larghezze delle colonne).
    -   Presentazione (esempi: dimensioni della finestra, posizione e contenuto).

**Eccezione:** Non rendere questi valori mantenuti per le finestre di dialogo comuni quando il loro utilizzo è tale che è molto più probabile che gli utenti debbano iniziare completamente.

-   Quando si determinano i valori predefiniti, è opportuno considerare quali utenti di destinazione sono più probabili in base agli scenari importanti. Considerare anche gli scenari all'interno di un'istanza di programma, in più istanze (sia consecutive che simultanee) e in più documenti. Non rendere i valori mantenuti in circostanze che non possono essere utili.
    -   **Esempio:** Per una tipica applicazione basata su documenti, è utile usare le impostazioni di file aperti persistenti e salvare le impostazioni di file all'interno di un'istanza di programma e tra istanze consecutive, mantenendo le istanze simultanee indipendenti. In questo modo, gli utenti possono lavorare in modo efficiente con diversi documenti alla volta.
-   Rendere le impostazioni mantenute in base ai singoli programmi, per ogni utente.

 

