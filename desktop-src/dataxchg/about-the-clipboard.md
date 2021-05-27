---
title: Informazioni sugli Appunti
description: Questa sezione illustra gli Appunti.
ms.assetid: 14c91730-a668-495b-9ec6-b835234821a5
keywords:
- Appunti, informazioni
- Appunti, formati
- appunti, comandi
- Appunti, finestre
- Appunti, numeri di sequenza
- Appunti, visualizzatori
- Appunti, finestre del visualizzatore
- Appunti, formati di visualizzazione
- Appunti, formati di visualizzazione del proprietario
- visualizzare i formati degli Appunti
- formati degli Appunti visualizzati dal proprietario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe22a16886c62824775b5f2d8174e2a8e244b9e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549586"
---
# <a name="about-the-clipboard"></a>Informazioni sugli Appunti

Gli *Appunti* sono un set di funzioni e messaggi che consentono alle applicazioni di trasferire i dati. Poiché tutte le applicazioni hanno accesso agli Appunti, i dati possono essere facilmente trasferiti tra applicazioni o all'interno di un'applicazione.

Gli Appunti sono guidati dall'utente. Una finestra deve trasferire i dati da o verso gli Appunti solo in risposta a un comando dell'utente. Una finestra non deve usare gli Appunti per trasferire i dati senza che l'utente ne sia a conoscenza.

Un oggetto memoria negli Appunti può essere in qualsiasi formato di dati, denominato formato degli Appunti. Ogni formato è identificato da un valore intero senza segno. Per i formati degli Appunti standard (predefiniti), questo valore è una costante definita in Winuser.h; per i formati degli Appunti registrati, è il valore restituito della [**funzione RegisterClipboardFormat.**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata)

Fatta eccezione per la registrazione dei formati degli Appunti, le singole finestre eseguono la maggior parte delle operazioni degli Appunti. In genere, una routine della finestra trasferisce informazioni da o verso gli Appunti in risposta al [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)

In questa sezione vengono illustrati gli elementi seguenti:

