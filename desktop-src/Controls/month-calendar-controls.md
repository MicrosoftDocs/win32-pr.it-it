---
title: Informazioni sui controlli calendario mensile
description: Un controllo calendario mensile implementa un'interfaccia utente simile al calendario.
ms.assetid: 81b8f233-272e-4043-92ff-5ff47b0610d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f21fba66f9fb71ad45f8853578821ad5f83da00e
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423751"
---
# <a name="about-month-calendar-controls"></a>Informazioni sui controlli calendario mensile

Un controllo calendario mensile implementa un'interfaccia utente simile al calendario. Ciò fornisce all'utente un metodo molto intuitivo e riconoscibile di immettere o selezionare una data. Inoltre, il controllo fornisce all'applicazione i mezzi per ottenere e impostare le informazioni relative alla data nel controllo utilizzando i tipi di dati esistenti.

-   [Funzionalità del controllo Calendario mensile](#month-calendar-control-features)
    -   [Selezione di un giorno](#selecting-a-day)
    -   [Selezione di un mese non adiacenti](#selecting-a-nonadjacent-month)
    -   [Selezione di un anno diverso](#selecting-a-different-year)
-   [Localizzazione](#localization)
-   [Ore nel controllo Calendario mensile](#times-in-the-month-calendar-control)

## <a name="month-calendar-control-features"></a>Funzionalità del controllo Calendario mensile

Lo screenshot seguente mostra un controllo calendario mensile che è stato ridimensionato per mostrare due mesi.

![Screenshot di una finestra di dialogo con un controllo calendario mensile che mostra due mesi affiancati](images/mc-simple.png)

> [!Note]  
> L'aspetto e il comportamento del controllo calendario mensile sono leggermente diversi nelle diverse versioni della libreria di runtime. Questo argomento è in particolare sul controllo così come viene visualizzato in Windows Vista con la versione 6 di Comctl32.dll.

 

Il controllo nell'illustrazione presenta le funzionalità facoltative seguenti.

-   La data corrente viene visualizzata su una riga separata nella parte inferiore del controllo . È l'impostazione predefinita.
-   Il "cerchio odierno" (in realtà un rettangolo in questa versione) viene visualizzato intorno al giorno corrente e accanto alla riga "Today" come segnale visivo. È l'impostazione predefinita.
-   I numeri delle settimane vengono visualizzati a sinistra di ogni riga di giorni. Questo stile deve essere specificato.
-   Alcune date vengono visualizzate in grassetto, in base allo stato del giorno impostato dall'applicazione. Ad esempio, le date con riunioni pianificate potrebbero essere visualizzate in grassetto. Questo stile deve essere specificato.

> [!Note]
>
> Windows non supporta date precedenti alla 1601. Per [**informazioni dettagliate, vedere FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
>
> Il controllo calendario mensile è basato sul calendario gregoriano, introdotto nel 1753. Non calcola le date coerenti con il calendario giuliano in uso prima del 1753.

 

### <a name="selecting-a-day"></a>Selezione di un giorno

Per impostazione predefinita, quando un utente fa clic sui pulsanti freccia in alto a sinistra o in alto a destra del controllo calendario mensile, il controllo aggiorna la visualizzazione per visualizzare il mese precedente o successivo. L'utente può anche eseguire la stessa azione facendo clic sui mesi parziali visualizzati prima del primo mese e dopo l'ultimo mese.

I comandi della tastiera seguenti possono essere usati anche per spostare la selezione. Il calendario scorre sempre in base alle esigenze per visualizzare il giorno selezionato. I [**codici della chiave virtuale**](/windows/desktop/inputdev/virtual-key-codes) sono visualizzati nella tabella.



|    Comando      |    Descrizione                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Freccia sinistra (VK \_ LEFT)   | Selezionare il giorno precedente.                                                                                                                                                                                                                 |
| Freccia destra (VK \_ RIGHT) | Selezionare il giorno successivo.                                                                                                                                                                                                                     |
| Freccia su (VK \_ UP)       | Selezionare lo stesso giorno della settimana precedente.                                                                                                                                                                                                |
| Freccia GIÙ (VK \_ DOWN)   | Selezionare lo stesso giorno della settimana successiva.                                                                                                                                                                                                    |
| P UP (VK \_ PRIOR)     | Selezionare lo stesso giorno del mese precedente. Se tale mese non ha il giorno, viene selezionato il giorno più vicino. Ad esempio, la selezione viene spostata dal 31 marzo al 28 febbraio o 29 febbraio.                                                      |
| PGGI GIÙ (VK \_ NEXT)    | Selezionare lo stesso giorno nel mese successivo.                                                                                                                                                                                                   |
| HOME (VK \_ HOME)         | Selezionare il primo giorno del mese corrente.                                                                                                                                                                                               |
| END (VK \_ END)           | Selezionare l'ultimo giorno del mese corrente.                                                                                                                                                                                                |
| CTRL+HOME             | Scorrere indietro di un mese e selezionare un giorno nella colonna più a sinistra.                                                                                                                                                                       |
| CTRL+FINE              | Scorrere in avanti di un mese e selezionare un giorno nella colonna più a destra.                                                                                                                                                                       |
| CTRL+P SU          | Selezionare lo stesso giorno di un mese precedente. Il numero di mesi in base al quale la selezione viene spostata è il numero di mesi visualizzati nel controllo . Ad esempio, se vengono visualizzati due mesi, la selezione verrà spostata dal 6 giugno al 6 maggio.    |
| CTRL+PGGI GIÙ        | Selezionare lo stesso giorno di un mese precedente. Il numero di mesi in base al quale la selezione viene spostata è il numero di mesi visualizzati nel controllo . Ad esempio, se vengono visualizzati due mesi, la selezione si sposterà dal 6 giugno al 6 agosto. |



 

Se un controllo calendario mensile non usa lo stile [**MCS \_ NOTODAY,**](month-calendar-control-styles.md) l'utente può tornare al giorno corrente facendo clic sul testo "Oggi" nella parte inferiore del controllo. Se il giorno corrente non è visibile, il controllo aggiorna la relativa visualizzazione per visualizzarlo.

Un'applicazione può modificare il numero di mesi entro cui il controllo aggiorna la visualizzazione usando il messaggio [**\_ MCM SETMONTHDELTA**](mcm-setmonthdelta.md) o la macro corrispondente, [**MonthCal \_ SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta). Tuttavia, i tasti PGGIS e PGGIUTO modificano il mese selezionato di uno, indipendentemente dal numero di mesi visualizzati o dal valore impostato da **MCM \_ SETMONTHDELTA**.

### <a name="selecting-a-nonadjacent-month"></a>Selezione di un mese non adiacenti

Quando un utente fa clic sul nome di un mese visualizzato, vengono elencati tutti i mesi dell'anno (nelle versioni precedenti si tratta di un menu a comparsa). L'utente può selezionare un mese nell'elenco. Se la selezione dell'utente non è visibile, il controllo calendario mensile scorre la visualizzazione per visualizzare il mese scelto. Nella schermata seguente un controllo calendario mensile mostra i mesi di due anni adiacenti.

![Screenshot di una finestra di dialogo con un controllo calendario mensile che mostra tutti i mesi del 2007 e 2008](images/mc-months.png)

### <a name="selecting-a-different-year"></a>Selezione di un anno diverso

Se l'utente fa clic sull'anno, viene elencato un gruppo di anni e l'utente può selezionarne uno diverso, come illustrato nello screenshot seguente.

![Screenshot di un controllo calendario mensile che mostra tutti gli anni dal 1999 al 2020](images/mc-years.png)

## <a name="localization"></a>Localizzazione

Il controllo month-calendar ottiene il formato e tutte le stringhe da LOCALE \_ USER \_ DEFAULT.

## <a name="times-in-the-month-calendar-control"></a>Ore nel controllo Calendario mensile

Il controllo calendario mensile non visualizza l'ora. Tuttavia, la [**struttura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) usata per impostare e recuperare la data selezionata o la data odierna contiene campi di ora. Quando una data viene impostata a livello di codice, il controllo copia i campi ora così come sono o li convalida prima e quindi, se non sono validi, archivia le ore predefinite correnti. Di seguito è riportato un elenco dei messaggi che impostano una data e una descrizione della modalità di trattamento dei campi dell'ora.



|  Message         |  Descrizione            |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCM \_ SETCURSEL**](mcm-setcursel.md)     | Il controllo copia i campi relativi all'ora così come sono, senza convalida o modifica.                                                                                                                                        |
| [**MCM \_ SETRANGE**](mcm-setrange.md)       | I campi relativi all'ora delle strutture passate vengono convalidati. Se sono validi, i campi relativi all'ora vengono copiati senza modifiche. Se non sono validi, il controllo copia i campi dell'ora dai dati di oggi.                  |
| [**MCM \_ SETSELRANGE**](mcm-setselrange.md) | I campi relativi all'ora delle strutture passate vengono convalidati. Se sono validi, i campi relativi all'ora vengono copiati senza modifiche. Se non sono validi, il controllo mantiene i campi relativi all'ora degli intervalli di selezione correnti. |
| [**MCM \_ SETTODAY**](mcm-settoday.md)       | Il controllo copia i campi relativi all'ora così come sono, senza convalida o modifica.                                                                                                                                        |



 

Quando una data viene recuperata dal controllo , i campi dell'ora verranno copiati dagli orari archiviati senza modifiche. La gestione dei campi dell'ora da parte del controllo viene fornita per comodità al programmatore. Il controllo non esamina o modifica i campi dell'ora come risultato di qualsiasi operazione diversa da quelle elencate in precedenza.

 

 