---
title: Dialoghe comuni
description: Le finestre Windows comuni di Microsoft sono costituite da finestre di dialogo Apri file, Salva file, Apri cartella, Trova e sostituisci, Stampa, Imposta pagina, Tipo di carattere e Colore.
ms.assetid: 3f9fb0c9-bc1a-48c4-b021-99f155f8ea9e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 9ddd0bf5af0a609c07550ec91e7482ce35270c85b81d553d4a5e262db6ed3683
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935606"
---
# <a name="common-dialogs"></a>Dialoghe comuni

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Le finestre Windows comuni di Microsoft sono costituite da finestre di dialogo Apri file, Salva file, Apri cartella, Trova e sostituisci, Stampa, Imposta pagina, Tipo di carattere e Colore.

## <a name="open-file"></a>Apri file

![Screenshot della finestra di dialogo Apri ](images/win-common-dlg-image1.png)

Open File è ottimizzato per trovare rapidamente gli elementi da usare con un programma.

## <a name="save-file"></a>Salva file

![Screenshot della finestra di dialogo Salva con nome ](images/win-common-dlg-image2.png)

Salva file chiude il ciclo salvando un file con i relativi metadati.

## <a name="open-folder"></a>Apri cartella

![Screenshot della finestra di dialogo Cerca file/cartelle ](images/win-common-dlg-image3.png)

Apri cartella è specifico per la scelta delle cartelle.

## <a name="find-and-replace"></a>Trova e sostituisci

![Screenshot delle finestre di dialogo trova e sostituisci ](images/win-common-dlg-image4.png)

Trova consente agli utenti di cercare stringhe di testo, mentre la versione Sostituisci consente facoltativamente agli utenti di sostituire le corrispondenze con un'altra stringa.

## <a name="print"></a>Stampa

![Screenshot della finestra di dialogo stampa ](images/win-common-dlg-image5.png)

Stampa consente agli utenti di selezionare gli elementi da stampare, il numero di copie da stampare e la sequenza di regole di confronto, oltre alla possibilità di scegliere e configurare le stampanti.

## <a name="page-setup"></a>Impostazioni di pagina

![Screenshot della finestra di dialogo di configurazione della pagina ](images/win-common-dlg-image6.png)

L'impostazione della pagina consente agli utenti di selezionare il formato e l'origine, l'orientamento della pagina e i margini.

## <a name="font"></a>Carattere

![Screenshot della finestra di dialogo tipo di carattere ](images/win-common-dlg-image7.png)

Tipo di carattere visualizza i tipi di carattere e le dimensioni dei punti dei tipi di carattere installati disponibili.

## <a name="color"></a>Color

![Screenshot della finestra di dialogo Modifica colori ](images/win-common-dlg-image8.png)

Colore consente agli utenti di selezionare un colore, tramite un set predefinito di colori o scegliendo un colore "personalizzato".

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Usando le finestre di dialogo comuni, è possibile offrire agli utenti un'esperienza coerente tra programmi diversi. Inoltre, usando le finestre di dialogo comuni, è anche possibile offrire agli utenti un'esperienza efficiente e piacevole.

È possibile migliorare significativamente l'esperienza degli utenti con queste finestre di dialogo scegliendo le impostazioni predefinite più appropriate per:

-   Valori di input (esempi: cartelle predefinite, nomi di file predefiniti).
-   Opzioni selezionate (esempi: stampante selezionata, opzioni di stampa).
-   Visualizzazioni (esempi: visualizzazione di immagini nella visualizzazione anteprima, visualizzazione di immagini senza nomi di file, ordinamento in base alla data, larghezza delle colonne).
-   Presentazione (esempi: dimensioni della finestra, posizione e contenuto).

È necessario determinare sia le impostazioni predefinite iniziali che le impostazioni predefinite successive. I valori predefiniti iniziali sono determinati dal programma e in base all'utilizzo previsto dell'utente di destinazione, mentre i valori predefiniti successivi sono basati sull'utilizzo effettivo. L'utilizzo passato è l'indicatore migliore dell'utilizzo futuro.

Le impostazioni predefinite del programma sono efficienti? Monitorare il numero di passaggi che gli utenti devono eseguire per eseguire le attività più comuni. Se gli utenti devono ripetere gli stessi passaggi potenzialmente non necessari ogni volta che eseguono un'attività, è possibile migliorare i valori predefiniti.

**Se si fa una sola cosa...**

Offrire agli utenti un'esperienza efficiente e piacevole selezionando le impostazioni predefinite iniziali e successive appropriate.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

