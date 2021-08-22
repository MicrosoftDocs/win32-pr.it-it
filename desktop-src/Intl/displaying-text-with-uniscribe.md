---
description: Le applicazioni possono usare le funzioni DELL'API Uniscribe per supportare la tipografia e la visualizzazione e la modifica del testo internazionale. Uniscribe usa il paragrafo come unità per la visualizzazione del testo e la funzionalità Uniscribe deve essere usata per l'intero paragrafo.
ms.assetid: e1adc567-0445-4deb-8634-25653f82127c
title: Visualizzazione di testo con Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17caf7e7880a61bdf9afbaf6db5b60065b01d3d3960f2ed5629a007aa304b7b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949606"
---
# <a name="displaying-text-with-uniscribe"></a>Visualizzazione di testo con Uniscribe

Le applicazioni possono usare le funzioni DELL'API Uniscribe per supportare la tipografia e la visualizzazione e la modifica del testo internazionale. Uniscribe usa il paragrafo come unità per la visualizzazione del testo e la funzionalità Uniscribe deve essere usata per l'intero paragrafo.

Quando si usa Uniscribe per la visualizzazione del testo, un'applicazione deve eseguire un processo di formattazione ("layout"), in genere usando Uniscribe. L'applicazione divide un paragrafo di testo in stringhe di caratteri con lo stesso stile, denominato "runs". Lo stile è determinato dall'implementazione specifica, ma in genere include attributi quali tipo di carattere, dimensioni e colore. Nella definizione delle esecuzioni, l'applicazione può anche applicare altre informazioni, ad esempio la lingua e i dati delle impostazioni locali mantenuti per l'uso con strumenti lessicali. Ad esempio, un'applicazione potrebbe considerare come un'esecuzione separata un passaggio in un testo principalmente in inglese di cui viene eseguito il rendering in francese.

Dopo aver determinato le esecuzioni per tutti i paragrafi, l'applicazione divide ogni paragrafo in stringhe con lo stesso script e la stessa direzione ("elementi"). L'applicazione applica le informazioni sull'elemento per produrre esecuzioni univoche nello script e nella direzione e che rientrano interamente in un singolo elemento ("intervalli").

La suddivisione di un elemento in intervalli è un po' arbitraria, anche se un intervallo deve essere costituito da uno o più raggruppamenti consecutivi di caratteri indivisibile definiti da script, detti "cluster". Per le lingue europae, un cluster corrisponde in genere a un singolo carattere della tabella codici o punto di codice Unicode ed è costituito da un singolo [glifo](uniscribe-glossary.md). Tuttavia, in lingue come il thai, un cluster è un raggruppamento di glifi e corrisponde a più caratteri consecutivi o punti di codice. Ad esempio, un cluster thai potrebbe contenere una consonante, una vocale e un tono. In modo che non interrompa i cluster, l'applicazione in genere deve usare gli intervalli più lunghi che può o usare le proprie informazioni lessicali per suddividere gli intervalli in posizioni che non si trovano al centro di un cluster.

Dopo aver identificato i cluster in ogni intervallo, l'applicazione deve determinare le dimensioni di ogni cluster. Usa Uniscribe per sommare i cluster per determinare le dimensioni di ogni intervallo. L'applicazione somma quindi le dimensioni degli intervalli fino a quando non causano l'overflow di una riga, cio' raggiunge il margine. L'intervallo che causa l'overflow della riga viene diviso tra la riga corrente e la riga successiva. Per ogni riga, l'applicazione compila una mappa dalla posizione visiva alla posizione logica per ogni intervallo. L'applicazione modella quindi i punti di codice per ogni intervallo in glifi, di cui può successivamente posizionarsi ed eseguirne il rendering.

Un'applicazione esegue il layout del testo una sola volta. Successivamente, salva i glifi e le posizioni a scopo di visualizzazione o li genera ogni volta che visualizza il testo, con un compromesso tra velocità e memoria. Un'applicazione tipica implementa il processo di layout una sola volta, quindi genera i glifi e le posizioni ogni volta che visualizza il testo.

Un'applicazione che [usa script complessi](uniscribe-glossary.md) presenta i problemi seguenti con un approccio semplice al layout e alla visualizzazione.

