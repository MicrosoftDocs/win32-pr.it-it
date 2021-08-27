---
title: Formato degli Appunti HTML
description: In questa sezione viene illustrato il formato degli Appunti HTML.
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Windows Interfaccia utente,Appunti
- Appunti, taglio dei dati
- Appunti, copia di dati
- Appunti, incollamento di dati
- Appunti, formati
- Appunti, formato HTML
- Appunti, taglio di testo HTML
- Appunti, incollamento di testo HTML
- CF_HTML formato degli Appunti
- Appunti, CF_HTML formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d73b5101d26fc55002d55e0c15144646b80445
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884976"
---
# <a name="html-clipboard-format"></a>Formato degli Appunti HTML

I requisiti per il trasferimento di testo HTML tramite gli Appunti variano a seconda dello scenario. Questo articolo riguarda il taglio e l'incolla di frammenti di un documento HTML. Potrebbero essere necessari per il trasferimento di interi documenti HTML tramite gli Appunti. Tuttavia, questo articolo è basato su un requisito per trasferire frammenti di testo HTML selezionato. Di conseguenza, un metodo che richiedeva la copia dell'intero documento HTML negli Appunti viene considerato troppo pesante.

Il formato degli Appunti HTML CF consente di archiviare negli Appunti un frammento di testo HTML non elaborato e il relativo contesto \_ come ASCII. In questo modo il contesto del frammento HTML, costituito da tutti i tag circostanti precedenti, può essere esaminato da un'applicazione in modo che i tag circostanti del frammento HTML possano essere notati con i relativi attributi. Anche se è necessario che le applicazioni decidano come interpretare questi frammenti, alcune linee guida di base sono incluse qui in base alle implementazioni IE4/MSHTML.

Il nome ufficiale degli Appunti (la stringa usata da RegisterClipboardFormat) è in formato HTML.

