---
title: Informazioni sui controlli Rich Edit
description: Questa sezione presenta i controlli Rich Edit.
ms.assetid: ab9dcdf4-a311-4159-8f37-e67e144f31f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 742295358be32fa318334ceac7f89607adcbba12
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423991"
---
# <a name="about-rich-edit-controls"></a>Informazioni sui controlli Rich Edit

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Versioni di Rich Edit](#versions-of-rich-edit)
    -   [Rich Edit versione 1.0](#rich-edit-version-10)
    -   [Rich Edit versione 2.0](#rich-edit-version-20)
    -   [Rich Edit versione 3.0](#rich-edit-version-30)
    -   [Rich Edit versione 4.1](#rich-edit-version-41)
-   [Funzionalità del controllo di modifica non supportate](#unsupported-edit-control-functionality)
-   [Tasti di scelta rapida rich edit](#rich-edit-shortcut-keys)
-   [Argomenti correlati](#related-topics)

## <a name="versions-of-rich-edit"></a>Versioni di Rich Edit

La specifica originale per i controlli Rich Edit è Microsoft Rich Edit 1.0. La specifica corrente è Microsoft Rich Edit 4.1. Ogni versione di Rich Edit è un superset di quella precedente, ad eccezione del fatto che solo le build asiatiche di Microsoft Rich Edit 1.0 hanno un'opzione di testo verticale. Prima di creare un controllo Rich Edit, è necessario chiamare la [**funzione LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) per verificare quale versione di Microsoft Rich Edit è installata.

Nella tabella seguente viene illustrata la DLL corrispondente alla versione di Rich Edit. Si noti che il nome del file non è cambiato dalla versione 2.0 alla versione 3.0. In questo modo è possibile aggiornare la versione 2.0 alla versione 3.0 senza interrompere il codice esistente.



| Versione rich edit | DLL          | Classe Window    |
|-------------------|--------------|-----------------|
| 1.0               | Riched32.dll | CLASSE \_ RICHEDIT |
| 2,0               | Riched20.dll | CLASSE \_ RICHEDIT |
| 3.0               | Riched20.dll | CLASSE \_ RICHEDIT |
| 4.1               | Msftedit.dll | CLASSE \_ MSFTEDIT |



 

### <a name="rich-edit-version-10"></a>Rich Edit versione 1.0

Microsoft Rich Edit 1.0 include le funzionalità seguenti.



|    Funzionalità   | Descrizione   |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Immissione e selezione di testo                                                           | Selezione e immissione di testo per lo più standard (controllo di modifica di sistema). Supporto della barra di selezione (la barra di selezione è un'area non contrassegnata a sinistra di ogni paragrafo che, quando si fa clic, seleziona la riga). Opzioni per il ritorno a capo automatico e la selezione automatica delle parole. Selezione a singolo, doppio e triplo clic. |
| Modifica di ANSI (set di caratteri a byte singolo ( SBCS) e set di caratteri multibyte (MBCS) | Non esiste tuttavia alcuna modifica Unicode.                                                                                                                                                                                                                                                     |
| Set di base di proprietà di formattazione carattere/paragrafo                             | Vedere [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) e [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat).                                                                                                                                                                                                                |
| Proprietà di formattazione dei caratteri                                                    | Nome e dimensioni del carattere, grassetto, corsivo, sottolineatura a tinta unita, barrato, protetto, collegamento, offset e colore del testo.                                                                                                                                                                                   |
| Proprietà di formattazione dei paragrafi                                                    | Rientro iniziale, rientro a destra, offset di riga successivo, punto elenco, allineamento (a sinistra, al centro, a destra) e tabulazioni.                                                                                                                                                                                    |
| Trova in avanti                                                                       | Include opzioni senza distinzione tra maiuscole e minuscole e intere parole.                                                                                                                                                                                                                                   |
| Interfaccia basata su messaggi                                                            | Quasi un superset del set di messaggi di controllo di modifica di sistema più due interfacce, [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) [**e IRichEditOleCallback.**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback)                                                                                                              |
| Oggetti incorporati                                                                   | Richiede la collaborazione client basata [**sulle interfacce IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) e [**IRichEditOleCallback.**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback)                                                                                                                                          |
| Supporto del menu del pulsante destro del mouse                                                          | Usa [**l'interfaccia IRichEditOleCallback.**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback)                                                                                                                                                                                                                      |
| Modifica con trascinamento della selezione                                                              | La modifica con trascinamento della selezione è supportata.                                                                                                                                                                                                                                                       |
| Notifiche                                                                      | [**WM \_ Messaggi COMMAND**](/windows/desktop/menurc/wm-command) inviati al client più alcuni altri. Si tratta di un superset di notifiche di controllo comune.                                                                                                                                                 |
| Annullamento/annullamento a livello singolo                                                             | Si comporta in modo analogo al controllo di modifica del sistema. Se **si seleziona** Annulla, l'ultima azione viene annullata e l'azione diventa la nuova azione Di **nuovo.**                                                                                                                                          |
| Testo verticale semplice                                                               | (solo compilazioni in Asia).                                                                                                                                                                                                                                                                      |
| Supporto IME (Input Method Editor)                                                  | (solo compilazioni in lingue asiatiche).                                                                                                                                                                                                                                                                      |
| Modifica WYSIWYG con metriche della stampante                                              | Questa funzionalità è necessaria in particolare per Microsoft WordPad.                                                                                                                                                                                                                              |
| Taglia/Copia/Incolla/StreamIn/StreamOut                                                  | Con testo normale (**CF \_ TEXT**) o RTF (Rich Text Format) con e senza oggetti .                                                                                                                                                                                                        |
| Codebase C                                                                        | Il codice è scritto in C, che fornisce una base solida e versatile.                                                                                                                                                                                                                |
| Compilazioni diverse per script diversi                                             | Microsoft Rich Edit 1.0 risolve i problemi di localizzazione con build diverse.                                                                                                                                                                                                              |



 

### <a name="rich-edit-version-20"></a>Rich Edit versione 2.0

Microsoft Rich Edit 2.0 ha incorporato diverse funzionalità aggiuntive, ad esempio il supporto per le lingue Unicode e asiatiche, l'annullamento a più livelli, le interfacce Component Object Model (COM) e numerosi miglioramenti dell'interfaccia utente.

Microsoft Rich Edit 2.0 include le funzionalità seguenti oltre alle funzionalità fornite da [Microsoft Rich Edit 1.0.](#rich-edit-version-10)



|    Funzionalità                                           |    Descrizione                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unicode                                       | Unicode semplifica la gestione del testo internazionale. Per mantenere la compatibilità con i documenti non Unicode esistenti, tuttavia, è necessaria la possibilità di eseguire la conversione in/da testo normale e RTF non Unicode.                                                                                                                                                             |
| Supporto internazionale generale                 | Algoritmo di interruzione di riga generale (estensione delle regole Kinsoku), collegamento semplice del tipo di carattere, cambio del tipo di carattere da tastiera.                                                                                                                                                                                                                                                                          |
| Supporto per l'Asia                                 | Il livello 2 (finestra di dialogo) e il 3 (inline) sono supportati negli IME.                                                                                                                                                                                                                                                                                                                            |
| Supporto per Trova/Trova in basso                     | La ricerca in avanti e indietro è supportata.                                                                                                                                                                                                                                                                                                                                         |
| Supporto bidirezionale                         | È incluso in Microsoft Rich Edit 2.1                                                                                                                                                                                                                                                                                                                                          |
| Annullamento multilivello                               | Un'architettura di annullamento estendibile consente al client di partecipare al modello di annullamento a livello di applicazione.                                                                                                                                                                                                                                                                                         |
| Supporto del mouse Magellan                        | Questo è il mouse con un rullo per lo scorrimento.                                                                                                                                                                                                                                                                                                                                       |
| Supporto di tipi di carattere doppi                             | La tastiera può cambiare automaticamente i tipi di carattere quando il tipo di carattere attivo non è appropriato per la tastiera corrente, ad esempio i caratteri Kanji in Times New Roman.                                                                                                                                                                                                                            |
| Applicare il tipo di carattere intelligente                              | La richiesta di modifica del tipo di carattere non applica i tipi di carattere occidentali ai caratteri asiatici.                                                                                                                                                                                                                                                                                                                |
| Visualizzazione migliorata                              | Una bitmap fuori schermo viene usata quando più tipi di carattere si verificano sulla stessa riga. In questo modo, ad esempio, l'ultima lettera della parola cool non può essere traslata.                                                                                                                                                                                                                           |
| Supporto della trasparenza                          | Anche in modalità senza finestra.                                                                                                                                                                                                                                                                                                                                                             |
| Colori di selezione del sistema                       | Usato per la selezione di testo.                                                                                                                                                                                                                                                                                                                                                             |
| Riconoscimento automatico degli URL                     | Può verificare la presenza di diversi formati di URL (ad esempio, http:)                                                                                                                                                                                                                                                                                                                           |
| Compatibilità dell'interfaccia utente di modifica di Microsoft Word          | Selezione, semantica della tastiera del cursore.                                                                                                                                                                                                                                                                                                                                                  |
| Word standard EOP                             | Il segno di fine paragrafo (CR) può anche gestire il ritorno a capo/avanzamento riga (CR/LF) (ritorno a capo, avanzamento riga).                                                                                                                                                                                                                                                                       |
| Funzionalità di testo normale e RTF | Formato a carattere singolo e formato a paragrafo singolo.                                                                                                                                                                                                                                                                                                                                 |
| Controlli a riga singola e multilinea            | Tronca alla prima fine del paragrafo e senza ritorno a capo.                                                                                                                                                                                                                                                                                                                                  |
| Tasti di scelta rapida                              | I tasti di scelta rapida sono supportati.                                                                                                                                                                                                                                                                                                                                                      |
| Stile della finestra password                         | I controlli di modifica delle password vengono forniti [**tramite EM \_ GETPASSWORDCHAR**](em-getpasswordchar.md) [**ed EM \_ SETPASSWORDCHAR**](em-setpasswordchar.md).                                                                                                                                                                                                                                 |
| Architettura scalabile                         | Per ridurre le dimensioni dell'istanza.                                                                                                                                                                                                                                                                                                                                                             |
| Interfacce e operazioni senza finestra           | Questo viene fornito tramite le [**interfacce ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) [**e ITextServices.**](/windows/desktop/api/Textserv/nl-textserv-itextservices)                                                                                                                                                                                                                                                                   |
| Interfacce duali COM                           | Interfacce TOM (Text Object Model).                                                                                                                                                                                                                                                                                                                                                  |
| CHARFORMAT2                                   | Aggiunta dello spessore del carattere, del colore di sfondo, dell'identificatore delle impostazioni locali, del tipo di sottolineatura, apice e pedice (oltre all'offset), effetto disabilitato. Solo per il roundtripping RTF, aggiunta quantità di spazio tra le lettere, dimensioni twip sopra le quali eseguire la crenatura della coppia di caratteri, tipo di testo animato, vari effetti: ombreggiatura/contorno del carattere, tutte maiuscole, maiuscoletto, nascosto, in rilievo, imprint e rivisto. |
| PARAFORMAT2                                   | Aggiunta di uno spazio prima e dopo e l'interlinea di Word. Solo per il roundtripping RTF, aggiunta di spessore/stile dell'ombreggiatura, numerazione di inizio/stile/tabulazione, spazio del bordo/larghezza/lati, allineamento delle schede/leader, vari effetti di paragrafo di Word: paragrafo RTL, keep, keep-next, page-break-before, no-line-number, no-hyphenate, do-not-hyphenate, side-by-side.                                         |
| Più roundtripping RTF                        | Tutte le proprietà FormatFont e FormatParagraph di Word.                                                                                                                                                                                                                                                                                                                           |
| Stabilità e stabilizzazione del codice              | Esempi: convalida di parametri e oggetti, invarianti delle funzioni, protezioni di reentrancy, stabilizzazione degli oggetti.                                                                                                                                                                                                                                                                             |
| Infrastruttura di test solida                 | Inclusi test di regressione estesi.                                                                                                                                                                                                                                                                                                                                               |
| prestazioni migliorate                          | Dimensioni working set, tempi di caricamento e visualizzazione più rapidi e così via.                                                                                                                                                                                                                                                                                                                     |
| Codebase C++                                 | Il codice è scritto in C++, che fornisce una solida base su cui creare Microsoft Rich Edit 3.0.                                                                                                                                                                                                                                                                             |



 

Con alcune eccezioni, Microsoft Rich Edit 2.0 usa le stesse funzioni, strutture e messaggi di Microsoft Rich Edit 1.0. Si notino tuttavia le differenze seguenti:

-   Il nome della classe della finestra Microsoft Rich Edit 1.0 è **RichEdit.** Microsoft Rich Edit 2.0 include entrambe le classi finestra ANSI e Unicode **RichEdit20A** e **RichEdit20W,** rispettivamente. Per specificare la classe della finestra rich edit appropriata, usare la costante RICHEDIT CLASS definita dal file Richedit.h a seconda della definizione del \_ flag di compilazione UNICODE.
-   In Microsoft Rich Edit 2.0, se si crea un controllo Rich Edit Unicode (che prevede messaggi di testo Unicode), è necessario specificare solo i dati Unicode in qualsiasi messaggio di finestra inviato al controllo. Analogamente, se si crea un controllo Rich Edit ANSI, inviare solo dati ANSI o DBCS (Double Byte Character Set). È possibile usare la [**funzione IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) per determinare se un controllo Rich Edit usa messaggi di testo Unicode. Si noti che le interfacce COM rich edit usano testo Unicode a meno che non si verifichi un argomento della tabella codici.
-   Microsoft Rich Edit 1.0 usa combinazioni di caratteri CR/LF per i marcatori di paragrafo. Microsoft Rich Edit 2.0 usava solo un carattere di ritorno a capo (' \\ r'). Microsoft Rich Edit 3.0 usa solo un carattere di ritorno a capo, ma può emulare Microsoft Rich Edit 1.0 a questo proposito.
-   Microsoft Rich Edit 2.0 ha introdotto i nuovi messaggi seguenti. 

    | Message                                           | Descrizione                                                             |
    |---------------------------------------------------|-------------------------------------------------------------------------|
    | [**EM \_ AUTOURLDETECT**](em-autourldetect.md)     | Abilita o disabilita il rilevamento automatico degli URL.                            |
    | [**EM \_ CANREDO**](em-canredo.md)                 | Determina se sono presenti azioni nella coda di redo.             |
    | [**EM \_ GETIMECOMPMODE**](em-getimecompmode.md)   | Recupera la modalità IME (Input Method Editor) corrente.                   |
    | [**EM \_ GETLANGOPTIONS**](em-getlangoptions.md)   | Recupera le opzioni per il supporto IME e delle lingue asiatiche.                   |
    | [**EM \_ GETREDONAME**](em-getredoname.md)         | Recupera il nome del tipo dell'azione successiva nella coda di redo.           |
    | [**EM \_ GETTEXTMODE**](em-gettextmode.md)         | Recupera la modalità testo o il livello di annullamento.                                  |
    | [**EM \_ GETUNDONAME**](em-getundoname.md)         | Recupera il nome del tipo dell'azione successiva nella coda di annullamento.           |
    | [**EM \_ REDO**](em-redo.md)                       | Ripristina l'azione successiva nella coda di ripeti.                               |
    | [**EM \_ SETLANGOPTIONS**](em-setlangoptions.md)   | Imposta le opzioni per il supporto delle lingue iME e dell'Asia.                        |
    | [**EM \_ SETTEXTMODE**](em-settextmode.md)         | Imposta la modalità testo o il livello di annullamento.                                       |
    | [**EM \_ SETUNDOLIMIT**](em-setundolimit.md)       | Imposta il numero massimo di azioni nella coda di annullamento.                   |
    | [**EM \_ STOPGROUPTYPING**](em-stopgrouptyping.md) | Arresta il raggruppamento di azioni di digitazione consecutive nell'azione di annullamento corrente. |

    

     

-   Microsoft Rich Edit 2.0 ha introdotto le nuove strutture seguenti. 

    | Struttura                          | Descrizione                                      |
    |------------------------------------|--------------------------------------------------|
    | [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) | Contiene informazioni sulla formattazione dei caratteri. |
    | [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) | Contiene informazioni sulla formattazione dei paragrafi. |

    

     

-   I messaggi seguenti sono supportati solo nelle versioni in lingua Asia di Microsoft Rich Edit 1.0. Non sono supportati nelle versioni successive di Rich Edit.

    [**EM \_ CONVPOSITION**](em-convposition.md)

    [**EM \_ GETIMECOLOR**](em-getimecolor.md)

    [**EM \_ GETIMEOPTIONS**](em-getimeoptions.md)

    [**EM \_ GETPUNCTUATION**](em-getpunctuation.md)

    [**EM \_ GETWORDWRAPMODE**](em-getwordwrapmode.md)

    [**EM \_ SETIMECOLOR**](em-setimecolor.md)

    [**EM \_ SETIMEOPTIONS**](em-setimeoptions.md)

    [**EM \_ SETPUNCTUATION**](em-setpunctuation.md)

    [**EM \_ SETWORDWRAPMODE**](em-setwordwrapmode.md)

### <a name="rich-edit-version-30"></a>Rich Edit versione 3.0

Microsoft Rich Edit 3.0 è una SINGOLA DLL scalabile a livello mondiale che offre prestazioni elevate e compatibilità con Word in un pacchetto di piccole dimensioni. Le nuove funzionalità per Microsoft Rich Edit 3.0 includono testo più ricco, zoom, associazione dei tipi di carattere, supporto IME più potente e supporto di script complessi (bidirezionale, indic e tailandese).

Microsoft Rich Edit 3.0 include le funzionalità seguenti oltre alle funzionalità fornite da [Rich Edit versione 2.0.](#rich-edit-version-20)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Zoom</td>
<td>Il fattore di zoom è dato da un rapporto.</td>
</tr>
<tr class="even">
<td>Numerazione dei paragrafi (a livello singolo)</td>
<td>Numeri numerici, alfabetici superiori e inferiori o numeri romani.</td>
</tr>
<tr class="odd">
<td>Tabelle semplici</td>
<td>L'eliminazione e l'inserimento di righe è possibile, ma non il ridimensionamento né il ritorno a capo all'interno delle celle. Con la tipografia avanzata attivata (vedere <a href="em-gettypographyoptions.md"><strong>EM_GETTYPOGRAPHYOPTIONS</strong></a>), Microsoft Rich Edit 3.0 può allineare le colonne al centro o a destra e includere i decimali. Le celle vengono simulate da tabulazioni, quindi le tabulazioni di testo e i ritorni a capo vengono sostituiti da spazi vuoti.</td>
</tr>
<tr class="even">
<td>Stili normali e di intestazione</td>
<td>Gli stili di stile normale e di intestazione predefiniti da 1 a 9 sono supportati dalle <a href="em-setparaformat.md"><strong>interfacce EM_SETPARAFORMAT</strong></a> e <a href="text-object-model.md">TOM (Text Object Model).</a></td>
</tr>
<tr class="odd">
<td>Altri tipi di sottolineatura</td>
<td>Sono state aggiunte sottolineatura tratteggiata, tratteggiata, punti e punti.</td>
</tr>
<tr class="even">
<td>Colorazione della sottolineatura</td>
<td>Il testo sottolineato può essere contrassegnato con una delle 15 opzioni disponibili per i colori di sottolineatura.</td>
</tr>
<tr class="odd">
<td>Testo nascosto</td>
<td>Contrassegnato dall'attributo CHARFORMAT2. Utile per il roundtripping (scrittura in un file di ciò che è stato letto) di informazioni che normalmente non devono essere visualizzate.</td>
</tr>
<tr class="even">
<td>Altri tasti di scelta rapida predefiniti</td>
<td>Questi tasti di scelta rapida funzionano come quelli in Word. Ad esempio, i tasti non accentati europai (solo tastiere degli Stati Uniti). Il tasto di scelta rapida (CTRL+L) consente di scorrere le opzioni di numerazione disponibili, a partire dal punto elenco.</td>
</tr>
<tr class="odd">
<td>HexToUnicode IME</td>
<td>Consente a un utente di eseguire la conversione tra formato esadecimale e Unicode usando i tasti di scelta rapida.</td>
</tr>
<tr class="even">
<td>Inglesi</td>
<td>Questa funzionalità è attivata e disattivata da CTRL+ALT+' per le tastiere degli Stati Uniti.</td>
</tr>
<tr class="odd">
<td>Trattini soft</td>
<td>Per il testo normale, usare 0xAD. Per RTF, usare \- .</td>
</tr>
<tr class="even">
<td>Cursore corsivo</td>
<td>Inoltre, il cursore del mouse assume la forma di una mano quando viene posizionato su URL.</td>
</tr>
<tr class="odd">
<td>Opzione tipografica avanzata</td>
<td>Microsoft Rich Edit 3.0 può usare un'opzione tipografica avanzata per l'interruzione di riga e la visualizzazione (vedere <a href="em-gettypographyoptions.md"><strong>EM_GETTYPOGRAPHYOPTIONS</strong></a>). Questa opzione elegante è stata aggiunta principalmente per facilitare la gestione di script complessi (bidirezionali, indic e thai). Inoltre, si verificano una serie di miglioramenti per gli script semplici. Alcuni esempi:
<ul>
<li>Tabulazioni al centro, a destra e decimali</li>
<li>Testo completamente giustificato</li>
<li>Sottolineatura media, che fornisce una sottolineatura uniforme anche quando le esecuzioni di testo adiacenti hanno dimensioni del carattere diverse.</li>
</ul></td>
</tr>
<tr class="even">
<td> Supporto di lingue con alfabeti non latini</td>
<td>Microsoft Rich Edit 3.0 supporta il testo bidirezionale (testo con arabo e/o ebraico misto con altri script), Indic (script in india come Devangari) e testo tailandese. Per il supporto di questi script complessi, vengono usati i componenti tipografici avanzati e Uniscribe.</td>
</tr>
<tr class="odd">
<td>Associazione dei tipi di carattere</td>
<td>Microsoft Rich Edit 3.0 sceglierà automaticamente un tipo di carattere appropriato per i caratteri che chiaramente non appartengono al set di caratteri corrente. Questa operazione viene eseguita assegnando set di caratteri alle esecuzioni di testo e associando i tipi di carattere a tali set di caratteri. Per altre informazioni, vedere <a href="using-rich-edit-controls.md">Associazione di tipi di carattere</a>.</td>
</tr>
<tr class="even">
<td>Opzioni di lettura/scrittura di testo normale specifiche per i set di caratteri</td>
<td>In questo modo è possibile leggere un file usando un set di caratteri e scrivere con un set di caratteri diverso.</td>
</tr>
<tr class="odd">
<td>UTF-8 RTF</td>
<td>Questa opzione è consigliata per le operazioni di taglia, copia e incolla. Questo formato di file è più compatto rispetto al formato RTF normale, più veloce e compatibile con Unicode.</td>
</tr>
<tr class="even">
<td>Microsoft Office 9 supporto IME (IME98)</td>
<td>Questa funzionalità IME più potente è stata separata in un modulo indipendente. Funzionalità incluse:
<ul>
<li>Riconversione Nelle versioni precedenti, l'utente deve prima eliminare la stringa finale e quindi digitare una nuova stringa per ottenere il candidato corretto. Questa nuova funzionalità consente all'utente di riconvertire la stringa finale in modalità composizione, consentendo di selezionare facilmente una stringa candidata diversa.<br/></li>
<li>Feed di documenti Questa funzionalità fornisce a IME98 il testo per il paragrafo corrente, che consente a IME98 di eseguire una conversione più accurata durante la digitazione.<br/></li>
<li>Operazione del mouse Questa funzionalità offre un controllo migliore sulle finestre candidate e dell'interfaccia utente durante la digitazione.<br/></li>
<li>Posizione del cursore Questa funzionalità fornisce le informazioni correnti relative al cursore e alla riga, utilizzate da IME98 per posizionare le finestre dell'interfaccia utente, ad esempio un elenco di candidati.<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Supporto di IMM (Active Input Method Manager)</td>
<td>Gli utenti possono richiamare l'oggetto IMM attivo, che consente agli utenti di immettere caratteri asiatici nei sistemi degli Stati Uniti.</td>
</tr>
<tr class="even">
<td>Supporto di HexToUnicode</td>
<td>Gli utenti possono eseguire la conversione tra la notazione esadecimale e Unicode usando i tasti di scelta rapida.</td>
</tr>
<tr class="odd">
<td>Più roundtripping RTF</td>
<td>Il testo RTF letto da un file verrà scritto senza modifica.</td>
</tr>
<tr class="even">
<td>Modalità di compatibilità 1.0 migliorata</td>
<td>Microsoft Rich Edit 3.0 può emulare il comportamento di Microsoft Rich Edit 1.0. Ad esempio, è possibile passare dal mapping MBCS al mapping della posizione dei caratteri Unicode (cp).</td>
</tr>
<tr class="odd">
<td>Maggiore controllo di blocco</td>
<td>La visualizzazione può essere bloccata su più chiamate API e quindi annullare il controllo per visualizzare gli aggiornamenti.</td>
</tr>
<tr class="even">
<td>Maggiore controllo di annullamento</td>
<td>L'annullamento può essere sospeso e ripreso (un requisito IME).</td>
</tr>
<tr class="odd">
<td>Aumentare/ridurre le dimensioni del carattere</td>
<td>Aumenta o riduce le dimensioni del carattere a uno dei sei valori standard (12, 28, 36, 48, 72 e 80 punti).</td>
</tr>
</tbody>
</table>



 

### <a name="rich-edit-version-41"></a>Rich Edit versione 4.1

La classe window per Microsoft Rich Edit 4.1 è MSFTEDIT \_ CLASS. Le nuove funzionalità per Microsoft Rich Edit 4.1 includono la sillabazione, la rotazione delle pagine e Framework servizi di testo (TSF).

Microsoft Rich Edit 4.1 include le funzionalità seguenti oltre alle funzionalità fornite da [Rich Edit versione 3.0.](#rich-edit-version-30)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Sillabazione</td>
<td>La sillabazione è supportata tramite le API <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>seguenti: HyphenateProc,</em></a> <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a>e <a href="em-gethyphenateinfo.md"><strong>EM_GETHYPHENATEINFO</strong></a>.</td>
</tr>
<tr class="even">
<td>Rotazione della pagina</td>
<td>Il layout dall'alto verso il basso e dal basso verso l'alto è supportato <a href="em-setpagerotate.md"><strong>tramite</strong></a> EM_SETPAGEROTATE e <a href="em-getpagerotate.md"><strong>EM_GETPAGEROTATE</strong></a>.</td>
</tr>
<tr class="odd">
<td>Framework servizi di testo supporto</td>
<td><ul>
<li>Per attivare TSF e alcune funzionalità di TSF, usare gli stili seguenti in <a href="em-seteditstyle.md"><strong>EM_SETEDITSTYLE</strong></a>: SES_USECTF, SES_CTFALLOWEMBED, SES_CTFALLOWPROOFING e SES_CTFALLOWSMARTTAG.</li>
<li>Per impostare e ottenere la distorsione della modalità TSF, <a href="em-setctfmodebias.md"><strong>usare</strong></a> EM_SETCTFMODEBIAS e <a href="em-getctfmodebias.md"><strong>EM_GETCTFMODEBIAS</strong></a>.</li>
<li>Per impostare e ottenere lo stato della tastiera TSF, <a href="em-setctfopenstatus.md"><strong>usare</strong></a> EM_SETCTFOPENSTATUS e <a href="em-getctfopenstatus.md"><strong>EM_GETCTFOPENSTATUS</strong></a>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Supporto IME aggiuntivo</td>
<td><ul>
<li>Per impostare e ottenere la distorsione della modalità IME, <a href="em-setimemodebias.md"><strong>usare</strong></a> EM_SETIMEMODEBIAS e <a href="em-getimemodebias.md"><strong>EM_GETIMEMODEBIAS</strong></a>.</li>
<li>Per ottenere le proprietà e le funzionalità dell'IME, <a href="em-getimeproperty.md"><strong>usare EM_GETIMEPROPERTY</strong></a>.</li>
<li>Per ottenere il testo della composizione IME, <a href="em-getimecomptext.md"><strong>usare</strong></a>EM_GETIMECOMPTEXT .</li>
<li>Per determinare se le impostazioni locali sono impostazioni locali dell'Asia orientale, <a href="em-isime.md"><strong>usare EM_ISIME</strong></a>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Impostazioni <a href="em-seteditstyle.md"><strong>EM_SETEDITSTYLE</strong></a> aggiuntive</td>
<td>Oltre alle impostazioni di TSF, sono disponibili nuove impostazioni che escludono gli IME, impostano il flusso di testo bidirezionale, usano tipi di carattere draftmode e altro ancora.</td>
</tr>
<tr class="even">
<td>Impostazioni <a href="em-setcharformat.md"><strong>EM_SETCHARFORMAT</strong></a> aggiuntive</td>
<td>I nuovi flag consentono al client di impostare il tipo di carattere e le dimensioni dei caratteri predefiniti per un determinato LCID o set di caratteri, per impostare il tipo di carattere predefinito per il controllo, per impedire che la tastiera corrisponda al tipo di carattere e altro ancora.</td>
</tr>
<tr class="odd">
<td>Limitazione dell'input al testo ANSI</td>
<td><a href="/windows/win32/api/richedit/ne-richedit-textmode"><strong>L'TM_SINGLECODEPAGE</strong></a> in <a href="em-settextmode.md"><strong>EM_SETTEXTMODE</strong></a> input Unicode impedisce l'immissione di un controllo Rich Edit.</td>
</tr>
<tr class="even">
<td>Notifica delle parole chiave RTF non supportata</td>
<td><a href="en-lowfirtf.md">EN_LOWFIRTF</a> avvisa un'applicazione quando è presente una parola chiave RTF non supportata.</td>
</tr>
<tr class="odd">
<td>Elementi del linguaggio aggiuntivi supportati</td>
<td>Altre lingue includono Armeno, Divehi, Telugu e altri.</td>
</tr>
<tr class="even">
<td>Supporto migliorato per le tabelle</td>
<td>Le funzionalità includono: ritorno a capo all'interno delle celle, gestione migliorata tramite RTF e navigazione migliorata.</td>
</tr>
<tr class="odd">
<td>ES_VERTICAL</td>
<td>Lo <a href="rich-edit-control-styles.md"><strong>stile ES_VERTICAL</strong></a> finestra è supportato.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-unichar"><strong>WM_UNICHAR</strong></a> supporto</td>
<td>Per inviare o pubblicare caratteri Unicode in finestre ANSI, <a href="/windows/desktop/inputdev/wm-unichar"><strong>usare WM_UNICHAR</strong></a>. Equivale a <a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a>, ma usa (UTF)-32.</td>
</tr>
</tbody>
</table>



 

## <a name="unsupported-edit-control-functionality"></a>Funzionalità del controllo di modifica non supportate

I controlli Rich Edit supportano la maggior parte delle funzionalità, ma non tutte, per i controlli di modifica su più righe. Questa sezione elenca i messaggi di controllo di modifica e gli stili delle finestre *non* supportati dai controlli Rich Edit.

I messaggi seguenti vengono elaborati dai controlli di modifica, *ma non* dai controlli Rich Edit.



| Messaggio non supportato                         | Commenti                                                                                                                    |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**EM \_ FMTLINES**](em-fmtlines.md)         | Non supportata.                                                                                                              |
| [**EM \_ GETHANDLE**](em-gethandle.md)       | I controlli Rich Edit non archiviano il testo come una semplice matrice di caratteri.                                                       |
| [**EM \_ GETIMESTATUS**](em-getimestatus.md) | Non supportata.                                                                                                              |
| [**EM \_ GETMARGINS**](em-getmargins.md)     | Non supportata.                                                                                                              |
| [**EM \_ SETHANDLE**](em-sethandle.md)       | I controlli Rich Edit non archiviano il testo come semplice matrice di caratteri.                                                       |
| [**EM \_ SETIMESTATUS**](em-setimestatus.md) | Non supportata.                                                                                                              |
| [**EM \_ SETMARGINS**](em-setmargins.md)     | Supportato in Microsoft Rich Edit 3.0.                                                                                       |
| [**EM \_ SETRECTNP**](em-setrectnp.md)       | Non supportata.                                                                                                              |
| [**EM \_ SETTABSTOPS**](em-settabstops.md)   | Viene invece usato il messaggio [**EM \_ SETPARAFORMAT.**](em-setparaformat.md) Supportato in Microsoft Rich Edit 3.0.<br/> |
| [**WM \_ CTLCOLOR**](/windows/desktop/DevNotes/wm-ctlcolor-)    | Viene invece usato il messaggio [**EM \_ SETBKGNDCOLOR.**](em-setbkgndcolor.md)                                                  |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)        | Viene invece usato il messaggio [**EM \_ GETCHARFORMAT.**](em-getcharformat.md)                                                  |



 

Gli stili di finestra seguenti vengono usati con i controlli di modifica su più righe, ma non con i controlli Rich Edit: [**ES \_ LOWERCASE,**](edit-control-styles.md) [**ES \_ UPPERCASE**](edit-control-styles.md)ed [**ES \_ OEMCONVERT**](edit-control-styles.md).

## <a name="rich-edit-shortcut-keys"></a>Tasti di scelta rapida rich edit

I controlli Rich Edit supportano i tasti di scelta rapida seguenti.



| Chiavi                      | Gestione operativa                                                                                                                               | Commenti                                                                                                                                                                                                                       |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MAIUSC+BACKSPACE           | Generare un LRM/LRM su una tastiera bidi                                                                                                    | BiDi specifico                                                                                                                                                                                                                  |
| CTRL+TAB                  | Scheda                                                                                                                                      |                                                                                                                                                                                                                                |
| CTRL+CANCELLA                | Seleziona tutto                                                                                                                               |                                                                                                                                                                                                                                |
| CTRL+numero pad 5         | Seleziona tutto                                                                                                                               |                                                                                                                                                                                                                                |
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
| CTRL+'+' (CTRL+MAIUSC+'=') | Apice                                                                                                                              |                                                                                                                                                                                                                                |
| CTRL+'='                  | Indice                                                                                                                                |                                                                                                                                                                                                                                |
| CTRL+1                    | Interlinea = 1 riga.                                                                                                                   |                                                                                                                                                                                                                                |
| CTRL+2                    | Interlinea = 2 righe.                                                                                                                  |                                                                                                                                                                                                                                |
| CTRL+5                    | Interlinea = 1,5 righe.                                                                                                                |                                                                                                                                                                                                                                |
| CTRL+' (apostrofo)       | Accenta acuto                                                                                                                             | Dopo aver premuto il tasto taglia breve, premere la lettera appropriata, ad esempio a, e o u. Questo vale solo per le tastiere inglese, francese, tedesco, italiano e spagnolo.                                                         |
| CTRL+ \` (grave)           | Accento grave                                                                                                                             | Vedere i commenti CTRL+'.                                                                                                                                                                                                           |
| CTRL+~ (tilde)            | Tilde accentato                                                                                                                             | Vedere i commenti ctrl+'.                                                                                                                                                                                                           |
| CTRL+; (punto e virgola)        | Umlaut in evidenza                                                                                                                            | Vedere i commenti ctrl+'.                                                                                                                                                                                                           |
| CTRL+MAIUSC+6              | Accento circonflesso                                                                                                                | Vedere i commenti ctrl+'.                                                                                                                                                                                                           |
| CTRL+, (virgola)            | Accento cedilla                                                                                                                           | Vedere i commenti ctrl+'.                                                                                                                                                                                                           |
| CTRL+MAIUSC+' (apostrofo) | Attivare le virgolette intelligenti                                                                                                                    |                                                                                                                                                                                                                                |
| Backspace                 | Se il testo è protetto, eseguire un segnale acustico e non eliminarlo. In caso contrario, eliminare il carattere precedente.                                                   |                                                                                                                                                                                                                                |
| CTRL+BACKSPACE            | Eliminare la parola precedente. Viene generato un codice \_ VK F16.                                                                                     |                                                                                                                                                                                                                                |
| F16                       | Uguale a Backspace.                                                                                                                       |                                                                                                                                                                                                                                |
| CTRL+INS               | Copia                                                                                                                                     |                                                                                                                                                                                                                                |
| Maiusc+Ins              | Incolla                                                                                                                                    |                                                                                                                                                                                                                                |
| Insert                    | Overwrite                                                                                                                                | DBCS non viene sovrascritto.                                                                                                                                                                                                       |
| CTRL+Freccia SINISTRA           | Spostare il cursore di una parola a sinistra.                                                                                                        | Sulla tastiera offeri, questo dipende dalla direzione del testo.                                                                                                                                                                   |
| CTRL+Freccia DESTRA          | Spostare il cursore di una parola a destra.                                                                                                       | Vedere i commenti ctrl+freccia sinistra.                                                                                                                                                                                                  |
| CTRL+MAIUSC sinistro           | Allineamento a sinistra                                                                                                                           | Nei documenti BiDi questa opzione è per l'ordine di lettura da sinistra a destra.                                                                                                                                                                    |
| CTRL+MAIUSC destro          | Allineamento a destra                                                                                                                          | Nei documenti BiDi questa opzione è per l'ordine di lettura da destra a sinistra.                                                                                                                                                                    |
| CTRL+Freccia SU             | Passare alla riga precedente.                                                                                                                  |                                                                                                                                                                                                                                |
| CTRL+Freccia GIÙ           | Passare alla riga seguente.                                                                                                                  |                                                                                                                                                                                                                                |
| CTRL+HOME                 | Spostarsi all'inizio del documento.                                                                                                   |                                                                                                                                                                                                                                |
| CTRL+FINE                  | Passare alla fine del documento.                                                                                                         |                                                                                                                                                                                                                                |
| CTRL+P SU              | Spostare una pagina verso l'alto.                                                                                                                        | Se nei controlli SystemEditMode e Single Line non eseguire alcuna operazione.                                                                                                                                                                      |
| CTRL+PGGI GIÙ            | Spostarsi di una pagina verso il basso.                                                                                                                      | Vedere i commenti CTRL+P SU.                                                                                                                                                                                                     |
| CTRL+CANC               | Eliminare la parola o i caratteri selezionati successivi.                                                                                             |                                                                                                                                                                                                                                |
| MAIUSC+CANC              | Tagliare i caratteri selezionati.                                                                                                             |                                                                                                                                                                                                                                |
| ESC                       | Arrestare il trascinamento della selezione.                                                                                                                          | Durante l'esecuzione di un trascinamento del testo.                                                                                                                                                                                               |
| ALT+ESC                   | Modificare l'applicazione attiva.                                                                                                           |                                                                                                                                                                                                                                |
| ALT+X                     | Converte il valore esadecimale Unicode che precede il punto di inserimento nel carattere Unicode corrispondente.                             |                                                                                                                                                                                                                                |
| ALT+MAIUSC+X               | Converte il carattere Unicode che precede il punto di inserimento nel valore esadecimale Unicode corrispondente.                             |                                                                                                                                                                                                                                |
| ALT+0xxx (tastierino numerico)     | Inserisce valori Unicode se xxx è maggiore di 255. Quando xxx è minore di 256, il testo dell'intervallo ASCI viene inserito in base alla tastiera corrente. | È necessario immettere valori decimali.                                                                                                                                                                                                     |
| ALT+MAIUSC+CTRL+F12        | Da esadecimale a Unicode.                                                                                                                          | Nel caso in cui ALT+X sia già utilizzato per un altro uso.                                                                                                                                                                                |
| ALT+MAIUSC+CTRL+F11        | Il testo selezionato verrà restituito nella finestra del debugger e salvato in %temp% \\DumpFontInfo.txt.                                               | Solo per il debug (è necessario impostare Flag=8 in Win.ini)                                                                                                                                                                                 |
| CTRL+MAIUSC+A              | Impostare tutti i caratteri maiuscoli.                                                                                                                            |                                                                                                                                                                                                                                |
| CTRL+MAIUSC+L              | Stile punto elenco Fiddle.                                                                                                                     |                                                                                                                                                                                                                                |
| CTRL+MAIUSC+Freccia DESTRA    | Aumentare le dimensioni del carattere.                                                                                                                      | Le dimensioni del carattere cambiano di 1 punto nell'intervallo 4pt-11pt; di 2 punti per 12pt-28pt; cambia da 28pt -> 36pt -> 48pt -> 72pt -> 80pt; cambia di 10 punti nell'intervallo 80pt - 1630pt; il valore massimo è 1638. |
| CTRL+MAIUSC+Freccia SINISTRA     | Ridurre le dimensioni del carattere.                                                                                                                      | Vedere i commenti CTRL+MAIUSC+Freccia DESTRA.                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Uso dei controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Controlli Rich Edit senza finestra](windowless-rich-edit-controls.md)
</dt> </dl>

