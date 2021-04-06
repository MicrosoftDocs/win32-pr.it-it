---
title: Formato degli Appunti HTML
description: In questa sezione viene illustrato il formato degli Appunti HTML.
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Interfaccia utente di Windows, appunti
- Appunti, taglio di dati
- Appunti, copia di dati
- Appunti, incolla di dati
- Appunti, formati
- Appunti, formato HTML
- Appunti, taglio del testo HTML
- Appunti, incollare testo HTML
- Formato degli Appunti CF_HTML
- Appunti, formato CF_HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75cdcd9c2fc982a7cbde38bba4b7dec6738f1793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044887"
---
# <a name="html-clipboard-format"></a>Formato degli Appunti HTML

I requisiti per il trasferimento del testo HTML per mezzo degli Appunti variano a seconda dello scenario. In questo articolo si tratta di tagliare e incollare frammenti di un documento HTML. Potrebbero esserci requisiti per il trasferimento di interi documenti HTML tramite gli Appunti. Tuttavia, questo articolo è determinato da un requisito per trasferire frammenti del testo HTML selezionato. Di conseguenza, un metodo che ha richiesto l'intero documento HTML da copiare negli Appunti viene considerato troppo pesante.

Il \_ formato degli Appunti HTML CF consente a un frammento di testo HTML non elaborato e del relativo contesto di essere archiviato negli Appunti come ASCII. Questo consente il contesto del frammento HTML, che è costituito da tutti i tag circostanti precedenti, che devono essere esaminati da un'applicazione in modo che i tag circostanti del frammento HTML possano essere annotati con i relativi attributi. Sebbene le applicazioni decidano come interpretare tali frammenti, alcune linee guida di base sono incluse in questo articolo, in base alle implementazioni IE4/MSHTML.

Il nome ufficiale degli Appunti (la stringa utilizzata da RegisterClipboardFormat) è formato HTML.

