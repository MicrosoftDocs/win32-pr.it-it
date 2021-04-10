---
title: Controllo controllo
description: Definisce un controllo definito dall'utente.
ms.assetid: e5e7b7af-e2b0-41ff-b697-b9ea80e7c61f
keywords:
- Menu di controllo controllo e altre risorse
topic_type:
- apiref
api_name:
- CONTROL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703f95778c66522d67e40a51293c8fb8fe956ecb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963015"
---
# <a name="control-control"></a>Controllo controllo

Definisce un controllo definito dall'utente.

``` syntax
CONTROL text, id, class, style, x, y, width, height [, extended-style]
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*classe*
</dt> <dd>

Nome ridefinito, stringa di caratteri o valore Unsigned Integer a 16 bit che definisce la classe. Può trattarsi di una delle classi di controlli. per un elenco delle classi di controlli, vedere il primo elenco che segue questa descrizione. Se il valore è un nome ridefinito fornito dall'applicazione, deve essere una stringa racchiusa tra virgolette doppie (").

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Nome o valore intero ridefinito che specifica lo stile del controllo specificato. Il significato esatto dello *stile* dipende dal valore della *classe* . Le sezioni che seguono questa descrizione mostrano le classi di controlli e gli stili corrispondenti.

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="remarks"></a>Commenti

Nelle sezioni seguenti sono descritte le sei classi di controllo possibili.

### <a name="the-button-control-class"></a>Classe del controllo Button

Un controllo Button è una piccola finestra figlio rettangolare che l'utente può attivare o disattivare facendo clic su di esso con il mouse. I controlli Button possono essere usati singolarmente o in gruppi e possono essere etichettati o visualizzati senza testo. I controlli pulsante in genere cambiano aspetto quando l'utente fa clic su di essi.

Gli stili dei pulsanti sono descritti nell'argomento: [stili dei pulsanti](../controls/button-styles.md).

### <a name="the-combo-box-control-class"></a>Classe del controllo casella combinata

I controlli casella combinata sono costituiti da un campo di selezione simile a un controllo di modifica più una casella di riepilogo. È possibile che la casella di riepilogo venga visualizzata in qualsiasi momento o venga rilasciata quando l'utente seleziona una "casella di riepilogo" accanto al campo di selezione.

A seconda dello stile della casella combinata, l'utente può o non può modificare il contenuto del campo di selezione. Se la casella di riepilogo è visibile, la digitazione dei caratteri nella casella di selezione comporterà l'evidenziazione della prima voce che corrisponde ai caratteri digitati. Viceversa, la selezione di un elemento nella casella di riepilogo Visualizza il testo selezionato nel campo di selezione.

Gli stili del controllo casella combinata sono descritti nel seguente argomento: [stili casella combinata](../controls/combo-box-styles.md).

### <a name="the-edit-control-class"></a>Classe del controllo di modifica

Un controllo di modifica è una finestra figlio rettangolare in cui l'utente può immettere testo dalla tastiera. L'utente seleziona il controllo e lo mette in stato attivo per l'input facendo clic sul mouse al suo interno o premendo il tasto TAB. L'utente può immettere testo quando il controllo Visualizza un punto di inserimento lampeggiante. È possibile utilizzare il mouse per spostare il cursore e selezionare i caratteri da sostituire oppure per posizionare il cursore per l'inserimento di caratteri. È possibile utilizzare il tasto BACKSPACE per eliminare i caratteri.

I controlli di modifica usano il tipo di carattere a passo fisso e visualizzano caratteri Unicode. Espandendo i caratteri di tabulazione in tutti i caratteri di spazio necessari per spostare il cursore alla successiva tabulazione. Si presuppone che le tabulazioni si trovino in ogni ottavo punto.

Gli stili di modifica del controllo sono descritti nell'argomento seguente: [modificare gli stili dei controlli](../controls/edit-control-styles.md).

### <a name="the-list-box-control-class"></a>Classe del controllo casella di riepilogo

I controlli casella di riepilogo sono costituiti da un elenco di stringhe di caratteri. Il controllo viene usato ogni volta che un'applicazione deve presentare un elenco di nomi, ad esempio nomi file, che l'utente può visualizzare e selezionare. L'utente può selezionare una stringa posizionando il puntatore del mouse sulla stringa e facendo clic su un pulsante del mouse. Quando si seleziona una stringa, questa viene evidenziata e un messaggio di notifica viene passato alla finestra padre. È possibile utilizzare una barra di scorrimento con un controllo casella di riepilogo per scorrere gli elenchi che sono troppo lunghi o troppo larghi per la finestra del controllo.

Gli stili del controllo casella di riepilogo sono descritti nell'argomento seguente: [stili casella di riepilogo](../controls/list-box-styles.md).

### <a name="the-scroll-bar-control-class"></a>Classe del controllo Scroll-Bar

Un controllo barra di scorrimento è un rettangolo che contiene un cursore di scorrimento e con frecce di direzione a entrambe le estremità. La barra di scorrimento invia un messaggio di notifica al padre ogni volta che l'utente fa clic sul mouse nel controllo. Se necessario, l'elemento padre è responsabile dell'aggiornamento della posizione del cursore. I controlli barra di scorrimento hanno lo stesso aspetto e la stessa funzione delle barre di scorrimento utilizzate nelle finestre normali. Tuttavia, a differenza delle barre di scorrimento, i controlli barra di scorrimento possono essere posizionati in qualsiasi punto all'interno di una finestra e usati quando necessario per fornire input di scorrimento per una finestra.

Gli stili della barra di scorrimento sono descritti nell'argomento seguente: [stili del controllo barra di scorrimento](../controls/scroll-bar-control-styles.md).

### <a name="the-static-control-class"></a>Classe del controllo statico

I controlli statici sono semplici campi di testo, caselle e rettangoli che possono essere usati per etichettare, box o separare altri controlli. I controlli statici non accettano input e non forniscono alcun output.

Gli stili del controllo statico sono descritti nell'argomento seguente: [stili del controllo statico](../controls/static-control-styles.md).

 

 