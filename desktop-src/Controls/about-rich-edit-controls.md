---
title: Informazioni sui controlli Rich Edit
description: In questa sezione vengono introdotti i controlli Rich Edit.
ms.assetid: ab9dcdf4-a311-4159-8f37-e67e144f31f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d95f6dc1cc1f37bf604e6c0a891f92cd20bb7af6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "106300604"
---
# <a name="about-rich-edit-controls"></a>Informazioni sui controlli Rich Edit

In questa sezione vengono descritti gli argomenti seguenti.

-   [Versioni di Rich Edit](#versions-of-rich-edit)
    -   [Modifica avanzata versione 1,0](#rich-edit-version-10)
    -   [Modifica avanzata versione 2,0](#rich-edit-version-20)
    -   [Modifica avanzata versione 3,0](#rich-edit-version-30)
    -   [Modifica avanzata versione 4,1](#rich-edit-version-41)
-   [Funzionalità di controllo di modifica non supportata](#unsupported-edit-control-functionality)
-   [Tasti di scelta rapida modifica Rich](#rich-edit-shortcut-keys)
-   [Argomenti correlati](#related-topics)

## <a name="versions-of-rich-edit"></a>Versioni di Rich Edit

La specifica originale per i controlli Rich Edit è Microsoft Rich Edit 1,0; la specifica corrente è Microsoft Rich Edit 4,1. Ogni versione di Rich Edit è un superset del precedente, ad eccezione del fatto che solo le build asiatiche di Microsoft Rich Edit 1,0 hanno un'opzione di testo verticale. Prima di creare un controllo Rich Edit, è necessario chiamare la funzione [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) per verificare quale versione di Microsoft Rich Edit è installata.

Nella tabella seguente viene illustrata la DLL corrispondente alla versione di Rich Edit. Si noti che il nome del file non è stato modificato dalla versione 2,0 alla versione 3,0. Ciò consente di aggiornare la versione 2,0 alla versione 3,0 senza compromettere il codice esistente.



| Versione Rich Edit | DLL          | Classe Window    |
|-------------------|--------------|-----------------|
| 1.0               | Riched32.dll | RichEdit ( \_ classe) |
| 2.0               | Riched20.dll | RichEdit ( \_ classe) |
| 3.0               | Riched20.dll | RichEdit ( \_ classe) |
| 4.1               | Msftedit.dll | \_classe MSFTEDIT |



 

### <a name="rich-edit-version-10"></a>Modifica avanzata versione 1,0

Microsoft Rich Edit 1,0 include le funzionalità seguenti.



|                                                                                    |                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Voce e selezione di testo                                                           | Per lo più standard (controllo di modifica di sistema) selezione e voce di testo. Supporto della barra di selezione (la barra di selezione è un'area non contrassegnata a sinistra di ogni paragrafo che, quando si fa clic, seleziona la riga). Opzioni per l'incapsulamento automatico e la parola. Selezione a singola, doppia e tripla. |
| Modifica di ANSI (set di caratteri a byte singolo (SBCS) e Multibyte Character Set (MBCS)) | Tuttavia, non è disponibile alcuna modifica Unicode.                                                                                                                                                                                                                                                     |
| Set di base di proprietà di formattazione carattere/paragrafo                             | Vedere [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) e [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat).                                                                                                                                                                                                                |
| Proprietà di formattazione carattere                                                    | Nome e dimensioni del carattere, grassetto, corsivo, sottolineatura continua, sciopero, protetto, collegamento, offset e colore del testo.                                                                                                                                                                                   |
| Proprietà di formattazione paragrafo                                                    | Rientro iniziale, rientro destro, offset riga successivo, punto elenco, allineamento (a sinistra, al centro, a destra) e tabulazioni.                                                                                                                                                                                    |
| Trova in futuro                                                                       | Include le opzioni senza distinzione tra maiuscole e minuscole e con l'intera parola.                                                                                                                                                                                                                                   |
| Interfaccia basata su messaggi                                                            | Quasi un superset del set di messaggi del controllo di modifica del sistema più due interfacce, [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) e [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback).                                                                                                              |
| Oggetti incorporati                                                                   | Richiede la collaborazione client basata sulle interfacce [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) e [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) .                                                                                                                                          |
| Supporto menu pulsante destro                                                          | Usa l'interfaccia [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) .                                                                                                                                                                                                                      |
| Modifica del trascinamento della selezione                                                              | La modifica del trascinamento della selezione è supportata.                                                                                                                                                                                                                                                       |
| Notifiche                                                                      | [**WM \_**](/windows/desktop/menurc/wm-command) Messaggi di comando inviati al client più diversi altri. Si tratta di un superset di notifiche di controllo comuni.                                                                                                                                                 |
| Annullamento/ripetizione a livello singolo                                                             | Si comporta in modo analogo al controllo di modifica del sistema. Se si seleziona **Annulla** , viene invertita l'ultima azione e tale azione diventa la nuova azione di **rollforward** .                                                                                                                                          |
| Testo verticale semplice                                                               | (Solo per le compilazioni asiatiche).                                                                                                                                                                                                                                                                      |
| Supporto IME (Input Method Editor)                                                  | (Solo per le compilazioni asiatiche).                                                                                                                                                                                                                                                                      |
| Modifica WYSIWYG con le metriche della stampante                                              | Questa funzionalità è necessaria per Microsoft WordPad, in particolare.                                                                                                                                                                                                                              |
| Taglia/copia/incolla/flusso/flusso                                                  | Con testo normale (**\_ testo CF**) o RTF (Rich Text Format) con e senza oggetti.                                                                                                                                                                                                        |
| Codebase C                                                                        | Il codice è scritto in C, che fornisce una base solida e versatile.                                                                                                                                                                                                                |
| Compilazioni diverse per script diversi                                             | Microsoft Rich Edit 1,0 risolve i problemi di localizzazione con diverse Build.                                                                                                                                                                                                              |



 

### <a name="rich-edit-version-20"></a>Modifica avanzata versione 2,0

Microsoft Rich Edit 2,0 ha incorporato diverse funzionalità aggiuntive, ad esempio il supporto per lingue Unicode e asiatiche, le interfacce di annullamento multilivello, Component Object Model (COM) e numerosi miglioramenti dell'interfaccia utente.

Microsoft Rich Edit 2,0 include le funzionalità seguenti, oltre alle funzionalità fornite da [Microsoft rich edit 1,0](#rich-edit-version-10).



|                                               |                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unicode                                       | Unicode semplifica il lavoro di gestione del testo internazionale. Tuttavia, lo sforzo è necessario per mantenere la compatibilità con i documenti non Unicode esistenti, ovvero la possibilità di eseguire la conversione da/verso testo normale e RTF non Unicode.                                                                                                                                                             |
| Supporto internazionale generale                 | Algoritmo di interruzione di riga generale (estensione delle regole kinsoku), collegamento di tipi di carattere semplice, cambio di carattere della tastiera.                                                                                                                                                                                                                                                                          |
| Supporto asiatico                                 | Il livello 2 (finestra di dialogo) e 3 (inline) sono supportati negli IME.                                                                                                                                                                                                                                                                                                                            |
| Trova il supporto tecnico                     | La ricerca in avanti e indietro è supportata.                                                                                                                                                                                                                                                                                                                                         |
| Supporto bidirezionale                         | Questa funzionalità è inclusa in Microsoft Rich Edit 2,1                                                                                                                                                                                                                                                                                                                                          |
| Annullamento a più livelli                               | Un'architettura di annullamento estensibile consente al client di partecipare al modello di annullamento a livello di applicazione.                                                                                                                                                                                                                                                                                         |
| Supporto del mouse Magellan                        | Si tratta del mouse con un rullo per lo scorrimento.                                                                                                                                                                                                                                                                                                                                       |
| Supporto per due tipi di carattere                             | La tastiera può cambiare automaticamente i tipi di carattere quando il tipo di carattere attivo non è appropriato per la tastiera corrente, ad esempio i caratteri Kanji in Times New Roman.                                                                                                                                                                                                                            |
| Carattere intelligente applicato                              | La richiesta di modifica del tipo di carattere non applica tipi di carattere occidentali ai caratteri asiatici.                                                                                                                                                                                                                                                                                                                |
| Visualizzazione migliorata                              | Una bitmap fuori schermo viene utilizzata quando si verificano più tipi di carattere nella stessa riga. Questo consente, ad esempio, che l'ultima lettera della parola cool non venga troncata.                                                                                                                                                                                                                           |
| Supporto per la trasparenza                          | Anche in modalità senza finestra.                                                                                                                                                                                                                                                                                                                                                             |
| Colori selezione sistema                       | Utilizzato per la selezione del testo.                                                                                                                                                                                                                                                                                                                                                             |
| Riconoscimento URL automatico                     | Può verificare la presenza di un numero di formati di URL, ad esempio http:)                                                                                                                                                                                                                                                                                                                           |
| Compatibilità dell'interfaccia utente di Microsoft Word Edit          | Semantica di selezione, tastiera del cursore.                                                                                                                                                                                                                                                                                                                                                  |
| EOP standard Word                             | Il contrassegno di fine del paragrafo (CR) può anche gestire il ritorno a capo/avanzamento riga (CR/LF) (ritorno a capo, avanzamento riga).                                                                                                                                                                                                                                                                       |
| Testo normale e funzionalità Rich Text | Formato a carattere singolo e formato a paragrafo singolo.                                                                                                                                                                                                                                                                                                                                 |
| Controlli a riga singola e su più righe            | Tronca alla prima fine del paragrafo e non WordWrap.                                                                                                                                                                                                                                                                                                                                  |
| Tasti di scelta rapida                              | Sono supportati i tasti di scelta rapida.                                                                                                                                                                                                                                                                                                                                                      |
| Stile finestra password                         | I controlli di modifica della password vengono forniti tramite [**em \_ GETPASSWORDCHAR**](em-getpasswordchar.md) e [**em \_ SETPASSWORDCHAR**](em-setpasswordchar.md).                                                                                                                                                                                                                                 |
| Architettura scalabile                         | Per ridurre le dimensioni dell'istanza.                                                                                                                                                                                                                                                                                                                                                             |
| Operazione senza finestra e interfacce           | Questa operazione viene fornita tramite le interfacce [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) e [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) .                                                                                                                                                                                                                                                                   |
| Interfacce duali COM                           | Interfacce di TOM (Text Object Model).                                                                                                                                                                                                                                                                                                                                                  |
| CHARFORMAT2                                   | Aggiunta di spessore carattere, colore di sfondo, identificatore delle impostazioni locali, tipo di sottolineatura, apice e pedice (oltre all'offset), effetto disabilitato. Solo per Roundtripping RTF, quantità aggiunta allo spazio tra le lettere, dimensioni twip sopra le quali la coppia di caratteri Kern, il tipo di testo animato, vari effetti: ombreggiatura o contorno del carattere, tutti i tappi, i tappi piccoli, nascosti, in rilievo, impronta e rivisti. |
| PARAFORMAT2                                   | Spazio aggiunto prima e dopo e spaziatura riga parole. Solo per Roundtripping RTF, aggiunta di spessore/stile ombreggiatura, numerazione di inizio/stile/tabulazione, spazio bordo/larghezza/lati, allineamento/leader di tabulazione, diversi effetti paragrafi di parola: RTL Paragraph, Keep, Keep-Next, page-break-before, no-line-number, no-Widow-Control                                         |
| Altri Roundtripping RTF                        | Tutte le proprietà di Word FormatFont e FormatParagraph.                                                                                                                                                                                                                                                                                                                           |
| Stabilità e stabilizzazione del codice              | Esempi: convalida di parametri e oggetti, invarianti di funzione, protezioni rientranti, stabilizzazione di oggetti.                                                                                                                                                                                                                                                                             |
| Infrastruttura di test avanzata                 | Inclusi i test di regressione estensivi.                                                                                                                                                                                                                                                                                                                                               |
| prestazioni migliorate                          | Working set più piccoli, tempi di caricamento e rivisualizzazione più veloci e così via.                                                                                                                                                                                                                                                                                                                     |
| Codebase C++                                 | Il codice è scritto in C++, che fornisce una solida base su cui compilare Microsoft Rich Edit 3,0.                                                                                                                                                                                                                                                                             |



 

Con alcune eccezioni, Microsoft Rich Edit 2,0 utilizza le stesse funzioni, le stesse strutture e i messaggi di Microsoft Rich Edit 1,0. Si noti, tuttavia, le differenze seguenti:

-   Il nome della classe della finestra Microsoft Rich Edit 1,0 è **RichEdit**. Microsoft Rich Edit 2,0 include rispettivamente le classi di finestra ANSI e Unicode **RichEdit20A** e **RichEdit20W** . Per specificare la classe della finestra Rich Edit appropriata, utilizzare la costante della classe RichEdit \_ , definita dal file RichEdit. h, a seconda della definizione del flag di compilazione Unicode.
-   In Microsoft Rich Edit 2,0, se si crea un controllo Rich Edit Unicode (uno che prevede messaggi di testo Unicode), è necessario specificare solo i dati Unicode nei messaggi della finestra inviati al controllo. Analogamente, se si crea un controllo Rich Edit ANSI, inviare solo dati ANSI o DBCS (Double byte character set). È possibile utilizzare la funzione [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) per determinare se un controllo Rich Edit utilizza messaggi di testo Unicode. Si noti che le interfacce COM Rich Edit usano il testo Unicode, a meno che non riscontrino un argomento della tabella codici.
-   Microsoft Rich Edit 1,0 usava le combinazioni di caratteri CR/LF per i marcatori di paragrafo. Microsoft Rich Edit 2,0 usava solo un carattere di ritorno a capo (' \\ r '). Microsoft Rich Edit 3,0 utilizza solo un carattere di ritorno a capo ma è in grado di emulare Microsoft Rich Edit 1,0 in questo senso.
-   Microsoft Rich Edit 2,0 ha introdotto i nuovi messaggi seguenti. 

    | Message                                           | Descrizione                                                             |
    |---------------------------------------------------|-------------------------------------------------------------------------|
    | [**\_AUTOURLDETECT em**](em-autourldetect.md)     | Abilita o Disabilita il rilevamento automatico degli URL.                            |
    | [**\_CANREDO em**](em-canredo.md)                 | Determina se sono presenti azioni nella coda di rollforward.             |
    | [**\_GETIMECOMPMODE em**](em-getimecompmode.md)   | Recupera la modalità di Input Method Editor corrente (IME).                   |
    | [**\_GETLANGOPTIONS em**](em-getlangoptions.md)   | Recupera le opzioni per l'IME e il supporto della lingua asiatica.                   |
    | [**\_GETredoname em**](em-getredoname.md)         | Recupera il nome del tipo dell'azione successiva nella coda di rollforward.           |
    | [**\_GETTEXTMODE em**](em-gettextmode.md)         | Recupera la modalità testo o il livello di annullamento.                                  |
    | [**EM \_ GETundoname**](em-getundoname.md)         | Recupera il nome del tipo dell'azione successiva nella coda di annullamento.           |
    | [**\_ripetizione em**](em-redo.md)                       | Ripete l'azione successiva nella coda di rollforward.                               |
    | [**\_SETLANGOPTIONS em**](em-setlangoptions.md)   | Imposta le opzioni per l'IME e il supporto della lingua asiatica.                        |
    | [**\_SETTEXTMODE em**](em-settextmode.md)         | Imposta la modalità testo o il livello di annullamento.                                       |
    | [**\_SETUNDOLIMIT em**](em-setundolimit.md)       | Imposta il numero massimo di azioni nella coda di annullamento.                   |
    | [**\_STOPGROUPTYPING em**](em-stopgrouptyping.md) | Interrompe il raggruppamento delle azioni di digitazione consecutive nell'azione di annullamento corrente. |

    

     

-   Microsoft Rich Edit 2,0 ha introdotto le nuove strutture seguenti. 

    | Struttura                          | Descrizione                                      |
    |------------------------------------|--------------------------------------------------|
    | [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) | Contiene informazioni sulla formattazione dei caratteri. |
    | [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) | Contiene informazioni sulla formattazione dei paragrafi. |

    

     

-   I messaggi seguenti sono supportati solo nelle versioni in lingua asiatica di Microsoft Rich Edit 1,0. Non sono supportate nelle versioni successive di Rich Edit.

    [**\_CONVPOSITION em**](em-convposition.md)

    [**\_GETIMECOLOR em**](em-getimecolor.md)

    [**\_GETIMEOPTIONS em**](em-getimeoptions.md)

    [**\_GETpunteggiatura em**](em-getpunctuation.md)

    [**\_GETWORDWRAPMODE em**](em-getwordwrapmode.md)

    [**\_SETIMECOLOR em**](em-setimecolor.md)

    [**\_SETIMEOPTIONS em**](em-setimeoptions.md)

    [**\_punteggiatura em**](em-setpunctuation.md)

    [**\_SETWORDWRAPMODE em**](em-setwordwrapmode.md)

### <a name="rich-edit-version-30"></a>Modifica avanzata versione 3,0

Microsoft Rich Edit 3,0 è una singola DLL scalabile e a livello globale che offre prestazioni elevate e compatibilità con Word in un pacchetto di piccole dimensioni. Le nuove funzionalità per Microsoft Rich Edit 3,0 includono testo più completo, zoom, associazione di tipi di carattere, supporto IME più potente e supporto avanzato per gli script (bidirezionale, lingue indiane e Thai).

Microsoft Rich Edit 3,0 include le funzionalità seguenti, oltre alle funzionalità fornite da [Rich Edit versione 2,0](#rich-edit-version-20).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Zoom</td>
<td>Il fattore di zoom viene fornito da un rapporto.</td>
</tr>
<tr class="even">
<td>Numerazione paragrafo (a livello singolo)</td>
<td>Numerici, alfabetici maiuscoli e minuscoli o numeri romani.</td>
</tr>
<tr class="odd">
<td>Tabelle semplici</td>
<td>L'eliminazione e l'inserimento di righe sono possibili, ma non il ridimensionamento né il ritorno a capo nelle celle. Con tipografia avanzata attivata (vedere <a href="em-gettypographyoptions.md"><strong>EM_GETTYPOGRAPHYOPTIONS</strong></a>), Microsoft Rich Edit 3,0 può allineare le colonne centrate o Flush Right e includere i decimali. Le celle vengono simulate in base alle schede, quindi le schede di testo e i ritorni a capo vengono sostituiti da spazi vuoti.</td>
</tr>
<tr class="even">
<td>Stili normali e di intestazione</td>
<td>Gli stili di intestazione e stile normali predefiniti da 1 a 9 sono supportati dalle interfacce di <a href="em-setparaformat.md"><strong>EM_SETPARAFORMAT</strong></a> e del <a href="text-object-model.md">modello a oggetti di testo</a> (Tom).</td>
</tr>
<tr class="odd">
<td>Altri tipi di sottolineatura</td>
<td>È stata aggiunta la sottolineatura tratteggiata, tratteggiata, trattino-punto-punto e punto.</td>
</tr>
<tr class="even">
<td>Colorazione sottolineata</td>
<td>Il testo sottolineato può essere contrassegnato con una delle 15 opzioni del documento per i colori di sottolineatura.</td>
</tr>
<tr class="odd">
<td>Testo nascosto</td>
<td>Contrassegnato dall'attributo CHARFORMAT2. Utile per Roundtripping (scrittura in un file in cui è stato letto) di informazioni che normalmente non devono essere visualizzate.</td>
</tr>
<tr class="even">
<td>Altri tasti di scelta rapida predefiniti</td>
<td>Questi tasti di scelta rapida funzionano in modo analogo a quelli di Word. Ad esempio, chiavi inutilizzate per l'accento europeo (solo tastiere USA). Il tasto di scelta rapida numero (CTRL + L) scorre le opzioni di numerazione disponibili, iniziando con Bullet.</td>
</tr>
<tr class="odd">
<td>IME HexToUnicode</td>
<td>Consente a un utente di eseguire la conversione tra esadecimali e Unicode usando tasti di scelta rapida.</td>
</tr>
<tr class="even">
<td>Virgolette intelligenti</td>
<td>Questa funzionalità è attivata e disattivata premendo CTRL + ALT +' per le tastiere statunitensi.</td>
</tr>
<tr class="odd">
<td>Trattini morbidi</td>
<td>Per testo normale, usare 0xAD. Per RTF, usare \- .</td>
</tr>
<tr class="even">
<td>Cursore corsivo</td>
<td>Inoltre, il cursore del mouse assume la forma di una mano quando si supera l'URL.</td>
</tr>
<tr class="odd">
<td>Advanced Typography-opzione</td>
<td>Microsoft Rich Edit 3,0 può utilizzare un'opzione di tipografia avanzata per l'interruzioni di riga e la visualizzazione (vedere <a href="em-gettypographyoptions.md"><strong>EM_GETTYPOGRAPHYOPTIONS</strong></a>). Questa elegante opzione è stata aggiunta principalmente per semplificare la gestione di script complessi (bidirezionali, indiane e Thai). Inoltre, per gli script semplici si verifica una serie di miglioramenti. Alcuni esempi:
<ul>
<li>Al centro, a destra, tabulazioni decimali</li>
<li>Testo completamente giustificato</li>
<li>Sottolineare la media, che fornisce una sottolineatura uniforme anche quando le esecuzioni di testo adiacenti hanno dimensioni del carattere differenti.</li>
</ul></td>
</tr>
<tr class="even">
<td> Supporto di lingue con alfabeti non latini</td>
<td>Microsoft Rich Edit 3,0 supporta la modalità bidirezionale (testo con lingua araba e/o ebraica mista ad altri script), indiane (script indiani come Devangari) e testo tailandese. Per il supporto di questi alfabeti complessi, vengono usati i componenti Advanced Typography e Uniscribe.</td>
</tr>
<tr class="odd">
<td>Associazione di tipi di carattere</td>
<td>Microsoft Rich Edit 3,0 sceglierà automaticamente un tipo di carattere appropriato per i caratteri che non appartengono chiaramente al timbro del set di caratteri corrente. Questa operazione viene eseguita assegnando set di caratteri alle esecuzioni di testo e associando i caratteri a questi set di caratteri. Per ulteriori informazioni, vedere <a href="using-rich-edit-controls.md">associazione di tipi di carattere</a>.</td>
</tr>
<tr class="even">
<td>Opzioni di lettura/scrittura del testo normale specifiche per i set di caratteri</td>
<td>In questo modo è possibile leggere un file usando un set di caratteri e scrivere con un set di caratteri diverso.</td>
</tr>
<tr class="odd">
<td>FORMATO RTF UTF-8</td>
<td>Questa operazione è consigliata per le operazioni di taglia, copia e incolla. Questo formato di file è più compatto rispetto al formato RTF comune, più veloce e compatibile con Unicode.</td>
</tr>
<tr class="even">
<td>Supporto IME Microsoft Office 9 (IME98)</td>
<td>Questa funzionalità IME più potente è stata suddivisa in un modulo indipendente. Funzionalità incluse:
<ul>
<li>Riconversione nelle versioni precedenti, l'utente deve prima eliminare la stringa finale e quindi digitare una nuova stringa per ottenere il candidato corretto. Questa nuova funzionalità consente all'utente di convertire la stringa finale in modalità di composizione, consentendo in tal modo una semplice selezione di una stringa candidata diversa.<br/></li>
<li>Feed di documenti questa funzionalità fornisce IME98 con il testo per il paragrafo corrente, che consente a IME98 di eseguire una conversione più precisa durante la digitazione.<br/></li>
<li>Operazione del mouse questa funzionalità offre un maggiore controllo sulle finestre dei candidati e dell'interfaccia utente durante la digitazione.<br/></li>
<li>Posizione del punto di inserimento questa funzionalità fornisce le informazioni sul punto di inserimento e la riga correnti, utilizzate da IME98 per posizionare le finestre dell'interfaccia utente, ad esempio un elenco di candidati.<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Supporto per Active Input Method Manager (IMM)</td>
<td>Gli utenti possono richiamare l'oggetto IMM attivo, che consente agli utenti di immettere caratteri asiatici nei sistemi statunitensi.</td>
</tr>
<tr class="even">
<td>Supporto di HexToUnicode</td>
<td>Gli utenti possono eseguire la conversione tra notazione esadecimale e Unicode usando i tasti di scelta rapida.</td>
</tr>
<tr class="odd">
<td>Altri Roundtripping RTF</td>
<td>Il testo RTF letto da un file verrà riscritto intatto.</td>
</tr>
<tr class="even">
<td>Modalità di compatibilità 1,0 migliorata</td>
<td>Microsoft Rich Edit 3,0 è in grado di emulare il comportamento di Microsoft Rich Edit 1,0. È ad esempio possibile modificare i mapping tra MBCS e Unicode Character-position (CP).</td>
</tr>
<tr class="odd">
<td>Maggiore controllo di blocco</td>
<td>La visualizzazione può essere bloccata su più chiamate API e quindi sbloccata per visualizzare gli aggiornamenti.</td>
</tr>
<tr class="even">
<td>Maggiore controllo di annullamento</td>
<td>Il rollback può essere sospeso e ripreso (requisito IME).</td>
</tr>
<tr class="odd">
<td>Aumenta/diminuisci dimensioni carattere</td>
<td>Aumenta o diminuisce le dimensioni del carattere in uno dei sei valori standard (12, 28, 36, 48, 72 e 80 punti).</td>
</tr>
</tbody>
</table>



 

### <a name="rich-edit-version-41"></a>Modifica avanzata versione 4,1

La classe della finestra per Microsoft Rich Edit 4,1 è la \_ classe MSFTEDIT. Le nuove funzionalità per Microsoft Rich Edit 4,1 includono la sillabazione, la rotazione della pagina e il supporto di Text Services Framework (TSF).

Microsoft Rich Edit 4,1 include le funzionalità seguenti, oltre alle funzionalità fornite da [Rich Edit versione 3,0](#rich-edit-version-30).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Sillabazione</td>
<td>La sillabazione è supportata tramite le API seguenti: <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a>, <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a>e <a href="em-gethyphenateinfo.md"><strong>EM_GETHYPHENATEINFO</strong></a>.</td>
</tr>
<tr class="even">
<td>Rotazione pagina</td>
<td>Il layout dall'alto verso il basso e dal basso verso l'alto è supportato tramite <a href="em-setpagerotate.md"><strong>EM_SETPAGEROTATE</strong></a> e <a href="em-getpagerotate.md"><strong>EM_GETPAGEROTATE</strong></a>.</td>
</tr>
<tr class="odd">
<td>Supporto del Framework dei servizi di testo</td>
<td><ul>
<li>Per attivare TSF e determinate funzionalità TSF, usare gli stili seguenti in <a href="em-seteditstyle.md"><strong>EM_SETEDITSTYLE</strong></a>: SES_USECTF, SES_CTFALLOWEMBED, SES_CTFALLOWPROOFING e SES_CTFALLOWSMARTTAG.</li>
<li>Per impostare e ottenere la distorsione della modalità TSF, utilizzare <a href="em-setctfmodebias.md"><strong>EM_SETCTFMODEBIAS</strong></a> e <a href="em-getctfmodebias.md"><strong>EM_GETCTFMODEBIAS</strong></a>.</li>
<li>Per impostare e ottenere lo stato della tastiera TSF, utilizzare <a href="em-setctfopenstatus.md"><strong>EM_SETCTFOPENSTATUS</strong></a> e <a href="em-getctfopenstatus.md"><strong>EM_GETCTFOPENSTATUS</strong></a>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Supporto IME aggiuntivo</td>
<td><ul>
<li>Per impostare e ottenere la distorsione della modalità IME, utilizzare <a href="em-setimemodebias.md"><strong>EM_SETIMEMODEBIAS</strong></a> e <a href="em-getimemodebias.md"><strong>EM_GETIMEMODEBIAS</strong></a>.</li>
<li>Per ottenere le proprietà e le funzionalità dell'IME, utilizzare <a href="em-getimeproperty.md"><strong>EM_GETIMEPROPERTY</strong></a>.</li>
<li>Per ottenere il testo della composizione IME, utilizzare <a href="em-getimecomptext.md"><strong>EM_GETIMECOMPTEXT</strong></a>.</li>
<li>Per determinare se le impostazioni locali sono le impostazioni locali dell'Asia orientale, utilizzare <a href="em-isime.md"><strong>EM_ISIME</strong></a>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Impostazioni <a href="em-seteditstyle.md"><strong>EM_SETEDITSTYLE</strong></a> aggiuntive</td>
<td>Oltre alle impostazioni di TSF, sono disponibili nuove impostazioni che escludono gli IME, impostano il flusso di testo bidirezionale, usano i tipi di carattere DRAFTMODE e altro ancora.</td>
</tr>
<tr class="even">
<td>Impostazioni <a href="em-setcharformat.md"><strong>EM_SETCHARFORMAT</strong></a> aggiuntive</td>
<td>I nuovi flag consentono al client di impostare il tipo di carattere e le dimensioni del carattere predefiniti per un determinato LCID o set di caratteri per impostare il tipo di carattere predefinito per il controllo, in modo da impedire che il cambio di tastiera corrisponda al tipo di carattere e altro ancora.</td>
</tr>
<tr class="odd">
<td>Limitazione dell'input al testo ANSI</td>
<td>L'utilizzo di <a href="/windows/win32/api/richedit/ne-richedit-textmode"><strong>TM_SINGLECODEPAGE</strong></a> in <a href="em-settextmode.md"><strong>EM_SETTEXTMODE</strong></a> impedisce l'immissione di un controllo Rich Edit da input Unicode.</td>
</tr>
<tr class="even">
<td>Notifica parole chiave RTF non supportata</td>
<td><a href="en-lowfirtf.md">EN_LOWFIRTF</a> avverte un'applicazione quando è presente una parola chiave RTF non supportata.</td>
</tr>
<tr class="odd">
<td>Elementi del linguaggio aggiuntivi supportati</td>
<td>Altre lingue includono armeno, Divehi, telugu e altri.</td>
</tr>
<tr class="even">
<td>Supporto migliorato per le tabelle</td>
<td>Le funzionalità includono: wrapping all'interno di celle, gestione migliorata tramite RTF e navigazione migliorata.</td>
</tr>
<tr class="odd">
<td>ES_VERTICAL</td>
<td>Lo stile della finestra di <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> è supportato.</td>
</tr>
<tr class="even">
<td>Supporto <a href="/windows/desktop/inputdev/wm-unichar"><strong>WM_UNICHAR</strong></a></td>
<td>Per inviare o inviare caratteri Unicode alle finestre ANSI, utilizzare <a href="/windows/desktop/inputdev/wm-unichar"><strong>WM_UNICHAR</strong></a>. Equivale a <a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a>, ma USA (UTF)-32.</td>
</tr>
</tbody>
</table>



 

## <a name="unsupported-edit-control-functionality"></a>Funzionalità di controllo di modifica non supportata

I controlli Rich Edit supportano la maggior parte delle funzionalità per i controlli di modifica su più righe. In questa sezione sono elencati i messaggi di controllo e gli stili della finestra di modifica *non* supportati dai controlli Rich Edit.

I messaggi seguenti vengono elaborati dai controlli di modifica ma *non* dai controlli Rich Edit.



| Messaggio non supportato                         | Commenti                                                                                                                    |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**\_FMTLINES em**](em-fmtlines.md)         | Non supportata.                                                                                                              |
| [**GetHandle EM \_**](em-gethandle.md)       | I controlli Rich Edit non archiviano il testo come una semplice matrice di caratteri.                                                       |
| [**\_GETIMESTATUS em**](em-getimestatus.md) | Non supportata.                                                                                                              |
| [**\_GETmargini em**](em-getmargins.md)     | Non supportata.                                                                                                              |
| [**filehandle EM \_**](em-sethandle.md)       | I controlli Rich Edit non archiviano il testo come una semplice matrice di caratteri.                                                       |
| [**\_SETIMESTATUS em**](em-setimestatus.md) | Non supportata.                                                                                                              |
| [**\_margini em**](em-setmargins.md)     | Supportato in Microsoft Rich Edit 3,0.                                                                                       |
| [**\_SETRECTNP em**](em-setrectnp.md)       | Non supportata.                                                                                                              |
| [**\_SETTABSTOPS em**](em-settabstops.md)   | Viene invece usato il messaggio [**\_ SETPARAFORMAT em**](em-setparaformat.md) . Supportato in Microsoft Rich Edit 3,0.<br/> |
| [**\_CTLCOLOR WM**](/windows/desktop/DevNotes/wm-ctlcolor-)    | Viene invece usato il messaggio [**\_ SETBKGNDCOLOR em**](em-setbkgndcolor.md) .                                                  |
| [**\_tipo di carattere WM GetFont**](/windows/desktop/winmsg/wm-getfont)        | Viene invece usato il messaggio [**\_ GETCHARFORMAT em**](em-getcharformat.md) .                                                  |



 

Gli stili della finestra seguenti vengono usati con i controlli di modifica su più righe, ma non con i controlli Rich Edit: [**es \_ minuscol**](edit-control-styles.md), [**es \_ maiuscole**](edit-control-styles.md)ed [**es \_ OEMCONVERT**](edit-control-styles.md).

## <a name="rich-edit-shortcut-keys"></a>Tasti di scelta rapida modifica Rich

I controlli Rich Edit supportano i seguenti tasti di scelta rapida.



| Chiavi                      | Gestione operativa                                                                                                                               | Commenti                                                                                                                                                                                                                       |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MAIUSC + BACKSPACE           | Generare un LRM/LRM su una tastiera BiDi                                                                                                    | Specifiche BiDi                                                                                                                                                                                                                  |
| CTRL+TAB                  | Scheda                                                                                                                                      |                                                                                                                                                                                                                                |
| Ctrl + Cancella                | Seleziona tutto                                                                                                                               |                                                                                                                                                                                                                                |
| Ctrl + tastierino numerico 5         | Seleziona tutto                                                                                                                               |                                                                                                                                                                                                                                |
| CTRL+A                    | Seleziona tutto                                                                                                                               |                                                                                                                                                                                                                                |
| CTRL+E                    | Allineamento al centro                                                                                                                         |                                                                                                                                                                                                                                |
| CTRL+J                    | Allineamento giustificato                                                                                                                        |                                                                                                                                                                                                                                |
| CTRL+R                    | Allineamento a destra                                                                                                                          |                                                                                                                                                                                                                                |
| CTRL+L                    | Allineamento a sinistra                                                                                                                           |                                                                                                                                                                                                                                |
| CTRL+C                    | Copia                                                                                                                                     |                                                                                                                                                                                                                                |
| CTRL+V                    | Incolla                                                                                                                                    |                                                                                                                                                                                                                                |
| CTRL+X                    | Taglia                                                                                                                                      |                                                                                                                                                                                                                                |
| CTRL+Z                    | Annulla                                                                                                                                     |                                                                                                                                                                                                                                |
| CTRL+Y                    | Ripeti                                                                                                                                     |                                                                                                                                                                                                                                |
| CTRL +' +' (CTRL + MAIUSC +' =') | Apice                                                                                                                              |                                                                                                                                                                                                                                |
| CTRL +' ='                  | Pedice                                                                                                                                |                                                                                                                                                                                                                                |
| CTRL+1                    | Interlinea = 1 riga.                                                                                                                   |                                                                                                                                                                                                                                |
| CTRL+2                    | Interlinea = 2 righe.                                                                                                                  |                                                                                                                                                                                                                                |
| CTRL+5                    | Spaziatura riga = 1,5 righe.                                                                                                                |                                                                                                                                                                                                                                |
| CTRL +' (apostrofo)       | Accento acuto                                                                                                                             | Dopo aver premuto il tasto scorciatoia, premere la lettera appropriata, ad esempio a, e o u. Si applica solo alle tastiere inglese, francese, tedesco, italiano e spagnolo.                                                         |
| CTRL + \` (grave)           | Accento grave                                                                                                                             | Vedere i commenti CTRL +'.                                                                                                                                                                                                           |
| Ctrl + ~ (tilde)            | Carattere tilde                                                                                                                             | Vedere i commenti CTRL +'.                                                                                                                                                                                                           |
| CTRL +; virgola        | Dieresto accento                                                                                                                            | Vedere i commenti CTRL +'.                                                                                                                                                                                                           |
| CTRL + MAIUSC + 6              | Accento circonflesso (accento circonflesso)                                                                                                                | Vedere i commenti CTRL +'.                                                                                                                                                                                                           |
| CTRL +, (virgola)            | Accento cediglia                                                                                                                           | Vedere i commenti CTRL +'.                                                                                                                                                                                                           |
| CTRL + MAIUSC +' (apostrofo) | Attiva virgolette intelligenti                                                                                                                    |                                                                                                                                                                                                                                |
| Backspace                 | Se il testo è protetto, emette un segnale acustico e non lo elimina. In caso contrario, eliminare il carattere precedente.                                                   |                                                                                                                                                                                                                                |
| CTRL+BACKSPACE            | Elimina parola precedente. Viene generato un \_ codice F16 VK.                                                                                     |                                                                                                                                                                                                                                |
| F16                       | Uguale a BACKSPACE.                                                                                                                       |                                                                                                                                                                                                                                |
| CTRL+INS               | Copia                                                                                                                                     |                                                                                                                                                                                                                                |
| Maiusc+Ins              | Incolla                                                                                                                                    |                                                                                                                                                                                                                                |
| Insert                    | Overwrite                                                                                                                                | DBCS non sovrascrive.                                                                                                                                                                                                       |
| CTRL+Freccia SINISTRA           | Spostare il cursore di una parola verso sinistra.                                                                                                        | Sulla tastiera BiDi questo dipende dalla direzione del testo.                                                                                                                                                                   |
| CTRL+Freccia DESTRA          | Spostare il cursore di una parola verso destra.                                                                                                       | Vedere i commenti CTRL + freccia sinistra.                                                                                                                                                                                                  |
| CTRL + MAIUSC di sinistra           | Allineamento a sinistra                                                                                                                           | Nei documenti BiDi questa operazione è per l'ordine di lettura da sinistra a destra.                                                                                                                                                                    |
| CTRL + MAIUSC a destra          | Allineamento a destra                                                                                                                          | Nei documenti BiDi questa operazione è per l'ordine di lettura da destra a sinistra.                                                                                                                                                                    |
| CTRL+Freccia SU             | Passare alla riga precedente.                                                                                                                  |                                                                                                                                                                                                                                |
| CTRL+Freccia GIÙ           | Passare alla riga seguente.                                                                                                                  |                                                                                                                                                                                                                                |
| CTRL+HOME                 | Passare all'inizio del documento.                                                                                                   |                                                                                                                                                                                                                                |
| CTRL+FINE                  | Passare alla fine del documento.                                                                                                         |                                                                                                                                                                                                                                |
| CTRL + PGSU              | Spostare una pagina verso l'alto.                                                                                                                        | Se in SystemEditMode e in un controllo a riga singola, non eseguire alcuna operazione.                                                                                                                                                                      |
| CTRL + PGGIÙ            | Spostare una pagina verso il basso.                                                                                                                      | Vedere la pagina relativa ai commenti CTRL + PGSU.                                                                                                                                                                                                     |
| CTRL+CANC               | Elimina la parola successiva o i caratteri selezionati.                                                                                             |                                                                                                                                                                                                                                |
| MAIUSC+CANC              | Taglia i caratteri selezionati.                                                                                                             |                                                                                                                                                                                                                                |
| ESC                       | Arresta trascinamento della selezione.                                                                                                                          | Durante il trascinamento della selezione del testo.                                                                                                                                                                                               |
| ALT + ESC                   | Modificare l'applicazione attiva.                                                                                                           |                                                                                                                                                                                                                                |
| ALT+X                     | Converte il valore esadecimale Unicode che precede il punto di inserimento nel carattere Unicode corrispondente.                             |                                                                                                                                                                                                                                |
| ALT + MAIUSC + X               | Converte il carattere Unicode che precede il punto di inserimento nel valore esadecimale Unicode corrispondente.                             |                                                                                                                                                                                                                                |
| Alt + 0xxx (tastierino numerico)     | Inserisce i valori Unicode se xxx è maggiore di 255. Quando xxx è minore di 256, viene inserito il testo dell'intervallo ASCI in base alla tastiera corrente. | Deve immettere valori decimali.                                                                                                                                                                                                     |
| ALT + MAIUSC + CTRL + F12        | Da esadecimale a Unicode.                                                                                                                          | Nel caso in cui ALT + X sia già usato per un altro uso.                                                                                                                                                                                |
| ALT + MAIUSC + CTRL + F11        | Il testo selezionato verrà restituito alla finestra del debugger e salvato in% temp% \\DumpFontInfo.txt.                                               | Solo per il debug (è necessario impostare il flag = 8 in Win.ini)                                                                                                                                                                                 |
| CTRL+MAIUSC+A              | Imposta tutte le maiuscole.                                                                                                                            |                                                                                                                                                                                                                                |
| CTRL+MAIUSC+L              | Stile del punto elenco di violino.                                                                                                                     |                                                                                                                                                                                                                                |
| CTRL+MAIUSC+Freccia DESTRA    | Aumentare le dimensioni del carattere.                                                                                                                      | Dimensioni del carattere modificate per 1 punto nell'intervallo 4PT-11pt; di 2points per 12pt-28pt; viene modificato da 28pt-> 36pt-> 48pt-> 72pt-> 80pt; viene modificato di 10 punti nell'intervallo 80pt-1630pt; il valore massimo è 1638. |
| CTRL+MAIUSC+Freccia SINISTRA     | Ridurre le dimensioni del carattere.                                                                                                                      | Vedere CTRL + MAIUSC + Commenti freccia destra.                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Uso di controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Controlli Rich Edit senza finestra](windowless-rich-edit-controls.md)
</dt> </dl>