-   [Descrizione](#description)
-   [Scenari](#scenarios)

## <a name="description"></a>Descrizione

CF HTML è interamente in formato testo (per essere, tra le altre cose, nello stato HTML e usa UTF-8) e include , un elemento facoltativo e, all'interno del \_ `description` `context` contesto, `fragment` .

Di seguito è riportato un esempio di Appunti:


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



La descrizione include il numero di versione degli Appunti e gli offset, che indicano dove iniziano e terminano il contesto e il frammento. La descrizione è un elenco di parole chiave di testo ASCII (min/maj non è significativo) seguite da una stringa e separate da due punti (:).

**Versione:** numero di versione vv degli Appunti. La versione iniziale è 0.9.

**StartHTML:** bytecount dall'inizio degli Appunti all'inizio del contesto oppure -1 se non è presente alcun contesto.

**EndHTML:** bytecount dall'inizio degli Appunti alla fine del contesto oppure -1 se non è presente alcun contesto.

**StartFragment:** bytecount dall'inizio degli Appunti all'inizio del frammento.

**EndFragment:** bytecount dall'inizio degli Appunti alla fine del frammento.

**StartSelection:** bytecount dall'inizio degli Appunti all'inizio della selezione.

**EndSelection:** bytecount dall'inizio degli Appunti alla fine della selezione.

Le parole chiave StartSelection ed EndSelection sono facoltative e devono essere entrambe omesse se non si vuole che l'applicazione generi queste informazioni.

Altre informazioni di questo tipo possono essere aggiunte qui in un secondo momento, poiché il codice HTML inizia in corrispondenza di StartHTMLoffset. Ad esempio, più coppie di StartFragment/EndFragment possono essere aggiunte in un secondo momento per supportare la selezione non contigua di frammenti.

Per comodità dei programmi che generano i conteggi dei byte, i conteggi dei byte possono essere lasciati riempiti di zeri. Ad esempio, i programmi che generano i conteggi dei byte potrebbero influire arbitrariamente su dieci (10) zeri per ogni parola chiave (StartHTML: 00000000000) e quindi, quando il numero esatto di byte StartHTML è noto (ad esempio, 71), il programma può sostituire il numero appropriato di zeri con bytecount (StartHTML: 0000000071).

L'unico set di caratteri supportato dagli Appunti è Unicode nella codifica UTF-8. Poiché i primi caratteri di UTF-8 e ASCII corrispondono, la descrizione è sempre ASCII, ma i byte del contesto (a partire da StartHTML) potrebbero usare qualsiasi altro carattere codificato in UTF-8.

La fine delle righe nell'intestazione del formato degli Appunti può essere CR o CR/LF o LF.

Il frammento contiene codice HTML puro e valido che rappresenta l'area selezionata dall'utente (ad esempio, per copiare). Contiene il testo selezionato più i tag di apertura e gli attributi di qualsiasi elemento che include un tag di fine all'interno del testo selezionato e i tag di fine alla fine del frammento per qualsiasi tag di inizio incluso. Si tratta di tutte le informazioni necessarie per l'incollamento di base di un frammento HTML.

Il frammento deve essere preceduto e seguito dai commenti HTML <!--StartFragment--> e <!--EndFragment--> (non è consentito spazio tra il !-- e il testo) per indicare in modo pratico dove inizia e termina il frammento. L'inizio e la fine del frammento sono quindi indicati dalla presenza di questi commenti e dai conteggi dei byte StartFragment ed EndFragment nella descrizione. È previsto che gli strumenti producano queste informazioni. Questa ridondanza è stata introdotta per poter trovare rapidamente l'inizio del frammento (dal numero di byte) e contrassegnare la posizione del frammento direttamente nell'albero HTML.

La selezione indica all'interno del frammento l'area HTML esatta selezionata dall'utente (ad esempio, copia). In questo modo vengono aggiunte altre informazioni al frammento indicando il testo selezionato esatto, senza i tag di apertura e di fine aggiunti per garantire che il frammento sia HTML ben formato.

La selezione è facoltativa, in quanto nel frammento sono incluse informazioni sufficienti per l'incollamento di base. Se la selezione non viene archiviata, sia StartSelection che EndSelection non vengono archiviati nell'intestazione.

Il contesto è un documento HTML valido e completo. Questo articolo contiene il frammento e tutti i tag adiacenti precedenti (tag di inizio e di fine; questi tag adiacenti precedenti rappresentano tutti i nodi padre del frammento, fino al nodo HTML). L'articolo contiene anche l'elemento HEAD completo e consente ad esempio di includere gli elementi BASE e TITLE in modo da ottenere queste informazioni aggiuntive. Un'applicazione che copia un frammento di CODICE HTML negli Appunti può scegliere di creare un elemento BASE da includere nel contesto se tale elemento non è già presente in modo che gli URL parziali nel frammento possano essere risolti.

Il contesto è facoltativo, poiché nel frammento sono incluse informazioni sufficienti per l'incollamento di base di un frammento HTML. Se il contesto non viene archiviato, viene archiviato solo il frammento e StartHTML=EndHTML=-1.

## <a name="scenarios"></a>Scenari

Gli scenari seguenti descrivono come l'editor HTML IE4/MSHTML gestisce il taglia e incolla HTML; altre applicazioni possono o meno seguire questi scenari. Il formato degli Appunti descritto qui è progettato per consentire la flessibilità per il funzionamento di un'applicazione. Questi scenari mostrano solo codice HTML, ovvero nessun tag sovrapposto.

1.  Frammento semplice di HTML.
    -   -   Testo HTML:

            &lt;BODY &gt; È normale Questo è grassetto Questo è <B>grassetto </B> <I> <B>corsivo </B>Questo è corsivo </I> &lt; /BODY&gt;

        -   Viene visualizzato come:

            This is normal **This is bold** This is bold **_italic_* This is italic*  

        -   Il testo tra \* \* l'oggetto viene selezionato e copiato negli Appunti:

            This is normal **This is** bold This is \* \* **bold****_italic_* This* is \* \* *italic*   

        -   Questo è ciò che sarà negli Appunti (si noti che questa è l'interpretazione di IE4/MSHTML):

            Versione:0.9

            StartHTML:71

            EndHTML:160

            StartFragment:130

            EndFragment:150

            **StartSelection:130**

            **EndSelection:150**

            <!DOCTYPE ...>

            &lt;CORPO&gt;

            <!-- StartFragment -->>

            **<B>bold</B><I><B>È in grassetto corsivo</B>Questo</I>**

            <!-- EndFragment -->

            &lt;/BODY&gt;

            &lt;/HTML&gt;

        -   In questo scenario solo il tag BODY e il tag HTML vengono visualizzati nel contesto come precede il frammento selezionato. Si noti che i tag di inizio e di fine sono inclusi nel contesto. La selezione, delimitata da StartSelection ed EndSelection, viene visualizzata in grassetto.

2.  Frammento di una tabella in HTML.
    -   -   Testo HTML:

            &lt;CORPO&gt;<TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Item 1</TD><TD>Elemento 2</TD><TD>Elemento 3</TD><TD>Elemento 4</TD></TR><TR><TD>Elemento 5</TD><TD>Elemento 6</TD><TD>Elemento 7</TD><TD>Elemento 8</TD></TR><TR><TH>Head2</TH><TD>Elemento 9</TD><TD>Elemento 10</TD><TD>Elemento 11</TD><TD>Elemento 12</TD></TR></TABLE>&lt;/BODY&gt;

        -   Viene visualizzato come: ><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>Item 1</TD><TD>Elemento 2</TD><TD>Elemento 3</TD><TD>Elemento 4</TD></TR><TR><TD>Elemento 5</TD><TD>Elemento 6</TD><TD>Elemento 7</TD><TD>Elemento 8</TD></TR><TR><TH>Head2</TH><TD>Elemento 9</TD><TD>Elemento 10</TD><TD>Elemento 11</TD><TD>Elemento 12</TD></TR></TABLE><! \[ CDATA\[\]\]>
        -   Gli elementi Item 6, Item7, Item 10 e Item 11 della tabella vengono selezionati come blocco e copiati negli Appunti.
        -   Questo è ciò che sarà negli Appunti (si noti che questa è l'interpretazione di IE4/MSHTML):

            <!DOCTYPE ...>

            &lt;CORPO &gt; &lt; HTML&gt;<TABLE BORDER>

            <!--StartFragment-->

            **<TR><TD>Elemento 6 </TD> <TD> Elemento 7 </TD> </TR> <TR> <TD> Elemento 10 </TD> <TD> Elemento 11</TD></TR>**

            <!--EndFragment-->

            </TABLE>

            &lt;/BODY &gt; &lt; /HTML &gt; La selezione, delimitata da StartSelection ed EndSelection, viene visualizzata in grassetto.

3.  Incollare un frammento di un elenco ordinato in testo normale.
    -   -   Testo HTML:

            &lt;CORPO&gt;<OL TYPE = a><LI>Item 1<LI>Elemento 2<LI>Elemento 3<LI>Elemento 4<LI>Elemento 5<LI>Elemento 6</OL>&lt;/BODY&gt;

        -   Viene visualizzato come:
            1.  Item 1
            2.  Elemento 2
            3.  Elemento 3
            4.  Elemento 4
            5.  Elemento 5
            6.  Elemento 6
        -   L'utente seleziona e copia negli Appunti gli elementi da 3 a 5. Negli Appunti è presente il codice HTML seguente:

            <DOCTYPE...>&lt; HTML &gt; &lt; BODY&gt;<OL TYPE = a>

            <!-- StartFragment-->

            **<LI>Elemento 3 <LI> Elemento 4 <LI> Elemento 5**

            <!-- EndFragment-->

            </OL>&lt;/BODY&gt;&lt;/HTML&gt;

            La selezione, delimitata da StartSelection ed EndSelection, viene mostrata in grassetto.

        -   Se questo frammento viene incollato in un documento vuoto, verrà creato il codice HTML seguente:

            &lt;CORPO&gt;<OL TYPE = a><LI>Elemento 3<LI>Elemento 4<LI>Elemento 5</OL>&lt;/BODY&gt;

        -   Visualizzato come:
            1.  Elemento 3
            2.  Elemento 4
            3.  Elemento 5

4.  Incollare un'area parzialmente selezionata.
    -   -   Testo HTML:

            <P> IE4/MSHTML è un editor WYSIWYG che supporta :<UL><LI>Taglia<LI>Copia<LI>Incolla</UL><P>Questo è un ottimo strumento.

        -   Viene visualizzato come:IE4/MSHTML è un editor WYSIWYG che supporta :
            -   -   Taglia
                -   Copia
                -   Incolla

        -   L'utente seleziona da "WYSIWYG" a "Cop". Negli Appunti è presente il codice HTML seguente:

            <DOCTYPE...>&lt; HTML &gt; &lt; BODY&gt;

            <!-- StartFragment-->

            <P>

            **Editor WYSIWYG, che supporta**

            **<UL><LI>Cut <LI> Cop**

            </UL>

            <!-- EndFragment-->

            &lt;/BODY &gt; &lt; /HTML &gt; La selezione, delimitata da StartSelection ed EndSelection, viene visualizzata in grassetto.

     
    -   -   L'utente seleziona da "opy" a "Great".

            Negli Appunti è presente il codice HTML seguente:

            <DOCTYPE...>&lt; HTML &gt; &lt; BODY&gt;

            <!-- StartFragment-->

            <UL><LI>

            **opy <LI> Paste This is a </UL> <P> Great**

            </P>

            <!-- EndFragment-->

            &lt;/BODY &gt; &lt; /HTML&gt;

            La selezione, delimitata da StartSelection ed EndSelection, viene visualizzata in grassetto.

 

 