-   La larghezza di un carattere di script complesso dipende dal contesto. Non è possibile salvare le larghezze nelle tabelle semplici.
-   L'interruzione tra le parole negli script, ad esempio il thai, richiede il supporto del dizionario. Ad esempio, tra le parole tailandesi non viene usato alcun carattere separatore.
-   Arabo, ebraico, persiano, Urdu e altre lingue di testo [bidirezionali](uniscribe-glossary.md) richiedono il riordinamento prima della visualizzazione.
-   Per usare facilmente script complessi è spesso necessaria una qualche forma di associazione dei tipi di carattere.

Il fatto che Uniscribe usi il paragrafo come unità di visualizzazione consente all'applicazione di gestire in modo adeguato questi complessi problemi di script.

> [!Note]  
> È necessario usare uniscribe per un intero paragrafo, anche se le sezioni del paragrafo non sono script complessi.

 

Come illustrato nella tabella seguente, Uniscribe versione 1.6 o successiva supporta diverse funzioni che sfruttano i tag OpenType. Possono essere sostituiti con le funzioni Uniscribe regolari corrispondenti. In genere le applicazioni devono funzionare interamente con le funzioni di un set o dell'altro e non devono tentare di combinare le funzioni.



| Funzione Uniscribe regolare             | Funzione OpenType equivalente                           |
|----------------------------------------|--------------------------------------------------------|
| [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) | [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) |
| [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)     | [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)     |
| [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)     | [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)     |



 

## <a name="lay-out-text-using-uniscribe"></a>Creare il testo con uniscribe

L'applicazione può usare la procedura seguente per creare il formato di un paragrafo di testo con Uniscribe. Questa procedura presuppone che l'applicazione abbia già diviso il paragrafo in esecuzioni.

1.  Chiamare [**ScriptRecordDigitSubstitution solo**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) all'avvio o alla ricezione di un [**messaggio WM \_ SETTINGCHANGE.**](../winmsg/wm-settingchange.md)
2.  (Facoltativo) Chiamare [**ScriptIsComplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex) per determinare se il paragrafo richiede un'elaborazione complessa.
3.  (Facoltativo) Se si usa Uniscribe per gestire la sostituzione bidirezionale di testo e/o cifra, chiamare [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) per preparare le strutture [**SCRIPT \_ CONTROL**](/windows/win32/api/usp10/ns-usp10-script_control) e [**SCRIPT \_ STATE**](/windows/win32/api/usp10/ns-usp10-script_state) come input per [**ScriptItemize.**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) Se si ignora questo passaggio, ma si richiede ancora la sostituzione delle cifre, sostituire le cifre nazionali con i caratteri Unicode da U+0030 a U+0039 (cifre Europae). Per informazioni sulla sostituzione delle cifre, vedere [Forme delle cifre.](digit-shapes.md)
4.  Chiamare [**ScriptItemize per**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) dividere il paragrafo in elementi. Se non si usa Uniscribe per la sostituzione di cifre e l'ordine bidirezionale è noto, ad esempio, a causa del layout di tastiera usato per immettere il carattere, chiamare **ScriptItemize**. Nella chiamata fornire puntatori Null per le [**strutture \_ SCRIPT CONTROL**](/windows/win32/api/usp10/ns-usp10-script_control) e [**SCRIPT \_**](/windows/win32/api/usp10/ns-usp10-script_state) STATE. Questa tecnica genera gli elementi solo usando il motore di data shaping e gli elementi possono essere riordinati usando le informazioni del motore.
    > [!Note]  
    > In genere, le applicazioni che funzionano solo con script da sinistra a destra e senza sostituzione di cifre devono passare puntatori Null per le strutture [**SCRIPT \_ CONTROL**](/windows/win32/api/usp10/ns-usp10-script_control) e [**SCRIPT \_ STATE.**](/windows/win32/api/usp10/ns-usp10-script_state)

     

