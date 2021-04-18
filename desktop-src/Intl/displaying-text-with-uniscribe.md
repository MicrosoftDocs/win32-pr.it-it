---
description: Le applicazioni possono utilizzare le funzioni API Uniscribe per supportare la tipografia e la visualizzazione e la modifica del testo internazionale. Uniscribe usa il paragrafo come unità per la visualizzazione del testo ed è necessario usare la funzionalità Uniscribe per l'intero paragrafo.
ms.assetid: e1adc567-0445-4deb-8634-25653f82127c
title: Visualizzazione di testo con Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baeb9a2be4d00efaa2681097ddefe3a6de4c576b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348161"
---
# <a name="displaying-text-with-uniscribe"></a>Visualizzazione di testo con Uniscribe

Le applicazioni possono utilizzare le funzioni API Uniscribe per supportare la tipografia e la visualizzazione e la modifica del testo internazionale. Uniscribe usa il paragrafo come unità per la visualizzazione del testo ed è necessario usare la funzionalità Uniscribe per l'intero paragrafo.

Quando si usa Uniscribe per la visualizzazione del testo, un'applicazione deve passare attraverso un processo di formattazione ("layout"), in genere usando Uniscribe. L'applicazione divide un paragrafo di testo in stringhe di caratteri con lo stesso stile, denominato "esecuzioni". Lo stile è determinato dalla particolare implementazione, ma in genere include attributi come il tipo di carattere, la dimensione e il colore. Durante la definizione delle esecuzioni, l'applicazione può applicare anche altre informazioni, ad esempio la lingua e i dati delle impostazioni locali mantenuti per l'uso con gli strumenti lessicali. Un'applicazione, ad esempio, potrebbe trattare come un passaggio di esecuzione separato in un testo principalmente in lingua inglese di cui viene eseguito il rendering in francese.

Una volta determinate le esecuzioni per tutti i paragrafi, l'applicazione divide ogni paragrafo in stringhe con lo stesso script e la stessa direzione ("Items"). L'applicazione applica le informazioni relative agli elementi per produrre esecuzioni univoche in uno script e in una direzione e rientrare interamente all'interno di un singolo elemento ("intervalli").

La suddivisione di un elemento in intervalli è arbitraria, anche se un intervallo deve essere costituito da uno o più raggruppamenti consecutivi definiti dallo script e indivisibili, detti "cluster". Per le lingue europee, un cluster corrisponde in genere a un singolo carattere della tabella codici o a un punto di codice Unicode ed è costituito da un solo [glifo](uniscribe-glossary.md). Tuttavia, in linguaggi come Thai, un cluster è un raggruppamento di glifi e corrisponde a più caratteri consecutivi o a punti di codice. Un cluster tailandese, ad esempio, può contenere una consonante, una vocale e un segno di tono. In modo che non interrompa i cluster, l'applicazione in genere deve usare gli intervalli più lunghi che può o usare le proprie informazioni lessicali per suddividere gli intervalli in posizioni che non si trovano al centro di un cluster.

Quando i cluster sono stati identificati in ogni intervallo, l'applicazione deve determinare le dimensioni di ogni cluster. USA Uniscribe per sommare i cluster per determinare le dimensioni di ogni intervallo. Quindi, l'applicazione somma le dimensioni degli intervalli fino a quando non viene riversata una riga, ovvero raggiunge il margine. L'intervallo che trabocca la riga viene diviso tra la riga corrente e la riga successiva. Per ogni riga, l'applicazione compila una mappa dalla posizione visiva alla posizione logica per ogni intervallo. Quindi, l'applicazione consente di modellare i punti di codice per ogni intervallo in glifi, che possono quindi essere posizionati e sottoposto a rendering.

Un'applicazione esegue il layout del testo solo una volta. In seguito, Salva i glifi e le posizioni a scopo di visualizzazione oppure li genera ogni volta che viene visualizzato il testo, con un compromesso di velocità rispetto alla memoria. Un'applicazione tipica implementa il processo di layout una volta, quindi genera le icone e le posizioni ogni volta che viene visualizzato il testo.

