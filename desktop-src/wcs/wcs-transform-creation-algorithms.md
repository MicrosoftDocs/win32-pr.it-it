---
title: Algoritmi di creazione della trasformazione WCS
description: Algoritmi di creazione della trasformazione WCS
ms.assetid: 526bbbfc-fb60-415d-b4f0-6a44a5d11a55
keywords:
- Windows Sistema di colori (WCS), creazione di trasformazioni
- WCS (Windows Color System), creazione di trasformazioni
- gestione del colore delle immagini, creazione di trasformazioni
- gestione dei colori, creazione di trasformazioni
- colori,creazione di trasformazioni
- creazione di trasformazioni
- Creazione della trasformazione WCS
- algoritmi, creazione di trasformazioni
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df199f0fa649e7ce545a7b371f1caba65686746766f5572bac8e43b47413eace
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118445723"
---
# <a name="wcs-transform-creation-algorithms"></a>Algoritmi di creazione della trasformazione WCS

[Creazione di trasformazioni](#creation-of-transforms)

 

[Esecuzione della trasformazione sequenziale](#sequential-transform-execution)

 

[Creazione di trasformazioni ottimizzate](#creation-of-optimized-transforms)

 

[ICCProfileFromWCSProfile](#iccprofilefromwcsprofile)

 

[Conservazione del nero e generazione nera](#black-preservation-and-black-generation)

 

[Controllare Gamut](#checkgamut)

## <a name="creation-of-transforms"></a>Creazione di trasformazioni

Per spiegare correttamente il funzionamento delle trasformazioni di colore, è utile spiegare il percorso di elaborazione completo tramite ICM 2.0 e gli elementi interni della CTE. La ICM 2.0 [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) crea una trasformazione di colore che le applicazioni possono usare per eseguire la gestione del colore. Questa funzione crea un contesto di colore dagli input [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) e finalità. Le finalità vengono mappate all'algoritmo di mapping della gamma ICC di base correlato. La funzione chiama quindi ICM 2.0 [**CreateMultiProfileTransform per**](/windows/desktop/api/Wingdi/) un'elaborazione dei colori coerente. La **funzione CreateColorTransform** copia in genere i dati nella struttura di trasformazione ottimizzata interna.

La funzione ICM 2.0 CreateMultiProfileTransform accetta una matrice di profili e una matrice di finalità o un singolo profilo di collegamento del dispositivo e crea una trasformazione colore che le applicazioni possono usare per eseguire il mapping dei colori. Elabora i profili di input e le finalità per creare modelli di dispositivo, modelli di aspetto dei colori, descrizioni dei limiti di gamut e modelli di mapping di gamut. Ecco come eseguire questa operazione:

-   I modelli di dispositivo vengono inizializzati direttamente dai profili DM. Nella chiamata a [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/)è stato creato un modello di dispositivo per ogni profilo.
-   I modelli di aspetto dei colori vengono inizializzati direttamente dai profili CAM. Nella chiamata a [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/)è presente un profilo CAM per ogni profilo. È tuttavia possibile specificare lo stesso profilo CAM per più di un profilo.
-   Le descrizioni dei limiti gamut vengono inizializzate da un oggetto modello di dispositivo e da un oggetto CAM. Nella chiamata a [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/)è presente una descrizione del limite gamut per ogni profilo.
-   I modelli di mapping gamut vengono inizializzati da due limiti di gamut e da una finalità. È necessario creare un modello di mapping gamut tra ogni coppia di modelli di dispositivo creati dalla chiamata a [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/). Si noti che ciò significa che si usa un modello di mappa gamut in meno rispetto al modello di dispositivo. Poiché il numero di finalità corrisponde al numero di modelli di dispositivo, esiste anche una finalità in più del necessario. La prima finalità nell'elenco viene ignorata. Viene descritto l'elenco dei modelli di dispositivo e delle finalità, creando modelli di mapping gamut. Selezionare il primo e il secondo modello di dispositivo e la seconda finalità, quindi inizializzare il primo modello di mapping gamut. Selezionare il secondo e il terzo modello di dispositivo e la terza finalità e quindi inizializzare il secondo modello di mapping di gamut. Continuare in questo modo fino a quando non sono stati creati tutti i modelli di mapping gamut.

Quando i profili sono stati elaborati correttamente e tutti gli oggetti intermedi sono stati creati e inizializzati, è possibile creare la trasformazione CITE con la chiamata seguente. *PDestCAM* e *pDestDM* sono quelli associati all'ultimo profilo nella chiamata a [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/).


```C++
HRESULT CreateCITEColorTransform(
 __inout     IDeviceModel          *pSourceDM,
 __inout     IColorAppearanceModel *pSourceCAM,
 __in        GamutMapArray         *pGamutMapArray,
 __inout     IColorAppearanceModel *pDestCAM,
 __inout     IDeviceModel          *pDestDM,
             EColorTransformMode    eTransformMode,
 __deref_out IColorTransform      **ppCTS
 );
```



## <a name="support-for-plug-ins"></a>Supporto per i plug-in

Un problema relativo alla configurazione dell'elenco di trasformazioni è la convalida della disponibilità di un plug-in necessario. L'opzione di modello seguente fornisce questo criterio per controllare questo comportamento. La gestione di questo elenco di trasformazioni è un metodo nella struttura di trasformazione ottimizzata interna, ma ogni metodo del modello fornisce il puntatore a se stesso e al proprio set di valori di parametro.

La modalità deve essere una delle seguenti.

-   TfmRobust: se un profilo di misurazione specifica un plug-in preferito e il plug-in non è disponibile, il nuovo sistema CTE userà il plug-in di base. Se nessuno dei plug-in è disponibile, la trasformazione segnala un errore.
-   TfmStrict: se ColorContext specifica un plug-in preferito, il plug-in deve essere disponibile. Se non viene trovato alcun plug-in preferito, verrà usato il plug-in di base. Se nessuno dei plug-in è disponibile, la trasformazione segnala un errore.
-   TfmBaseline: in AddMeasurementStep è possibile usare solo plug-in di base. Se ColorContext specifica un plug-in preferito, il plug-in verrà ignorato. Se il plug-in di base non è disponibile, la trasformazione segnala un errore.

## <a name="transform-execution"></a>Esecuzione della trasformazione

La ICM funzione [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) dell'API 2.0 converte una [](c.md) matrice di colori dallo spazio colori di origine allo spazio colori di destinazione, come definito da una trasformazione di colore. Questa funzione controlla internamente una matrice di colori memorizzati nella cache per abilitare la corrispondenza immediata dei colori trasformati comunemente. Questa trasformazione supporta matrici di byte a 8 bit per canale e matrici float a 32 bit per canale. Tutti gli altri formati verranno convertiti prima di passare alla nuova CTE.

La ICM funzione [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) dell'API 2.0 converte i colori di una bitmap con un formato definito per produrre un'altra bitmap in un formato richiesto. Questa funzione controlla internamente una matrice di colori memorizzati nella cache per abilitare la corrispondenza immediata dei colori trasformati comunemente. Per evitare troppi percorsi di codice, supporto e test della complessità, nel motore di trasformazione e interpolazione è effettivamente supportato solo un numero limitato di formati bitmap. Questa funzione deve convertire i formati bitmap in ingresso e in uscita non nativi in formati supportati in modo nativo per l'elaborazione. Questa trasformazione supporta solo bitmap a 8 bit per byte per canale e bitmap float a 32 bit per canale. Tutti gli altri formati verranno convertiti prima di passare alla nuova CTE.

 

### <a name="sequential-transform-execution"></a>Esecuzione della trasformazione sequenziale

Se il parametro *dwFlags* ha il bit SEQUENTIAL TRANSFORM impostato quando vengono chiamate le funzioni \_ ICM [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) o **CreateMultiProfileTransform,** i passaggi di trasformazione vengono eseguiti in sequenza. Ciò significa che il codice passa separatamente ogni modello di dispositivo, modello di aspetto del colore e modello di mapping gamut, come specificato dalla chiamata **a CreateColorTransform** o **CreateMultiProfileTransform.** Questo può essere utile per il debug di moduli plug-in, ma è molto più lento rispetto all'esecuzione tramite una trasformazione ottimizzata. L'esecuzione in modalità sequenziale non è pertanto consigliata per il software di produzione. Inoltre, possono esserci lievi differenze nei risultati ottenuti in modalità sequenziale e in modalità ottimizzata. Ciò è dovuto alle variazioni introdotte quando le funzioni vengono concatenate insieme.

### <a name="creation-of-optimized-transforms"></a>Creazione di trasformazioni ottimizzate

Una trasformazione ottimizzata è una tabella di ricerca multidimensionale. La tabella può essere elaborata da un motore di interpolazione multidimensionale, ad esempio l'interpolazione tetraedrale, che applica i colori di input alla trasformazione. La sezione seguente descrive come vengono create le tabelle di ricerca ottimizzate. La sezione successiva descrive come eseguire l'interpolazione all'interno delle tabelle di ricerca ottimizzate.

## <a name="sparse-lookup-tables"></a>Tabelle di ricerca di tipo sparse

Le stampanti convenzionali dispongono di inks CMYK. Per estendere la gamma, un approccio consiste nell'aggiungere nuovi inks al sistema. Gli inks aggiunti in genere sono colori con difficoltà di riproduzione degli inks CMYK. Le opzioni comuni sono arancione, verde, rosso, blu e così via. Per aumentare la "risoluzione apparente", è possibile usare inks con tinte diverse, ad esempio ciano chiaro, magenta chiaro e così via. In effetti, il dispositivo della stampante ha più di quattro canali.

Anche se le stampanti sono dispositivi di output, eseguono anche la conversione del colore dallo spazio del dispositivo a un altro spazio colore. Nel caso di una stampante CMYK, si tratta di una trasformazione da CMYK a XYZ o del "modello di inoltro" della stampante. Combinando il modello in avanti con altre trasformazioni, è possibile emulare una stampa CMYK su un altro dispositivo. Ad esempio, una stampante CMYK su un monitor RGB rende possibile un meccanismo di correzione che emula una stampa della stampante CMYK su un monitor. Analogamente, lo stesso vale anche per le stampanti hi-fi. Una conversione da CMYKOG a RGB consente la verifica della stampante CMYKOG su un monitor.

L'approccio convenzionale all'implementazione di questa conversione del colore consiste nell'usare un LUT uniforme. Ad esempio, in un profilo ICC per una stampante CMYKOG, la specifica ICC impone un tag A2B1 che archivia un LUT uniforme che rappresenta un campionamento uniforme nello spazio del dispositivo CMYKOG del modello di inoltro, che passa da CMYKOG allo spazio di connessione del profilo ICC (CIELAB o CIEXYZ). Il profilo di collegamento del dispositivo ICC consente una trasformazione diretta dallo spazio del dispositivo CMYKOG a qualsiasi spazio colore, incluso uno spazio del dispositivo, anche sotto forma di LUT campionato in modo uniforme nello spazio CMYKOG. Il campionamento non viene mai eseguito con 256 livelli (profondità in bit 8) a causa dell'enorme LUT risultante, tranne nel caso di dispositivi monocromatici (1 canale). Viene invece usato il campionamento con una profondità in bit inferiore. alcune scelte tipiche sono 9 (profondità bit 3), 17 (profondità bit 4), 33 (profondità bit 5). Con il numero di livelli inferiore a 256 in ogni canale, l'LUT viene usato insieme a un algoritmo di interpolazione per produrre il risultato se un livello è compreso tra due livelli campionati.

Sebbene un LUT uniforme sia concettualmente semplice da implementare e l'interpolazione su un LUT uniforme sia generalmente efficiente, le dimensioni dell'LUT aumentano in modo esponenziale con la dimensione di input. Infatti, se *d* è il numero di passaggi usati nell'LUT uniforme e *n* è il numero di canali nello spazio colore di origine, il numero di nodi in LUT è Mostra la variabile per il numero di nodi in un ![ LUT. ](images/transformcreation-image002.gif) . Ovviamente, il numero di nodi richiede rapidamente una quantità così elevata di spazio di archiviazione in memoria che anche i sistemi di elaborazione top-of-the-line hanno difficoltà a gestire la domanda. Per i dispositivi con sei o otto canali, un'implementazione ICC del profilo di dispositivo richiede l'uso di pochi passaggi nell'unità LUT, talvolta anche fino a cinque passaggi nella tabella A2B1 per mantenere il profilo entro megabyte anziché gigabyte. Ovviamente, l'uso di un numero minore di passaggi aumenta l'errore di interpolazione, perché ora sono presenti meno campioni. Poiché l'unità LUT deve essere uniforme, l'accuratezza dell'intero spazio colori risulta ridotta anche nelle aree dello spazio in cui una differenza di colore significativa può essere causata da una piccola modifica del valore del dispositivo.

Nei dispositivi con più di quattro coloranti, alcuni sottospazio dell'intero spazio del dispositivo sono più importanti di altri. Ad esempio, nello spazio CMYKOG gli inks ciano e verde vengono raramente usati insieme perché le tonalità si sovrappongono in gran parte. Analogamente, gli inks gialli e arancioni si sovrappongono in gran parte. Una riduzione uniforme del numero di passaggi può essere considerata come una riduzione complessiva della qualità nell'intero spazio colore, che è qualcosa che è possibile permettersi per le combinazioni di input penna improbabili, ma non per le combinazioni probabili o importanti.

Mentre un LUT campionato in modo uniforme è semplice ed efficiente per l'interpolazione, impone requisiti di memoria enormi con l'aumento delle dimensioni. In realtà, mentre un dispositivo può avere sei o otto canali, vengono usati raramente contemporaneamente. Nella maggior parte dei casi, la trasformazione dal colore di input al colore ha solo alcune coloranti "attive" e quindi risiede in uno spazio colore dimensionale inferiore. Ciò significa anche che l'interpolazione può essere eseguita in modo più efficiente in tale spazio dimensionale inferiore, perché l'interpolazione è più veloce quando la dimensione è inferiore.

Pertanto, l'approccio consiste nel stratificare l'intero spazio del dispositivo in sottospazio di varie dimensioni. E poiché le dimensioni inferiori (quelle che combinano tre o quattro coloranti) sono più importanti, la stratificazione dello spazio consente anche di applicare frequenze di campionamento diverse. ad esempio un numero diverso di passaggi. aumentando le frequenze di campionamento per dimensioni inferiori, riducendole per dimensioni più elevate.

Per correggere le notazioni, *n* è il numero di canali nello spazio colore di origine della trasformazione colore da campionare. È anche possibile fare riferimento a *n* come dimensione di input e ![ Mostra n maggiore o uguale a 5.](images/transformcreation-image004.gif) , se non diversamente specificato.

I blocchi predefiniti di base sono LUT di diverse dimensioni *e* dimensioni di input, anziché un LUT uniforme con dimensione di input *n*. Per maggiore precisione, un *LUT* è un reticolo rettangolare imposto a un cubo unità; ciò significa che tutte le coordinate del dispositivo vengono normalizzate nell'intervallo \[ 0, 1 \] ). se è la dimensione di input del lut (si noti che non deve essere uguale a *n*, anche se ![ mostra V minore o uguale a n.](images/transformcreation-image006.gif) è obbligatorio), quindi è costituito da griglie di campionamento unidimensionali:

Samp *i:* mostra ![ una griglia di campionamento unidimensionale.](images/transformcreation-image008.gif)

dove tutte *le x <sub>j</sub>s devono* essere nell'intervallo \[ 0, 1 \] , mostra un ![ apice d(i).](images/transformcreation-image010.gif) è il numero di passaggi per il campionamento del canale *i* che deve essere almeno 1 e Mostra uno ![ spuperscript di X (indice) d(i).](images/transformcreation-image012.gif) deve essere 1. D'altra parte, ![ mostra un apice X (pedice 1).](images/transformcreation-image014.gif) non deve essere 0.

Verranno definiti solo i due casi speciali seguenti di LUT.

*LUT chiuso:* si tratta di un LUT con il requisito aggiuntivo che per ogni Samp *<sub>i</sub>* mostra un apice ![ X (pedice 1) uguale a 0.](images/transformcreation-image016.gif) e ![ Visualizza un apice d(i) maggiore o uguale a 2.](images/transformcreation-image018.gif) . Un LUT chiuso uniforme è un LUT chiuso con lo stesso valore ![ di Shows a superscript d(i).](images/transformcreation-image010.gif) per ogni canale e i nodi sono divisi in modo uniforme tra 0 e 1.

*Open LUT:* si tratta di un LUT con il requisito aggiuntivo che per ogni Samp *i*, mostra un apice ![ X (pedice 1) maggiore di 0.](images/transformcreation-image020.gif) . È possibile che Mostra ![ un apice d(i) sia uguale a 1.](images/transformcreation-image022.gif) .

L'obiettivo è quello di stratificare il cubo unità 0, 1 n in una raccolta di LUN chiusi e LUT aperti, in modo che l'intera raccolta copre il cubo \[ \]  unità. Dal punto di vista concettuale, è più semplice organizzare questi "livelli LUT" in base alle relative dimensioni, in modo che al livello superiore:

![Mostra il livello superiore per l'organizzazione degli livelli L U T in base alle relative dimensioni.](images/transformcreation-image024.png)

where ![ Shows sigma subscript k.](images/transformcreation-image026.gif) è la *"k-dimensional* strata collection". Si noti che la dimensione degli strato inizia da 3 anziché da 0; ciò significa che i punti, perché l'interpolazione di combinazioni a tre colori può essere gestita senza un requisito di memoria troppo grande.

## <a name="description-of-the-lut-strata"></a>Descrizione dello strato LUT

In questa implementazione:

1. ![Mostra l'indice sigma 3.](images/transformcreation-image028.gif) è costituito da LUT chiusi con tre input, uno da ogni possibile combinazione di tre coloranti scelti tra *n* coloranti.

2. ![Mostra l'indice sigma 4.](images/transformcreation-image030.gif) è costituito da un LUT chiuso per la combinazione CMYK (o le prime quattro coloranti), insieme a ![Mostra (n su 4) meno 1.](images/transformcreation-image032.png) aprire LUN per tutte le altre combinazioni a quattro colori. Se si specifica la combinazione CMYK, si riconosce che si tratta di una combinazione importante.

3. Per ![ Mostra k uguale a 5, ..., n.](images/transformcreation-image034.gif) , ![ mostra sigma subscript k.](images/transformcreation-image026.gif) è costituito ![ da Shows (n over k).](images/transformcreation-image037.gif) LUT aperti, uno per ogni possibile combinazione di *k* coloranti dal totale di *n* coloranti.

Rimane da specificare le dimensioni dei LUN. La differenza principale tra LUN aperti e chiusi è che i LUN aperti non si sovrappongono e i LUN chiusi potrebbero sovrapporsi ai visi limite. Il fatto che il campionamento unidimensionale in un LUT aperto non contenga 0, significa essenzialmente che in un LUT aperto manca metà dei visi limite, da qui il nome "open". Se due LUN non si sovrappongono, è possibile usare un numero diverso di passaggi o posizioni dei nodi in ogni canale. Lo stesso non vale se due LUN si sovrappongono. In tal caso, se il numero di passaggi o le posizioni dei nodi sono diversi, un punto che si trova nell'intersezione dei due LUT riceverà un valore di interpolazione diverso a seconda del valore LUT usato nell'interpolazione. Una soluzione semplice a questo problema consiste nell'usare il campionamento uniforme con lo stesso numero di passaggi ogni volta che due LUN si sovrappongono. In altre parole:

Tutti i LUT chiusi (tutti i LUT a tre colori e l'LUT CMYK in questa implementazione) devono essere uniformi e avere lo stesso numero di passaggi, indicati *come d*.

I due algoritmi seguenti possono essere usati per determinare il numero di passaggi *d* per i LUN chiusi e il numero di passaggi per i LUN aperti.

## <a name="algorithm-1"></a>Algoritmo \# 1

Questo algoritmo non richiede input esterno.

Tutti i LUN chiusi saranno uniformi con *d* numero di passaggi.

Tutti i LUN aperti della dimensione *k* avranno lo stesso numero di passaggi ![ Mostra d(k).](images/transformcreation-image039.gif) in ogni canale di input e i nodi sono equidiquamente separati; ciò significa che per ogni ![ mostra i uguale a 1, 2, ..., k.](images/transformcreation-image041.gif) .

Samp *i:* mostra ![ l'algoritmo samp i.](images/transformcreation-image043.png)

Infine, specificare *d* e *d* (*k* ) nella tabella 1 seguente. Le tre modalità, "prova", "normale" e "migliore", sono le ICM di qualità 2.0. In questa implementazione, la modalità di prova ha il footprint di memoria più piccolo e la modalità migliore ha il footprint di memoria più grande.

Per implementare questo algoritmo, è necessario chiamare l'algoritmo \# 2 seguente. Gli utenti possono specificare le proprie posizioni di campionamento, usando le tabelle come guida.

## <a name="algorithm-2"></a>Algoritmo \# 2

Questo algoritmo richiede un input esterno sotto forma di un elenco di posizioni di campionamento "importanti", ma è più adattivo e può potenzialmente risparmiare spazio di memoria.

L'input richiesto è una matrice di valori di dispositivo forniti dall'utente. Questi valori del dispositivo indicano quale area dello spazio colore del dispositivo è importante; ovvero quale area deve essere campionata di più.

Tutti i LUN chiusi saranno uniformi con *d* numero di passaggi, come descritto in Algoritmo \# 1. I valori *per d* sono specificati nella tabella 1.

*(a) Uniform Closed LUT*



|         | Modalità di prova | Modalità normale | Modalità migliore |
|---------|------------|-------------|-----------|
| ***d*** | 9          | 17          | 33        |



 

*(b) Open LUT*



| Dimensione di input | Modalità di prova | Modalità normale | Modalità migliore |
|-----------------|------------|-------------|-----------|
| 4               | 5          | 7           | 9         |
| 5               | 2          | 3           | 3         |
| 6               | 2          | 3           | 3         |
| 7               | 2          | 2           | 2         |
| 8 o più       | 2          | 2           | 2         |



 

**Tabella 1:** Dimensioni LUT usate nell'algoritmo

Ogni unità LUT aperta può avere un numero diverso di passaggi in ogni canale di input e le posizioni di campionamento non devono essere dissodati allo stesso modo. Per un determinato strato LUT aperto, è presente una combinazione colorante associata, ad esempio, Mostra pedice ![ C 1, ..., C peddice k.](images/transformcreation-image045.gif) , dove mostra ![ il pedice C i.](images/transformcreation-image047.gif) s sono numeri interi distinti compresi tra 1 e *n*. Sono gli indici del canale corrispondenti alle coloranti "attive" in questo strato.

PASSAGGIO 1: Filtrare la matrice di valori del dispositivo immessa che non sono contenuti in questo livello. Un valore del ![ dispositivo mostra X pedice 1, X pedice 2, ..., X pedice n.](images/transformcreation-image049.gif) è contenuto negli strati, se e solo se ![ mostra un set di valori per un canale.](images/transformcreation-image051.gif) e tutti gli altri canali sono 0. Se il set filtrato contiene *N* voci, lasciare

![Mostra un'equazione da usare se il set filtrato contiene N voci.](images/transformcreation-image053.png)

Per ogni ![Mostra i uguale a 1, 2, ..., k.](images/transformcreation-image041.gif) , eseguire l'iterazione dei passaggi seguenti da 2 a 5:

PASSAGGIO 2: se ![ mostra d pscript tentative (k) uguale a 1.](images/transformcreation-image055.gif) , Samp *i* ha solo 1 punto, che deve essere 1.0. Passare al successivo *i*. In caso contrario, continuare con IL PASSAGGIO 3.

PASSAGGIO 3: Ordinare gli esempi filtrati in ordine crescente nel ![Mostra il pedice C i.](images/transformcreation-image047.gif) channel.

PASSAGGIO 4: Definire la griglia di campionamento "provvisoria" usando i nodi

![Mostra i nodi usati per definire la griglia di campionamento "provvisoria".](images/transformcreation-image057.png)

dove ![Mostra j uguale a 1, 2, ..., d pscript tentative (k).](images/transformcreation-image059.gif) .

PASSAGGIO 5: Regolarizzare la griglia provvisoria per assicurarsi che sia conforme alla rigida monotonicità e che termini anche con la versione 1.0. Poiché la matrice è già ordinata, i nodi nella griglia provvisoria non sono già monotonici. Tuttavia, i nodi adiacenti potrebbero essere identici. È possibile risolvere questo problema rimuovendo nodi identici, se necessario. Infine, dopo questa procedura, se l'end point è minore di 1.0, sostituirlo con 1.0.

Si noti che il passaggio 5 è il motivo per cui gli strata LUT possono avere un numero diverso di passaggi in ogni canale. Dopo la regolarizzazione, il numero di passaggi in un canale può essere minore di ![Mostra d pscript tentative (k).](images/transformcreation-image061.gif) .

## <a name="interpolation"></a>Interpolazione

È possibile costruire la stratificazione del cubo unità aprire gli stratamenti LUT e chiudere gli strati LUT. Per eseguire l'interpolazione usando questa "struttura LUT di tipo sparse", seguire questa procedura. Presupporre un determinato valore del dispositivo di input ![Mostra (X pedice 1, X pedice 2, ..., X pedice n).](images/transformcreation-image049.gif) .

PASSAGGIO 1: Determinare il numero di canali "attivi". Questo è il numero di canali diversi da zero. In questo modo si determina la dimensione *k* degli strata per la ricerca dello strato contenitore. Più precisamente, la dimensione strata è 3 se il numero di canali attivi è Mostra minore o ![ uguale a 3.](images/transformcreation-image063.gif) in caso contrario, la dimensione strata è uguale al numero di canali attivi.

PASSAGGIO 2: Entro ![Mostra sigma subscript k.](images/transformcreation-image026.gif) , cercare lo strato contenitore. Un valore del dispositivo è contenuto in uno strato aperto se tutti i canali corrispondenti allo strato hanno un valore diverso da zero e tutti gli altri canali sono pari a zero. Un valore del dispositivo è contenuto in uno strato chiuso se ogni canale non rappresentato dallo strato è zero. Se non viene trovato alcun strato contenitore, è presente una condizione di errore. Annullare e segnalare l'errore. Se viene trovato uno strato contenitore, procedere al passaggio successivo.

PASSAGGIO 3: se lo strato contenitore è chiuso, l'interpolazione all'interno dello strato può essere eseguita da qualsiasi algoritmo di interpolazione noto. In questa implementazione, la scelta dell'algoritmo è l'interpolazione tetraedrale. Se lo strato contenitore è aperto e il valore del dispositivo si trova esclusivamente all'interno dello strato,

![Mostra X pedice i maggiore o uguale a... ](images/transformcreation-image065.gif) primo nodo nel *canale i*

dove *i* è un indice di canale per lo strato, funziona l'algoritmo di interpolazione standard, ad esempio l'interpolazione tetraedrale.

Se mostra X pedice i less than... primo nodo in i th channel per alcuni i , il valore del dispositivo rientra nel "gap" tra lo strato e i sottospazio ![ ](images/transformcreation-image067.gif) dimensionali inferiori.   Questo moi non è interessato da un algoritmo di interpolazione per se stesso, quindi qualsiasi algoritmo di interpolazione può essere usato per eseguire l'interpolazione all'interno di questo "gap", anche se l'algoritmo preferito è l'interpolazione transfinita seguente.

L'architettura del modulo di interpolazione è illustrata nelle due parti della figura 1.

![Diagramma che illustra la prima parte dell'architettura del modulo di interpolazione.](images/transformcreation-image068.png)

![Diagramma che illustra la seconda parte dell'architettura del modulo di interpolazione.](images/transformcreation-image070.png)

**Figura 1:** Architettura del modulo di intepolazione

Come spiegato in precedenza, questo algoritmo è in grado di ottenere campionamento ragionevolmente denso nelle aree dello spazio del dispositivo che contengono una combinazione importante di coloranti, riducendo al minimo le dimensioni totali delle unità di misura necessarie. La tabella seguente illustra un confronto tra il numero di nodi necessari per l'implementazione LUT di tipo sparse (usando l'algoritmo 1 e la modalità normale) e l'implementazione \# LUT uniforme corrispondente.



| **Numero di canali di input** | **Sparse LUT** | **Uniform LUT** |
|------------------------------|----------------|-----------------|
| 5                            | 142498         | 1419857         |
| 6                            | 217582         | 24137567        |
| 7                            | 347444         | 410338673       |
| 8                            | 559618         | 6975757441      |



 

## <a name="interpolation-within-a-unit-cube"></a>Interpolazione all'interno di un cubo unità

Un passaggio di base nel caso di griglia rettangolare è l'interpolazione all'interno di una cella di inclusione. Per un punto di input, è possibile determinare facilmente la cella di inclusione. In una griglia rettangolare viene specificato il valore di output in ogni vertice (punti angolo) della cella che lo contiene. Sono anche le uniche condizioni limite che un interpolante deve soddisfare: l'interpolante deve passare attraverso tutti questi punti. Si noti che queste condizioni limite sono su punti "discreti", in questo caso i punti angolo 2n della cella, dove n è la dimensione dello spazio colore.

È utile formalizzare il concetto di condizioni limite prima di procedere. Per qualsiasi subset S del limite della cella contenitore (cubo unità in n dimensioni), una condizione limite in S è una specifica di una funzione BC: S → Rm, dove m è la dimensione di output. In altre parole, è necessario un interpolante, che può essere definito Interp: \[ 0,1 \] n→ Rm, per soddisfare: Interp(x) = BC(x) per tutte le x in S.

Nello scenario standard di interpolazione sul cubo unità, S è il set di punti discreti che rappresentano i vertici 2n del cubo.

È ora possibile generalizzare le condizioni limite per risolvere i problemi descritti in precedenza e fornire un nuovo algoritmo di interpolazione all'interno del cubo unità. Anziché consentire solo punti limite discreti, è possibile imporre condizioni di limite a un'intera faccia limite del cubo. I presupposti precisi sono i seguenti:

(a) Il punto vn =(1,1,...,1) è speciale ed è consentita solo una condizione di limite discreta. In altre parole, non è possibile imporre condizioni di limite continue ai n visi limite xi=1 (i=1,...,n).

(b) Per ognuno dei restanti n visi limite xi=0 (i=1,...,n), la condizione limite può essere imposta sull'intero viso, con la condizione di compatibilità che se due visi si intersecano, le condizioni limite sui visi devono essere concordate sull'intersezione.

(c) Tutti i vertici non contenuti nei visi con condizione limite avranno una condizione di limite singola (discreta).

È possibile fare riferimento a una condizione di limite discreta come dati finiti e a una condizione di limite continuo come dati transfiniti nel discutere l'interpolazione sui dati finiti e transfiniti.

Esaminare prima di tutto l'interpolazione tetraedrale standard (ad esempio quella usata nel brevetto di Sakamoto) che consente di impostare le notazioni per questa particolare formulazione del problema. È noto che il cubo unità \[ 0,1 \] n può essere suddiviso in n! tetrahedra, parametrizzata dal set di permutazioni su n simboli. In particolare, ogni tetraedro di questo tipo è definito da disuguaglianze

![Mostra la formula per le disuguaglianze dei tetraedri.](images/transformcreation-image073.gif)

dove σ:{1,2,..,n}→{1,2,...,n} è una permutazione di "simboli" 1, 2, ..., n, cio è un mapping bijective del set di n simboli. Ad esempio, se n = 3 e σ = (3, 2, 1), ovvero σ(1)=3, σ(2)=2, σ(3)=1, il tetraedro corrispondente viene definito da z≥y≥x, dove la notazione comune x, y, z viene usata per x1, x2, x3. Si noti che questi tetraedri non sono disgiunti l'uno dall'altro. Ai fini dell'interpolazione, i punti che si trovano su una faccia comune di due tetraedri distinti avranno lo stesso valore di interpolazione indipendentemente dal tetraedro usato nell'interpolazione. Tuttavia, nello scenario standard di interpolazione su punti finiti, per un determinato punto di input (x1, ..., xn), determinare prima in quale tetrahedro si trova o, in modo equivalente, il σ di permutazione corrispondente, quindi l'interpolante tetraedrale viene definito come

![Mostra l'equazione che definisce l'interpolante tetraedrale.](images/transformcreation-image075.png)

dove ![Mostra l'equazione per i vettori di base standard.](images/transformcreation-image077.png) per i=1, ..., n ed e1, ..., en sono i vettori di base standard. Prima di passare alla generalizzazione, si noti che v0, v1, ..., vn sono i vertici del tetraedro e ![Mostra le coordinate barycentriche.](images/transformcreation-image079.png) sono le "coordinate barycentriche".

Per il caso generale dei BC sui visi limite, è possibile usare il concetto di proiezione barycentrica. Come prima, per un determinato punto di input (x1, ..., xn), determinare prima in quale tetrahedron si trova o, in modo equivalente, la permutazione corrispondente σ. Eseguire quindi una serie di proiezioni barycentriche, come indicato di seguito. La prima proiezione ![Visualizza il pedice BProj 1 (x).](images/transformcreation-image081.gif) invia il punto al piano ![Mostra X peddice delta (1) uguale a 0.](images/transformcreation-image083.gif) a meno che ![Mostra X uguale a V pscript n.](images/transformcreation-image085.gif) nel qual caso non viene modificato. La definizione precisa della mappa BProj è definita come segue:

![Mostra l'equazione per la definizione precisa della mappa BProj.](images/transformcreation-image087.png)

con ![Mostra l'equazione per P pscript k.](images/transformcreation-image089.png) e k = 1, 2, ..., n.

Nel caso in cui ![Mostra che X è uguale a V pscript n.](images/transformcreation-image085.gif) , è possibile arrestare perché BC è definito in vn da Assumption (a). Nel caso in cui ![Mostra che X non è uguale a V pscript n.](images/transformcreation-image091.gif) , è chiaro che ![Visualizza il pedice BProj 1 (X).](images/transformcreation-image081.gif) ha il σ(1)esimo componente annichilito. In altre parole, si trova su uno dei visi limite. Si trova su un viso su cui è definito BC, nel qual caso è possibile arrestarsi oppure si esegue un'altra proiezione barycentrica ![Mostra il pedice BProj 2 (X').](images/transformcreation-image093.gif) dove ![Mostra X' uguale a BProj pscript 1 (X).](images/transformcreation-image095.gif) . E se ![Mostra X''= Pedice Bproj 1 (X').](images/transformcreation-image097.gif) è su un viso su cui è definito BC, è possibile arrestare; in caso contrario, eseguire un'altra proiezione ![Mostra il pedice BProj 3 (X').](images/transformcreation-image099.gif) . Poiché ogni proiezione annienta un componente, la dimensione effettiva diminuisce, quindi è necessario arrestare il processo. Nello scenario peggiore, si eseguono n proiezioni fino alla dimensione 0, ovvero i vertici del cubo, in base al presupposto (c), in base al quale verrà definito BC.

Supponendo che siano state eseguite proiezioni K, con

![Mostra un'equazione da usare presupponendo che sia stata eseguita la proiezione K.](images/transformcreation-image101.png)

x(0)= x, il punto di input e BC sono definiti in x(k). Rimuovere quindi le proiezioni definendo una serie di vettori di output:

![Mostra le equazioni per una serie di vettori di output.](images/transformcreation-image103.png)

dove ![Mostra l'equazione per apice Y (K).](images/transformcreation-image105.gif) e si ottiene infine la risposta

![Mostra Interp(x) uguale a y apice (0).](images/transformcreation-image107.gif)

## <a name="worked-example"></a>Esempio lavorato

![Diagramma che mostra un esempio di interpolazione con un cubo unità.](images/transformcreation-image108.png)

**Figura 2:** Esempio di lavoro

Si consideri la situazione illustrata nella figura 2, dove n = 3, m = 1 e si dispone dei seguenti BC:

(a) Quattro BC discreti sui vertici

(0, 0, 1): β001

(0, 1, 1): β011

(1, 0, 1): β101

(1, 1, 1): β111

(b) Bc continuo sul viso x3=0: F(x1, x2)

Calcolo \# 1: punto di input x = (0,8, 0,5, 0,2). Il tetraedro contenitore è associato alla permutazione &lt; 1, 2, &gt; 3.

Prima proiezione: ![Mostra l'equazione per la prima proiezione.](images/transformcreation-image110.png)

Questo è già sul viso x3=0, quindi è possibile arrestarsi. La sostituzione all'indietro offre quindi

![Mostra la risposta per la prima proiezione.](images/transformcreation-image112.png) che è la risposta.

Calcolo \# 2: punto di input x = (0,2, 0,5, 0,8). Il tetraedro contenitore è associato alla permutazione &lt; 3, 2, &gt; 1.

Prima proiezione: ![Mostra l'equazione per la prima proiezione del calcolo 2.](images/transformcreation-image113.png)

Seconda proiezione: ![Mostra l'equazione per la seconda proiezione del calcolo 2.](images/transformcreation-image115.png)

Terza proiezione: ![Mostra l'equazione per la terza proiezione del calcolo 2.](images/transformcreation-image117.png) , che si trova sul viso x3=0. La sostituzione all'indietro offre quindi

![Mostra le prime due equazioni per la sostituzione all'indietro.](images/transformcreation-image119.png)

![Mostra la terza equazione per la sostituzione con le versioni precedenti.](images/transformcreation-image123.png), che è la risposta finale.

## <a name="applications"></a>Applicazioni

*(a) Interpolazione tetrahedrale sequenziale*

![Diagramma che mostra l'interpolazione tetrahedre sequenziale.](images/transformcreation-image124.png)

**Figura 3:** Interpolazione tetraedrale sequenziale

Vedere la figura 3. Per eseguire l'interpolazione tra due piani su cui sono state imposte griglie incompatibili, prendere in considerazione una cella che racchiude un determinato punto P mostrato nella figura. I vertici "superiori" della cella provengono direttamente dalla griglia nel piano superiore. I vertici nella faccia inferiore non sono compatibili con la griglia nel piano inferiore, quindi l'intero viso viene considerato come un BC con valori ottenuti dall'interpolazione sulla griglia nel piano inferiore. È quindi chiaro che questa configurazione soddisfa i presupposti (a), (b) e (c) precedenti ed è possibile applicare l'algoritmo di interpolazione.

È anche chiaro che l'algoritmo ha ridotto di 1 la dimensione del problema di interpolazione, perché il risultato è una combinazione lineare di valori ai vertici nella griglia superiore e l'interpolazione nel piano inferiore, con dimensione minore di 1. Se nel piano inferiore esiste una configurazione simile del piano di sandwiching, è possibile applicare la procedura in tale piano, riducendo ulteriormente la dimensione di 1. Questa procedura può continuare fino a raggiungere la dimensione 0. Questa catena di proiezioni e interpolazioni può essere chiamata "interpolazione tetrahedrale sequenziale".

*(b) Interpolazione di gap*

![Diagramma che mostra l'interpolazione di gap.](images/transformcreation-image126.jpg)

**Figura 4:** Interpolazione gap

Si tratta di una griglia imposta su un cubo che si trova rigorosamente all'interno del quadrante positivo. Il cubo stesso contiene una griglia e ogni piano delle coordinate ha griglie che non sono necessariamente compatibili. Lo "spazio" tra il cubo e i piani delle coordinate ha una sezione incrociata a "forma di L" e non è utilizzabile con le tecniche standard. Tuttavia, con la tecnica introdotta qui, è possibile introdurre facilmente celle che coprono questo gap. La figura 4 illustra uno di questi elementi. Le griglie sui piani delle coordinate supportano l'interpolazione che fornisce i BC necessari per tutte le visi inferiori della cella, con un vertice rimanente il cui BC viene fornito dall'angolo inferiore del cubo.

## <a name="final-note-on-implementation"></a>Nota finale sull'implementazione

Nell'applicazione effettiva, il "cubo unità" che rappresenta l'impostazione di base dell'algoritmo viene estratto da lattici più grandi e i valori ai vertici possono richiedere un calcolo costoso. D'altra parte, è anche chiaro che l'interpolazione tetrahedrale richiede solo i valori ai vertici della tetrahedron, che è un subset di tutti i vertici del cubo unità. Pertanto, è più efficiente implementare quella che può essere chiamata "valutazione posticipata". In un'implementazione software dell'algoritmo precedente è in genere presente una subroutine che accetta come input il cubo unità e i valori ai vertici. La valutazione posticipata significa che invece di passare i valori ai vertici, vengono passate le informazioni necessarie per valutare i valori dei vertici, senza eseguire effettivamente la valutazione. All'interno della subroutine, la valutazione effettiva di questi valori verrà eseguita solo per i vertici che appartengono al tetrahedron contenitore, dopo aver determinato il tetrahedron contenitore.

## <a name="lookup-table-for-use-with-high-dynamic-range-virtual-rgb-source-devices"></a>Tabella di ricerca da usare con dispositivi di origine RGB virtuali a intervallo dinamico elevato

Nel caso in cui una trasformazione venga costruita con un dispositivo di origine modellato come dispositivo RGB virtuale, è possibile che i valori coloranti di origine siano negativi o maggiori di unity (1.0). In questo caso, il dispositivo di origine viene definito con un intervallo dinamico elevato (HDR). Per questo caso vengono effettuate considerazioni speciali.

Nel caso di trasformazioni HDR, i valori minimo e massimo per ogni canale colorante possono essere determinati dal limite di gamut del dispositivo. Usando questi valori, viene applicato un ridimensionamento semplice per ogni canale colorante in modo che i valori coloranti uguali alla colorazione minima siano convertiti in 0,0 e i valori coloranti uguali alla colorazione massima siano convertiti in 1,0, con una scala lineare dei valori tra per eseguire il mapping lineare tra 0,0 e 1,0.

### <a name="iccprofilefromwcsprofile"></a>ICCProfileFromWCSProfile

Poiché lo scopo principale di questa funzionalità è supportare le versioni precedenti a Vista di Windows, è necessario generare profili ICC versione 2.2 come definito nella specifica ICC.1:1998-09. In alcuni casi (vedere la tabella seguente "Mapping classi profilo da dispositivo di base a ICC"), è possibile creare una matrice o un profilo ICC basato su TRC da un profilo WCS. In altri casi, il profilo ICC è costituito da LUN. Il processo seguente descrive come creare i LUT AToB e BToA. Naturalmente, anche i profili ICC hanno altri campi. Alcuni dati possono essere derivati dal profilo WCS. Per altri dati, è necessario sviluppare impostazioni predefinite intelligenti. Il copyright verrà assegnato a Microsoft; poiché è la tecnologia Microsoft che viene usata per creare i LUN.

Questa progettazione dovrebbe funzionare per tutti i tipi di modelli di dispositivo, inclusi i plug-in. Se al plug-in è associato un modello di dispositivo di base, è possibile determinare il tipo di dispositivo sottostante.

La parte difficile della creazione di un profilo ICC è la creazione delle tabelle di ricerca AToB e BToA. Queste tabelle sono mappate tra lo spazio del dispositivo, ad esempio RGB o CMYK, e lo spazio di connessione del profilo (PCS), che è una variante di CIELAB. Si tratta fondamentalmente dello stesso processo di gestione dei colori usato nella trasformazione CITE per eseguire il mapping dallo spazio del dispositivo allo spazio del dispositivo. Per eseguire la trasformazione, tuttavia, è necessario disporre delle informazioni seguenti.

1) Condizioni di visualizzazione dei riferimenti per pcS.

2) Gamut PCS di riferimento.

3) Modello di dispositivo che esegue la conversione tra valori PCS e colorimetria.

Il profilo WCS e la relativa camma associata vengono forniti come parametri. Esistono due modelli di dispositivo di base che esegono la conversione tra colorimetria e codifica PCS. Il motivo per cui sono necessari due elementi è illustrato di seguito.

1) È possibile ottenere le condizioni di visualizzazione dei riferimenti per pcS dalla specifica del formato del profilo ICC. Le informazioni fornite nella specifica del formato del profilo ICC sono sufficienti per calcolare tutti i dati necessari per inizializzare l'istanza di CAM usata da CMS. Per coerenza e flessibilità, queste informazioni vengono archiviate in un profilo colori WCS.

2) È anche possibile usare un profilo WCS per archiviare esempi che definiscono la gamma di riferimento del PCS. Il sistema di gestione dei colori CITE (CMS) consente di creare limiti di gamut in due modi. Uno è quello di campionare lo spazio completo del dispositivo e usare il modello di dispositivo per creare valori di misurazione. Il secondo metodo è usare campioni misurati dal profilo per creare un limite di gamut di riferimento. Poiché la gamma di ICC PCS è troppo grande per rendere disponibile un riferimento utile, il primo metodo non è appropriato. Il secondo metodo, tuttavia, è un approccio flessibile basato sul profilo. Per ridefinire la gamut PCS di riferimento, è possibile modificare i dati di misurazione nel profilo del dispositivo PCS.

3) ICC PCS è una modellazione di un dispositivo ideale. Creando un modello del PCS come dispositivo reale, è possibile sfruttare il processo di gestione dei colori usato in Smart CMM. La creazione di un modello di dispositivo dalla colorimetria alla codifica PCS è semplice. È sufficiente eseguire il mapping tra i valori colorimetrici effettivi e i valori con codifica PCS. Poiché l'interfaccia CMS per i modelli di dispositivo supporta solo valori XYZ, potrebbe anche essere necessario eseguire il mapping tra XYZ e LAB. Si tratta di una trasformazione nota. Questo modello è descritto nel documento 2.2.02 "Modelli di dispositivo di base" nelle sezioni 7.9 e 7.10.

Potrebbe essere necessario eseguire alcuni mapping di gamut, se la gamma del dispositivo è maggiore della gamma del PCS. A questo scopo, è possibile usare gli GMM di base. Si noti che un profilo ICC creato correttamente include tabelle di ricerca per le finalità Relative Colorimetric, Perceptual e Saturation, anche se queste possono puntare tutte allo stesso LUT internamente.

![Diagramma che illustra la creazione di un'unità A T o B L U T.](images/transformcreation-image128.png)

**Figura 5:** Creazione di un LUT AToB

Questo processo è illustrato nella figura 5. In primo luogo, il modello di dispositivo viene inizializzato dai dati nel profilo DM. Costruire quindi un limite di gamut del dispositivo come indicato di seguito. Un campionamento di dati dal modello di dispositivo viene eseguito tramite il modello di dispositivo per ottenere dati colorimetrici. I dati della colorimetrica vengono eseguiti tramite LA CAM per creare dati relativi all'aspetto. I dati di aspetto vengono usati per creare il limite di gamut del dispositivo.

Usare quindi i dati del profilo di misurazione PCS di riferimento per creare un limite di gamut per il PCS.

Usare i due limiti gamut appena creati per inizializzare un GMM. Usare quindi il modello di dispositivo, il GMM e il modello di dispositivo PCS per creare una trasformazione. Eseguire un campionamento dello spazio del dispositivo tramite la trasformazione per creare un LUT AToB.

![Diagramma che illustra la creazione di un'unità A T o B L U T usando un campionamento di spazio P C S.](images/transformcreation-image130.png)

**Figura 6:** Creazione di un LUT BToA

La figura 6 illustra la creazione dell'LUT BToA. Questo è quasi identico alla creazione di un LUT AToB, con i ruoli di origine e destinazione s scambiati. È anche necessario campionare la gamma completa di PCS per creare l'LUT.

Si noti che poiché il PROCESSO è coinvolto nel processo, l'adattamento cromatico tra il punto bianco multimediale e il punto bianco PCS (obbligatorio da ICC per essere quello di D50) viene interessato in modo trasparente dalla CAM.

## <a name="hdr-virtual-rgb-devices"></a>Dispositivi RGB virtuali HDR

Quando si generano profili per i dispositivi RGB virtuali HDR, è necessario tenere conto di una considerazione speciale. ovvero i dispositivi per cui i valori coloranti possono essere minori di 0,0 o maggiori di 1,0. Nella generazione dell'LUT ATOB viene creato un set più ampio di LUN di input 1D. I valori coloranti vengono ridimensionati e l'offset viene adattato all'intervallo 0 .. 1 utilizzando i valori di colorazione minimo e massimo nel profilo WCS.

Poiché è probabile che lo spazio colorato per i dispositivi HDR non sia completamente popolato, viene fornito un supporto speciale anche nell'LUT 3D per il tag. Per gestire i colori nell'area poco popolata, le coloranti vengono ricodificate in modo che sia possibile ottenere l'estrapolazione superiore a 0.0 e 1.0. L'intervallo usato è -1 . +4.

A causa della scalabilità applicata per l'LUT 3D, viene creato un set di LUN di output 1D per eseguire il mapping del risultato all'intervallo 0 . 1.

## <a name="more-than-one-pcs"></a>Più PCS

ICC ha rilevato che un PCS non era sufficientemente flessibile per soddisfare tutti gli usi di un CMS previsto. Nella versione 4 della specifica del profilo, il controllo di accesso ha chiarito che esistono effettivamente due codifiche PCS. Uno viene usato per le finalità colorimetriche. un altro viene usato per la finalità percettiva. Non viene specificato alcun PCS per la finalità Saturazione. L'ICC ha lasciato questa parte ambigua. Il PCS colorimetrico ha una leggerezza minima e massima specificata, ma i valori di chroma e tonalità sono approssimativamente ± 127. Questo PCS ha l'aspetto di un prism rettangolare. Come accennato in precedenza, il volume PCS percettivo è simile alla gamma di una stampante ink ink ink.

I due PCS ICC hanno anche due codifiche digitali diverse. Nel PCS percettiva, un valore pari a zero rappresenta una leggerezza pari a zero. Nel PCS colorimetrico, un valore pari a zero rappresenta la leggerezza minima del PCS, che è maggiore di zero. È possibile risolvere questo problema con un modello di dispositivo diverso per ognuna delle codifiche PCS.

## <a name="gamut-mapping"></a>Mapping di gamut

Per creare i LUT AToB in un profilo ICC, si esegue il mapping dalla gamma di dispositivi allo spazio PCS appropriato. Per creare i LUN BToA, eseguire il mapping dallo spazio PCS alla gamma di dispositivi. Il mapping per i LUN AToB è molto simile a quello usato in un CMS basato su misurazioni. Per il PCS percettibile, eseguire il mapping della gamma plausibile del dispositivo al limite di gamut percettibile del PCS, usando il ritaglio o la compressione per tutti i colori out-of-gamut. Per le finalità colorimetriche, potrebbe essere necessario ritagliare la leggerezza, ma i valori di chroma e tonalità rientrano tutti nella gamma colorimetrica PCS.

Il mapping per i LUN BToA è leggermente diverso. Le finalità colorimetriche sono ancora semplici. È sufficiente ritagliare i valori PCS nella gamma dei dispositivi. L'ICC richiede tuttavia che tutti i possibili valori PCS eseere mappati a un valore del dispositivo, non solo a quelli all'interno della gamma di riferimento del PCS percettivo. È quindi necessario assicurarsi che i GMM siano in grado di gestire i colori di origine esterni alla gamma di riferimenti. Questa operazione può essere gestita ritagliando i colori fino al limite di gamut del dispositivo.

## <a name="baseline-device-to-icc-profile-class-mapping"></a>Mapping della classe di profilo da dispositivo di base a profilo ICC



| Tipo di dispositivo di base              | Classe di profilo ICC       | Commento                                                                      |
|-----------------------------------|-------------------------|-----------------------------------------------------------------------------|
| Dispositivo di acquisizione RGB                | Dispositivo di input ("scnr")   | PCS è CIELAB. AToB0Tag è da dispositivo a PCS con finalità colorimetriche relative. |
| CRT, monitor LCD                  | Dispositivo di visualizzazione ("mntr") | PCS è CIEXYZ. Per la conversione del modello, vedere quanto segue.                      |
| Proiettore RGB                     | Spazio colore ("spac")    | PCS è CIELAB.                                                              |
| Stampante RGB e CMYK              | Dispositivo di output ("prtr")  | PCS è CIELAB.                                                              |
| Dispositivo virtuale RGB (caso non HDR) | Dispositivo di visualizzazione ("mntr") | PCS è CIEXYZ.                                                              |
| Dispositivo virtuale RGB (caso HDR)     | Spazio colore ("spac")    | PCS è CIELAB.                                                              |



 

La conversione dei profili di monitoraggio non implica la creazione di UNITÀ lun, ma consiste invece nella creazione di una matrice o di un modello TRC. Il modello usato in ICC è leggermente diverso da quello usato nella modellazione WCS CRT o LCD in cui manca il termine "correzione nera". ovvero:

Modello WCS: ![Mostra un modello W C S.](images/transformcreation-image132.png)

Modello ICC: ![Mostra un modello I C C.](images/transformcreation-image134.png)

La conversione dal modello WCS al modello ICC viene eseguita come segue.

Definire nuove curve:

![Mostra una matrice per definire nuove curve.](images/transformcreation-image136.png)

Non si tratta di curve di riproduzione del tono perché non vengono mappate da 1 a 1. Una normalizzazione consente di ottenere questo risultato. Le definizioni finali del modello ICC sono:

![Mostra le definizioni finali del modello I C C.](images/transformcreation-image138.png)

![Mostra la matrice finale per il modello I C C.](images/transformcreation-image140.png)

Per i dispositivi virtuali RGB non HDR, si genera anche un profilo ICC di visualizzazione per l'efficienza dello spazio. In tal caso, la matrice tristimulus *M ICC* può essere ottenuta direttamente dalle primarie del profilo WCS senza la conversione del modello precedente. Un aspetto finale, ma importante, è che questa matrice tristimulus deve essere adattata in modo cromatico a D50 per essere conforme alla specifica ICC del PCS. In altre parole, le voci in ogni riga della matrice da codificare nel profilo ICC devono essere sommate rispettivamente a 96,42, 100 e 82,49. Nell'implementazione corrente l'adattamento cromatico viene eseguito da CAT02, che è anche la trasformazione di adattamento cromatico usata in CAM02.

## <a name="black-preservation-and-black-generation"></a>Conservazione del nero e generazione nera

L'implementazione della conservazione del nero è associata alla generazione del canale nero nei dispositivi che supportano un canale nero. A tale scopo, vengono raccolte informazioni su ogni colore di origine per consentire ai modelli di dispositivo che supportano un canale nero di determinare il modo migliore per impostare il canale nero nell'output. Mentre la conservazione del nero è pertinente per le trasformazioni di colore che si convertono tra un dispositivo a canale nero e un altro, la generazione del nero viene implementata per tutte le trasformazioni che coinvolgono un dispositivo di destinazione del canale nero.

Le informazioni sul canale nero vengono registrate in una struttura di dati denominata [**BlackInformation.**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation) La **struttura BlackInformation** contiene un valore booleano che indica se il colore contiene solo colorante nero e un valore numerico che indica il grado di "blackness" denominato peso nero. Per i dispositivi di origine che supportano un canale nero, il peso nero è la percentuale di colorazione nera nel colore di origine. Per i dispositivi di origine che non contengono un canale nero, il peso nero viene calcolato usando le altre coloranti e il valore dell'aspetto. Un valore denominato "color purezza" viene calcolato prendendo la differenza tra il valore massimo di colorazione e il valore di colorazione minimo diviso per il valore di colorazione massimo. Un valore denominato "leggerezza relativa" viene calcolato prendendo la differenza tra la leggerezza del colore e la leggerezza minima per il dispositivo di destinazione divisa per la differenza tra la leggerezza minima e massima per il dispositivo di destinazione. Se il dispositivo di origine è un dispositivo additivo (monitor o proiettore), il peso nero viene determinato come 1,0 meno la luminosità del colore moltiplicata per la luce relativa. Ad esempio, se il dispositivo di origine è un monitor RGB, il valore massimo e il valore minimo di R, G e B per ogni colore vengono calcolati e il peso nero è determinato dalla formula:

BW = (1,0 – (max(R,G,B) – min(R,G,B)) / max(R, G, B)) \* relativa leggerezza

Se il dispositivo di origine supporta la colorazione sottrazione, ad esempio una stampante CMY, le singole coloranti devono essere "completate" (sottratto da 1.0) prima dell'uso nella formula precedente. Pertanto, per una stampante CMY, R = 1.0 – C, G = 1.0 – M e B = 1.0 – Y.

Le informazioni sul nero per ogni colore elaborato dalla trasformazione del colore vengono determinate durante il processo di conversione dei colori. Le informazioni solo di colore nero vengono determinate solo se è specificata la conservazione del nero. Il peso nero viene sempre determinato se il modello di dispositivo di destinazione supporta una colorazione nera. Le informazioni nere vengono passate al modello di dispositivo di destinazione tramite il metodo [**ColorimetricToDeviceColorsWithBlack,**](/previous-versions/windows/desktop/api/WcsPlugIn/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack) che usa l'LUT risultante.

Si noti che, a causa dell'ottimizzazione della trasformazione del colore, il processo precedente si verifica solo durante la creazione della trasformazione ottimizzata LUT, non durante l'esecuzione del metodo TranslateColors.

## <a name="optimization-for-transforms-with-more-than-three-source-channels"></a>Ottimizzazione per le trasformazioni con più di tre canali di origine

Le dimensioni della trasformazione ottimizzata sono determinate da diversi fattori: il numero di canali di colore nel dispositivo di origine, il numero di passaggi nella tabella per ogni canale di colore di origine e il numero di canali di colore nel dispositivo di output. La formula per determinare le dimensioni della tabella di trasformazione è:

Dimensioni = Numero di passaggi per ogni origine <sub>canale\ dispositivo(Numero\ di\ canali\ in\ origine\ dispositivo)</sub> x numero di canali nel dispositivo di output

Come si può vedere, le dimensioni della tabella aumentano in modo esponenziale a seconda del numero di canali nel dispositivo di origine. Molti dispositivi di origine supportano tre canali di colore, ad esempio Rosso, Verde e Blu. Tuttavia, se un dispositivo di origine supporta quattro canali, ad esempio CMYK, le dimensioni della tabella e il tempo necessario per costruire la tabella aumentano di un fattore del numero di passaggi. In un CMS basato su misurazioni in cui le trasformazioni vengono costruite "in tempo reale", questa volta potrebbe non essere accettabile.

Per ridurre il tempo necessario per costruire la tabella di conversione dei colori, è possibile sfruttare due fatti. In primo luogo, mentre il dispositivo di origine può supportare più di tre canali di colore, lo spazio colore indipendente dal dispositivo intermedio (SIM02 Ja <sub>C</sub> b <sub>C</sub> ) ha solo tre canali di colore. In secondo piano, la parte più dispendiosa in termini di tempo dell'elaborazione non è la modellazione del dispositivo (conversione dalle coordinate del colore del dispositivo ai valori tristimuli), ma il mapping della gamma. Usando questi fatti, è possibile costruire una tabella preliminare di conversione dei colori che converte i colori nello spazio colori indipendente dal dispositivo tramite i passaggi di mapping della gamma e infine tramite il modello di colore del dispositivo di output. La costruzione di questa tabella è della dimensione tre. Si costruisce quindi la tabella finale di conversione dei colori della dimensione quattro convertendo le combinazioni di colori di origine in uno spazio indipendente dal dispositivo intermedio e quindi, usando la tabella preliminare di conversione dei colori, completare la conversione nello spazio colori del dispositivo di output. È quindi possibile ridurre dal calcolo (numero di passaggi nella tabella di ricerca) number\ of\ channels gamut mapping computations to the number of steps in the intermediate table ₃ gamut mapping computations ( Numero di passaggi nella tabella di ricerca) <sub>number\ of\ channels</sub> gamut mapping computations to the number of steps in the intermediate table ₃ gamut mapping computations (Numero di passaggi nella tabella intermedia) e calcoli di mapping a gamut. Anche se è necessario eseguire il numero di passaggi nel numero (tabella di ricerca) <sub>number\ of\ channels</sub> computations of device modeling and three-dimensional table lookups (Numero tabella di ricerca) dei canali di modellazione dei dispositivi e delle ricerche di tabelle tridimensionali, questa operazione è ancora molto più veloce del calcolo originale.

Il processo precedente funzionerà correttamente se non è necessario che le informazioni passino tra il modello di dispositivo di origine e qualsiasi altro componente nella trasformazione del colore. Tuttavia, se il dispositivo di output e il dispositivo di origine supportano entrambi un colorante nero e la colorante nera di origine viene usata per determinare il colorante nero di output, il processo non riuscirà a comunicare correttamente le informazioni sul nero di origine. Un processo alternativo consiste nel costruire una tabella preliminare di conversione dei colori che converta i colori nello spazio colori indipendente dal dispositivo solo tramite i passaggi di mapping della gamma. Costruire quindi la tabella finale di conversione dei colori della dimensione quattro seguendo questa procedura: a) convertire le combinazioni di colori di origine in uno spazio indipendente dal dispositivo intermedio, b) eseguire i passaggi di mapping della gamma interpolando nella tabella dei colori preliminare invece di applicare i processi di mapping della gamut effettivi e c) usare i valori risultanti dai passaggi di mapping della gamut e le informazioni sul canale nero di origine per calcolare i coloranti del dispositivo di output usando il modello di dispositivo di output. Questo processo può essere usato anche quando sono presenti informazioni trasferite tra i modelli di dispositivo di origine e di output anche se non è presente alcun canale nero. ad esempio se i due moduli vengono implementati con un'architettura plug-in che consente l'interscambio dei dati tra i moduli.

I due processi precedenti possono essere usati per migliorare in modo efficace il tempo necessario per costruire la tabella di trasformazione dei colori quadridimensionale.

### <a name="checkgamut"></a>CheckGamut

Il ICM chiama CreateTransform e **CreateMultiProfileTransform** accettano una parola di valori di flag, uno dei quali è ENABLE \_ GAMUT \_ CHECKING. Quando questo flag è impostato, CITE deve creare la trasformazione in modo diverso. I passaggi iniziali sono gli stessi: le macchine virtuali di origine e di destinazione devono essere inizializzate, quindi i descrittori limite gamut di origine e di destinazione devono essere inizializzati. Indipendentemente dalla finalità specificata, è necessario usare CheckGamut GMM. Il GMM CheckGamut deve essere inizializzato usando i modelli di dispositivo di origine e di destinazione e i descrittori limite gamut. Tuttavia, la trasformazione deve quindi creare una trasformazione troncata che comprende il modello di dispositivo di origine, la CAM di origine, qualsiasi GMM interviene e checkGamut GMM. Ciò garantisce che i valori delta J, delta C e delta h restituiti dal CMM CheckGamut diventino i valori finali risultanti.

Il significato di CheckGamut è chiaro quando nella trasformazione sono presenti solo due profili di dispositivo. Quando sono presenti più di due profili di dispositivo e più di due GMM, CheckGamut segnala se i colori trasformati tramite il primo modello di dispositivo e tutti gli altri GMM rientrano nella gamma del dispositivo di destinazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base sulla gestione dei colori](basic-color-management-concepts.md)
</dt> <dt>

[Windows Schemi e algoritmi del sistema di colori](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




