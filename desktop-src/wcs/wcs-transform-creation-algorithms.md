---
title: Algoritmi di creazione della trasformazione WCS
description: Algoritmi di creazione della trasformazione WCS
ms.assetid: 526bbbfc-fb60-415d-b4f0-6a44a5d11a55
keywords:
- Windows Color System (WCS), trasformazione creazione
- WCS (sistema di colori Windows), creazione trasformazione
- Gestione colori immagine, creazione trasformazione
- Gestione colori, creazione trasformazione
- colori, creazione trasformazione
- creazione trasformazione
- Creazione della trasformazione WCS
- algoritmi, creazione trasformazione
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418596c0e57571f3e504727d4606921d36ff9461
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "104559523"
---
# <a name="wcs-transform-creation-algorithms"></a>Algoritmi di creazione della trasformazione WCS

[Creazione di trasformazioni](#creation-of-transforms)

 

[Esecuzione di trasformazione sequenziale](#sequential-transform-execution)

 

[Creazione di trasformazioni ottimizzate](#creation-of-optimized-transforms)

 

[ICCProfileFromWCSProfile](#iccprofilefromwcsprofile)

 

[Conservazione nera e generazione nera](#black-preservation-and-black-generation)

 

[Verifica gamut](#checkgamut)

## <a name="creation-of-transforms"></a>Creazione di trasformazioni

Per spiegare correttamente il funzionamento delle trasformazioni dei colori, è utile illustrare il percorso di elaborazione completo sia per ICM 2,0 che per gli elementi interni della CTE. La funzione MCI 2,0 [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) crea una trasformazione colore che le applicazioni possono usare per eseguire la gestione dei colori. Questa funzione crea un contesto di colore dagli input [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) e Intent. Viene eseguito il mapping degli Intent all'algoritmo di mapping della gamma ICC di base. La funzione chiama quindi la funzione MCI 2,0 [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/) per l'elaborazione dei colori coerente. La funzione **CreateColorTransform** copia in genere i dati nella struttura di trasformazione ottimizzata interna.

La funzione MCI 2,0 CreateMultiProfileTransform accetta una matrice di profili e una matrice di Intent o un profilo di collegamento a dispositivo singolo e crea una trasformazione colore che le applicazioni possono usare per eseguire il mapping dei colori. Elabora i profili di input e gli Intent per creare modelli di dispositivo, modelli di aspetto dei colori, descrizioni dei limiti della gamma e modelli di mapping di gamut. Ecco come eseguire questa operazione:

-   I modelli di dispositivo vengono inizializzati direttamente dai profili DM. È presente un modello di dispositivo creato per ogni profilo nella chiamata a [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/).
-   I modelli di aspetto dei colori vengono inizializzati direttamente dai profili CAM. Esiste un profilo di camma per ogni profilo nella chiamata a [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/). È tuttavia possibile specificare lo stesso profilo di camma per più di un profilo.
-   Le descrizioni dei limiti della gamma vengono inizializzate da un oggetto modello di dispositivo e da un oggetto camma. Esiste una descrizione del limite di gamut per ogni profilo nella chiamata a [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/).
-   I modelli di mapping gamut vengono inizializzati da due limiti di gamut e da un Intent. È necessario creare un modello di mapping di gamut tra ogni coppia di modelli di dispositivo creati dalla chiamata a [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/). Si noti che questo significa che si usa un modello di mappa a gamut inferiore rispetto al modello di dispositivo. Poiché il numero di Intent corrisponde al numero di modelli di dispositivo, esiste anche un altro scopo rispetto al necessario. Il primo intento nell'elenco viene ignorato. Viene illustrato l'elenco dei modelli di dispositivo e degli Intent, creando modelli di mapping di gamut. Prelevare il primo e il secondo modello di dispositivo e il secondo scopo, quindi inizializzare il primo modello di mapping di gamut. Prelevare il secondo e il terzo modello di dispositivo e il terzo scopo, quindi inizializzare il modello di mapping del secondo gamut. Continuare in questo modo fino a quando non sono stati creati tutti i modelli di mapping di gamut.

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

Un problema relativo alla configurazione dell'elenco delle trasformazioni consiste nel verificare se è disponibile un plug-in obbligatorio. Il seguente parametro di modello fornisce questo criterio per controllare questo comportamento. La gestione di questo elenco di trasformazione è un metodo nella struttura di trasformazione ottimizzata interna, ma ogni metodo del modello fornisce il puntatore a se stesso e il proprio set di valori di parametro.

La modalità deve essere una delle seguenti.

-   TfmRobust: se un profilo di misurazione specifica un plug-in preferito e il plug-in non è disponibile, il nuovo sistema CTE utilizzerà il plug-in baseline. Se non è disponibile alcun plug-in, la trasformazione segnalerà un errore.
-   TfmStrict: se ColorContext specifica un plug-in preferito, il plug-in deve essere disponibile. Se non viene trovato alcun plug-in preferito, verrà usato il plug-in baseline. Se non è disponibile alcun plug-in, la trasformazione segnalerà un errore.
-   TfmBaseline: è possibile usare solo plug-in di base in AddMeasurementStep. Se ColorContext specifica un plug-in preferito, il plug-in verrà ignorato. Se il plug-in Baseline non è disponibile, la trasformazione segnalerà un errore.

## <a name="transform-execution"></a>Esecuzione della trasformazione

La funzione [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) dell'API MCI 2,0 converte una matrice di colori dallo [spazio](c.md) dei colori di origine allo spazio dei colori di destinazione in base a quanto definito da una trasformazione colore. Questa funzione controlla internamente in base a una matrice di colori memorizzati nella cache per consentire la corrispondenza immediata dei colori comunemente trasformati. Questa trasformazione supporta le matrici di byte a 8 bit per canale e le matrici float a 32 bit per canale. Tutti gli altri formati verranno convertiti prima del passaggio alla nuova CTE.

La funzione [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) dell'API MCI 2,0 converte i colori di una bitmap con un formato definito per produrre un'altra bitmap in un formato richiesto. Questa funzione controlla internamente in base a una matrice di colori memorizzati nella cache per consentire la corrispondenza immediata dei colori comunemente trasformati. Per evitare troppi percorsi di codice, supporto e complessità dei test, solo un numero limitato di formati bitmap è effettivamente supportato nel motore di trasformazione e interpolazione. Questa funzione deve tradurre i formati bitmap in entrata e in uscita non nativi in formati supportati in modo nativo per l'elaborazione. Questa trasformazione supporta solo bitmap a 8 bit per byte di canale e bitmap float a 32 bit per canale. Tutti gli altri formati verranno convertiti prima del passaggio alla nuova CTE.

 

### <a name="sequential-transform-execution"></a>Esecuzione di trasformazione sequenziale

Se il parametro *dwFlags* dispone del bit di trasformazione sequenziale \_ impostato quando vengono chiamate le funzioni ICM [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) o **CreateMultiProfileTransform** , i passaggi della trasformazione vengono eseguiti in sequenza. Questo significa che il codice scorre ogni modello di dispositivo, modello di aspetto dei colori e modello di mapping di gamut separatamente, come specificato dalla chiamata a **CreateColorTransform** o **CreateMultiProfileTransform** . Questo può essere utile per il debug dei moduli plug-in, ma è molto più lento rispetto all'esecuzione tramite una trasformazione ottimizzata. L'esecuzione in modalità sequenziale non è quindi consigliata per il software di produzione. Inoltre, è possibile che si verifichino lievi differenze nei risultati ottenuti in modalità sequenziale e in modalità ottimizzata. Ciò è dovuto a variazioni introdotte quando le funzioni vengono concatenate insieme.

### <a name="creation-of-optimized-transforms"></a>Creazione di trasformazioni ottimizzate

Una trasformazione ottimizzata è una tabella di ricerca multidimensionale. La tabella può essere elaborata da un motore di interpolazione multidimensionale, ad esempio l'interpolazione tetraedrica, che applica i colori di input alla trasformazione. Nella sezione seguente viene descritto come vengono create le tabelle di ricerca ottimizzate. La sezione successiva descrive come interpolare nelle tabelle di ricerca ottimizzata.

## <a name="sparse-lookup-tables"></a>Tabelle di ricerca di tipo sparse

Le stampanti convenzionali hanno inchiostri CMYK. Per estendere la gamma, un approccio consiste nell'aggiungere nuovi inchiostri al sistema. Gli inchiostri che vengono in genere aggiunti sono colori che gli inchiostri CMYK presentano difficoltà di riproduzione. Le scelte comuni sono arancio, verde, rosso, blu e così via. Per aumentare la "risoluzione apparente", è possibile usare inchiostri con tinte diverse, ad esempio, ciano chiaro, magenta chiaro e così via. In effetti, il dispositivo della stampante ha più di quattro canali.

Sebbene le stampanti siano dispositivi di output, eseguono anche la conversione dei colori dallo spazio del dispositivo a un altro spazio colore. Nel caso di una stampante CMYK, si tratta di una trasformazione da CMYK a XYZ o dal "modello di avanzamento" della stampante. Combinando il modello di tipo avanti con altre trasformazioni, è possibile emulare una stampa CMYK in un altro dispositivo. Ad esempio, una stampante CMYK per un monitor RGB renderebbe possibile un meccanismo di correzione che emula una stampa di tale stampante CMYK su un monitor. Analogamente, lo stesso vale anche per le stampanti Hi-Fi. Una conversione da CMYKOG a RGB consente la correzione della stampante CMYKOG su un monitor.

L'approccio convenzionale all'implementazione di tale conversione dei colori consiste nell'usare un LUT uniforme. Ad esempio, in un profilo ICC per una stampante CMYKOG, la specifica ICC impone un tag A2B1 che archivia un LUT uniforme che rappresenta un campionamento uniforme nello spazio del dispositivo CMYKOG del modello di avanzamento, che passa da CMYKOG allo spazio di connessione del profilo ICC, ovvero CIELAB o CIE XYZ. Il profilo di collegamento del dispositivo ICC consente una trasformazione diretta dallo spazio del dispositivo CMYKOG a qualsiasi spazio di colore incluso uno spazio del dispositivo, anche sotto forma di un LUT campionato in modo uniforme nello spazio CMYKOG. Il campionamento non viene mai eseguito con livelli di 256 (profondità di bit 8) a causa della grande LUT risultante, tranne nel caso di dispositivi monocromi (1 canale). Viene invece utilizzato il campionamento con una profondità di bit inferiore; alcune scelte tipiche sono 9 (profondità bit 3), 17 (profondità bit 4), 33 (profondità bit 5). Con il numero di livelli inferiore a 256 in ogni canale, LUT viene usato in combinazione con un algoritmo di interpolazione per produrre il risultato se un livello è compreso tra due livelli campionati.

Anche se un LUT uniforme è concettualmente semplice da implementare e l'interpolazione in un LUT uniforme è in genere efficiente, la dimensione LUT aumenta in modo esponenziale con la dimensione di input. Infatti, se *d* è il numero di passaggi utilizzati nell'LUT uniforme e *n* è il numero di canali nello spazio colore di origine, il numero di nodi in LUT è ![ Mostra la variabile per il numero di nodi in un LUT. ](images/transformcreation-image002.gif) Ovviamente, il numero di nodi richiede rapidamente una quantità di spazio di archiviazione in memoria che anche i sistemi di elaborazione Top-of-line hanno difficoltà a gestire la richiesta. Per i dispositivi con sei o otto canali, un'implementazione ICC del profilo di dispositivo richiede l'uso di pochi passaggi in LUT, a volte anche fino a cinque passaggi nella tabella A2B1 per preservare il profilo in megabyte anziché in gigabyte. Ovviamente, l'utilizzo di un numero inferiore di passaggi aumenta l'errore di interpolazione, perché ora sono presenti meno esempi. Poiché il valore di LUT deve essere uniforme, l'accuratezza sull'intero spazio dei colori viene ridotta anche in queste aree dello spazio in cui una differenza di colore significativa può essere causata da una piccola modifica del valore del dispositivo.

Nei dispositivi con più di quattro coloranti, determinati spazi sottospazi dell'intero spazio del dispositivo sono più importanti di altri. Nello spazio CMYKOG, ad esempio, gli inchiostri cyan e verde vengono usati raramente insieme perché le tonalità si sovrappongono in gran parte. In modo analogo, gli inchiostri giallo e arancione si sovrappongono. Una riduzione uniforme del numero di passaggi può essere considerata come un calo generale della qualità in tutto lo spazio dei colori, che è un elemento che è possibile permettersi per le combinazioni di inchiostro improbabile, ma non per le combinazioni probabili o importanti.

Anche se un LUT campionato in modo uniforme è semplice ed efficiente per l'interpolazione, impone requisiti di memoria elevati in quanto aumenta la dimensione. In realtà, sebbene un dispositivo possa avere sei o otto canali, viene usato raramente simultaneamente. Nella maggior parte dei casi, la trasformazione colore di input per colore ha solo pochi coloranti "attivi" e pertanto si trova in uno spazio di colore più basso. Ciò significa anche che l'interpolazione può essere eseguita in modo più efficiente nello spazio di dimensioni inferiori perché l'interpolazione è più veloce quando la dimensione è inferiore.

Pertanto, l'approccio consiste nel stratificare l'intero spazio del dispositivo in sottospazi di varie dimensioni. Poiché le dimensioni inferiori, ovvero quelle che combinano tre o quattro coloranti, sono più importanti, stratifica lo spazio, è anche possibile applicare frequenze di campionamento diverse; ovvero un numero diverso di passaggi, per le parti; aumento delle frequenze di campionamento per le dimensioni inferiori, riduzione per dimensioni maggiori.

Per correggere le annotazioni, *n* è il numero di canali nello spazio dei colori di origine della trasformazione colore che si desidera campionare. È anche possibile fare riferimento a *n* come dimensione di input e ![ indica che n è maggiore o uguale a 5.](images/transformcreation-image004.gif) , se non diversamente specificato.

I blocchi predefiniti di base sono LUTs di diverse *dimensioni* e dimensioni di input, anziché un LUT uniforme con dimensione di input *n*. Per maggiore precisione, un *LUT* è un reticolo rettangolare imposto per un cubo di unità; ovvero tutte le coordinate del dispositivo vengono normalizzate nell'intervallo compreso tra \[ 0 e 1 \] . Se è la dimensione di input di LUT (si noti che non deve essere uguale a *n*, sebbene ![ mostri V minore o uguale a n.](images/transformcreation-image006.gif) è obbligatorio), quindi è costituito da griglie di campionamento unidimensionale ν:

SAMP *i*: ![ Mostra una griglia di campionamento unidimensionale.](images/transformcreation-image008.gif)

dove tutte le *x <sub>j</sub>* devono trovarsi nell'intervallo \[ 0, 1 \] , ![ Mostra un superscript d (i).](images/transformcreation-image010.gif) è il numero di passaggi per il campionamento del canale *i* , che deve essere almeno 1, e ![ Mostra un spuperscript di X (pedice) d (i).](images/transformcreation-image012.gif) deve essere 1. D'altra parte, ![ Mostra un superscript X (pedice 1).](images/transformcreation-image014.gif) non deve essere 0.

Verranno definiti solo i due casi speciali seguenti di LUT.

*Closed LUT*: si tratta di un LUT con il requisito aggiuntivo per ogni SAMP *<sub>i</sub>*, che ![ Mostra un superscript X (pedice 1) uguale a 0.](images/transformcreation-image016.gif) e ![ Mostra un apice d (i) maggiore o uguale a 2.](images/transformcreation-image018.gif) . Un LUT chiuso uniforme è un LUT chiuso con lo stesso valore che ![ Mostra un apice d (i).](images/transformcreation-image010.gif) per ogni canale e i nodi sono distanziati in modo uniforme tra 0 e 1.

*Open LUT*: si tratta di un LUT con il requisito aggiuntivo per ogni SAMP *i*, che ![ Mostra un superscript X (pedice 1) maggiore di 0.](images/transformcreation-image020.gif) . È possibile fare in modo che ![ mostri un apice d (i) uguale a 1.](images/transformcreation-image022.gif) .

L'obiettivo è stratificare il cubo di unità \[ 0, 1 \] *n* in una raccolta di LUTs chiusi e Open LUTS, in modo che l'intera raccolta copra il cubo di unità. È concettualmente più semplice organizzare questi "LUT strati" in base alle dimensioni, in modo che al livello superiore:

![Mostra il primo livello per organizzare gli strati L U T in base alle dimensioni.](images/transformcreation-image024.png)

dove ![ Mostra l'indice Sigma k.](images/transformcreation-image026.gif) è la "raccolta di strati *k* -dimensionali". Si noti che la dimensione Strata inizia da 3 anziché da 0; ovvero punti, perché l'interpolazione di combinazioni a tre colori può essere gestita senza una quantità eccessiva di memoria richiesta.

## <a name="description-of-the-lut-strata"></a>Descrizione degli strati LUT

In questa implementazione:

1. ![Mostra l'indice Sigma 3.](images/transformcreation-image028.gif) è costituito da LUTs chiusi con tre input, uno da ogni possibile combinazione di tre coloranti scelti da *n* coloratori.

2. ![Mostra l'indice Sigma 4.](images/transformcreation-image030.gif) è costituito da un LUT chiuso per la combinazione di CMYK (o dei primi quattro coloranti), insieme a ![Mostra (n su 4) meno 1.](images/transformcreation-image032.png) Aprire LUTs per tutte le altre combinazioni a quattro colori. Individuando la combinazione di CMYK, si conferma che si tratta di una combinazione importante.

3. Per ![ Mostra k uguale a 5,..., n.](images/transformcreation-image034.gif) , ![ Mostra l'indice Sigma k.](images/transformcreation-image026.gif) è costituito da ![ esposizioni (n su k).](images/transformcreation-image037.gif) Aprire LUTs, una per ogni possibile combinazione di scelta di *k* coloranti dal totale di *n* coloranti.

Rimane per specificare le dimensioni del LUTs. La differenza principale tra LUTs aperti e chiusi è che i LUTs aperti non si sovrappongono e la LUTs chiusa potrebbe sovrapporsi ai visi limite. Poiché il campionamento unidimensionale in un LUT aperto non contiene 0, significa essenzialmente che un LUT aperto manca la metà delle facce limite, quindi il nome "Apri". Se due LUTs non si sovrappongono, è possibile usare un numero diverso di passaggi o posizioni dei nodi in ogni canale. Lo stesso non è vero se due LUTs si sovrappongono. In tal caso, se il numero di passaggi o i percorsi del nodo sono diversi, un punto che si trova nell'intersezione dei due LUTs riceverà un valore di interpolazione diverso a seconda del LUT usato nell'interpolazione. Una soluzione semplice a questo problema consiste nell'usare il campionamento uniforme con lo stesso numero di passaggi ogni volta che due LUTs si sovrappongono. In altre parole:

Tutti i LUTs chiusi (tutti i LUTs a tre colori e i LUT CMYK in questa implementazione) devono essere uniformi e avere lo stesso numero di passaggi, che sono indicati *d*.

I due algoritmi seguenti possono essere usati per determinare il numero di passaggi *d* per LUTS chiuse e il numero di passaggi per LUTS aperti.

## <a name="algorithm-1"></a>Algoritmo \# 1

Questo algoritmo non richiede input esterno.

Tutte le LUTs chiuse saranno uniformi con il numero *d* passaggi.

Tutti i LUTs aperti della dimensione *k* avranno lo stesso numero di passaggi che ![ mostrano d (k).](images/transformcreation-image039.gif) in ogni canale di input e i nodi sono equidistanti. ovvero, per ogni ![ Mostra i è uguale a 1, 2,..., k.](images/transformcreation-image041.gif) .

SAMP *i*: ![ Mostra l'algoritmo SAMP i.](images/transformcreation-image043.png)

Infine, specificare *d* e *d* (*k* ) nella tabella seguente 1. Le tre modalità "Proof", "Normal" e "Best" sono le impostazioni di qualità MCI 2,0. In questa implementazione, la modalità di prova ha il footprint di memoria più piccolo e la modalità migliore ha il footprint di memoria più grande.

Per implementare questo algoritmo, è necessario chiamare il seguente algoritmo \# 2. Gli utenti possono specificare le proprie posizioni di campionamento, usando le tabelle come guida.

## <a name="algorithm-2"></a>Algoritmo \# 2

Questo algoritmo richiede un input esterno sotto forma di un elenco di percorsi di campionamento "importanti", ma è più adattivo e può ridurre potenzialmente lo spazio di memoria.

L'input richiesto è una matrice di valori di dispositivo forniti dall'utente. Questi valori del dispositivo indicano quale area dello spazio dei colori del dispositivo è importante; ovvero, quale area deve essere campionata più.

Tutti i LUTs chiusi saranno uniformi con il numero di passaggi *d* , come descritto nell'algoritmo \# 1. I valori per *d* sono riportati nella tabella 1.

*(a) Uniform closed LUT*



|         | Modalità di prova | Modalità normale | Modalità migliore |
|---------|------------|-------------|-----------|
| ***d*** | 9          | 17          | 33        |



 

*(b) aprire LUT*



| Dimensione di input | Modalità di prova | Modalità normale | Modalità migliore |
|-----------------|------------|-------------|-----------|
| 4               | 5          | 7           | 9         |
| 5               | 2          | 3           | 3         |
| 6               | 2          | 3           | 3         |
| 7               | 2          | 2           | 2         |
| 8 o più       | 2          | 2           | 2         |



 

**Tabella 1:** Dimensioni LUT utilizzate nell'algoritmo

Ogni LUT aperto può avere un numero diverso di passaggi in ogni canale di input e i percorsi di campionamento non devono essere equidistanti. Per un determinato strato LUT aperto, è presente una combinazione di colori associata. ad esempio, Mostra il sottoscript ![ c 1,..., c indice k.](images/transformcreation-image045.gif) , dove ![ Mostra gli indici C.](images/transformcreation-image047.gif) i sono numeri interi distinti compresi tra 1 e *n*. Si tratta degli indici del canale corrispondenti ai coloranti "attivi" in questo strato.

PASSAGGIO 1: filtrare la matrice inputted dei valori del dispositivo che non sono contenuti in questo strato. Un valore del dispositivo ![ Mostra x indice 1, x indice 2,..., x indice n.](images/transformcreation-image049.gif) è contenuto negli strati, se e solo se ![ Mostra un set di valori per un canale.](images/transformcreation-image051.gif) tutti gli altri canali sono pari a 0. Se il set filtrato contiene *N* voci, Let

![Mostra un'equazione da usare se il set filtrato contiene N voci.](images/transformcreation-image053.png)

Per ogni ![Mostra i uguali a 1, 2,..., k.](images/transformcreation-image041.gif) , eseguire l'iterazione dei passaggi seguenti 2-5:

PASSAGGIO 2: se ![ Mostra il tentativo di indice d (k) è uguale a 1.](images/transformcreation-image055.gif) , SAMP *i* ha un solo punto, che deve essere 1,0. Passare alla successiva *i*. In caso contrario, continuare con il passaggio 3.

PASSAGGIO 3: ordinare gli esempi filtrati in ordine crescente nel ![Mostra gli indici C.](images/transformcreation-image047.gif) channel.

PASSAGGIO 4: definire la griglia di campionamento "provvisorio" usando i nodi

![Mostra i nodi utilizzati per definire la griglia di campionamento "provvisorio".](images/transformcreation-image057.png)

dove ![Mostra j uguale a 1, 2,..., d pedice provvisorio (k).](images/transformcreation-image059.gif) .

PASSAGGIO 5: regolarizzare la griglia provvisoria per assicurarsi che sia conforme a una rigida monotona e anche che termini con 1,0. Poiché la matrice è già ordinata, i nodi nella griglia provvisoria sono già nondecreasing monotonic. Tuttavia, i nodi adiacenti potrebbero essere identici. È possibile risolvere il problema rimuovendo i nodi identici, se necessario. Infine, dopo questa procedura, se il punto finale è inferiore a 1,0, sostituirlo con 1,0.

Si noti che il passaggio 5 indica il motivo per cui gli strati LUT possono avere un numero diverso di passaggi in ogni canale. Dopo la regolarizzazione, il numero di passaggi in un canale può essere minore di ![Viene mostrato il tentativo di esecuzione di un indice d (k).](images/transformcreation-image061.gif) .

## <a name="interpolation"></a>Interpolazione

È possibile costruire la stratificazione del cubo di unità aprendo LUT strati e LUT strati chiusi. Per eseguire l'interpolazione utilizzando questa "struttura LUT di tipo sparse", attenersi alla seguente procedura. Si supponga un valore di dispositivo di input specificato ![Mostra (X pedice 1, X indice 2,..., X indice n).](images/transformcreation-image049.gif) .

PASSAGGIO 1: determinare il numero di canali "attivi". Questo è il numero di canali diversi da zero. In questo modo viene determinata la dimensione dello strato *k* per la ricerca dello strato contenitore. Più precisamente, la dimensione degli strati è 3 Se il numero di canali attivi è ![ minore o uguale a 3.](images/transformcreation-image063.gif) in caso contrario, la dimensione dello strato è uguale al numero di canali attivi.

PASSAGGIO 2: all'interno di ![Mostra l'indice Sigma k.](images/transformcreation-image026.gif) , cercare lo strato contenitore. Un valore del dispositivo è contenuto in uno strato aperto se tutti i canali corrispondenti allo strato hanno un valore diverso da zero e tutti gli altri canali sono pari a zero. Un valore del dispositivo è contenuto in uno strato chiuso se ogni canale non rappresentato dallo strato è zero. Se non viene trovato alcuno strato contenitore, si verifica una condizione di errore. Annulla e segnala errore. Se viene trovato uno strato contenitore, procedere al passaggio successivo.

PASSAGGIO 3: se lo strato contenitore è chiuso, l'interpolazione all'interno dello strato può essere eseguita da qualsiasi algoritmo di interpolazione noto. In questa implementazione, la scelta dell'algoritmo è l'interpolazione tetraedrica. Se lo strato contenitore è aperto e il valore del dispositivo si trova esclusivamente all'interno dello strato, ovvero

![Mostra X indice i maggiore o uguale a... ](images/transformcreation-image065.gif) primo nodo nel canale *i* TH

dove *i* è un indice di canale per lo strato, l'algoritmo di interpolazione standard, ad esempio l'interpolazione tetraedrica, funziona.

Se ![ Mostra X pedice i, minore di... ](images/transformcreation-image067.gif) primo nodo nel canale *i* TH per alcuni *i*, il valore del dispositivo rientra nel "gap" tra lo strato e gli spazi subdimensionali inferiori. Questo MOI non è interessato da un algoritmo di interpolazione per se, pertanto è possibile usare qualsiasi algoritmo di interpolazione per interpolare in questo "gap", sebbene l'algoritmo preferito sia l'interpolazione transfinita seguente.

L'architettura del modulo di interpolazione è illustrata nelle due parti della figura 1.

![Diagramma che mostra parte di un'architettura del modulo di interpolazione.](images/transformcreation-image068.png)

![Diagramma che illustra la seconda parte dell'architettura del modulo di interpolazione.](images/transformcreation-image070.png)

**Figura 1:** Architettura del modulo Intepolation

Come spiegato in precedenza, questo algoritmo è in grado di ottenere un campionamento ragionevolmente denso nelle aree dello spazio del dispositivo che contengono una combinazione importante di coloranti, riducendo al minimo le dimensioni totali di LUTs necessarie. La tabella seguente illustra un confronto tra il numero di nodi necessari per l'implementazione di LUT di tipo sparse (usando l'algoritmo \# 1 e la modalità normale) e l'implementazione LUT uniforme corrispondente.



| **Numero di canali di input** | **LUT sparse** | **Uniform LUT** |
|------------------------------|----------------|-----------------|
| 5                            | 142498         | 1419857         |
| 6                            | 217582         | 24137567        |
| 7                            | 347444         | 410338673       |
| 8                            | 559618         | 6975757441      |



 

## <a name="interpolation-within-a-unit-cube"></a>Interpolazione in un cubo di unità

Un passaggio di base nel caso della griglia rettangolare è l'interpolazione all'interno di una cella di inclusione. Per un punto di input, è possibile determinare facilmente la cella contenitore. In una griglia rettangolare, viene specificato il valore di output in corrispondenza di ogni vertice (angoli) della cella di inclusione. Sono anche le uniche condizioni limite (BCs) che devono essere soddisfatte da un Interpol: l'interpolatore deve superare tutti questi punti. Si noti che queste condizioni limite si trovano su punti "discreti", in questo caso i punti dell'angolo 2n della cella, dove n è la dimensione dello spazio colore.

È utile per formalizzare il concetto di condizioni di limite prima di procedere. Per tutti i subset del limite della cella di inclusione (il cubo di unità in n dimensioni), una condizione di limite su S è una specifica di una funzione BC: S → RM, dove m è la dimensione di output. In altre parole, un interpolatore, che può essere indicato interp: \[ 0, 1 \] n → RM, deve soddisfare i requisiti seguenti: interp (x) = BC (x) per tutte le x in S.

Nello scenario standard di interpolazione sul cubo di unità, S è il set di punti discreti che sono i vertici 2n del cubo.

È ora possibile generalizzare le condizioni limite per risolvere i problemi descritti in precedenza e fornire un nuovo algoritmo di interpolazione all'interno del cubo di unità. Anziché consentire solo punti di limite discreti, le condizioni di limite possono essere imposte su una faccia perimetrale intera del cubo. Le ipotesi esatte sono le seguenti:

(a) il punto VN = (1, 1,..., 1) è speciale ed è consentita solo una condizione di limite discreta. In altre parole, non è possibile imporre alcuna condizione di limite continuo ai bordi n, XI = 1 (i = 1,..., n).

(b) per ognuno dei restanti n limiti XI = 0 (i = 1,..., n), è possibile imporre la condizione di limite sull'intero quadrante, con la condizione di compatibilità che se due facce si intersecano, le condizioni limite sulle facce devono accettare l'intersezione.

(c) i vertici non inclusi nei visi con la condizione di limite avranno una singola condizione di limite (discreto).

È possibile fare riferimento a una condizione di limite discreta come dati limitati e una condizione di limite continuo come dati translimitati in discussione dell'interpolazione su dati finiti e transfiniti.

Esaminare prima di tutto l'interpolazione tetraedrica standard (come quella usata nel brevetto di Sakamoto), che consente di impostare le annotazioni per questa particolare formulazione del problema. È noto che il cubo di unità \[ 0, 1 \] n può essere suddiviso in n! tetraedri, con parametri per il set di permutazioni su n simboli. In particolare, ogni tetraedro viene definito dalle disuguaglianze

![Mostra la formula per il inequalites di tetraedri.](images/transformcreation-image073.gif)

dove σ: {1, 2,.., n} → {1, 2,..., n} è una permutazione di "symbols" 1, 2,..., n, ovvero un mapping bigettivo del set di n simboli. Ad esempio, se n = 3 e σ = (3, 2, 1), ovvero σ (1) = 3, σ (2) = 2, σ (3) = 1, il tetraedro corrispondente viene definito da z ≥ y ≥ x, in cui la notazione comune x, y, z viene utilizzata per X1, X2, X3. Si noti che queste tetraedri non sono disgiunte l'una dall'altra. Ai fini dell'interpolazione, i punti che si trovano su una faccia comune di due tetraedri distinti avranno lo stesso valore di interpolazione indipendentemente dal tetraedro usato nell'interpolazione. Tuttavia, nello scenario standard di interpolazione su punti finiti, per un punto di input specificato (x1,..., Xn), determinare prima di tutto il tetraedro in cui si trova o, in modo equivalente, la permutazione σ corrispondente, quindi il tetraedrica Interpol è definito come

![Mostra l'equazione che definisce la tetraedrica interpolata.](images/transformcreation-image075.png)

dove ![Mostra l'equazione per i vettori di base standard.](images/transformcreation-image077.png) per i = 1,..., n e E1,..., en sono i vettori di base standard. Prima di procedere alla generalizzazione, si noti che V0, V1,..., VN sono i vertici del tetraedro e ![Mostra le coordinate del baricentrica.](images/transformcreation-image079.png) sono le coordinate "baricentrica".

Per il caso generale di BCs sui visi limite, è possibile usare il concetto di proiezione baricentrica. Come prima, per un punto di input specificato (x1,..., Xn), determinare innanzitutto in quale tetraedro si trova o in modo equivalente la permutazione σ corrispondente. Eseguire quindi una serie di proiezioni baricentrica, come indicato di seguito. Prima proiezione ![Mostra BProj indice 1 (x).](images/transformcreation-image081.gif) Invia il punto al piano ![Mostra X Indice Delta (1) uguale a 0.](images/transformcreation-image083.gif) a meno che ![Mostra X uguale a V indice n.](images/transformcreation-image085.gif) in tal caso, non viene modificato. La definizione esatta della mappa BProj è definita nel modo seguente:

![Mostra l'equazione per la definizione precisa della BProj della mappa.](images/transformcreation-image087.png)

con ![Mostra l'equazione per l'indice P.](images/transformcreation-image089.png) e k = 1, 2,..., n.

Nel caso ![Mostra X è uguale a V indice n.](images/transformcreation-image085.gif) , è possibile arrestare, perché BC viene definito in VN da presupposto (a). Nel caso ![Mostra X non è uguale a V indice n.](images/transformcreation-image091.gif) , è chiaro che ![Mostra BProj indice 1 (X).](images/transformcreation-image081.gif) il componente σ (1) esimo è stato annientato. In altre parole, si trova su uno dei visi limite. Si tratta di una faccia su cui è definito BC, nel qual caso è possibile arrestare o eseguire un'altra proiezione baricentrica ![Mostra l'indice BProj 2 (X ').](images/transformcreation-image093.gif) dove ![Mostra X ' uguale a BProj indice 1 (X).](images/transformcreation-image095.gif) . E se ![Mostra X '' = Bproj indice 1 (X ').](images/transformcreation-image097.gif) si trova su una faccia in cui è definito BC, è possibile arrestare; in caso contrario, eseguire un'altra proiezione ![Mostra l'indice BProj 3 (X '').](images/transformcreation-image099.gif) . Poiché ogni proiezione annienta un componente, la dimensione effettiva diminuisce, in modo da essere certi che il processo debba arrestarsi. Nel peggiore dei casi, è possibile eseguire n proiezioni fino alla dimensione 0, ovvero i vertici del cubo, che in base al presupposto (c), si sa che BC verrà definito in.

Supponendo che siano state eseguite le proiezioni K, con

![Mostra un'equazione da usare supponendo che sia stata eseguita la proiezione K.](images/transformcreation-image101.png)

x (0) = x, il punto di input e BC viene definito in x (k). Rimuovere quindi le proiezioni definendo una serie di vettori di output:

![Mostra le equazioni per una serie di vettori di output.](images/transformcreation-image103.png)

dove ![Mostra l'equazione per l'apice Y (K).](images/transformcreation-image105.gif) e infine ottenere la risposta

![Mostra interp (x) uguale a y superscript (0).](images/transformcreation-image107.gif)

## <a name="worked-example"></a>Esempio di lavoro

![Diagramma che illustra un esempio di interpolazione lavorato con un cubo di unità.](images/transformcreation-image108.png)

**Figura 2:** Esempio di lavoro

Si consideri la situazione illustrata nella figura 2, dove n = 3, m = 1 ed è presente il BCs seguente:

(a) quattro BCs discreto sui vertici

(0, 0, 1): β001

(0, 1, 1): β011

(1, 0, 1): β 101

(1, 1,1): β 111

(b) A continuazione BC sulla faccia X3 = 0: F (x1, X2)

Calcolo \# 1: punto di input x = (0,8, 0,5, 0,2). Il tetraedro contenitore è associato alla permutazione &lt; 1, 2, 3 &gt; .

prima proiezione: ![Mostra l'equazione per la prima proiezione.](images/transformcreation-image110.png)

Questo è già presente nella faccia X3 = 0, quindi è possibile arrestare. La sostituzione con le versioni precedenti restituisce quindi

![Mostra la risposta per la prima proiezione.](images/transformcreation-image112.png) risposta.

Calcolo \# 2: punto di input x = (0,2, 0,5, 0,8). Il tetraedro contenitore è associato alla permutazione &lt; 3, 2, 1 &gt; .

prima proiezione: ![Mostra l'equazione per la prima proiezione del calcolo 2.](images/transformcreation-image113.png)

seconda proiezione: ![Mostra l'equazione per la seconda proiezione del calcolo 2.](images/transformcreation-image115.png)

terza proiezione: ![Mostra l'equazione per la terza proiezione del calcolo 2.](images/transformcreation-image117.png) , che si trova sulla superficie X3 = 0. La sostituzione con le versioni precedenti restituisce quindi

![Mostra le prime due equazioni per la sostituzione con le versioni precedenti.](images/transformcreation-image119.png)

![Mostra la terza equazione per la sostituzione con le versioni precedenti.](images/transformcreation-image123.png), ovvero la risposta finale.

## <a name="applications"></a>Applicazioni

*(a) interpolazione tetraedrica sequenziale*

![Diagramma che mostra l'interpolazione tetraedrica sequenziale.](images/transformcreation-image124.png)

**Figura 3:** Interpolazione tetraedrica sequenziale

Vedere la figura 3. Per eseguire l'interpolazione tra due piani su cui sono state imposte griglie incompatibili, prendere in considerazione una cella che include un punto specificato P illustrato nella figura. I vertici "Top" della cella provengono direttamente dalla griglia nel piano superiore. I vertici nella parte inferiore del quadrante non sono compatibili con la griglia nel piano inferiore, quindi l'intero viso viene considerato come avente un BC con i valori ottenuti dall'interpolazione sulla griglia nel piano in basso. È quindi chiaro che questa configurazione soddisfa i presupposti (a), (b) e (c) indicati in precedenza ed è possibile applicare l'algoritmo di interpolazione.

È inoltre chiaro che l'algoritmo ha ridotto la dimensione del problema di interpolazione di 1, perché il risultato è una combinazione lineare di valori ai vertici nella griglia superiore e l'interpolazione nel piano inferiore, con una dimensione minore di 1. Se nel piano inferiore esiste una configurazione simile a un piano di sandwich, è possibile applicare la procedura in tale piano, riducendone ulteriormente la dimensione di 1. Questa procedura può continuare fino a raggiungere la dimensione 0. Questa catena di proiezioni e interpolazioni può essere denominata "interpolazione tetraedrica sequenziale".

*(b) interpolazione Gap*

![Diagramma che mostra l'interpolazione del gap.](images/transformcreation-image126.jpg)

**Figura 4:** Interpolazione Gap

Si tratta di una griglia imposta su un cubo che si trova strettamente all'interno del quadrante positivo. Il cubo contiene una griglia e ogni piano coordinato dispone di griglie che non sono necessariamente compatibili. Il "gap" tra il cubo e i piani delle coordinate presenta una sezione incrociata che è "L-shaped" e non è suscettibile alle tecniche standard. Tuttavia, con la tecnica introdotta in questo articolo, è possibile introdurre facilmente le celle che coprono questo gap. Nella figura 4 viene illustrata una di queste. Le griglie sui piani delle coordinate supportano l'interpolazione che fornisce il BCs necessario per tutti i visi inferiori della cella, con un vertice rimanente il cui BC viene fornito dall'angolo inferiore del cubo.

## <a name="final-note-on-implementation"></a>Nota finale sull'implementazione

Nell'applicazione effettiva, il "cubo di unità" che rappresenta l'impostazione di base dell'algoritmo viene Estratto da reticoli più grandi e i valori nei vertici possono richiedere un calcolo oneroso. D'altra parte, è anche chiaro che l'interpolazione tetraedrica richiede solo i valori nei vertici del tetraedro, ovvero un subset di tutti i vertici del cubo di unità. Pertanto, è più efficiente implementare ciò che può essere definito "valutazione posticipata". In un'implementazione software dell'algoritmo precedente, in genere è presente una subroutine che accetta il cubo di unità e i valori nei vertici come input. La valutazione posticipata indica che anziché passare i valori nei vertici, le informazioni necessarie per valutare i valori dei vertici vengono passate, senza eseguire effettivamente la valutazione. All'interno della subroutine, la valutazione effettiva di questi valori verrà eseguita solo per i vertici che appartengono al tetraedro di inclusione, dopo che il tetraedro di inclusione è stato determinato.

## <a name="lookup-table-for-use-with-high-dynamic-range-virtual-rgb-source-devices"></a>Tabella di ricerca da usare con i dispositivi di origine RGB virtuali con intervallo dinamico elevato

Nel caso in cui una trasformazione venga costruita con un dispositivo di origine modellato come dispositivo RGB virtuale, è possibile che i valori coloranti di origine siano negativi o maggiori di Unity (1,0). In questo caso, il dispositivo di origine viene definito con un intervallo dinamico elevato (HDR). Per questo caso viene presa particolare attenzione.

Nel caso di trasformazioni HDR, i valori minimo e massimo per ogni canale colorante possono essere determinati dal limite della gamma del dispositivo. Usando questi valori, viene applicata una semplice scalabilità per ogni canale colorante, in modo che i valori coloranti uguali al colore minimo vengano convertiti in 0,0 e i valori coloranti uguali al colore massimo vengano convertiti in 1,0, con una scala lineare di valori tra per eseguire il mapping lineare tra 0,0 e 1,0.

### <a name="iccprofilefromwcsprofile"></a>ICCProfileFromWCSProfile

Poiché lo scopo principale di questa funzionalità è supportare le versioni precedenti a vista di Windows, è necessario generare i profili ICC della versione 2,2 come definito nella specifica ICC ICC. 1:1998-09. In alcuni casi (vedere la tabella seguente "dispositivo di base per il mapping della classe del profilo ICC"), è possibile creare un profilo ICC basato su una matrice o su TRC da un profilo WCS. In altri casi, il profilo ICC è costituito da LUTs. Il processo seguente descrive come creare AToB e BToA LUTs. Naturalmente, i profili ICC hanno anche altri campi. Alcuni dati possono essere derivati dal profilo WCS. Per altri dati, è necessario sviluppare impostazioni predefinite intelligenti. Il copyright verrà assegnato a Microsoft; Poiché si tratta di una tecnologia Microsoft utilizzata per creare il LUTs.

Questa progettazione dovrebbe funzionare per tutti i tipi di modelli di dispositivo, inclusi i plug-in. Fino a quando il plug-in ha un modello di dispositivo Baseline associato, è possibile determinare il tipo di dispositivo sottostante.

La parte difficile della creazione di un profilo ICC consiste nel creare le tabelle di ricerca AToB e BToA. Queste tabelle sono mappate tra lo spazio del dispositivo, ad esempio RGB o CMYK, e lo spazio di connessione del profilo (PC), che è una variante di CIELAB. Questo è fondamentalmente lo stesso del processo di gestione dei colori usato nella trasformazione CITE per eseguire il mapping dallo spazio del dispositivo allo spazio del dispositivo. Per eseguire la trasformazione è tuttavia necessario disporre delle informazioni seguenti.

1) Condizioni di visualizzazione dei riferimenti per i PC.

2) Gamut del PC di riferimento.

3) Modello di dispositivo che esegue la conversione tra i valori dei PC e colorimetria.

Il profilo WCS e la relativa camma associata vengono forniti come parametri. Esistono due modelli di dispositivo di base che eseguono la conversione tra colorimetria e la codifica PCS. Il motivo per cui sono necessarie due è illustrato di seguito.

1) È possibile ottenere le condizioni di visualizzazione dei riferimenti per i PC dalla specifica del formato del profilo ICC. Le informazioni fornite nella specifica del formato del profilo ICC sono sufficienti per calcolare tutti i dati necessari per inizializzare la camma usata dal CMS. Per coerenza e flessibilità, queste informazioni vengono archiviate in un profilo colori WCS.

2) È anche possibile usare un profilo WCS per archiviare esempi che definiscono la gamma di riferimento dei PC. Il sistema di gestione dei colori CITE (CMS) presenta due modi per creare i limiti della gamma. Uno consiste nel campionare lo spazio completo del dispositivo e utilizzare il modello di dispositivo per creare valori di misurazione. Il secondo metodo consiste nell'usare campioni misurati dal profilo per creare un limite di gamut di riferimento. Poiché la gamma dei PC ICC è troppo grande per creare una gamut di riferimento utile, il primo metodo non è appropriato. Il secondo metodo, tuttavia, è un approccio flessibile basato sul profilo. Per ridefinire il gamut dei PC di riferimento, è possibile modificare i dati di misurazione nel profilo del dispositivo PCS.

3) I PC ICC sono una modellazione di un dispositivo ideale. Creando un modello dei PC come un vero e proprio dispositivo, è possibile sfruttare i vantaggi del processo di gestione dei colori usato nella smart CMM. La creazione di un modello di dispositivo da colorimetria alla codifica dei PC è semplice. È sufficiente eseguire il mapping tra i valori di colorimetrico true e quelli codificati per i PC. Poiché l'interfaccia CMS per i modelli di dispositivo supporta solo i valori XYZ, potrebbe anche essere necessario eseguire il mapping tra XYZ e LAB. Si tratta di una trasformazione ben nota. Questo modello è descritto nel documento 2.2.02 "modelli di dispositivo di base" nelle sezioni 7,9 e 7,10.

Potrebbe essere necessario eseguire un mapping di gamut, se la gamma del dispositivo è maggiore della gamma dei PC. Per questo scopo è possibile usare il MGM di base. Si noti che un profilo ICC creato correttamente dispone di tabelle di ricerca per gli Intent di colorimetrico, percettivo e saturazione relativi, sebbene questi possano puntare allo stesso LUT internamente.

![Diagramma che illustra la creazione di un A T o B L U T.](images/transformcreation-image128.png)

**Figura 5:** Creazione di un LUT AToB

Questo processo è illustrato nella figura 5. In primo luogo, il modello di dispositivo viene inizializzato in base ai dati nel profilo DM. Quindi, costruire un limite di gamut del dispositivo come segue. Un campionamento dei dati dal modello di dispositivo viene eseguito tramite il modello di dispositivo per ottenere i dati colorimetrico. I dati colorimetrico vengono eseguiti attraverso la camma per creare dati di aspetto. I dati relativi all'aspetto vengono usati per creare il limite della gamma di dispositivi.

Usare quindi i dati del profilo di misurazione PC di riferimento per creare un limite di gamut per i PC.

Usare i due limiti di gamut appena creati per inizializzare un MGM. Usare quindi il modello di dispositivo, il MGM e il modello di dispositivo PCS per creare una trasformazione. Eseguire un campionamento dello spazio del dispositivo attraverso la trasformazione per creare un LUT AToB.

![Diagramma che illustra la creazione di un A T o B L U T usando un campionamento dello spazio P C.](images/transformcreation-image130.png)

**Figura 6:** Creazione di un LUT BToA

Nella figura 6 viene illustrata la creazione di LUT BToA. Questa operazione è quasi identica alla creazione di un LUT AToB con i ruoli di origine e di destinazione scambiati. Inoltre, è necessario campionare il gamut dei PC completi per creare il LUT.

Si noti che poiché la camma (CIECAM02 in WCS) è implicata nel processo, l'adattamento cromatico tra il punto bianco multimediale e il punto bianco dei PC (imposto da ICC come D50) viene applicato in modo trasparente dalla camma.

## <a name="hdr-virtual-rgb-devices&quot;></a>Dispositivi RGB virtuali HDR

È necessario prestare particolare attenzione durante la generazione di profili per i dispositivi RGB virtuali HDR; ovvero i dispositivi per i quali i valori coloranti possono essere inferiori a 0,0 o maggiori di 1,0. Nella generazione di ATOB LUT, viene compilato un set più ampio di LUTs di input 1D. I valori coloranti vengono ridimensionati e spostati nell'intervallo 0. 1 uso dei valori di colore minimo e massimo nel profilo WCS.

Poiché lo spazio colorante per i dispositivi HDR non è probabilmente completamente popolato, il supporto speciale viene fornito nel LUT 3D anche per il tag. Per gestire i colori nell'area popolata a bassa densità, i coloranti vengono ricodificati in modo che sia possibile ottenere l'estrapolazione oltre 0,0 e 1,0. L'intervallo usato è-1. + 4.

A causa del ridimensionamento applicato per LUT 3D, viene creato un set di output 1D LUTs per eseguire il mapping del risultato all'intervallo 0. 1.

## <a name=&quot;more-than-one-pcs&quot;></a>Più di un PC

Il TPI ha rilevato che uno dei PC non era sufficientemente flessibile per soddisfare tutti gli usi previsti di un CMS. Nella versione 4 della specifica del profilo, il TPI ha chiarito che esistono effettivamente due codifiche di PC. Uno viene usato per gli Intent colorimetrico; un altro viene usato per finalità percettive. (Nessun PC specificato per l'intento di saturazione. Il TPI ha lasciato ambiguo questa parte. I PC colorimetrico hanno una luminosità minima e massima specificata, ma i valori di Chroma e Hue variano approssimativamente a ± 127. Questi PC sembrano un prisma rettangolare. Come indicato in precedenza, il volume dei PC percettivi è simile alla gamma di una stampante a getto d'inchiostro.

Le due PCSs ICC hanno anche due codifiche digitali diverse. Nei PC percettivi, un valore pari a zero rappresenta una luminosità pari a zero. Nei PC colorimetrico, un valore pari a zero rappresenta la luminosità minima dei PC, che è maggiore di zero. Per risolvere questo problema, è necessario disporre di un modello di dispositivo diverso per ogni codifica dei PC.

## <a name=&quot;gamut-mapping&quot;></a>Mapping gamut

Per creare il LUTs di AToB in un profilo ICC, è possibile eseguire il mapping dal gamut del dispositivo allo spazio dei PC appropriato. Per creare il LUTs BToA, è necessario eseguire il mapping dallo spazio dei PC al gamut del dispositivo. Il mapping per il LUTs AToB è molto simile a quello usato in un CMS basato su misura. Per i PC percettivi, mappare la gamma plausibile del dispositivo al limite di gamut dei PC percettivi, usando il ritaglio o la compressione per tutti i colori fuori gamma. Per gli Intent di colorimetrico, potrebbe essere necessario ritagliare la luminosità, ma i valori di Chroma e Hue verranno tutti inseriti nel gamut dei PC colorimetrico.

Il mapping per il LUTs BToA è leggermente diverso. Gli Intent colorimetrico sono ancora facili; è sufficiente ritagliare i valori dei PC nel gamut del dispositivo. Tuttavia, il TPI richiede che tutti i valori dei PC possibili siano mappati a un valore di dispositivo, non solo quelli all'interno della gamma di riferimento dei PC percettivi. Pertanto, è necessario assicurarsi che MGM sia in grado di gestire i colori di origine che si trovano all'esterno della gamma di riferimento. Questo può essere gestito ritagliando tali colori al limite della gamma di dispositivi.

## <a name=&quot;baseline-device-to-icc-profile-class-mapping&quot;></a>Mapping della classe del profilo del dispositivo di base al profilo ICC



| Tipo di dispositivo Baseline              | Classe profilo ICC       | Commento                                                                      |
|-----------------------------------|-------------------------|-----------------------------------------------------------------------------|
| Dispositivo di acquisizione RGB                | Dispositivo di input (&quot;SCNR")   | I PC sono CIELAB. AToB0Tag è un dispositivo a PC con finalità colorimetrico relativa. |
| CRT, monitor LCD                  | Visualizza dispositivo ("mntr") | I PC sono CIE XYZ. Vedere quanto segue per la conversione del modello.                      |
| Proiettore RGB                     | Spazio colore ("SPAC")    | I PC sono CIELAB.                                                              |
| Stampante RGB e CMYK              | Dispositivo di output ("PRTR")  | I PC sono CIELAB.                                                              |
| Dispositivo virtuale RGB (caso non HDR) | Visualizza dispositivo ("mntr") | I PC sono CIE XYZ.                                                              |
| Dispositivo virtuale RGB (caso HDR)     | Spazio colore ("SPAC")    | I PC sono CIELAB.                                                              |



 

La conversione dei profili di monitoraggio non implica la compilazione di LUTs, ma consiste invece nella compilazione di un modello Matrix o TRC. Il modello usato in ICC è leggermente diverso da quello usato nella modellazione CRT o nel modello LCD di WCS in quanto manca il termine "correzione nera". ovvero:

Modello WCS: ![Mostra un modello W C S.](images/transformcreation-image132.png)

Modello ICC: ![Mostra un modello I C c.](images/transformcreation-image134.png)

La conversione dal modello WCS al modello ICC viene eseguita come indicato di seguito.

Definire nuove curve:

![Mostra una matrice per definire nuove curve.](images/transformcreation-image136.png)

Non si tratta di curve per la riproduzione di suoni perché non eseguono il mapping tra 1 e 1. La normalizzazione lo raggiungerà. Le definizioni finali del modello ICC sono le seguenti:

![Mostra le definizioni finali del modello i C c.](images/transformcreation-image138.png)

![Mostra la matrice finale per il modello I C c.](images/transformcreation-image140.png)

Per i dispositivi virtuali RGB non HDR, viene generato anche un profilo ICC di visualizzazione per l'efficienza dello spazio. In tal caso, la matrice di tristimolo *M ICC* può essere ottenuta direttamente dalle primarie del profilo WCS senza la conversione del modello precedente. Un aspetto finale, ma importante, è che questa matrice tristimolo deve essere adattata in modo cromatico a D50 per essere conforme alla specifica ICC dei PC. In altre parole, le voci in ogni riga della matrice da codificare nel profilo ICC devono essere sommate rispettivamente a 96,42, 100 e 82,49. Nell'implementazione corrente, l'adattamento cromatico viene eseguito da CAT02, che è anche la trasformazione di adattamento cromatico utilizzata in CAM02.

## <a name="black-preservation-and-black-generation"></a>Conservazione nera e generazione nera

L'implementazione della conservazione del nero è legata alla generazione del canale nero nei dispositivi che supportano un canale nero. A tale scopo, vengono raccolte le informazioni su ogni colore di origine per consentire ai modelli di dispositivo che supportano un canale nero di determinare il modo migliore per impostare il canale nero nell'output. Sebbene la conservazione nera sia pertinente per le trasformazioni dei colori che si convertono tra un dispositivo del canale nero e l'altro, la generazione nera viene implementata per tutte le trasformazioni che coinvolgono un dispositivo di destinazione del canale nero.

Le informazioni sul canale nero vengono registrate in una struttura di dati denominata [**BlackInformation**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation). La struttura **BlackInformation** contiene un valore booleano che indica se il colore contiene solo colori neri e un valore numerico che indica il grado di "nero" denominato peso nero. Per i dispositivi di origine che supportano un canale nero, il peso nero è la percentuale di colore nero nel colore di origine. Per i dispositivi di origine che non contengono un canale nero, il peso nero viene calcolato usando gli altri coloranti e il valore dell'aspetto. Un valore denominato "purezza colore" viene calcolato prendendo la differenza tra il valore colore massimo e il valore colore minimo diviso per il valore colore massimo. Un valore denominato "luminosità relativa" viene calcolato prendendo la differenza tra la luminosità del colore e la luminosità minima per il dispositivo di destinazione divisa per la differenza tra la luminosità minima e massima per il dispositivo di destinazione. Se il dispositivo di origine è un dispositivo additivo (monitor o proiettore), il peso nero viene determinato come 1,0 meno la purezza del colore moltiplicata per la luminosità relativa. Se ad esempio il dispositivo di origine è un monitor RGB, viene calcolato il valore massimo e il valore minimo di R, G e B per ogni colore e il peso nero è determinato dalla formula:

BW = (1,0 – (Max (R, G, B)-min (R, G, B))/Max (R, G, B)) \* luminosità relativa

Se il dispositivo di origine supporta la colorazione sottrattiva, ad esempio una stampante CMY, i singoli coloranti devono essere "quelli a complemento" (sottratti da 1,0) prima di essere utilizzati nella formula precedente. Per una stampante CMY, quindi, R = 1,0 – C, G = 1,0-M e B = 1,0 – Y.

Le informazioni nere per ogni colore elaborato dalla trasformazione colore vengono determinate durante il processo di conversione dei colori. Le informazioni solo nere vengono determinate solo se è stata specificata la conservazione nera. Il peso nero viene sempre determinato se il modello di dispositivo di destinazione supporta un colore nero. Le informazioni nere vengono passate al modello di dispositivo di destinazione tramite il metodo [**ColorimetricToDeviceColorsWithBlack**](/previous-versions/windows/desktop/api/WcsPlugIn/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack) , che usa il LUT risultante.

Si noti che, a causa dell'ottimizzazione della trasformazione dei colori, il processo precedente si verifica solo durante la creazione del LUT di trasformazione ottimizzato, non durante l'esecuzione del metodo TranslateColors.

## <a name="optimization-for-transforms-with-more-than-three-source-channels"></a>Ottimizzazione per le trasformazioni con più di tre canali di origine

La dimensione della trasformazione ottimizzata è determinata da diversi fattori: il numero di canali di colore nel dispositivo di origine, il numero di passaggi nella tabella per ogni canale di colore di origine e il numero di canali di colore nel dispositivo di output. La formula per determinare le dimensioni della tabella di trasformazione è:

Dimensioni = numero di passaggi per <sub>origine canale \ dispositivo (numero \ di \ canali \ in \ origine \ dispositivo)</sub> x numero di canali nel dispositivo di output

Come si può notare, le dimensioni della tabella aumentano esponenzialmente in base al numero di canali nel dispositivo di origine. Molti dispositivi di origine supportano tre canali di colore, ad esempio rosso, verde e blu. Tuttavia, se un dispositivo di origine supporta quattro canali, ad esempio CMYK, le dimensioni della tabella e il tempo necessario per costruire la tabella crescono in base a un fattore del numero di passaggi. In un CMS basato su misurazione, in cui le trasformazioni vengono costruite in modo immediato, questo tempo potrebbe non essere accettabile.

Per ridurre il tempo necessario per costruire la tabella di conversione dei colori, è possibile sfruttare i vantaggi di due fact. In primo luogo, mentre il dispositivo di origine può supportare più di tre canali di colore, lo spazio di colore intermedio indipendente dal dispositivo (CIECAM02 ja <sub>c</sub> b <sub>c</sub> ) ha solo tre canali colori. In secondo luogo, la parte più dispendiosa in termini di tempo dell'elaborazione non è la modellazione del dispositivo (conversione dalle coordinate dei colori del dispositivo ai valori tristimolo), ma il mapping della gamma. Usando questi fatti, è possibile creare una tabella di conversione dei colori preliminare che converte i colori nello spazio di colore indipendente dal dispositivo attraverso i passaggi di mapping gamut e infine, tramite il modello di colore del dispositivo di output. La costruzione di questa tabella è della dimensione tre. Si costruisce quindi la dimensione quattro tabella di conversione dei colori finale convertendo le combinazioni di colori di origine in spazio intermedio indipendente dal dispositivo e quindi, usando la tabella di conversione dei colori preliminare, completare la conversione nello spazio colore del dispositivo di output. Si riducono quindi i calcoli (numero di passaggi nella tabella di ricerca) <sub>Number \ of \ Channels</sub> gamut mapping computing al numero di passaggi della tabella intermedia ₃ gamut mapping mapping. Anche se è necessario eseguire un numero di passaggi nel numero di calcoli (tabella di ricerca) <sub>numero \ di</sub> calcoli dei canali per la modellazione del dispositivo e le ricerche di tabelle tridimensionali, questo è ancora molto più veloce rispetto al calcolo originale.

Il processo precedente funziona correttamente purché non siano necessarie informazioni da passare tra il modello di dispositivo di origine e qualsiasi altro componente nella trasformazione colore. Tuttavia, se il dispositivo di output e il dispositivo di origine supportano entrambi una colorazione nera e il colore nero di origine viene usato per determinare il colore nero di output, il processo non riuscirà a comunicare correttamente le informazioni nere di origine. Un processo alternativo consiste nel creare una tabella di conversione dei colori preliminare che converte i colori nello spazio di colore indipendente dal dispositivo solo attraverso i passaggi di mapping della gamma. Costruire quindi la dimensione quattro tabella di conversione dei colori finale usando la procedura seguente: a) convertire le combinazioni di colori di origine in spazio intermedio indipendente dal dispositivo, b) eseguire i passaggi di mapping di gamut eseguendo l'interpolazione nella tabella dei colori preliminare anziché applicare i processi di mapping di gamut effettivi e c) usare i valori risultanti dai passaggi di mapping gamut e da eventuali informazioni sul canale nero di origine per calcolare i coloranti del dispositivo di output usando il Questo processo può essere usato anche quando sono presenti informazioni trasferite tra i modelli di dispositivo di origine e di output anche se non è presente alcun canale nero; ad esempio, se i due moduli sono implementati con un'architettura plug-in che consente l'interscambio dei dati tra i moduli.

I due processi precedenti possono essere usati per migliorare efficacemente il tempo necessario per costruire la tabella di trasformazione dei colori a quattro dimensioni.

### <a name="checkgamut"></a>CheckGamut

ICM chiama CreateTransform e **CreateMultiProfileTransform** accettano una parola dei valori del flag, uno dei quali è enable \_ gamut \_ checking. Quando questo flag è impostato, CITE deve creare la trasformazione in modo diverso. I passaggi iniziali sono gli stessi: le camme di origine e di destinazione devono essere inizializzate, quindi è necessario inizializzare i descrittori di limite della gamma di origine e di destinazione. Indipendentemente dall'intento specificato, è necessario usare CheckGamut MGM. Il MGM di CheckGamut deve essere inizializzato usando i modelli di dispositivo di origine e di destinazione e i descrittori di limite della gamma. Tuttavia, la trasformazione deve quindi creare una trasformazione troncata che comprende il modello di dispositivo di origine, la camma di origine, eventuali MGM interattivi e CheckGamut MGM. Ciò garantisce che i valori Delta J, Delta C e Delta h restituiti dal CheckGamut CMM diventino i valori risultanti finali.

Il significato di CheckGamut è chiaro quando sono presenti solo due profili di dispositivo nella trasformazione. Quando sono presenti più di due profili di dispositivo e più di due MGM, CheckGamut segnala se i colori che sono stati trasformati tramite il primo modello di dispositivo e tutti gli ultimi MGM rientrano nella gamma del dispositivo di destinazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base sulla gestione dei colori](basic-color-management-concepts.md)
</dt> <dt>

[Schemi e algoritmi del sistema di colori Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