-   [Descrizione](#description)
-   [Scenari](#scenarios)

## <a name="description"></a>Descrizione

\_Il formato HTML CF è interamente formato da testo (per essere, tra le altre cose, nello spirito HTML e usa UTF-8) e include un `description` , un facoltativo `context` e, all'interno del contesto, il `fragment` .

Di seguito è riportato un esempio di uno degli Appunti:


```
Version:0.9
    StartHTML:71
    EndHTML:170
    StartFragment:140
    EndFragment:160
    StartSelection:140
    EndSelection:160
    <!DOCTYPE>
    <HTML>
    <HEAD>
    <TITLE> The HTML Clipboard</TITLE>
    <BASE HREF="https://sample/specs">
    </HEAD>
    <BODY>
    <UL>
    <!--StartFragment -->
    <LI> The Fragment </LI>
    <!--EndFragment -->
    </UL>
    </BODY>
    </HTML>
```



La descrizione include il numero di versione e gli offset degli Appunti, che indicano dove il contesto e l'inizio e la fine del frammento. La descrizione è un elenco di parole chiave di testo ASCII (min/Maj non è significativo) seguite da una stringa e separate da due punti (:).

**Versione**: il numero di versione degli Appunti. La versione iniziale è 0,9.

**StartHTML**: GetByteCount dall'inizio degli Appunti all'inizio del contesto, oppure-1 se non è presente alcun contesto.

È possibile eseguire l' **indhtml**, dall'inizio degli Appunti alla fine del contesto oppure-1 se non è presente alcun contesto.

**StartFragment**: GetByteCount dall'inizio degli Appunti all'inizio del frammento.

**EndFragment**: GetByteCount dall'inizio degli Appunti alla fine del frammento.

**StartSelection**: GetByteCount dall'inizio degli Appunti all'inizio della selezione.

Di cui è possibile eseguire la **selezione, dall'** inizio degli Appunti alla fine della selezione.

Le parole chiave StartSelection e sono facoltative e devono essere omesse se non si vuole che l'applicazione generi queste informazioni.

Altre informazioni di questo tipo potrebbero essere aggiunte in un secondo momento, perché il codice HTML inizia in corrispondenza del StartHTMLoffset. Ad esempio, è possibile aggiungere più coppie di StartFragment/EndFragment in un secondo momento per supportare la selezione non contigua dei frammenti.

Per praticità dei programmi che generano il valore di getbytecounts, è possibile lasciare gli zeri imbottiti. Ad esempio, i programmi che generano l'oggetto GetByteCount possono influenzare arbitrariamente dieci (10) zeri per ogni parola chiave (StartHTML: 0000000000) e quindi, quando il valore esatto StartHTML GetByteCount è noto (ad esempio, 71), il programma può sostituire il numero appropriato di zeri con l'oggetto GetByteCount (StartHTML: 0000000071).

L'unico set di caratteri supportato dagli Appunti è Unicode nella codifica UTF-8. Poiché i primi caratteri di UTF-8 e ASCII corrispondono, la descrizione è sempre ASCII, ma i byte del contesto (a partire da StartHTML) potrebbero usare qualsiasi altro carattere codificato in UTF-8.

La fine delle righe nell'intestazione del formato degli Appunti può essere CR o CR/LF o LF.

Il frammento contiene un HTML puro e valido che rappresenta l'area selezionata dall'utente, ad esempio per la copia. Contiene il testo selezionato più i tag di apertura e gli attributi di qualsiasi elemento con un tag di fine all'interno del testo selezionato e i tag di fine alla fine del frammento per qualsiasi tag di inizio incluso. Si tratta di tutte le informazioni necessarie per incollare di base di un frammento HTML.

Il frammento deve essere preceduto e seguito dai commenti HTML <!--StartFragment--> e <!--EndFragment--> non è consentito alcuno spazio tra il!--e il testo) per indicare facilmente la posizione in cui il frammento inizia e termina. Pertanto, l'inizio e la fine del frammento sono indicate dalla presenza di questi commenti e dai conteggi dei byte StartFragment e EndFragment nella descrizione. Si prevede che gli strumenti producano queste informazioni. Questa ridondanza è stata introdotta per poter trovare rapidamente l'inizio del frammento (dal numero di byte) e contrassegnare la posizione del frammento direttamente nell'albero HTML.

La selezione indica all'interno del frammento l'area HTML esatta selezionata dall'utente, ad esempio per la copia. Verranno aggiunte altre informazioni al frammento indicando il testo selezionato esatto, senza i tag di apertura e i tag di fine che sono stati aggiunti per garantire che il frammento sia HTML ben formato.

La selezione è facoltativa, poiché nel frammento viene inclusa una quantità di informazioni sufficiente per l'incollatura di base. Se la selezione non viene archiviata, i StartSelection e l'inclusione non vengono archiviati nell'intestazione.

Il contesto è un documento HTML completo e valido. Questo articolo contiene il frammento e tutti i tag circostanti (tag di inizio e di fine) che precedono rappresentano tutti i nodi padre del frammento fino al nodo HTML. L'articolo contiene anche l'intestazione completa e consente di includere, ad esempio, gli elementi di BASE e titolo, in modo da poter ottenere queste informazioni aggiuntive. Un'applicazione che copia un frammento di codice HTML negli Appunti può scegliere di creare un elemento di BASE da includere nel contesto se tale elemento non è già presente, in modo da poter risolvere gli URL parziali nel frammento.

Il contesto è facoltativo, dal momento che nel frammento sono incluse informazioni sufficienti per l'incollamento di base di un frammento HTML. Se il contesto non è archiviato, viene archiviato solo il frammento e StartHTML = dHTML =-1.

## <a name="scenarios"></a>Scenari

Negli scenari seguenti viene descritto il modo in cui l'editor HTML IE4/MSHTML gestisce le operazioni Taglia e Incolla HTML; è possibile che altre applicazioni non seguano questi scenari. Il formato degli Appunti descritto di seguito ha lo scopo di consentire la flessibilità del modo in cui un'applicazione sceglie di funzionare. Questi scenari mostrano solo codice HTML valido, ovvero nessun tag sovrapposto.

1.  Semplice frammento di codice HTML.
    -   -   Testo HTML:

            <BODY>Si tratta di una situazione normale in <B>grassetto </B>. si tratta di <I> <B> </B>un corsivo</I></BODY>

        -   Viene visualizzato come:

            Si tratta di una situazione normale in **grassetto**. si tratta di un corsivo    *    *

        -   Il testo tra \* \* è selezionato e copiato negli Appunti:

            Si tratta di una **situazione normale in** \* \* **grassetto**    *    . \* \*  questo è il corsivo

        -   Questo è ciò che si troverà negli Appunti (si noti che si tratta dell'interpretazione di IE4/MSHTML):

            Versione: 0.9

            StartHTML: 71

            Con dHTML: 160

            StartFragment: 130

            EndFragment: 150

            **StartSelection: 130**

            **: 150**

            <!DOCTYPE ...>

            <BODY>

            <!-- StartFragment -->>

            **<B>grassetto</B><I><B>corsivo</B></I>**

            <!-- EndFragment -->

            </BODY>

            </HTML>

        -   In questo scenario solo il tag BODY e il tag HTML vengono visualizzati nel contesto, perché precede il frammento selezionato. Si noti che i tag di inizio e di fine sono inclusi nel contesto. La selezione, come delimitato da StartSelection e l'opzione di visualizzazione, viene visualizzata in grassetto.

2.  Frammento di una tabella in HTML.
    -   -   Testo HTML:

            <BODY><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Item 1</TD><TD>Elemento 2</TD><TD>Elemento 3</TD><TD>Elemento 4</TD></TR><TR><TD>Elemento 5</TD><TD>Elemento 6</TD><TD>Elemento 7</TD><TD>Elemento 8</TD></TR><TR><TH>Head2</TH><TD>Elemento 9</TD><TD>Elemento 10</TD><TD>Elemento 11</TD><TD>Elemento 12</TD></TR></TABLE></BODY>

        -   Viene visualizzato come: ><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Item 1</TD><TD>Elemento 2</TD><TD>Elemento 3</TD><TD>Elemento 4</TD></TR><TR><TD>Elemento 5</TD><TD>Elemento 6</TD><TD>Elemento 7</TD><TD>Elemento 8</TD></TR><TR><TH>Head2</TH><TD>Elemento 9</TD><TD>Elemento 10</TD><TD>Elemento 11</TD><TD>Elemento 12</TD></TR></TABLE><. \[ CDATA\[\]\]>
        -   Gli elementi 6, Item7, Item 10 e Item 11 della tabella sono selezionati come blocchi e copiati negli Appunti.
        -   Questo è ciò che si troverà negli Appunti (si noti che si tratta dell'interpretazione di IE4/MSHTML):

            <!DOCTYPE ...>

            <HTML><BODY><TABLE BORDER>

            <!--StartFragment-->

            **<TR><TD>Elemento 6 </TD> <TD> elemento 7 elemento </TD> </TR> <TR> <TD> 10 elemento </TD> <TD> 11</TD></TR>**

            <!--EndFragment-->

            </TABLE>

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

3.  Incollare un frammento di un elenco ordinato in testo normale.
    -   -   Testo HTML:

            <BODY><OL TYPE = a><LI>Item 1<LI>Elemento 2<LI>Elemento 3<LI>Elemento 4<LI>Elemento 5<LI>Elemento 6</OL></BODY>

        -   Viene visualizzato come:
            1.  Item 1
            2.  Elemento 2
            3.  Elemento 3
            4.  Elemento 4
            5.  Elemento 5
            6.  Elemento 6
        -   L'utente seleziona e copia gli elementi da 3 a 5 negli Appunti. Negli Appunti è riportato il codice HTML seguente:

            <DOCTYPE... ><HTML><BODY><OL TYPE = a>

            <!-- StartFragment-->

            **<LI>Elemento 3 <LI> elemento 4 elemento <LI> 5**

            <!-- EndFragment-->

            </OL></BODY></HTML>

            La selezione, come delimitato da StartSelection e l'esposizione, viene visualizzata in grassetto.

        -   Se questo frammento viene ora incollato in un documento vuoto, verrà creato il codice HTML seguente:

            <BODY><OL TYPE = a><LI>Elemento 3<LI>Elemento 4<LI>Elemento 5</OL></BODY>

        -   Visualizzato come:
            1.  Elemento 3
            2.  Elemento 4
            3.  Elemento 5

4.  Incollare un'area parzialmente selezionata.
    -   -   Testo HTML:

            <P> IE4/MSHTML è un editor WYSIWYG che supporta:<UL><LI>Taglia<LI>Copia<LI>Incolla</UL><P>Si tratta di uno strumento straordinario.

        -   Viene visualizzato come: IE4/MSHTML è un editor WYSIWYG che supporta:
            -   -   Taglia
                -   Copia
                -   Incolla

        -   L'utente seleziona da "WYSIWYG" fino a "Cop". Negli Appunti è riportato il codice HTML seguente:

            <DOCTYPE... ><HTML><BODY>

            <!-- StartFragment-->

            <P>

            **Editor WYSIWYG, che supporta**

            **<UL><LI>Taglia <LI> COP**

            </UL>

            <!-- EndFragment-->

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

     
    -   -   L'utente seleziona da "OPY" fino a "Great".

            Negli Appunti è riportato il codice HTML seguente:

            <DOCTYPE... ><HTML><BODY>

            <!-- StartFragment-->

            <UL><LI>

            **OPY <LI> incollare </UL> <P> questo è un ottimo**

            </P>

            <!-- EndFragment-->

            </BODY></HTML>

            La selezione, come delimitato da StartSelection e l'opzione di visualizzazione, viene visualizzata in grassetto.

 

 




