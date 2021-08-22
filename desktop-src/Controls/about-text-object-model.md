---
title: Informazioni sul modello a oggetti di testo
description: Questo argomento offre una panoramica generale di TOM.
ms.assetid: e304ec18-ec2e-4ea7-91c6-6f6ab63b72ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ec5c2f4156e7afce8765626a475a9b922ec428826d90789752c86f51bd69513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079449"
---
# <a name="about-text-object-model"></a>Informazioni sul modello a oggetti di testo

Il modello TOM (Text Object Model) definisce un set di interfacce di manipolazione del testo supportate in vari gradi da diverse soluzioni di testo Microsoft, incluso il controllo Rich Edit. Questo argomento offre una panoramica generale di TOM. Vengono illustrati gli argomenti seguenti.

-   [Oggetti TOM versione 2](#tom-version-2-objects)
-   [Convenzioni dell'interfaccia TOM](#tom-interface-conventions)
-   [Tipo tomBool](#the-tombool-type)
-   [Compilazione matematica e compilazione](#math-buildup-and-build-down)
-   [TOM RTF](#tom-rtf)
-   [Ricerca di testo RTF](#finding-rich-text)
-   [Accessibilità tom](#tom-accessibility)
    -   [Interfaccia dalla tabella di oggetti in esecuzione](#interface-from-running-object-table)
    -   [Interfaccia dai messaggi di finestra](#interface-from-window-messages)
    -   [Metodi orientati all'accessibilità](#accessibility-oriented-methods)
-   [Set di corrispondenze di caratteri](#character-match-sets)

## <a name="tom-version-2-objects"></a>Oggetti TOM versione 2

TOM versione 2 (TOM 2) estende il modello a oggetti di testo originale; Le nuove interfacce derivano da quelle precedenti. L'API TOM aggiornata include il supporto per le nuove proprietà del formato carattere e paragrafo, un modello di tabella, la selezione multipla e il supporto degli oggetti inline per matematica e ruby.

L'oggetto TOM 2 di primo livello è definito [**dall'interfaccia ITextDocument2,**](/windows/desktop/api/Tom/nn-tom-itextdocument2) che dispone di metodi per la creazione e il recupero di oggetti più in basso nella gerarchia di oggetti. Per una semplice elaborazione di testo normale, è possibile ottenere un [**oggetto ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) da un **oggetto ITextDocument2** ed eseguire la maggior parte delle operazioni. Se è necessario aggiungere la formattazione RTF, è possibile ottenere gli oggetti [**ITextFont2**](/windows/desktop/api/Tom/nn-tom-itextfont2) e [**ITextPara2**](/windows/desktop/api/Tom/nn-tom-itextpara2) da un **oggetto ITextRange2.** **ITextFont2 fornisce** l'equivalente di programmazione della finestra di dialogo formato-carattere di Microsoft Word e **ITextPara2** fornisce l'equivalente della finestra di dialogo formato-paragrafo di Word.

Oltre a questi tre oggetti di livello inferiore, TOM 2 ha un oggetto di selezione ([**ITextSelection2**](/windows/win32/api/tom/nn-tom-itextselection2)), che è un [**oggetto ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) con evidenziazione della selezione e alcuni metodi orientati all'interfaccia utente.

Gli oggetti intervallo e selezione includono metodi orientati allo schermo che consentono ai programmi di esaminare il testo sullo schermo o il testo che è possibile scorrere sullo schermo. Queste funzionalità consentono, ad esempio, di rendere il testo accessibile a persone con problemi di vista.

Ogni interfaccia con il suffisso 2 eredita dall'interfaccia corrispondente senza il suffisso 2. Ad esempio, [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) eredita da [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument).

Gli oggetti TOM 2 hanno la gerarchia seguente.

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

Un [**oggetto ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) descrive uno o più intervalli contigui di testo denominati *storie.* Le storie rappresentano varie parti di un documento, ad esempio il testo principale del documento, le intestazioni e i piè di pagina, le note a piè di pagina, le annotazioni e i blocchi di testo rtf. Una storia di scratch pad viene usata per la traduzione tra espressioni matematiche formattate in modo lineare e una forma incorporata. Quando si salva il contenuto di un intervallo che rappresenta l'origine di copia corrente quando il contenuto sta per essere modificato, viene usata anche una storia del riquadro scratch.

Un [**oggetto ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) è definito dagli offset di posizione del carattere iniziale e finale e da un oggetto story. Non esiste indipendentemente dall'oggetto brano padre, anche se il testo può essere copiato negli Appunti o in altre destinazioni. Un oggetto intervallo di testo è diverso dal foglio di calcolo e da altri oggetti intervallo, definiti da altri tipi di offset. ad esempio, riga/colonna o posizione grafica (x, y). Un oggetto intervallo di testo può modificare se stesso in vari modi, può restituire un duplicato di se stesso e può essere comando per copiare le posizioni dei caratteri iniziale e finale e il relativo puntatore alla storia nella selezione corrente.

Non è necessario un oggetto storia esplicito, poiché è sempre possibile creare un [**oggetto ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange) per rappresentare qualsiasi storia specificata. In particolare, l'oggetto [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) può creare un oggetto [**ITextStoryRanges**](/windows/desktop/api/Tom/nn-tom-itextstoryranges) per enumerare le storie nel documento in termini di intervalli con valori di posizione del carattere iniziale e finale che descrivono storie complete (ad esempio, 0 e **tomForward).**

Con un [**oggetto ITextStoryRanges2,**](/windows/desktop/api/Tom/nn-tom-itextstoryranges2) non è necessario un oggetto storia esplicito, poiché ogni storia è descritta da un [**oggetto ITextRange2.**](/windows/desktop/api/Tom/nn-tom-itextrange2) In particolare, l'oggetto [**ITextDocument2**](/windows/desktop/api/tom/nn-tom-itextdocument2) può creare un oggetto [**ITextStoryRanges2**](/windows/desktop/api/tom/nn-tom-itextstoryranges2) per enumerare le storie nel documento in termini di intervalli con valori di posizione del carattere iniziale e finale che descrivono storie complete (ad esempio, 0 e **tomForward).**

[**L'interfaccia ITextRow**](/windows/desktop/api/Tom/nn-tom-itextrow) insieme ai metodi [**ITextRange::Move**](/windows/desktop/api/Tom/nf-tom-itextrange-move) e [**ITextRange::Expand**](/windows/desktop/api/Tom/nf-tom-itextrange-expand) consente di inserire, eseguire query e modificare tabelle.

## <a name="tom-interface-conventions"></a>Convenzioni dell'interfaccia TOM

Tutti i metodi TOM **restituiscono valori HRESULT.** In generale, i metodi TOM restituiscono i valori standard seguenti.

-   E \_ OUTOFMEMORY
-   E \_ INVALIDARG
-   E \_ NOTIMPL
-   E \_ FILENOTFOUND
-   E \_ ACCESSO NEGATO
-   E \_ FAIL
-   CO \_ E \_ RILASCIATO
-   NOERROR (uguale a S \_ OK)
-   S \_ FALSE

Tenere presente che se l'istanza di modifica associata a un oggetto TOM, ad esempio [**ITextRange,**](/windows/desktop/api/Tom/nn-tom-itextrange) viene eliminata, l'oggetto TOM diventa inutile e tutti i relativi metodi restituiscono CO \_ E \_ RELEASED.

Oltre ai valori **restituiti HRESULT,** molti metodi includono parametri out, che sono puntatori usati per restituire valori. Per tutte le interfacce, è necessario controllare tutti i parametri del puntatore per assicurarsi che siano diversi da zero prima di usarli. Se si passa un valore Null a un metodo che richiede un puntatore valido, il metodo restituisce E \_ INVALIDARG. I puntatori out facoltativi con valori Null vengono ignorati.

Usare i metodi con prefissi Get e Set per ottenere e impostare le proprietà. Le variabili booleane **usano tomFalse** (0) per **FALSE** e **tomTrue** (-1) per **TRUE.**

Le costanti TOM sono definite nel tipo di [**enumerazione tomConstants**](/windows/win32/api/tom/ne-tom-tomconstants) e iniziano con il prefisso *tom*, ad esempio **tomWord**.

## <a name="the-tombool-type"></a>Tipo tomBool

Molti metodi TOM usano un tipo speciale di variabile denominata "tomBool" per gli attributi di testo RTF con stati binari. Il tipo tomBool è diverso dal tipo **booleano** perché può assumere quattro valori: **tomTrue**, **tomFalse**, **tomToggle** e **tomUndefined**. I **valori tomTrue** **e tomFalse** indicano true e false. Il **valore tomToggle** viene usato per attivare o disattivare una proprietà. Il **valore tomUndefined,** più tradizionalmente denominato NINCH, è uno speciale valore senza input e senza modifiche che funziona con valori long, float e **COLORREF.** Per le stringhe, **tomUndefined** (o NINCH) è rappresentato dalla stringa Null. Per le operazioni di impostazione delle proprietà, l'uso **di tomUndefined** non modifica la proprietà di destinazione. Per le operazioni di recupero delle proprietà, **tomUndefined** indica che i caratteri nell'intervallo hanno valori diversi (viene visualizzata la casella di controllo in grigio nelle finestre di dialogo delle proprietà).

## <a name="math-buildup-and-build-down"></a>Compilazione matematica e compilazione

È possibile usare il [**metodo ITextRange2::BuildUpMath**](/windows/desktop/api/Tom/nf-tom-itextrange2-buildupmath) per convertire espressioni matematiche formattate in modo lineare in versioni incorporate. Il [**metodo ITextRange2::Linearize**](/windows/desktop/api/Tom/nf-tom-itextrange2-linearize) esegue la conversione opposta, denominata linearizzazione o compilazione, per convertire le versioni incorporate delle espressioni matematiche in formato lineare. La funzionalità di compilazione matematica è utile quando è necessario esportare testo normale o abilitare determinati tipi di modifica.

## <a name="tom-rtf"></a>TOM RTF

In TOM, lo scambio di testo RTF può essere ottenuto da set di chiamate di metodo esplicite o da trasferimenti di testo RTF (Rich Text Format). In questa sezione vengono fornite tabelle di parole di controllo RTF per le proprietà dei paragrafi e per le proprietà dei caratteri.

**Parole di controllo del paragrafo RTF TOM**

| Parola di controllo   | Significato                                                                                                                                                                                                                                                                        |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\ fi *n*      | Rientro della prima riga (il valore predefinito è zero).                                                                                                                                                                                                                                       |
| \\ Mantenere        | Mantenere intatto il paragrafo.                                                                                                                                                                                                                                                         |
| \\ keepn       | Continuare con il paragrafo successivo.                                                                                                                                                                                                                                                  |
| \\ li *n*      | Rientro sinistro (il valore predefinito è zero).                                                                                                                                                                                                                                             |
| \\ noline      | Nessuna numerazione delle righe.                                                                                                                                                                                                                                                             |
| \\ nowidctlpar | Disattivare il controllo orphan/vedova.                                                                                                                                                                                                                                                 |
| \\ pagebb      | Interrompi pagina prima del paragrafo.                                                                                                                                                                                                                                                   |
| \\ Comma         | Nuovo paragrafo.                                                                                                                                                                                                                                                                 |
| \\ Pard        | Reimposta le proprietà predefinite del paragrafo.                                                                                                                                                                                                                                        |
| \\ Ql          | Allineato a sinistra (impostazione predefinita).                                                                                                                                                                                                                                                    |
| \\ Qr          | Allineato a destra.                                                                                                                                                                                                                                                                 |
| \\ Qj          | Giustificato.                                                                                                                                                                                                                                                                     |
| \\ Qc          | Centrato.                                                                                                                                                                                                                                                                      |
| \\ ri *n*      | Rientro a destra (il valore predefinito è zero).                                                                                                                                                                                                                                            |
| \\ s *n*       | Stile *n*.                                                                                                                                                                                                                                                                     |
| \\ sa *n*      | Spazio dopo (il valore predefinito è zero).                                                                                                                                                                                                                                             |
| \\ sb *n*      | Spazio prima (il valore predefinito è zero).                                                                                                                                                                                                                                            |
| \\ sl *n*      | Se manca o se *n*=1000, l'interlinea è determinata dal carattere più alto nella riga (interlinea singola); se *n*> zero, viene usata almeno questa dimensione. se *n* è < zero, viene usato \| *esattamente n.* \| L'interlinea è un'interlinea multipla se \\ segue slmult 1. |
| \\ slmult *m*  | Segue \\ sl. *m* = zero: interlinea minima o esatta come descritto da \\ sl *n*. *m* = 1: interlinea = *n*/240 volte l'interlinea singola.                                                                                                                              |
| \\ tb *n*      | Posizione della scheda della barra, in twip, dal margine sinistro.                                                                                                                                                                                                                              |
| \\ tldot       | Punti del carattere di tabulazione.                                                                                                                                                                                                                                                               |
| \\ tleq        | Segno di uguale del carattere di tabulazione.                                                                                                                                                                                                                                                         |
| \\ tifo      | Trattini del carattere di tabulazione.                                                                                                                                                                                                                                                            |
| \\ tlth        | Linea spessore del carattere di tabulazione.                                                                                                                                                                                                                                                         |
| \\ tlul        | Sottolineatura del carattere di tabulazione.                                                                                                                                                                                                                                                          |
| \\ Tqc         | Scheda centrata.                                                                                                                                                                                                                                                                  |
| \\ tqdec       | Tabulazione decimale.                                                                                                                                                                                                                                                                   |
| \\ tqr         | Scheda scaricamento a destra.                                                                                                                                                                                                                                                               |
| \\ tx *n*      | Posizione della scheda, in twip, dal margine sinistro.                                                                                                                                                                                                                                  |



 

**Parole di controllo in formato carattere RTF TOM**

| Parola di controllo     | Significato                                                                                                                                                                                                                                  |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\ animation *n* | Imposta il tipo di animazione *su n*.                                                                                                                                                                                                              |
| \\ B             | Grassetto.                                                                                                                                                                                                                                    |
| \\ Tappi          | Tutte maiuscole.                                                                                                                                                                                                                            |
| \\ cf *n*        | Colore primo piano (il valore predefinito **è tomAutocolor).**                                                                                                                                                                                      |
| \\ cs *n*        | Stile carattere *n*.                                                                                                                                                                                                                     |
| \\ dn *n*        | Posizione di indice in mezzo punto (il valore predefinito è 6).                                                                                                                                                                                    |
| \\ Embo          | In rilievo.                                                                                                                                                                                                                                |
| \\ f *n*         | Numero carattere, *n* fa riferimento a una voce nella tabella dei tipi di carattere.                                                                                                                                                                                   |
| \\ fs *n*        | Dimensioni del carattere in metà punti (il valore predefinito è 24).                                                                                                                                                                                            |
| \\ highlight *n* | Colore di sfondo (il valore predefinito **è tomAutocolor).**                                                                                                                                                                                      |
| \\ Ho             | Corsivo.                                                                                                                                                                                                                                  |
| \\ impr          | Impronta.                                                                                                                                                                                                                                 |
| \\ lang *n*      | Applica una lingua a un carattere. *n* è un numero corrispondente a una lingua. La parola di controllo normale reimposta la proprietà language sulla lingua \\ definita da \\ deflang *n* nelle proprietà del documento.                             |
| \\ nosupersub    | Disattiva l'apice o l'indice.                                                                                                                                                                                                      |
| \\ outl          | Contorno.                                                                                                                                                                                                                                 |
| \\ Pianura         | Reimposta le proprietà di formattazione dei caratteri su un valore predefinito definito dall'applicazione. Vengono reimpostate anche le proprietà di formattazione dei caratteri associate (descritte nella sezione Proprietà carattere associate nella specifica RTF). |
| \\ scaps         | Maiuscole di piccole dimensioni.                                                                                                                                                                                                                          |
| \\ Shad          | Ombra.                                                                                                                                                                                                                                  |
| \\ sciopero        | Barrato.                                                                                                                                                                                                                           |
| \\ Sub           | Applica l'indice al testo e riduce le dimensioni in punti in base alle informazioni sul tipo di carattere.                                                                                                                                                          |
| \\ Super         | Applica l'apice al testo e riduce le dimensioni in punti in base alle informazioni sul tipo di carattere.                                                                                                                                                        |
| \\ Ul            | Sottolineatura continua. \\ ul0 disattiva tutte le sottolineatura.                                                                                                                                                                                  |
| \\ Uld           | Sottolineatura tratteggiata.                                                                                                                                                                                                                        |
| \\ uldb          | Sottolineatura doppia.                                                                                                                                                                                                                        |
| \\ ulnone        | Arresta tutte le sottolineatura.                                                                                                                                                                                                                   |
| \\ ulw           | Sottolineatura della parola.                                                                                                                                                                                                                          |
| \\ up *n*        | Posizione dell'apice in mezzo punto (il valore predefinito è 6).                                                                                                                                                                                  |
| \\ Presso             | Testo nascosto.                                                                                                                                                                                                                             |



 

## <a name="finding-rich-text"></a>Ricerca di testo RTF

È possibile usare i metodi TOM per trovare testo RTF come definito da un intervallo di testo. L'individuazione di questo tipo di testo RTF è spesso necessaria nell'elaborazione di testo, anche se non è mai stata soddisfatta in un elaboratore di testo "what you see is what you get" (WYSIWYG). Esiste chiaramente un dominio più ampio di corrispondenza di testo RTF che consente di ignorare alcune proprietà di formattazione dei caratteri (o di includere la formattazione dei paragrafi e/o il contenuto dell'oggetto), ma tali generalizzazioni es vanno oltre l'ambito di questa sezione.

Uno degli scopi di questa funzionalità  è usare una finestra di dialogo Trova in formato RTF per definire il testo RTF da individuare in un documento. La finestra di dialogo viene implementata usando un controllo Rich Edit e i metodi TOM vengono usati per eseguire la ricerca nel documento. È possibile copiare il testo RTF  desiderato dal documento nella finestra di dialogo Trova oppure immetterlo e formattarlo direttamente nella **finestra di dialogo** Trova .

L'esempio seguente illustra come usare i metodi TOM per trovare testo contenente combinazioni di formattazione esatta dei caratteri. L'algoritmo cerca il testo normale nell'intervallo di corrispondenze, denominato `pr1` . Se il testo normale viene trovato, viene puntato a un intervallo di prova, denominato `pr2` . Vengono quindi usati due intervalli di punti di inserimento ( e ) per scorrere l'intervallo di prova confrontando la formattazione dei caratteri `prip1` `prip2` con quella di `pr1` . Se corrispondono esattamente, l'intervallo di input (fornito da ) viene aggiornato in modo che punti al testo dell'intervallo di prova e la funzione restituisce il numero di caratteri `ppr` nell'intervallo corrispondente. Nel confronto della formattazione dei caratteri vengono usati due oggetti [**ITextFont,**](/windows/desktop/api/Tom/nn-tom-itextfont) `pf1` `pf2` e . Sono collegati agli intervalli di punti di inserimento `prip1` e `prip2` .


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



## <a name="tom-accessibility"></a>Accessibilità tom

TOM offre supporto per l'accessibilità tramite le interfacce [**ITextSelection**](/windows/desktop/api/Tom/nn-tom-itextselection) [**e ITextRange.**](/windows/desktop/api/Tom/nn-tom-itextrange) In questa sezione vengono descritti i metodi utili per l'accessibilità, nonché il modo in cui un programma può determinare la posizione dello schermo *x*, *y* di un oggetto .

Poiché i programmi di accessibilità basati sull'interfaccia utente in genere funzionano con lo schermo e il mouse, un problema comune è trovare l'interfaccia [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) corrispondente per la posizione corrente del mouse (nelle coordinate dello schermo). Le sezioni seguenti illustrano due modi per determinare l'interfaccia appropriata:

-   [Tramite la tabella dell'oggetto in esecuzione](#interface-from-running-object-table)
-   Tramite il [**messaggio EM \_ GETOLEINTERFACE,**](em-getoleinterface.md) che funziona per le istanze rich edit finestra, purché il client si trova nello stesso spazio di processo (non è necessario *il marshalling)*

Per altre informazioni, vedere la specifica Microsoft Active Accessibility. Dopo aver ottenuto un oggetto da una posizione sullo schermo, è possibile usare per un'interfaccia [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) e chiamare il [**metodo RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint) per ottenere un oggetto intervallo vuoto in corrispondenza del parametro corrispondente alla posizione dello schermo.

### <a name="interface-from-running-object-table"></a>Interfaccia dalla tabella oggetti in esecuzione

Una tabella ROT (Running Object Table) indica quali istanze dell'oggetto sono attive. Eseguendo una query su questa tabella, è possibile accelerare il processo di connessione di un client a un oggetto quando l'oggetto è già in esecuzione. Prima che i programmi possano accedere alle interfacce TOM tramite la tabella di oggetti in esecuzione, un'istanza tom con una finestra deve registrarsi nella rot usando un moniker. Il moniker viene costruito da una stringa contenente il valore esadecimale del relativo [**oggetto HWND.**](/windows/desktop/WinProg/windows-data-types) Nell'esempio di codice seguente viene illustrato come eseguire questa operazione.


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



### <a name="interface-from-window-messages"></a>Interfaccia dai messaggi della finestra

Il [**messaggio EM \_ GETOLEINTERFACE**](em-getoleinterface.md) fornisce un altro modo per ottenere [**un'interfaccia IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) per un oggetto in una determinata posizione dello schermo. Come descritto in [Interfaccia dall'esecuzione della](#interface-from-running-object-table)tabella oggetti , si ottiene un [**oggetto HWND**](/windows/desktop/WinProg/windows-data-types) per la posizione sullo schermo e quindi si invia questo messaggio a **tale HWND.** Il **messaggio EM \_ GETOLEINTERFACE** è specifico della modifica e restituisce un puntatore a [**un'interfaccia IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) nella variabile a cui fa riferimento *lParam*.

**Suggerimento** Se viene restituito un puntatore (assicurarsi di impostare l'oggetto su cui *lParam* punta a Null prima di inviare il messaggio), è possibile chiamare il relativo metodo [**IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere un'interfaccia [**ITextDocument.**](/windows/desktop/api/Tom/nn-tom-itextdocument) Il seguente esempio di codice illustra questo approccio.


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

Alcuni metodi TOM sono particolarmente utili per spostarsi all'interno dello schermo, mentre altri metodi TOM migliorano le attività che è possibile eseguire quando si arriva a luoghi di interesse. Nella tabella seguente vengono descritti i metodi più utili.



| Metodo                                                 | Come promuove l'accessibilità                                                                                                                                                                 |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSelection**](/windows/desktop/api/Tom/nf-tom-itextdocument-getselection)     | Questo metodo ottiene la selezione attiva che può essere usata per un'ampia gamma di scopi orientati alla visualizzazione, ad esempio l'evidenziazione del testo e lo scorrimento.                                                      |
| [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint) | Se usato su una selezione attiva, questo metodo ottiene un intervallo associato a una determinata visualizzazione.                                                                                 |
| [**Espandere**](/windows/desktop/api/Tom/nf-tom-itextrange-expand)                    | Ingrandisce un intervallo di testo in modo che tutte le unità parziali in esso contenute siano completamente contenute. Ad esempio, `Expand(tomWindow)` espande l'intervallo per includere la parte visibile della storia dell'intervallo. |
| [**GetDuplicate**](/windows/desktop/api/Tom/nf-tom-itextrange-getduplicate)        | Se usato su una selezione attiva, questo metodo ottiene un intervallo associato a una determinata visualizzazione. Vedere la descrizione di [**RangeFromPoint.**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint)  |
| [**GetPoint**](/windows/desktop/api/Tom/nf-tom-itextrange-getpoint)                | Ottiene le coordinate dello schermo per la posizione del carattere iniziale o finale nell'intervallo di testo.                                                                                                        |
| [**ScrollIntoView**](/windows/desktop/api/Tom/nf-tom-itextrange-scrollintoview)    | Scorre un intervallo di testo nella visualizzazione.                                                                                                                                                               |
| [**Setpoint**](/windows/desktop/api/Tom/nf-tom-itextrange-setpoint)                | Seleziona il testo in corrispondenza o verso l'alto fino a un punto specificato.                                                                                                                                              |



 

## <a name="character-match-sets"></a>Set di corrispondenze di caratteri

Il *parametro variant* dei vari metodi **Move** in \* [**ITextRange,**](/windows/desktop/api/Tom/nn-tom-itextrange)ad esempio [**MoveWhile**](/windows/desktop/api/Tom/nf-tom-itextrange-movewhile) e [**MoveUntil,**](/windows/desktop/api/Tom/nf-tom-itextrange-moveuntil)può prendere una stringa esplicita o un indice a 32 bit del set di corrispondenze di caratteri. Gli indici sono definiti da intervalli Unicode o set [**di caratteri GetStringTypeEx.**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw) L'intervallo Unicode che inizia da *n* e di lunghezza *l* (< 32768) viene fornito dall'indice *n* + (*l <*< 16) + 0x80000000. Ad esempio, le lettere greche di base sono definite da CR Greco = 0x805f0370 e i caratteri ASCII stampabili sono definiti da \_ CR \_ ASCIIPrint = 0x805e0020. Inoltre, i metodi **MoveWhile** e **MoveUntil** consentono di ignorare rapidamente un intervallo di caratteri in qualsiasi set di caratteri **GetStringTypeEx** o in un intervallo di caratteri che non si trova in nessuno di questi set di caratteri.

I [**set GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw) vengono specificati dai valori per *Ctype1*, *Ctype2* e *Ctype3* e vengono definiti come segue.



| Cset                 | Significato                          |
|----------------------|----------------------------------|
| *Ctype1*             | Combinazione di tipi CT \_ CTYPE1. |
| *Ctype2* + tomCType2 | Qualsiasi tipo CT \_ CTYPE2.             |
| *Ctype3* + tomCType3 | Combinazione di tipi \_ CTYPE3 CT. |



 

In particolare, *Ctype1* può essere qualsiasi combinazione di quanto segue.



| Nome Ctype1 | Valore  | Significato                                                           |
|-------------|--------|-------------------------------------------------------------------|
| C1 \_ UPPER   | 0x0001 | Maiuscolo.                                                        |
| C1 \_ LOWER   | 0x0002 | Minuscolo.                                                        |
| C1 \_ DIGIT   | 0x0004 | Cifre decimali.                                                   |
| SPAZIO \_ C1   | 0x0008 | Spazi.                                                 |
| C1 \_ PUNCT   | 0x0010 | Punteggiatura.                                                      |
| C1 \_ CNTRL   | 0x0020 | Caratteri di controllo.                                               |
| C1 \_ BLANK   | 0x0040 | Caratteri vuoti.                                                 |
| C1 \_ XDIGIT  | 0x0080 | Cifre esadecimali.                                               |
| C1 \_ ALPHA   | 0x0100 | Qualsiasi carattere linguistico (alfabetico, sillabico o ideografico). |
| C1 \_ DEFINED | 0x0200 | Carattere definito, ma non uno degli altri tipi \_ \* C1.       |



 

I *tipi Ctype2* supportano il layout corretto del testo Unicode. Gli attributi di direzione vengono assegnati in modo che l'algoritmo di layout bidirezionale standardizzato da Unicode produca risultati accurati. Questi tipi si escludono a vicenda. Per altre informazioni sull'uso di questi attributi, vedere *The Unicode Standard: Worldwide Character Encoding, Volumes 1 and 2*, Addison-Wesley Publishing Company: 1991, 1992.



| Nome CType2          | Valore | Significato                          |
|----------------------|-------|----------------------------------|
| Forte:              |       |                                  |
| C2 \_ LEFTTORIGHT      | 0x1   | Da sinistra a destra.                   |
| C2 \_ RIGHTTOLEFT      | 0x2   | Da destra a sinistra.                   |
| Debole:                |       |                                  |
| C2 \_ EUROPENUMBER     | 0x3   | Numero europa, cifra europea. |
| C2 \_ EUROPESEPARATOR  | 0x4   | Separatore numerico europa.      |
| C2 \_ EUROPETERMINATOR | 0x5   | Carattere di terminazione numerico europa.     |
| C2 \_ ARABICNUMBER     | 0x6   | Numero arabo.                   |
| C2 \_ COMMONSEPARATOR  | 0x7   | Separatore numerico comune.        |
| Neutro:             |       |                                  |
| BLOCCHI \_ C2EPARATOR   | 0x8   | Separatore di blocchi.                 |
| C2 \_ SEGMENTSEPARATOR | 0x9   | Separatore di segmenti.               |
| SPAZIO \_ VUOTO C2       | 0xA   | Spazio vuoto.                     |
| C2 \_ OTHERNEUTRAL     | 0xB   | Altri neutri.                  |
| Non applicabile:      |       |                                  |
| C2 \_ NOTAPPLICABLE    | 0x0   | Nessuna direzione implicita.           |



 

I *tipi Ctype3* sono destinati a essere segnaposto per le estensioni ai tipi POSIX necessari per l'elaborazione di testo generale o per le funzioni della libreria C standard.



| Nome CType3       | Valore  | Significato                                                             |
|-------------------|--------|---------------------------------------------------------------------|
| C3 \_ NONSPACING    | 0x1    | Segno di nonspacing.                                                    |
| DIACRITICO C3 \_     | 0x2    | Segno diacritico nonspacing.                                          |
| C3 \_ VOWELMARK     | 0x4    | Segno di nonspacing vocale.                                              |
| SIMBOLO \_ C3        | 0x8    | Simbolo.                                                             |
| C3 \_ KATAKANA      | 0x10   | Carattere Katakana.                                                 |
| C3 \_ HIRAGANA      | 0x20   | Carattere hiragana.                                                 |
| C3 \_ HALFWIDTH     | 0x40   | Carattere a metà larghezza.                                               |
| C3 \_ FULLWIDTH     | 0x80   | Carattere a larghezza intera.                                               |
| C3 \_ IDEOGRAPH     | 0x100  | Carattere ideografico.                                              |
| C3 \_ KASHIDA       | 0x200  | Carattere kashida arabo.                                           |
| C3 \_ ALPHA         | 0x8000 | Tutti i caratteri linguistici (alfabetici, sillabari e ideografici). |
| C3 \_ NOTAPPLICABLE | 0x0    | Non applicabile.                                                     |



 

Edit Development Kit (EDK) può includere definizioni di *indice pVar* per gli intervalli seguenti descritti nello standard Unicode.



| Set di caratteri         | Intervallo Unicode | Set di caratteri             | Intervallo Unicode |
|-----------------------|---------------|---------------------------|---------------|
| ASCII                 | 0x0— 0x7f      | ANSI                      | 0x0— 0xff      |
| ASCIIPrint            | 0x20: 0x7e     | Latin1                    | 0x20— 0xff     |
| Latin1Supp            | 0xa0: 0xff     | LatinXA                   | 0x100— 0x17f   |
| LatinXB               | 0x180— 0x24f   | IPAX                      | 0x250— 0x2af   |
| SpaceMod              | 0x2b0— 0x2ff   | Combinazione                 | 0x300— 0x36f   |
| Greco                 | 0x370— 0x3ff   | BasicGreek                | 0x370— 0x3cf   |
| GreekSymbols          | 0x3d0— 0x3ff   | Cirillico                  | 0x400— 0x4ff   |
| Armeno              | 0x530— 0x58f   | Ebraico                    | 0x590— 0x5ff   |
| BasicHebrew           | 0x5d0: 0x5ea   | EbraicoXA                  | 0x590— 0x5cf   |
| EbraicoXB              | 0x5eb— 0x5ff   | Arabo                    | 0x600— 0x6ff   |
| BasicArabic           | 0x600— 0x652   | ArabicX                   | 0x653— 0x6ff   |
| Devangari             | 0x900— 0x97f   | Bangla (in precedenza bengali) | 0x980— 0x9ff   |
| Gurmukhi              | 0xa00— 0xa7f   | Gujarati                  | 0xa80— 0xaff   |
| Odia (in precedenza Oriya) | 0xb00— 0xb7f   | Tamil                     | 0xb80— 0xbff   |
| Teluga                | 0xc00— 0xc7f   | Kannada                   | 0xc80— 0xcff   |
| Malayalam             | 0xd00— 0xd7f   | Thai                      | 0xe00— 0xe7f   |
| Lao                   | 0xe80— 0xeff   | Carattere alfabeto mastofale                 | 0x10a0— 0xa0cf |
| BascGeorgian          | 0x10d0: 0x10ff | Jamo                      | 0x1100— 0x11ff |
| LatinXAdd             | 0x1e00— 0x1eff | GreekX                    | 0x1f00— 0x1fff |
| GenPunct              | 0x2000— 0x206f | Apice               | 0x2070— 0x207f |
| Indice             | 0x2080— 0x208f | SuperSubscript            | 0x2070— 0x209f |
| Valuta              | 0x20a0: 0x20cf | CombMarkSym               | 0x20d0— 0x20ff |
| LetterLike            | 0x2100— 0x214f | NumberForms               | 0x2150— 0x218f |
| Frecce                | 0x2190: 0x21ff | MathOps                   | 0x2200— 0x22ff |
| MiscTech              | 0x2300: 0x23ff | CTRLPictures              | 0x2400, 0x243f |
| OptCharRecog          | 0x2440, 0x245f | EnclAlphaNum              | 0x2460— x24ff  |
| BoxDrawing            | 0x2500 0x257f | BlockElement              | 0x2580, 0x259f |
| GeometShapes          | 0x25a0 0x25ff | MiscSymbols               | 0x2600 0x26ff |
| Dingbats              | 0x2700, 0x27bf | CJKSymPunct               | 0x3000: 0x303f |
| Hiragana              | 0x3040: 0x309f | Katakana                  | 0x30a0 0x30ff |
| Bopomofo              | 0x3100: 0x312f | HangulJamo                | 0x3130, 0x318f |
| CJLMisc               | 0x3190: 0x319f | EnclCJK                   | 0x3200, 0x32ff |
| CJKCompatibl          | 0x3300, 0x33ff | Han                       | 0x3400, 0xabff |
| Hangul                | 0xac00 0xd7ff | UTF16Lead                 | 0xd800: 0xdbff |
| UTF16Trail            | 0xdc00 0xdfff | PrivateUse                | 0xe000, 0xf800 |
| CJKCompIdeog          | 0xf900: 0xfaff | Valori alfapres                 | 0xfb00 0xfb4f |
| ArabicPresA           | 0xfb50 0xfdff | CombHalfMark              | 0xfe20, 0xfe2f |
| CJKCompForm           | 0xfe30, 0xfe4f | SmallFormVar              | 0xfe50, 0xfe6f |
| ArabicPresB           | 0xfe70 0xfefe | HalfFullForm              | 0xff00: 0xffef |
| Speciali              | 0xfff0, 0xfffd |                           |               |



 

 

 