**Sì! Usare le finestre di dialogo comuni per un'esperienza utente coerente. Non crearne uno personalizzato.** È particolarmente difficile creare uri personalizzate che esplorano lo spazio dei nomi in modo corretto e sicuro. Si noti che è possibile personalizzare le finestre di dialogo comuni, se necessario.

Per Windows Vista, Open File e Save File hanno una nuova architettura estendibile per semplificare l'esposizione di funzionalità aggiuntive. Questo meccanismo è sufficientemente flessibile da soddisfare i requisiti minimi dei principali fornitori di software indipendenti (ISV), ma non può essere interrotto dalle versioni future Windows.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   Se appropriato, fornire alternative più dirette o [non](glossary.md) modali. Consenti agli utenti di:
    -   Aprire i file eliminandoli nel programma.
    -   Salvare i file usando il nome e il percorso correnti con un comando Salva.
    -   Trovare l'occorrenza successiva di una stringa usando il tasto F3.
    -   Stampare una copia di un intero documento sulla stampante predefinita con un comando Stampa.
    -   Modificare i tipi di carattere e gli attributi dei tipi di carattere usando una barra degli strumenti o una finestra del riquadro.
    -   Modificare i colori usando una barra degli strumenti o una finestra della tavolozza.
-   Usare i comandi seguenti per visualizzare le finestre di dialogo comuni (fornite insieme alle chiavi di [accesso preferite):](glossary.md)



| Finestra di dialogo comune          | Comando                                 |
|------------------------|-----------------------------------------|
| Apri file<br/>         | Apri...<br/>                            |
| Salva file<br/>         | Salva con nome...<br/>                         |
| Apri cartella<br/>       | Apri cartella... o Scegliere la cartella...<br/> |
| Trova e sostituisci<br/>  | Trovare... o Sostituisci...<br/>              |
| Stampa<br/>             | Stampa...<br/>                           |
| Imposta pagina<br/>        | Configurazione della pagina in corso...<br/>                      |
| Carattere<br/>              | Carattere... o Scegliere il tipo di carattere...<br/>          |
| Color<br/>             | Colore... o Scegliere il colore...<br/>        |



 

-   È possibile usare comandi più specifici, in base alle esigenze. Esempio: per esportare un file, usare il comando Esporta file anziché Salva con nome.
-   Impostare il titolo della finestra di dialogo in modo da riflettere il comando che l'ha avviata. Esempio: se Salva file viene avviato da un comando Esporta file, rinominare la finestra di dialogo in Esporta file.

### <a name="open-file"></a>Apri file

-   Per la cartella predefinita iniziale, usare una cartella specializzata (Immagini, Musica, Video) in base alle esigenze, in caso contrario usare Documenti.
-   Per le cartelle predefinite successive, usare l'ultima cartella aperta dall'utente usando il programma.
-   Quando si aprono file di foto, eliminare i nomi di file per impostazione predefinita. Foto sono in genere identificati dalle anteprime e i relativi nomi in genere non sono significativi.

### <a name="save-file"></a>Salva file

-   Per la cartella predefinita iniziale (se un nuovo file viene salvato per la prima volta), usare la cartella specializzata (Immagini, Musica, Video) in base alle esigenze, altrimenti usare Documenti.
-   Per i file temporanei, usare la cartella temporanea dell'utente corrente. Scegliere nomi di file semplici, ma univoci. Esempio: usare File0001.tmp anziché ~DF1A92.tmp.
    -   **Sviluppatori:** È possibile ottenere la cartella temporanea dell'utente corrente usando la funzione API GetTempPath.
-   Per il nome file predefinito iniziale, usare un nome predefinito univoco in base a:
    -   Contenuto del file, se noto. Esempio: le prime parole in un documento.
    -   Modello scelto dall'utente. Esempio: se il file precedente è stato denominato "1.jpg", scegliere "2.jpg" come file successivo.
    -   Modello generico basato sul tipo di file. Esempio: "Photo1.jpg".
-   Per le impostazioni predefinite successive (se il file esiste già), usare la cartella e il nome correnti del file.
-   Quando si salva un file, mantenere la data di creazione. Se il programma salva i file creando un file temporaneo, elimina il file originale e rinomina il file temporaneo con il nome del file originale, assicurarsi di copiare la data di creazione dal file originale.
-   Usare Salva file se l'utente seleziona il comando Salva senza specificare un nome file.

### <a name="file-types-lists"></a>Elenchi di tipi di file