Un'applicazione che utilizza [script complessi](uniscribe-glossary.md) presenta i seguenti problemi con un semplice approccio al layout e alla visualizzazione.

-   La larghezza di un carattere di script complesso dipende dal contesto. Non è possibile salvare le larghezze nelle tabelle semplici.
-   Per suddividere le parole negli script, ad esempio Thai, è necessario il supporto del dizionario. Ad esempio, non viene utilizzato alcun carattere separatore tra le parole tailandesi.
-   L'arabo, l'ebraico, il persiano, l'urdu e altre lingue di [testo bidirezionali](uniscribe-glossary.md) richiedono il riordinamento prima della visualizzazione.
-   Una forma di associazione di tipi di carattere è spesso necessaria per usare facilmente script complessi.

Il fatto che Uniscribe usi il paragrafo come unità di visualizzazione consente all'applicazione di occuparsi adeguatamente di questi complessi problemi di script.

> [!Note]  
> Uniscribe deve essere usato per un intero paragrafo, anche se le sezioni del paragrafo non sono script complessi.

 

Come illustrato nella tabella seguente, Uniscribe versione 1,6 o successiva supporta varie funzioni che sfruttano i tag OpenType. Possono essere sostituiti con le corrispondenti funzioni Uniscribe normali. In genere, le applicazioni dovrebbero funzionare interamente con le funzioni di un set o l'altra e non devono tentare di "combinare" e trovare la corrispondenza con le funzioni.



| Normale funzione Uniscribe             | Funzione OpenType equivalente                           |
|----------------------------------------|--------------------------------------------------------|
| [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) | [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) |
| [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)     | [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)     |
| [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)     | [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)     |



 

## <a name="lay-out-text-using-uniscribe"></a>Layout del testo con Uniscribe

L'applicazione può usare i passaggi seguenti per disporre un paragrafo di testo con Uniscribe. Questa procedura presuppone che l'applicazione abbia già diviso il paragrafo in esecuzioni.

1.  Chiamare [**ScriptRecordDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) solo all'avvio o alla ricezione di un messaggio [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) .
2.  Opzionale Chiamare [**ScriptIsComplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex) per determinare se il paragrafo richiede un'elaborazione complessa.
3.  Opzionale Se si usa Uniscribe per gestire il testo bidirezionale e/o la sostituzione di cifre, chiamare [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) per preparare le strutture di [**\_ controllo script**](/windows/win32/api/usp10/ns-usp10-script_control) e [**\_ stato script**](/windows/win32/api/usp10/ns-usp10-script_state) come input per [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize). Se si ignora questo passaggio, ma è ancora richiesta la sostituzione delle cifre, sostituire le cifre nazionali per Unicode U + 0030 con U + 0039 (cifre europee). Per informazioni sulla sostituzione di cifre, vedere [forme digit](digit-shapes.md).
4.  Chiamare [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) per dividere il paragrafo in elementi. Se non si utilizza Uniscribe per la sostituzione delle cifre e l'ordine bidirezionale è noto, ad esempio, a causa del layout della tastiera utilizzato per immettere il carattere, chiamare **ScriptItemize**. Nella chiamata, fornire puntatori null per le strutture [**di \_ controllo script**](/windows/win32/api/usp10/ns-usp10-script_control) e [**\_ stato script**](/windows/win32/api/usp10/ns-usp10-script_state) . Questa tecnica genera gli elementi solo usando il motore di shaping ed è possibile riordinare gli elementi usando le informazioni del motore.
    > [!Note]  
    > In genere, le applicazioni che funzionano solo con gli script da sinistra a destra e senza alcuna sostituzione di cifre devono passare i puntatori null per le strutture di [**\_ controllo script**](/windows/win32/api/usp10/ns-usp10-script_control) e [**\_ dello stato dello script**](/windows/win32/api/usp10/ns-usp10-script_state) .

     