-   [Comandi degli Appunti](#clipboard-commands)
-   [Numero di sequenza degli Appunti](#clipboard-sequence-number)
-   [Visualizzatori Appunti](#clipboard-viewers)
    -   [Finestre del Visualizzatore Appunti](#clipboard-viewer-windows)
    -   [Formati di visualizzazione](#display-formats)
    -   [Formato di visualizzazione del proprietario](#owner-display-format)
-   [Argomenti correlati](#related-topics)

## <a name="clipboard-commands"></a>Comandi degli Appunti

Un utente esegue in genere operazioni sugli Appunti scegliendo i comandi dal menu **Modifica di un'applicazione.** Di seguito è riportata una breve descrizione dei comandi degli Appunti standard.



|  Comando        |  Descrizione                                                                                                                                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Taglia**    | Inserisce negli Appunti una copia della selezione corrente ed elimina la selezione dal documento. Il contenuto precedente degli Appunti viene eliminato.                                                          |
| **Copia**   | Inserisce negli Appunti una copia della selezione corrente. Il documento rimane invariato. Il contenuto precedente degli Appunti viene eliminato.                                                                      |
| **Incolla**  | Sostituisce la selezione corrente con il contenuto degli Appunti. Il contenuto degli Appunti non viene modificato.                                                                                                    |
| **Elimina** | Elimina la selezione corrente dal documento. Il contenuto degli Appunti non viene modificato. Questo comando non interessa gli Appunti, ma dovrebbe essere visualizzato con i comandi degli Appunti nel menu **Modifica.** |



 

## <a name="clipboard-sequence-number"></a>Numero di sequenza degli Appunti

Agli Appunti per ogni stazione finestra è associato un numero di sequenza degli Appunti. Questo numero viene incrementato ogni volta che il contenuto degli Appunti cambia. Per ottenere il numero di sequenza degli Appunti, chiamare [**la funzione GetClipboardSequenceNumber.**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber)

## <a name="clipboard-viewers"></a>Visualizzatori Appunti

Un visualizzatore Appunti è una finestra che visualizza il contenuto corrente degli Appunti. La finestra del visualizzatore Appunti è un'operazione comoda per l'utente e non influisce sulle funzioni di transazione dei dati degli Appunti.

In genere, una finestra del visualizzatore Appunti può visualizzare almeno i tre formati più comuni: **CF \_ TEXT,** **CF \_ BITMAP** e **CF \_ METAFILEPICT.** Se una finestra non rende disponibili i dati in uno di questi tre formati, deve fornire i dati in un formato di visualizzazione o usare il formato di visualizzazione del proprietario.

Una *catena di visualizzatore* degli Appunti è il collegamento tra due o più entità in modo che siano dipendenti l'una dall'altra per l'operazione. Questa interdipendenze (catena) consente a tutte le applicazioni del visualizzatore Appunti in esecuzione di ricevere i messaggi inviati agli Appunti correnti.

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Finestre del Visualizzatore Appunti](#clipboard-viewer-windows)
-   [Formati di visualizzazione](#display-formats)
-   [Formato di visualizzazione del proprietario](#owner-display-format)

### <a name="clipboard-viewer-windows"></a>Finestre del Visualizzatore Appunti

Una finestra si aggiunge alla catena del visualizzatore appunti chiamando la [**funzione SetClipboardViewer.**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) Il valore restituito è l'handle per la finestra successiva nella catena. Per recuperare l'handle per la prima finestra della catena, chiamare la [**funzione GetClipboardViewer.**](/windows/desktop/api/Winuser/nf-winuser-getclipboardviewer)

Ogni finestra del visualizzatore Appunti deve tenere traccia della finestra successiva nella catena del visualizzatore Appunti. Quando il contenuto degli Appunti cambia, il sistema invia un [**messaggio WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) alla prima finestra della catena. Dopo aver aggiornato la visualizzazione, ogni finestra del visualizzatore Appunti deve passare questo messaggio alla finestra successiva nella catena.

Prima della chiusura, una finestra del visualizzatore Appunti deve rimuovere se stessa dalla catena di visualizzatore degli Appunti chiamando la [**funzione ChangeClipboardChain.**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) Il sistema invia quindi un [**messaggio WM \_ CHANGECBCHAIN**](wm-changecbchain.md) alla prima finestra della catena.

Per altre informazioni sull'elaborazione dei [**messaggi WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) e [**WM \_ CHANGECBCHAIN,**](wm-changecbchain.md) vedere [Creazione di una finestra del Visualizzatore Appunti](using-the-clipboard.md).

### <a name="display-formats"></a>Formati di visualizzazione

Un formato di visualizzazione è un formato degli Appunti usato per visualizzare le informazioni in una finestra del visualizzatore Appunti. Un proprietario degli Appunti che usa un formato degli Appunti privato o registrato e nessuno dei formati standard più comuni deve fornire dati in un formato di visualizzazione per la visualizzazione in una finestra del visualizzatore appunti. I formati di visualizzazione sono destinati solo alla visualizzazione e non devono essere incollati in un documento.

I quattro formati di visualizzazione sono: **CF \_ DSPBITMAP,** **CF \_ DSPMETAFILEPICT,** **CF \_ DSPTEXT** e **CF \_ DSPENHMETAFILE.** Il rendering di questi formati di visualizzazione viene eseguito nello stesso modo dei formati standard, ovvero **CF \_ BITMAP,** **CF \_ TEXT,** **CF \_ METAFILEPICT** e **CF \_ ENHMETAFILE.**

### <a name="owner-display-format"></a>Formato di visualizzazione del proprietario

Per un proprietario degli Appunti che non usa uno dei formati di Appunti standard comuni, un'alternativa alla specifica di un formato di visualizzazione consiste nell'usare il formato degli Appunti owner-display (**CF \_ OWNERDISPLAY).**

Usando il formato di visualizzazione proprietario, un proprietario degli Appunti può evitare l'overhead del rendering dei dati in un formato aggiuntivo assumendo il controllo diretto sul disegno della finestra del visualizzatore degli Appunti. La finestra del Visualizzatore Appunti invia messaggi al proprietario degli Appunti ogni volta che è necessario ridisegnare una parte della finestra o quando la finestra viene scorreta o ridimensionata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formati degli Appunti standard](standard-clipboard-formats.md)
</dt> </dl>

 

 