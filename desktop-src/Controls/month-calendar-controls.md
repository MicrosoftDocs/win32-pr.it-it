---
title: Informazioni sui controlli calendario mensile
description: Un controllo calendario mensile implementa un'interfaccia utente simile al calendario.
ms.assetid: 81b8f233-272e-4043-92ff-5ff47b0610d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f61b0ffc291473b330469910d1dad0317668e1
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118527"
---
# <a name="about-month-calendar-controls"></a>Informazioni sui controlli calendario mensile

Un controllo calendario mensile implementa un'interfaccia utente simile al calendario. Ciò fornisce all'utente un metodo molto intuitivo e riconoscibile di immettere o selezionare una data. Inoltre, il controllo fornisce all'applicazione i mezzi per ottenere e impostare le informazioni relative alla data nel controllo utilizzando i tipi di dati esistenti.

-   [Funzionalità del controllo calendario mensile](#month-calendar-control-features)
    -   [Selezione di un giorno](#selecting-a-day)
    -   [Selezione di un mese non adiacente](#selecting-a-nonadjacent-month)
    -   [Selezione di un anno diverso](#selecting-a-different-year)
-   [Localizzazione](#localization)
-   [Orari del controllo calendario mensile](#times-in-the-month-calendar-control)

## <a name="month-calendar-control-features"></a>Funzionalità del controllo calendario mensile

Lo screenshot seguente mostra un controllo calendario mensile che è stato ridimensionato per mostrare due mesi.

![Screenshot di una finestra di dialogo con un controllo calendario mensile che mostra due mesi, affiancati](images/mc-simple.png)

> [!Note]  
> L'aspetto e il comportamento del controllo calendario mensile differiscono leggermente nelle diverse versioni della libreria di Runtime. Questo argomento è incentrato sul controllo visualizzato in Windows Vista con la versione 6 di Comctl32.dll.

 

Il controllo nell'illustrazione presenta le funzionalità facoltative seguenti.

-   La data corrente viene visualizzata in una riga distinta nella parte inferiore del controllo. È l'impostazione predefinita.
-   Il "cerchio odierno" (effettivamente un rettangolo in questa versione) viene visualizzato intorno al giorno corrente e accanto alla riga "Today" come segnale visivo. È l'impostazione predefinita.
-   I numeri settimanali vengono visualizzati a sinistra di ogni riga di giorni. Questo stile deve essere specificato.
-   Alcune date sono visualizzate in grassetto, in base allo stato del giorno impostato dall'applicazione. Ad esempio, le date con riunioni pianificate potrebbero essere visualizzate in grassetto. Questo stile deve essere specificato.

> [!Note]
>
> Windows non supporta le date precedenti alla 1601. Per informazioni dettagliate, vedere [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .
>
> Il controllo calendario mensile è basato sul calendario gregoriano, introdotto in 1753. Non verranno calcolate le date coerenti con il calendario giuliano utilizzato prima del 1753.

 

### <a name="selecting-a-day"></a>Selezione di un giorno

Per impostazione predefinita, quando un utente fa clic sui pulsanti freccia in alto a sinistra o in alto a destra del controllo calendario mensile, il controllo Aggiorna la visualizzazione per visualizzare il mese precedente o successivo. L'utente può anche eseguire la stessa azione facendo clic sui mesi parziali visualizzati prima del primo mese e dopo l'ultimo mese.

Per spostare la selezione, è anche possibile usare i comandi della tastiera seguenti. Il calendario scorre sempre in modo necessario per visualizzare il giorno selezionato. I [**codici delle chiavi virtuali**](/windows/desktop/inputdev/virtual-key-codes) sono visualizzati nella tabella.



|                         |                                                                                                                                                                                                                                          |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Freccia sinistra (VK a \_ sinistra)   | Selezionare il giorno precedente.                                                                                                                                                                                                                 |
| Freccia destra (VK a \_ destra) | Selezionare il giorno successivo.                                                                                                                                                                                                                     |
| Freccia su (VK \_ )       | Selezionare lo stesso giorno della settimana precedente.                                                                                                                                                                                                |
| Freccia giù (VK in \_ basso)   | Selezionare lo stesso giorno nella settimana successiva.                                                                                                                                                                                                    |
| PGSU (VK \_ precedente)     | Selezionare lo stesso giorno nel mese precedente. Se il mese non ha il giorno, il giorno più vicino è selezionato. ad esempio, la selezione viene spostata dal 31 marzo al 28 febbraio o 29.                                                      |
| PGGIÙ (VK \_ Avanti)    | Selezionare lo stesso giorno nel mese successivo.                                                                                                                                                                                                   |
| HOME (casa VK \_ )         | Selezionare il primo giorno del mese corrente.                                                                                                                                                                                               |
| FINE ( \_ fine VK)           | Selezionare l'ultimo giorno del mese corrente.                                                                                                                                                                                                |
| CTRL + HOME             | Scorrere un mese indietro e selezionare un giorno nella colonna più a sinistra.                                                                                                                                                                       |
| CTRL + FINE              | Scorrere un mese in poi e selezionare un giorno nella colonna più a destra.                                                                                                                                                                       |
| CTRL + PGSU          | Selezionare lo stesso giorno in un mese precedente. Il numero di mesi in base al quale lo spostamento della selezione è il numero di mesi visualizzato nel controllo. Se, ad esempio, vengono visualizzati due mesi, la selezione viene spostata dal 6 giugno al 6 maggio.    |
| CTRL + PGGIÙ        | Selezionare lo stesso giorno in un mese precedente. Il numero di mesi in base al quale lo spostamento della selezione è il numero di mesi visualizzato nel controllo. Se, ad esempio, vengono visualizzati due mesi, la selezione passerà dal 6 giugno al 6 agosto. |



 

Se un controllo calendario mensile non utilizza lo stile [**MCS \_ notoday**](month-calendar-control-styles.md) , l'utente può tornare al giorno corrente facendo clic sul testo "Today" nella parte inferiore del controllo. Se il giorno corrente non è visibile, il controllo ne aggiorna la visualizzazione per visualizzarlo.

Un'applicazione può modificare il numero di mesi per cui il controllo Aggiorna la visualizzazione tramite il messaggio [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md) o la macro corrispondente, [**MonthCal \_ SETMONTHDELTA**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta). Tuttavia, i tasti PGSU e PGGIÙ cambiano il mese selezionato di uno, indipendentemente dal numero di mesi visualizzato o dal valore impostato da **MCM \_ SETMONTHDELTA**.

### <a name="selecting-a-nonadjacent-month"></a>Selezione di un mese non adiacente

Quando un utente fa clic sul nome di un mese visualizzato, vengono elencati tutti i mesi dell'anno (nelle versioni precedenti, si tratta di un menu a comparsa). L'utente può selezionare un mese nell'elenco. Se la selezione dell'utente non è visibile, il controllo calendario mensile scorre la visualizzazione per visualizzare il mese scelto. Nello screenshot seguente un controllo calendario mensile Mostra i mesi di due anni adiacenti.

![Screenshot di una finestra di dialogo con un controllo calendario mensile che Mostra tutti i mesi 2007 e 2008](images/mc-months.png)

### <a name="selecting-a-different-year"></a>Selezione di un anno diverso

Se l'utente fa clic sull'anno, viene elencato un gruppo di anni e l'utente può selezionarne uno diverso, come illustrato nella schermata seguente.

![Screenshot di un controllo calendario mensile che Mostra tutti gli anni da 1999 a 2020](images/mc-years.png)

## <a name="localization"></a>Localizzazione

Il controllo Month-Calendar ottiene il formato e tutte le stringhe da impostazioni locali \_ dell'utente \_ .

## <a name="times-in-the-month-calendar-control"></a>Orari del controllo calendario mensile

Il controllo calendario mensile non Visualizza l'ora. Tuttavia, la struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) utilizzata per impostare e recuperare la data selezionata o la data odierna contiene campi temporali. Quando una data viene impostata a livello di programmazione, il controllo copia i campi temporali così come sono o li convalida prima e quindi, se non sono validi, archivia le ore predefinite correnti. Di seguito è riportato un elenco dei messaggi che impostano una data e una descrizione della modalità di trattamento dei campi temporali.



|                                             |                                                                                                                                                                                                                            |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCM \_**](mcm-setcursel.md)     | Il controllo copia i campi temporali così come sono, senza convalida o modifica.                                                                                                                                        |
| [**\_SEtrange MCM**](mcm-setrange.md)       | I campi relativi all'ora delle strutture passate sono convalidati. Se sono validi, i campi dell'ora vengono copiati senza modifiche. Se non sono validi, il controllo copia i campi temporali dai dati odierni.                  |
| [**\_SETSELRANGE MCM**](mcm-setselrange.md) | I campi relativi all'ora delle strutture passate sono convalidati. Se sono validi, i campi dell'ora vengono copiati senza modifiche. Se non sono validi, il controllo mantiene i campi temporali dagli intervalli di selezione correnti. |
| [**\_attualmente MCM**](mcm-settoday.md)       | Il controllo copia i campi temporali così come sono, senza convalida o modifica.                                                                                                                                        |



 

Quando una data viene recuperata dal controllo, i campi dell'ora verranno copiati dagli orari archiviati senza modifiche. La gestione dei campi temporali da parte del controllo viene fornita per comodità al programmatore. Il controllo non esamina né modifica i campi temporali come risultato di un'operazione diversa da quelle elencate in precedenza.

 

 