5.  Unire le informazioni sull'elemento con le informazioni sull'esecuzione per produrre intervalli.
6.  Chiamare [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) per identificare i cluster e generare glifi.
7.  Se [**ScriptShape restituisce**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) il codice USP E SCRIPT NOT IN FONT o S OK con l'output contenente glifi mancanti, selezionare i caratteri da \_ un tipo di carattere \_ \_ \_ \_ \_ diverso. Sostituire un altro tipo di carattere o disabilitare il data shaping impostando il membro **eScript** della struttura [**SCRIPT \_ ANALYSIS**](/windows/win32/api/usp10/ns-usp10-script_analysis) passata a **ScriptShape** su SCRIPT \_ UNDEFINED. Per altre informazioni, vedere [Uso del fallback dei caratteri.](using-font-fallback.md)
8.  Chiamare [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) per [generare larghezze di](uniscribe-glossary.md) avanzamento e posizioni x e y per i glifi in ogni intervallo successivo. Questo è il primo passaggio per cui la dimensione del testo diventa un fattore da considerare.
9.  Sommare le dimensioni dell'intervallo fino all'overflow della riga.
10. Suddividere l'intervallo in un confine di parola usando i membri **fSoftBreak** e **fWhiteSpace** negli attributi logici. Per interrompere l'esecuzione di un cluster a carattere singolo, usare le informazioni restituite chiamando [**ScriptBreak.**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)
    > [!Note]  
    > Decidere se il primo punto di codice di un intervallo deve essere un punto di interruzione di parola perché l'ultimo carattere dell'intervallo precedente lo richiede. Ad esempio, se un intervallo termina con una virgola, considerare il primo carattere dell'intervallo successivo come punto di interruzione di parola.

     

11. Ripetere i passaggi da 6 a 10 per ogni riga del paragrafo. Tuttavia, se si interrompe l'ultima esecuzione sulla riga, chiamare [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) per modificare la forma della parte rimanente dell'esecuzione come prima esecuzione nella riga successiva.

## <a name="display-text-using-uniscribe"></a>Visualizzare il testo usando Uniscribe

L'applicazione può usare la procedura seguente per visualizzare un paragrafo di testo. Questa procedura presuppone che l'applicazione abbia già disposto il testo e non abbia salvato i glifi e le posizioni dal processo di layout. Se la velocità rappresenta un problema, l'applicazione può salvare i glifi e le posizioni dalla procedura di layout e iniziare dal passaggio 2 della procedura di visualizzazione.

> [!Note]  
> L'applicazione può omettere il passaggio 2 se il testo non contiene caratteri da script da destra a sinistra, non contiene caratteri di controllo bidirezionali e usa un livello di incorporamento di base da sinistra a destra.

 

1.  Per ogni esecuzione, eseguire le operazioni seguenti:
    1.  Se lo stile è stato modificato dall'ultima esecuzione, aggiornare l'handle al contesto di dispositivo rilasciandolo e ottenendolo nuovamente.
    2.  Chiamare [**ScriptShape per**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) generare glifi per l'esecuzione.
    3.  Chiamare [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) per generare una larghezza di avanzamento e un offset x,y per ogni glifo.
2.  Eseguire le operazioni seguenti per stabilire l'ordine visivo corretto per le esecuzioni nella riga :
    1.  Estrarre una matrice di livelli di incorporamento [bidirezionali,](uniscribe-glossary.md)uno per intervallo. Il livello di incorporamento viene fornito da (SCRIPT \_ ITEM) si.( SCRIPT \_ ANALYSIS) a. (SCRIPT) \_ STATE) s.uBidiLevel.
    2.  Passare questa matrice a [**ScriptLayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout) per generare una mappa delle posizioni visive alle posizioni logiche.
3.  (Facoltativo) Per giustificare il testo, chiamare [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify) o usare una conoscenza specializzata del testo.
4.  Usare la mappa da oggetto visivo a logico per visualizzare le esecuzioni in ordine visivo. A partire dall'estremità sinistra della riga, chiamare [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) per visualizzare l'esecuzione specificata dalla prima voce nella mappa. Per ogni voce successiva nella mappa, chiamare **ScriptTextOut** per visualizzare l'esecuzione indicata a destra dell'esecuzione visualizzata in precedenza.

    Se si omette il passaggio 2, iniziare dall'estremità sinistra della riga e chiamare [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) per visualizzare la prima esecuzione logica e quindi visualizzare ogni esecuzione logica a destra dell'esecuzione precedente.

5.  Ripetere i passaggi precedenti per tutte le righe del paragrafo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
