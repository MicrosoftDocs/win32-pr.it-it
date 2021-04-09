---
title: Informazioni sul modello a oggetti di testo
description: In questo argomento viene fornita una panoramica di alto livello di TOM.
ms.assetid: e304ec18-ec2e-4ea7-91c6-6f6ab63b72ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b934aab1cbd3dca932b58e4aa99498843cb8cc97
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047474"
---
# <a name="about-text-object-model"></a>Informazioni sul modello a oggetti di testo

Il modello a oggetti di testo (TOM) definisce un set di interfacce di manipolazione del testo supportate in vari gradi da diverse soluzioni di testo Microsoft, incluso il controllo Rich Edit. In questo argomento viene fornita una panoramica di alto livello di TOM. Vengono illustrati gli argomenti seguenti.

-   [Oggetti di TOM versione 2](#tom-version-2-objects)
-   [Convenzioni dell'interfaccia TOM](#tom-interface-conventions)
-   [Tipo tomBool](#the-tombool-type)
-   [Accumulo matematico e compilazione](#math-buildup-and-build-down)
-   [RTF TOM](#tom-rtf)
-   [Ricerca di testo RTF](#finding-rich-text)
-   [Accessibilità di TOM](#tom-accessibility)
    -   [Interfaccia da esecuzione tabella oggetti](#interface-from-running-object-table)
    -   [Interfaccia da messaggi della finestra](#interface-from-window-messages)
    -   [Metodi orientati all'accessibilità](#accessibility-oriented-methods)
-   [Set di corrispondenze di caratteri](#character-match-sets)

## <a name="tom-version-2-objects"></a>Oggetti di TOM versione 2

TOM versione 2 (TOM 2) estende il modello a oggetti testo originale; le nuove interfacce sono derivate da quelle precedenti. L'API TOM aggiornata include il supporto per le nuove proprietà di formato carattere e paragrafo, un modello di tabella, la selezione multipla e il supporto degli oggetti inline per Math e Ruby.

L'oggetto TOM 2 di livello superiore viene definito dall'interfaccia [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) , che dispone di metodi per la creazione e il recupero di oggetti di livello inferiore nella gerarchia di oggetti. Per l'elaborazione semplice del testo normale, è possibile ottenere un oggetto [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) da un oggetto **ITextDocument2** ed eseguire la maggior parte delle operazioni. Se è necessario aggiungere la formattazione Rich-Text, è possibile ottenere oggetti [**ITextFont2**](/windows/desktop/api/Tom/nn-tom-itextfont2) e [**ITextPara2**](/windows/desktop/api/Tom/nn-tom-itextpara2) da un oggetto **ITextRange2** . **ITextFont2** fornisce l'equivalente di programmazione della finestra di dialogo Format-font di Microsoft Word e **ITextPara2** fornisce l'equivalente della finestra di dialogo del formato di Word.

Oltre a questi tre oggetti di livello inferiore, TOM 2 ha un oggetto Selection ([**ITextSelection2**](/windows/win32/api/tom/nn-tom-itextselection2)), ovvero un oggetto [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) con l'evidenziazione della selezione e alcuni metodi orientati all'interfaccia utente.

Gli oggetti intervallo e selezione includono metodi orientati allo schermo che consentono ai programmi di esaminare il testo sullo schermo o sul testo che è possibile scorrere sullo schermo. Queste funzionalità consentono, ad esempio, di rendere il testo accessibile a utenti con visione disaccoppiata.

Ogni interfaccia con il suffisso 2 eredita dall'interfaccia corrispondente senza il suffisso 2. Ad esempio, [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) eredita da [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument).

Gli oggetti di TOM 2 hanno la seguente gerarchia.

``` syntax
ITextDocument2         Top-level editing object
    ITextRange2        Primary text interface: a range of text
        ITextFont2     Character-attribute interface
        ITextPara2     Paragraph-attribute interface
        ITextRow       Table interface
    ITextSelection2    Screen highlighted text range
        ITextRange2    Selection inherits all range methods
    ITextDisplays      Displays collection (not yet defined)
    ITextStrings       Rich-text strings collection
    ITextStoryRanges2  Enumerator for stories in document
```

Un oggetto [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) descrive uno o più intervalli contigui di testo denominati *storie*. Le storie rappresentano le varie parti di un documento, ad esempio il testo principale del documento, le intestazioni e i piè di pagina, le note a piè di pagina, le annotazioni e i rilievi Scratch di testo RTF. Una storia di blocco Scratch viene utilizzata per la conversione tra espressioni matematiche con formattazione lineare e un modulo predefinito. Quando si salva il contenuto di un intervallo che rappresenta l'origine della copia corrente quando il contenuto sta per essere modificato, viene usata anche una storia di blocco Scratch.

Un oggetto [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) viene definito dagli offset della posizione dei caratteri iniziale e finale e da un oggetto Story. Non esiste indipendentemente dall'oggetto storia padre, sebbene il testo possa essere copiato negli Appunti o in altre destinazioni. Un oggetto intervallo di testo è diverso dal foglio di calcolo e da altri oggetti intervallo, definiti da altri tipi di offset; ad esempio, riga/colonna o posizione grafica (x, y). Un oggetto intervallo di testo può modificare se stesso in diversi modi, può restituire un duplicato di se stesso e può essere ordinato di copiare le posizioni dei caratteri iniziale e finale e il puntatore della storia alla selezione corrente.

Un oggetto Story esplicito non è necessario, poiché è sempre possibile creare un oggetto [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange) per rappresentare una determinata storia. In particolare, l'oggetto [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) può creare un oggetto [**ITextStoryRanges**](/windows/desktop/api/Tom/nn-tom-itextstoryranges) per enumerare le storie nel documento in termini di intervalli con valori di posizione dei caratteri iniziale e finale che descrivono le storie complete (ad esempio, 0 e **tomForward**).

Con un oggetto [**ITextStoryRanges2**](/windows/desktop/api/Tom/nn-tom-itextstoryranges2) , non è necessario un oggetto Story esplicito, perché ogni storia è descritta da un oggetto [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) . In particolare, l'oggetto [**ITextDocument2**](/windows/desktop/api/tom/nn-tom-itextdocument2) può creare un oggetto [**ITextStoryRanges2**](/windows/desktop/api/tom/nn-tom-itextstoryranges2) per enumerare le storie nel documento in termini di intervalli con valori di posizione dei caratteri iniziale e finale che descrivono le storie complete (ad esempio, 0 e **tomForward**).

L'interfaccia [**ITextRow**](/windows/desktop/api/Tom/nn-tom-itextrow) insieme ai metodi [**ITextRange:: Move**](/windows/desktop/api/Tom/nf-tom-itextrange-move) e [**ITextRange:: Expand**](/windows/desktop/api/Tom/nf-tom-itextrange-expand) fornisce la possibilità di inserire, eseguire query e modificare le tabelle.

## <a name="tom-interface-conventions"></a>Convenzioni dell'interfaccia TOM

Tutti i metodi TOM restituiscono valori **HRESULT** . In generale, i metodi TOM restituiscono i valori standard seguenti.

-   E \_ OutOfMemory
-   E \_ INVALIDARG
-   E \_ NOTIMPL
-   E \_ FileNotFound
-   E \_ AccessDenied
-   E \_ non riescono
-   CO \_ E \_ rilasciato
-   NOERROR (uguale a S \_ OK)
-   S \_ false

Tenere presente che se l'istanza di modifica associata a un oggetto TOM, ad esempio [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange) , viene eliminata, l'oggetto Tom diventa inutile e tutti i relativi metodi restituiscono la co \_ E \_ rilasciata.

Oltre ai valori restituiti **HRESULT** , molti metodi includono parametri out, che sono puntatori usati per restituire valori. Per tutte le interfacce, è consigliabile controllare tutti i parametri del puntatore per assicurarsi che siano diversi da zero prima di utilizzarli. Se si passa un valore null a un metodo che richiede un puntatore valido, il metodo restituisce E \_ INVALIDARG. I puntatori facoltativi out con valori null vengono ignorati.

Usare i metodi con i prefissi get e set per ottenere e impostare le proprietà. Le variabili booleane utilizzano **tomFalse** (0) per **false** e **tomTrue** (-1) per **true**.

Le costanti di TOM sono definite nel tipo di enumerazione [**tomConstants**](/windows/win32/api/tom/ne-tom-tomconstants) e iniziano con il prefisso *Tom*, ad esempio **tomWord**.

## <a name="the-tombool-type"></a>Tipo tomBool

Molti metodi di TOM usano un tipo speciale di variabile denominata "tomBool" per gli attributi Rich-Text con stati binari. Il tipo tomBool è diverso dal tipo **booleano** perché può assumere quattro valori: **tomTrue**, **tomFalse**, **tomToggle** e **tomUndefined**. I valori **tomTrue** e **tomFalse** indicano true e false. Il valore **tomToggle** viene usato per impostare o disabilitare una proprietà. Il valore **tomUndefined** , più tradizionalmente denominato NINCH, è un valore speciale senza input e senza modifiche che funziona con Long, float e **COLORREF** s. Per le stringhe, **tomUndefined** (o NINCH) è rappresentato dalla stringa null. Per le operazioni di impostazione delle proprietà, l'utilizzo di **tomUndefined** non comporta la modifica della proprietà di destinazione. Per le operazioni di recupero delle proprietà, **tomUndefined** significa che i caratteri nell'intervallo hanno valori diversi (viene assegnata la casella di controllo in grigio nelle finestre di dialogo delle proprietà).

## <a name="math-buildup-and-build-down"></a>Accumulo matematico e compilazione

È possibile usare il metodo [**ITextRange2:: BuildUpMath**](/windows/desktop/api/Tom/nf-tom-itextrange2-buildupmath) per convertire le espressioni matematiche con formattazione lineare in versioni predefinite. Il metodo [**ITextRange2:: linearizzare**](/windows/desktop/api/Tom/nf-tom-itextrange2-linearize) esegue la conversione opposta, detta linearizzazione o compilazione, per convertire le versioni predefinite delle espressioni matematiche in formato lineare. La funzionalità di compilazione matematica è utile quando è necessario esportare testo normale o abilitare determinati tipi di modifica.

## <a name="tom-rtf"></a>RTF TOM

In TOM, lo scambio di testo RTF può essere eseguito tramite set di chiamate esplicite al metodo o da trasferimenti di testo RTF nel formato RTF (Rich Text Format). In questa sezione vengono fornite tabelle di parole di controllo RTF per le proprietà dei paragrafi e per le proprietà dei caratteri.

**Parole di controllo paragrafo di TOM RTF**

| Parola di controllo   | Significato                                                                                                                                                                                                                                                                        |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\ Fi *n*      | Rientro prima riga (il valore predefinito è zero).                                                                                                                                                                                                                                       |
| \\ mantenere        | Mantieni il paragrafo intatto.                                                                                                                                                                                                                                                         |
| \\ Mantieni       | Mantieni il paragrafo successivo.                                                                                                                                                                                                                                                  |
| \\ li *n*      | Rientro sinistro (il valore predefinito è zero).                                                                                                                                                                                                                                             |
| \\ NoLine      | Nessun numero di riga.                                                                                                                                                                                                                                                             |
| \\ nowidctlpar | Disattiva il controllo vedove/orfano.                                                                                                                                                                                                                                                 |
| \\ pagebb      | Interrompi pagina prima del paragrafo.                                                                                                                                                                                                                                                   |
| \\ par         | Nuovo paragrafo.                                                                                                                                                                                                                                                                 |
| \\ Pard        | Reimposta le proprietà di paragrafo predefinite.                                                                                                                                                                                                                                        |
| \\ QL          | Allineato a sinistra (impostazione predefinita).                                                                                                                                                                                                                                                    |
| \\ a matrice          | Allineamento a destra.                                                                                                                                                                                                                                                                 |
| \\ QJ          | Giustificato.                                                                                                                                                                                                                                                                     |
| \\ QC          | Centrato.                                                                                                                                                                                                                                                                      |
| \\ ri *n*      | Rientro destro (il valore predefinito è zero).                                                                                                                                                                                                                                            |
| \\ s *n*       | Stile *n*.                                                                                                                                                                                                                                                                     |
| \\ sa *n*      | Spazio dopo (il valore predefinito è zero).                                                                                                                                                                                                                                             |
| \\ SB *n*      | Spazio prima (il valore predefinito è zero).                                                                                                                                                                                                                                            |
| \\ SL *n*      | Se mancante o *n*= 1000, l'interlinea viene determinata dal carattere più alto nella riga (spaziatura a riga singola); Se *n*> zero, viene utilizzata almeno questa dimensione. Se *n* è < zero, \|  \| viene utilizzato esattamente n. L'interlinea è a più righe se \\ slmult 1 segue. |
| \\ slmult *m*  | Segue \\ SL. *m* = zero: almeno o esattamente la spaziatura di riga come descritto da \\ SL *n*. *m* = 1: spaziatura riga = *n*/240 volte interlinea a riga singola.                                                                                                                              |
| \\ TB *n*      | Posizione della scheda della barra, in twip, dal margine sinistro.                                                                                                                                                                                                                              |
| \\ tldot       | Punti di leader della scheda.                                                                                                                                                                                                                                                               |
| \\ tleq        | Segno di uguale del leader della scheda.                                                                                                                                                                                                                                                         |
| \\ tlhyph      | Trattino del leader della scheda.                                                                                                                                                                                                                                                            |
| \\ tlth        | Linea spessa direttrice scheda.                                                                                                                                                                                                                                                         |
| \\ tlul        | Sottolineatura scheda.                                                                                                                                                                                                                                                          |
| \\ TQC         | Scheda centrata.                                                                                                                                                                                                                                                                  |
| \\ tqdec       | Scheda decimale.                                                                                                                                                                                                                                                                   |
| \\ TQR         | Scarica-scheda a destra.                                                                                                                                                                                                                                                               |
| \\ TX *n*      | Posizione di tabulazione, in twip, dal margine sinistro.                                                                                                                                                                                                                                  |



 

**Parole di controllo del formato carattere di TOM RTF**

| Parola di controllo     | Significato                                                                                                                                                                                                                                  |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\ animazione *n* | Imposta il tipo di animazione su *n*.                                                                                                                                                                                                              |
| \\ b             | Grassetto.                                                                                                                                                                                                                                    |
| \\ tappi          | Tutti i caratteri maiuscoli.                                                                                                                                                                                                                            |
| \\ CF *n*        | Colore primo piano (il valore predefinito è **tomAutocolor**).                                                                                                                                                                                      |
| \\ cs *n*        | Stile carattere *n*.                                                                                                                                                                                                                     |
| \\ DN *n*        | Posizione di indice in mezzo (il valore predefinito è 6).                                                                                                                                                                                    |
| \\ EMBO          | In rilievo.                                                                                                                                                                                                                                |
| \\ f *n*         | Numero di carattere, *n* fa riferimento a una voce nella tabella dei tipi di carattere.                                                                                                                                                                                   |
| \\ FS *n*        | Dimensioni del carattere in due punti (il valore predefinito è 24).                                                                                                                                                                                            |
| \\ evidenzia *n* | Colore di sfondo (il valore predefinito è **tomAutocolor**).                                                                                                                                                                                      |
| \\ i             | Corsivo.                                                                                                                                                                                                                                  |
| \\ impr          | Impronta.                                                                                                                                                                                                                                 |
| \\ lang *n*      | Applica una lingua a un carattere. *n* è un numero corrispondente a una lingua. La \\ parola di controllo normale Reimposta la proprietà Language sul linguaggio definito da \\ deflange *n* nelle proprietà del documento.                             |
| \\ nosupersub    | Disattiva l'apice o l'indice.                                                                                                                                                                                                      |
| \\ OUTL          | Struttura.                                                                                                                                                                                                                                 |
| \\ pianura         | Reimposta le proprietà di formattazione dei caratteri su un valore predefinito definito dall'applicazione. Vengono reimpostate anche le proprietà di formattazione dei caratteri associate (descritte nella sezione proprietà dei caratteri associate nella specifica RTF). |
| \\ scaps         | Maiuscole minuscole.                                                                                                                                                                                                                          |
| \\ Shad          | Ombra.                                                                                                                                                                                                                                  |
| \\ Strike        | Barrato.                                                                                                                                                                                                                           |
| \\ Sub           | Applica gli indici a testo e riduce le dimensioni dei punti in base alle informazioni sui tipi di carattere.                                                                                                                                                          |
| \\ Super         | Applica superscript al testo e riduce le dimensioni dei punti in base alle informazioni sui tipi di carattere.                                                                                                                                                        |
| \\ UL            | Sottolineatura continua. \\ UL0 disattiva la sottostruttura.                                                                                                                                                                                  |
| \\ ULD           | Sottolineatura punteggiata.                                                                                                                                                                                                                        |
| \\ uldb          | Sottolineatura doppia.                                                                                                                                                                                                                        |
| \\ ulnone        | Arresta tutta la sottostruttura.                                                                                                                                                                                                                   |
| \\ ulw           | Sottolineatura di Word.                                                                                                                                                                                                                          |
| \\*n*        | Posizione di apice in mezzo (il valore predefinito è 6).                                                                                                                                                                                  |
| \\ v             | Testo nascosto.                                                                                                                                                                                                                             |



 

## <a name="finding-rich-text"></a>Ricerca di testo RTF

È possibile usare i metodi di TOM per trovare testo RTF come definito da un intervallo di testo. La ricerca di un testo RTF è spesso necessaria per l'elaborazione di Word, sebbene non sia mai stata soddisfatta in un elaboratore di testi "What You See is what you get" (WYSIWYG). Esiste ovviamente un dominio più ampio di corrispondenza di testo RTF che consente di ignorare alcune proprietà di formattazione dei caratteri (o includere la formattazione del paragrafo e/o il contenuto dell'oggetto), ma tali generalizzazioni esulano dall'ambito di questa sezione.

Uno scopo di questa funzionalità è utilizzare una finestra di dialogo di **ricerca** con testo RTF per definire il testo RTF che si desidera individuare in un documento. La finestra di dialogo verrà implementata utilizzando un controllo Rich Edit e verranno utilizzati i metodi TOM per eseguire la ricerca nel documento. È possibile copiare il testo RTF desiderato dal documento nella finestra di dialogo **trova** oppure immetterlo e formattarlo direttamente nella finestra di dialogo **trova** .

Nell'esempio seguente viene illustrato come utilizzare i metodi TOM per trovare testo contenente le combinazioni di formattazione dei caratteri esatta. L'algoritmo Cerca il testo normale nell'intervallo di corrispondenze, denominato `pr1` . Se il testo normale viene trovato, viene puntato da un intervallo di valutazione, denominato `pr2` . Quindi, vengono usati due intervalli di punti `prip1` di inserimento (e `prip2` ) per esaminare l'intervallo di valutazione confrontando la relativa formattazione dei caratteri con quella di `pr1` . Se corrispondono esattamente, l'intervallo di input (fornito da `ppr` ) viene aggiornato in modo da puntare al testo dell'intervallo di valutazione e la funzione restituisce il numero di caratteri nell'intervallo corrispondente. Due oggetti [**ITextFont**](/windows/desktop/api/Tom/nn-tom-itextfont) , `pf1` e `pf2` , vengono usati nel confronto di formattazione dei caratteri. Sono allegati agli intervalli di punti di inserimento `prip1` e `prip2` .


```
LONG FindRichText (
    ITextRange **ppr,             // Ptr to range to search
    ITextRange *pr1)              // Range with rich text to find
{
    BSTR        bstr;             // pr1 plain-text to search for
    LONG        cch;              // Text string count
    LONG        cch1, cch2;       // tomCharFormat run char counts
    LONG        cchMatch = 0;     // Nothing matched yet
    LONG        cp;               // Handy char position
    LONG        cpFirst1;         // pr1 cpFirst
    LONG        cpFirst2;         // pr2 cpFirst
    ITextFont  *    pf1, *pf      // Fonts corresponding to IPs prip1 and prip2
    ITextRange *pr2;              // Range duplicate to search with
    ITextRange *prip1, *prip      // Insertion points to walk pr1, pr2

    if (!ppr || !*ppr || !pr1)
        return E_INVALIDARG;

    // Initialize range and font objects used in search
    if ((*ppr)->GetDuplicate(&pr2)    != NOERROR ||
        pr1->GetDuplicate(&prip1)     != NOERROR ||
        pr2->GetDuplicate(&prip2)     != NOERROR ||
        prip1->GetFont(&pf1)          != NOERROR ||
        prip2->GetFont(&pf2)          != NOERROR ||
        pr1->GetText(&bstr)           != NOERROR )
    {
        return E_OUTOFMEMORY;
    }

    pr1->GetStart(&cpFirst1);

    // Keep searching till rich text is matched or no more plain-text hits
    while(!cchMatch && pr2->FindText(bstr, tomForward, 0, &cch) == NOERROR)
    {
        pr2->GetStart(&cpFirst2);                 // pr2 is a new trial range
        prip1->SetRange(cpFirst1, cpFirst1);      // Set up IPs to scan match
        prip2->SetRange(cpFirst2, cpFirst2);      //  and trial ranges

        while(cch > 0 &&
            pf1->IsEqual(pf2, NULL) == NOERROR)   // Walk match & trial ranges
        {                                         //  together comparing font
            prip1->GetStart(&cch1);               //  properties
            prip1->Move(tomCharFormat, 1, NULL);
            prip1->GetStart(&cp);
            cch1 = cp - cch1;                     // cch of next match font run

            prip2->GetStart(&cch2);
            prip2->Move(tomCharFormat, 1, NULL);
            prip2->GetStart(&cp);
            cch2 = cp - cch2;                      // cch of next trial font run

            if(cch1 < cch)                         // There is more to compare
            {
                if(cch1 != cch2)                   // Different run lengths:
                    break;                         //  no formatting match
                cch = cch - cch1;                  // Matched format run
            }
            else if(cch2 < cch)                    // Trial range format run too
                break;                             //  short

            else                                   // Both match and trial runs
            {                                      //  reach at least to match
                pr2->GetEnd(&cp);                  //  text end: rich-text match
                (*ppr)->SetRange(cpFirst2, cp)     // Set input range to hit
                cchMatch = cp - cpFirst2;          //  coordinates and return
                break;                             //  length of matched string
            }
        }
    }
    pr2->Release();
    prip1->Release();
    prip2->Release();
    pf1->Release();
    pf2->Release();
    SysFreeString(bstr);

    return cchMatch;
}
```



## <a name="tom-accessibility"></a>Accessibilità di TOM

TOM fornisce supporto per l'accessibilità tramite le interfacce [**ITextSelection**](/windows/desktop/api/Tom/nn-tom-itextselection) e [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange) . In questa sezione vengono descritti i metodi utili per l'accessibilità e il modo in cui un programma è in grado di determinare la posizione dello schermo *x*, *y* di un oggetto.

Poiché i programmi di accessibilità basati sull'interfaccia utente in genere funzionano con lo schermo e con il mouse, un problema comune è trovare l'interfaccia [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) corrispondente per la posizione del mouse corrente (in coordinate dello schermo). Le sezioni seguenti presentano due modi per determinare l'interfaccia appropriata:

-   [Tramite la tabella degli oggetti in esecuzione](#interface-from-running-object-table)
-   Tramite il messaggio [**em \_ GETOLEINTERFACE**](em-getoleinterface.md) , che funziona per le istanze Rich Edit a finestra, purché il client si trovi nello stesso spazio di processo (nessun *marshalling* necessario)

Per ulteriori informazioni, vedere la specifica di Microsoft Active Accessibility. Dopo aver ottenuto un oggetto da una posizione dello schermo, è possibile usare per un'interfaccia [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) e chiamare il metodo [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint) per ottenere un oggetto intervallo vuoto nel CP corrispondente alla posizione dello schermo.

### <a name="interface-from-running-object-table"></a>Interfaccia da esecuzione tabella oggetti

Una tabella degli oggetti in esecuzione (ROT) indica le istanze dell'oggetto attive. Eseguendo una query su questa tabella, è possibile accelerare il processo di connessione di un client a un oggetto quando l'oggetto è già in esecuzione. Prima che i programmi possano accedere alle interfacce di TOM tramite la tabella degli oggetti in esecuzione, un'istanza di TOM con una finestra deve essere registrata in ROT usando un moniker. Il moniker viene costruito da una stringa contenente il valore esadecimale del relativo [**HWND**](/windows/desktop/WinProg/windows-data-types). Nell'esempio di codice riportato di seguito viene illustrato come eseguire questa operazione.


```
// This TOM implementation code is executed when a new windowed 
// instance starts up. 
// Variables with leading underscores are members of this class.

HRESULT hr;
OLECHAR szBuf[10];            // Place to put moniker
MONIKER *pmk;

hr = StringCchPrintf(szBuff, 10, "%x", _hwnd);
if (FAILED(hr))
{
    //
    // TODO: write error handler
    //
}
CreateFileMoniker(szBuf, &pmk);
OleStdRegisterAsRunning(this, pmk, &_dwROTcookie);
....................
 
// Accessibility Client: 
//    Find hwnd for window pointed to by mouse cursor.

GetCursorPos(&pt);
hwnd = WindowFromPoint(pt);

// Look in ROT (running object table) for an object attached to hwnd

hr = StringCchPrintf(szBuff, 10, "%x", hwnd);
if (FAILED(hr))
{
    //
    // TODO: write error handler
    //
}
CreateFileMoniker(szBuf, &pmk);
CreateBindContext(0, &pbc);
pmk->BindToObject(pbc, NULL, IID_ITextDocument, &pDoc);
pbc->Release();

if( pDoc )
{
    pDoc->RangeFromPoint(pt.x, pt.y, &pRange);
    // ...now do whatever with the range pRange
}
```



### <a name="interface-from-window-messages"></a>Interfaccia da messaggi della finestra

Il [**messaggio \_ GETOLEINTERFACE em**](em-getoleinterface.md) fornisce un altro modo per ottenere un'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) per un oggetto in una determinata posizione dello schermo. Come descritto in [interfaccia da esecuzione tabella oggetti](#interface-from-running-object-table), si ottiene un [**HWND**](/windows/desktop/WinProg/windows-data-types) per la posizione dello schermo e quindi si invia questo messaggio a tale **HWND**. Il **messaggio \_ GETOLEINTERFACE em** è specifico per le modifiche complete e restituisce un puntatore a un'interfaccia [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) nella variabile a cui è associato *lParam*.

**Suggerimento** Se viene restituito un puntatore (assicurarsi di impostare l'oggetto su cui *lParam* fa riferimento a null prima di inviare il messaggio), è possibile chiamare il relativo metodo [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere un'interfaccia [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) . Il seguente esempio di codice illustra questo approccio.


```
    HWND    hwnd;
    ITextDocument *pDoc;
    ITextRange *pRange;
    POINT    pt;
    IUnknown *pUnk = NULL;
    
    GetCursorPos(&pt);
    hwnd = WindowFromPoint(pt);
    SendMessage(hwnd, EM_GETOLEINTERFACE, 0, (LPARAM)&pUnk);
    if(pUnk && 
        pUnk->QueryInterface(IID_ITextDocument, &pDoc) == NOERROR)
    {
        pDoc->RangeFromPoint(pt.x, pt.y, &pRange);
        //  ... continue with rest of program
    }
```



### <a name="accessibility-oriented-methods"></a>Metodi orientati all'accessibilità

Alcuni metodi di TOM sono particolarmente utili per spostarsi sullo schermo, mentre altri metodi TOM migliorano le operazioni che è possibile eseguire quando si arriva a luoghi di interesse. Nella tabella seguente vengono descritti i metodi più utili.



| Metodo                                                 | Promozione dell'accessibilità                                                                                                                                                                 |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSelection**](/windows/desktop/api/Tom/nf-tom-itextdocument-getselection)     | Questo metodo ottiene la selezione attiva che può essere utilizzata per diversi scopi orientati alla visualizzazione, ad esempio l'evidenziazione del testo e dello scorrimento.                                                      |
| [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint) | Quando viene usato in una selezione attiva, questo metodo garantisce l'ottenimento di un intervallo associato a una visualizzazione specifica.                                                                                 |
| [**Espandere**](/windows/desktop/api/Tom/nf-tom-itextrange-expand)                    | Ingrandisce un intervallo di testo in modo che tutte le unità parziali contenute siano completamente contenute. Ad esempio, `Expand(tomWindow)` espande l'intervallo per includere la parte visibile della storia dell'intervallo. |
| [**Getduplicato**](/windows/desktop/api/Tom/nf-tom-itextrange-getduplicate)        | Quando viene usato in una selezione attiva, questo metodo garantisce l'ottenimento di un intervallo associato a una visualizzazione specifica. Vedere la descrizione di [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint).  |
| [**GetPoint**](/windows/desktop/api/Tom/nf-tom-itextrange-getpoint)                | Ottiene le coordinate dello schermo per la posizione del carattere iniziale o finale nell'intervallo di testo.                                                                                                        |
| [**ScrollIntoView**](/windows/desktop/api/Tom/nf-tom-itextrange-scrollintoview)    | Scorre un intervallo di testo nella visualizzazione.                                                                                                                                                               |
| [**SetPoint**](/windows/desktop/api/Tom/nf-tom-itextrange-setpoint)                | Seleziona il testo in corrispondenza di un punto specificato o verso l'alto.                                                                                                                                              |



 

## <a name="character-match-sets"></a>Set di corrispondenze di caratteri

Il parametro *Variant* dei vari metodi di **spostamento** \* in [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange), ad esempio [**MoveWhile**](/windows/desktop/api/Tom/nf-tom-itextrange-movewhile) e [**MoveUntil**](/windows/desktop/api/Tom/nf-tom-itextrange-moveuntil), può assumere una stringa esplicita o un indice a 32 bit di corrispondenza caratteri. Gli indici vengono definiti da intervalli Unicode o set di caratteri [**GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw) . L'intervallo Unicode a partire da *n* e di lunghezza *l* (< 32768) viene fornito dall'indice *n* + (*l <*< 16) + 0x80000000. Le lettere greche di base, ad esempio, sono definite da CR \_ Greek = 0x805f0370 e i caratteri ASCII stampabili sono definiti da CR \_ ASCIIPrint = 0x805e0020. Inoltre, i metodi **MoveWhile** e **MoveUntil** consentono di ignorare rapidamente un intervallo di caratteri in qualsiasi set di caratteri **GetStringTypeEx** o in un intervallo di caratteri che non si trova in uno di questi set di caratteri.

I set di [**GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw) sono specificati dai valori di *Ctype1*, *Ctype2* e *Ctype3* e sono definiti nel modo seguente.



| Cset                 | Significato                          |
|----------------------|----------------------------------|
| *Ctype1*             | Combinazione di \_ tipi di CTYPE1 CT. |
| *Ctype2* + tomCType2 | Qualsiasi \_ tipo di CTYPE2 CT.             |
| *Ctype3* + tomCType3 | Combinazione di \_ tipi di CTYPE3 CT. |



 

In particolare, *Ctype1* può essere una qualsiasi combinazione dei seguenti elementi.



| Nome Ctype1 | Valore  | Significato                                                           |
|-------------|--------|-------------------------------------------------------------------|
| C1 \_ superiore   | 0x0001 | Maiuscolo.                                                        |
| C1 \_ inferiore   | 0x0002 | Minuscolo.                                                        |
| \_Cifra C1   | 0x0004 | Cifre decimali.                                                   |
| \_Spazio C1   | 0x0008 | Caratteri spazio.                                                 |
| \_Punct C1   | 0x0010 | Punteggiatura.                                                      |
| \_Tasti CTRL C1   | 0x0020 | Caratteri di controllo.                                               |
| C1 \_ vuoto   | 0x0040 | Caratteri vuoti.                                                 |
| \_XDIGIT C1  | 0x0080 | Cifre esadecimali.                                               |
| \_Alfa C1   | 0x0100 | Qualsiasi carattere linguistico (alfabetico, sillabario o ideogrammi). |
| C1 \_ definito | 0x0200 | Un carattere definito, ma non uno degli altri tipi C1 \_ \* .       |



 

I tipi *Ctype2* supportano il layout appropriato del testo Unicode. Gli attributi di direzione vengono assegnati in modo che l'algoritmo di layout bidirezionale standardizzato da Unicode produca risultati accurati. Questi tipi si escludono a vicenda. Per ulteriori informazioni sull'utilizzo di questi attributi, vedere la pagina relativa *allo standard Unicode: codifica dei caratteri in tutto il mondo, volumi 1 e 2*, Addison-Wesley società di pubblicazione: 1991, 1992.



| Nome CType2          | Valore | Significato                          |
|----------------------|-------|----------------------------------|
| Forte              |       |                                  |
| \_LEFTTORIGHT C2      | 0x1   | Da sinistra a destra.                   |
| \_RightToLeft C2      | 0x2   | Da destra a sinistra.                   |
| Debole                |       |                                  |
| \_EUROPENUMBER C2     | 0x3   | Numero europeo, cifra europea. |
| \_EUROPESEPARATOR C2  | 0x4   | Separatore numerico europeo.      |
| \_EUROPETERMINATOR C2 | 0x5   | Terminatore numerico europeo.     |
| \_ARABICNUMBER C2     | 0x6   | Numero arabo.                   |
| \_COMMONSEPARATOR C2  | 0x7   | Separatore numerico comune.        |
| Indipendente dalla             |       |                                  |
| \_BLOCKSEPARATOR C2   | 0x8   | Separatore di blocco.                 |
| \_SEGMENTSEPARATOR C2 | 0x9   | Separatore di segmenti.               |
| \_Spazi vuoti C2       | 0xA   | Spazio vuoto.                     |
| \_OTHERNEUTRAL C2     | 0xB   | Altri tipi neutri.                  |
| Non applicabile:      |       |                                  |
| \_NONAPPLICABILE C2    | 0x0   | Nessuna direzione implicita.           |



 

I tipi *Ctype3* sono intesi come segnaposto per le estensioni ai tipi POSIX richiesti per l'elaborazione generale del testo o per le funzioni della libreria C standard.



| Nome CType3       | Valore  | Significato                                                             |
|-------------------|--------|---------------------------------------------------------------------|
| Non \_ spaziatura C3    | 0x1    | Contrassegno senza spaziatura.                                                    |
| \_Segni diacritici C3     | 0x2    | Segno di non spaziatura diacritici.                                          |
| \_VOWELMARK C3     | 0x4    | Segno di non spaziatura vocale.                                              |
| \_Simbolo C3        | 0x8    | Simbolo.                                                             |
| \_Katakana C3      | 0x10   | Carattere katakana.                                                 |
| \_Hiragana C3      | 0x20   | Carattere hiragana.                                                 |
| \_Carattere C3     | 0x40   | Carattere a metà larghezza.                                               |
| \_Fullwidth C3     | 0x80   | Carattere a larghezza intera.                                               |
| \_Ideogramma C3     | 0x100  | Carattere ideogrammi.                                              |
| \_KASHIDA C3       | 0x200  | Carattere kashida arabo.                                           |
| \_Alfa C3         | 0x8000 | Tutti i caratteri linguistici (alfabetici, sillabari e ideogrammi). |
| \_NONAPPLICABILE C3 | 0x0    | Non applicabile.                                                     |



 

Un EDK (Edit Development Kit) può includere definizioni di indice *pvar* per gli intervalli seguenti descritti nello standard Unicode.



| Set di caratteri         | Intervallo Unicode | Set di caratteri             | Intervallo Unicode |
|-----------------------|---------------|---------------------------|---------------|
| ASCII                 | 0x0-0x7F      | ANSI                      | 0x0-0xFF      |
| ASCIIPrint            | 0x20-0x7E     | Latin1                    | 0x20-0xFF     |
| Latin1Supp            | messaggi 0XA0-0xFF     | LatinXA                   | 0x100-0x17f   |
| LatinXB               | 0x180—0x24f   | IPAX                      | 0x250-0x2af   |
| SpaceMod              | 0x2b0—0x2ff   | Combinando                 | 0x300-0x36f   |
| Greco                 | 0x370-0x3FF   | BasicGreek                | 0x370—0x3cf   |
| GreekSymbols          | 0x3d0-0x3FF   | Cirillico                  | 0x400-0x4ff   |
| Armeno              | 0x530—0x58f   | Ebraico                    | 0x590—0x5ff   |
| BasicHebrew           | 0x5d0—0x5ea   | HebrewXA                  | 0x590—0x5cf   |
| HebrewXB              | 0x5eb—0x5ff   | Arabo                    | 0x600-0x6ff   |
| BasicArabic           | 0x600-0x652   | ArabicX                   | 0x653—0x6ff   |
| Devangari             | 0x900—0x97f   | Bangla (in precedenza Bengali) | 0x980—0x9ff   |
| Gurmukhi              | 0xa00—0xa7f   | Gujarati                  | 0xa80—0xaff   |
| Odia (in precedenza Oriya) | 0xb00—0xb7f   | Tamil                     | 0xb80—0xbff   |
| Teluga                | 0xc00—0xc7f   | Kannada                   | 0xc80-0xcff   |
| Malayalam             | 0xd00—0xd7f   | Thai                      | 0xe00—0xe7f   |
| Lao                   | 0xe80—0xeff   | GeorgianX                 | 0x10a0—0xa0cf |
| BascGeorgian          | 0x10d0—0x10ff | Jamo                      | 0x1100—0x11ff |
| LatinXAdd             | 0x1e00—0x1eff | GreekX                    | 0x1f00—0x1fff |
| GenPunct              | 0x2000-0x206f | Apice               | 0x2070—0x207f |
| Pedice             | 0x2080—0x208f | SuperSubscript            | 0x2070—0x209f |
| Valuta              | 0x20a0—0x20cf | CombMarkSym               | 0x20d0—0x20ff |
| Alfabetici            | 0x2100—0x214f | NumberForms               | 0x2150—0x218f |
| Frecce                | 0x2190—0x21ff | MathOps                   | 0x2200—0x22ff |
| MiscTech              | 0x2300—0x23ff | CtrlPictures              | 0x2400—0x243f |
| OptCharRecog          | 0x2440—0x245f | EnclAlphaNum              | 0x2460—x24ff  |
| BoxDrawing            | 0x2500—0x257f | BlockElement              | 0x2580—0x259f |
| GeometShapes          | 0x25a0—0x25ff | MiscSymbols               | 0x2600—0x26ff |
| Dingbat              | 0x2700—0x27bf | CJKSymPunct               | 0x3000-0x303f |
| Hiragana              | 0x3040—0x309f | Katakana                  | 0x30a0—0x30ff |
| Bopomofo              | 0x3100—0x312f | HangulJamo                | 0x3130—0x318f |
| CJLMisc               | 0x3190—0x319f | EnclCJK                   | 0x3200—0x32ff |
| CJKCompatibl          | 0x3300—0x33ff | Han                       | 0x3400—0xabff |
| Hangul                | 0xac00—0xd7ff | UTF16Lead                 | 0xD800-0xDBFF |
| UTF16Trail            | 0xDC00-0xDFFF | PrivateUse                | 0xE000-0xf800 |
| CJKCompIdeog          | 0xf900—0xfaff | AlphaPres                 | 0xfb00—0xfb4f |
| ArabicPresA           | 0xfb50—0xfdff | CombHalfMark              | 0xfe20—0xfe2f |
| CJKCompForm           | 0xfe30—0xfe4f | SmallFormVar              | 0xfe50—0xfe6f |
| ArabicPresB           | 0xfe70—0xfefe | HalfFullForm              | 0xff00—0xffef |
| Speciali              | 0xFFF0-0xFFFD |                           |               |



 

 

 