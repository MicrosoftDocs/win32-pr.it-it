---
title: Controllo CONTROL
description: Definisce un controllo definito dall'utente.
ms.assetid: e5e7b7af-e2b0-41ff-b697-b9ea80e7c61f
keywords:
- Menu e altre risorse del controllo CONTROL
topic_type:
- apiref
api_name:
- CONTROL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 069449b5eef83cef7b7bdfac1c61aacb0ceac97cbbdd6e6fb2c139c43b3bae13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663061"
---
# <a name="control-control"></a>Controllo CONTROL

Definisce un controllo definito dall'utente.

``` syntax
CONTROL text, id, class, style, x, y, width, height [, extended-style]
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*Classe*
</dt> <dd>

Nome ridefinito, stringa di caratteri o valore intero senza segno a 16 bit che definisce la classe. Può trattarsi di una qualsiasi delle classi di controllo. Per un elenco delle classi di controllo, vedere il primo elenco che segue questa descrizione. Se il valore è un nome ridefinito fornito dall'applicazione, deve essere una stringa racchiusa tra virgolette doppie (").

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Nome ridefinito o valore intero che specifica lo stile del controllo specificato. Il significato esatto dello *stile* dipende dal valore *della* classe . Le sezioni che seguono questa descrizione illustrano le classi di controllo e gli stili corrispondenti.

</dd> </dl>

Per altre informazioni sulla sintassi generale di un'istruzione di controllo, vedere [Parametri di controllo comuni](common-control-parameters.md).

## <a name="remarks"></a>Commenti

Le sei classi di controllo possibili sono descritte nelle sezioni seguenti.

### <a name="the-button-control-class"></a>Classe di controllo Button

Un controllo pulsante è una piccola finestra figlio rettangolare che l'utente può attivare o disattivare facendo clic con il mouse. I controlli pulsante possono essere usati da soli o in gruppi e possono essere etichettati o visualizzati senza testo. I controlli pulsante cambiano in genere l'aspetto quando l'utente fa clic su di essi.

Gli stili dei pulsanti sono descritti nell'argomento seguente: [Stili dei pulsanti](../controls/button-styles.md).

### <a name="the-combo-box-control-class"></a>Classe di controllo Casella combinata

I controlli casella combinata sono costituiti da un campo di selezione simile a un controllo di modifica e da una casella di riepilogo. La casella di riepilogo può essere sempre visualizzata o eliminata quando l'utente seleziona una "casella popup" accanto al campo di selezione.

A seconda dello stile della casella combinata, l'utente può o non può modificare il contenuto del campo di selezione. Se la casella di riepilogo è visibile, digitando caratteri nella casella di selezione verrà evidenziata la prima voce corrispondente ai caratteri digitati. Al contrario, selezionando un elemento nella casella di riepilogo viene visualizzato il testo selezionato nel campo di selezione.

Gli stili dei controlli casella combinata sono descritti nell'argomento seguente: [Stili casella combinata](../controls/combo-box-styles.md).

### <a name="the-edit-control-class"></a>Classe del controllo Edit

Un controllo di modifica è una finestra figlio rettangolare in cui l'utente può immettere testo dalla tastiera. L'utente seleziona il controllo e gli assegna lo stato attivo per l'input, facendo clic con il mouse al suo interno o premendo TAB. L'utente può immettere testo quando il controllo visualizza un punto di inserimento lampeggiante. Il mouse può essere usato per spostare il cursore e selezionare i caratteri da sostituire o per posizionare il cursore per l'inserimento di caratteri. Il tasto BACKSPACE può essere usato per eliminare i caratteri.

I controlli di modifica usano il tipo di carattere a passo fisso e visualizzano i caratteri Unicode. Espandono i caratteri di tabulazione in tutti gli spazi necessari per spostare il cursore alla tabulazione successiva. Si presuppone che le tabulazioni siano in corrispondenza di ogni ottava posizione di carattere.

Gli stili del controllo di modifica sono descritti nell'argomento seguente: [Modifica stili di controllo](../controls/edit-control-styles.md).

### <a name="the-list-box-control-class"></a>Classe di controllo Casella di riepilogo

I controlli casella di riepilogo sono costituiti da un elenco di stringhe di caratteri. Il controllo viene usato ogni volta che un'applicazione deve presentare un elenco di nomi, ad esempio nomi di file, che l'utente può visualizzare e selezionare. L'utente può selezionare una stringa puntando alla stringa con il mouse e facendo clic su un pulsante del mouse. Quando si seleziona una stringa, viene evidenziata e viene passato un messaggio di notifica alla finestra padre. Una barra di scorrimento può essere usata con un controllo casella di riepilogo per scorrere gli elenchi troppo lunghi o troppo larghi per la finestra del controllo.

Gli stili dei controlli casella di riepilogo sono descritti nell'argomento seguente: [Stili casella di riepilogo](../controls/list-box-styles.md).

### <a name="the-scroll-bar-control-class"></a>Classe Scroll-Bar control

Un controllo barra di scorrimento è un rettangolo che contiene una casella di scorrimento e ha frecce di direzione a entrambe le estremità. La barra di scorrimento invia un messaggio di notifica al relativo elemento padre ogni volta che l'utente fa clic con il mouse nel controllo . L'elemento padre è responsabile dell'aggiornamento della posizione del cursore, se necessario. I controlli barra di scorrimento hanno lo stesso aspetto e la stessa funzione delle barre di scorrimento usate nelle normali finestre. A differenza delle barre di scorrimento, tuttavia, i controlli barra di scorrimento possono essere posizionati in qualsiasi punto all'interno di una finestra e usati quando necessario per fornire l'input di scorrimento per una finestra.

Gli stili della barra di scorrimento sono descritti nell'argomento seguente: [Stili del controllo Barra di scorrimento](../controls/scroll-bar-control-styles.md).

### <a name="the-static-control-class"></a>Classe di controllo statico

I controlli statici sono semplici campi di testo, caselle e rettangoli che possono essere usati per etichettare, boxare o separare altri controlli. I controlli statici non accettano input e non forniscono alcun output.

Gli stili dei controlli statici sono descritti nell'argomento seguente: [Stili di controllo statici](../controls/static-control-styles.md).

 

 