**Nota:** Gli elenchi di tipi di file vengono usati da Apri file e Salva file per determinare i tipi di file visualizzati e l'estensione di file predefinita.

-   Se l'elenco dei tipi di file è breve (cinque o meno), ordinare l'elenco in base alla probabilità di utilizzo. Se l'elenco è lungo (sei o più), usare un ordine alfabetico per semplificare la ricerca dei tipi.
-   Per Salva file includere tutte le varianti delle estensioni di file supportate, anche se non comuni, e inserire prima l'estensione più comune. La logica di gestione dei file esamina questo elenco per determinare se l'utente ha fornito un'estensione di file supportata. Esempio: se un elenco di tipi di file JPEG include solo .jpg e jpeg, il file test.jpe potrebbe essere salvato come test.jpe.jpg.
-   Per Salva file, il tipo di file predefinito iniziale è il più probabilmente scelto dall'utente di destinazione. Il valore predefinito successivo è il tipo corrente del file.
-   Per Apri file, il tipo di file predefinito iniziale è il più probabilmente scelto dall'utente di destinazione. Il valore predefinito successivo deve essere l'ultimo tipo di file usato.
-   Per Apri file, includere una voce "Tutti i file" come primo elemento se gli utenti possono aprire qualsiasi tipo di file o potrebbe essere necessario visualizzare tutti i file in una cartella contemporaneamente. Valutare la possibilità di specificare altri meta filtri, ad esempio "Tutte le immagini", "Tutta la musica" e "Tutti i video". Posizionare questi file immediatamente dopo "Tutti i file".
-   Usare il formato "Nome tipo di file ( \* .ext1; \* . ext2)." Il nome del tipo di file deve essere il nome del tipo di file registrato, che è possibile visualizzare nell'elemento del Pannello di controllo Opzioni cartella. Esempio: "Documento HTML ( \*.htm; \*.html)."
    -   **Eccezione:** Per i meta-filtri, rimuovere l'elenco di estensioni di file per evitare confusione. Esempi: "Tutti i file", "Tutte le immagini", "Tutta la musica" e "Tutti i video".
-   Usare [la combinazione di maiuscole e minuscole](glossary.md) in stile frase per i nomi dei tipi di file e minuscola per le estensioni del tipo di file.

### <a name="open-folder"></a>Apri cartella

-   **Per i nuovi programmi, usare la finestra di dialogo Apri file in modalità "Seleziona cartelle".** Questa operazione richiede Windows Vista o versioni successive, quindi usare la finestra di dialogo Apri cartella per i programmi eseguiti nelle versioni precedenti di Windows.
    -   **Sviluppatori:** È possibile usare la finestra di dialogo Apri file in modalità "Seleziona cartelle" usando il \_ flag FOS PICKFOLDERS.

### <a name="font"></a>Carattere

-   Se necessario, è possibile filtrare l'elenco dei tipi di carattere per visualizzare solo i tipi di carattere disponibili per il programma.

### <a name="persistence"></a>Persistenza

-   È consigliabile rendere persistenti i valori seguenti da usare come impostazioni predefinite successive:
    -   Valori di input (esempi: cartelle predefinite, nomi di file predefiniti).
    -   Opzioni selezionate (esempi: stampante selezionata, opzioni di stampa).
    -   Visualizzazioni (esempi: visualizzazione di immagini nella visualizzazione anteprima, visualizzazione di immagini senza nomi di file, ordinamento per data, larghezza delle colonne).
    -   Presentazione (esempi: dimensioni della finestra, posizione e contenuto).

**Eccezione:** Non rendere questi valori persistenti per le finestre di dialogo comuni quando il loro utilizzo è tale che gli utenti hanno maggiori probabilità di voler ricominciare completamente.

-   Quando si determinano i valori predefiniti, considerare gli utenti di destinazione più probabilmente desiderati in base agli scenari importanti. Considerare anche gli scenari all'interno di un'istanza del programma, tra più istanze (consecutive o simultanee) e tra più documenti. Non rendere persistenti i valori in circostanze che probabilmente non saranno utili.
    -   **Esempio:** Per una tipica applicazione basata su documenti, è utile usare le impostazioni persistenti Apri file e Salva file all'interno di un'istanza del programma e tra istanze consecutive, ma mantenere indipendenti le istanze simultanee. In questo modo, gli utenti possono lavorare in modo efficiente con più documenti contemporaneamente.
-   Rendere persistenti le impostazioni in base al programma e all'utente.

 