5.  Unire le informazioni sull'elemento con le informazioni sull'esecuzione per produrre gli intervalli.
6.  Chiamare [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) per identificare i cluster e generare glifi.
7.  Se [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) restituisce lo script del codice USP \_ E \_ \_ non \_ \_ è in carattere o \_ OK con l'output che contiene glifi mancanti, selezionare i caratteri da un tipo di carattere diverso. Sostituire un altro tipo di carattere o disabilitare il data shaping impostando il membro **escript** della struttura di [**\_ analisi dello script**](/windows/win32/api/usp10/ns-usp10-script_analysis) passata a **ScriptShape** per lo script non \_ definito. Per ulteriori informazioni, vedere [utilizzo del fallback dei tipi di carattere](using-font-fallback.md).
8.  Chiamare [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) per generare le [larghezze di avanzamento](uniscribe-glossary.md) e le posizioni x e y per i glifi in ogni intervallo successivo. Questo è il primo passaggio per cui la dimensione del testo diventa una considerazione.
9.  Sommare le dimensioni dell'intervallo fino all'overflow della riga.
10. Suddividere l'intervallo su un confine di parola usando i membri **fSoftBreak** e **fWhiteSpace** negli attributi logici. Per interrompere l'esecuzione di un singolo cluster di caratteri, usare le informazioni restituite chiamando [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).
    > [!Note]  
    > Decidere se il primo punto di codice di un intervallo deve essere un punto di break Word perché l'ultimo carattere dell'intervallo precedente lo richiede. Se, ad esempio, un intervallo termina con una virgola, prendere in considerazione il primo carattere dell'intervallo successivo come punto di break di parole.

     

11. Ripetere i passaggi da 6 a 10 per ogni riga del paragrafo. Tuttavia, se si interrompe l'ultima esecuzione sulla riga, chiamare [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) per rimodellare la parte rimanente dell'esecuzione come la prima esecuzione nella riga successiva.

## <a name="display-text-using-uniscribe"></a>Visualizzare il testo con Uniscribe

L'applicazione può usare i passaggi seguenti per visualizzare un paragrafo di testo. Questa procedura presuppone che l'applicazione abbia già disposto il testo e non abbia salvato i glifi e le posizioni dal processo di layout. Se la velocità rappresenta un problema, l'applicazione può salvare i glifi e le posizioni dalla procedura di layout e iniziare dal passaggio 2 nella procedura di visualizzazione.

> [!Note]  
> L'applicazione può omettere il passaggio 2 Se il testo non contiene caratteri da script da destra a sinistra, non contiene caratteri di controllo bidirezionali e utilizza un livello di incorporamento di base da sinistra a destra.

 

1.  Per ogni esecuzione eseguire le operazioni seguenti:
    1.  Se lo stile è stato modificato dopo l'ultima esecuzione, aggiornare l'handle al contesto di dispositivo rilasciando e ottenendo nuovamente.
    2.  Chiamare [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) per generare glifi per l'esecuzione.
    3.  Chiamare [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) per generare una larghezza di avanzamento e un offset x, y per ogni glifo.
2.  Eseguire le operazioni seguenti per stabilire l'ordine visivo corretto per le esecuzioni nella riga:
    1.  Estrae una matrice di livelli di [incorporamento](uniscribe-glossary.md)bidirezionale, uno per ogni intervallo. Il livello di incorporamento è fornito da ( \_ elemento script) si. Analisi degli SCRIPT \_ ) a. (SCRIPT \_ STATO) s. uBidiLevel.
    2.  Passare questa matrice a [**ScriptLayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout) per generare una mappa delle posizioni visive in posizioni logiche.
3.  Opzionale Per giustificare il testo, chiamare [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify) o utilizzare una conoscenza specializzata del testo.
4.  Usare la mappa visiva-logica per visualizzare le esecuzioni in ordine visivo. A partire dall'estremità sinistra della riga, chiamare [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) per visualizzare l'esecuzione specificata dalla prima voce della mappa. Per ogni voce successiva nella mappa, chiamare **ScriptTextOut** per visualizzare l'esecuzione indicata a destra dell'esecuzione visualizzata in precedenza.

    Se si omette il passaggio 2, iniziare dall'estremità sinistra della riga e chiamare [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) per visualizzare la prima esecuzione logica e quindi per visualizzare ogni esecuzione logica a destra dell'esecuzione precedente.

5.  Ripetere i passaggi precedenti per tutte le righe nel paragrafo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
