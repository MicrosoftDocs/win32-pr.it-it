---
title: Informazioni sugli Appunti
description: In questa sezione vengono illustrati gli Appunti.
ms.assetid: 14c91730-a668-495b-9ec6-b835234821a5
keywords:
- Appunti, informazioni
- Appunti, formati
- Appunti, comandi
- Appunti, Windows
- Appunti, numeri di sequenza
- Appunti, visualizzatori
- Appunti, finestre del Visualizzatore
- Appunti, formati di visualizzazione
- Appunti, formati di visualizzazione del proprietario
- visualizzare i formati degli Appunti
- formati degli Appunti di visualizzazione del proprietario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94757a95fb8c40152a0018d04cef64e8efae624
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338766"
---
# <a name="about-the-clipboard"></a>Informazioni sugli Appunti

Gli *Appunti* sono un set di funzioni e messaggi che consentono alle applicazioni di trasferire i dati. Poiché tutte le applicazioni hanno accesso agli Appunti, i dati possono essere trasferiti facilmente tra le applicazioni o all'interno di un'applicazione.

Gli Appunti sono basati sull'utente. Una finestra deve trasferire i dati da e verso gli Appunti solo in risposta a un comando dell'utente. Una finestra non deve usare gli Appunti per trasferire i dati senza le informazioni dell'utente.

Un oggetto Memory negli Appunti può essere in qualsiasi formato dati, denominato formato degli Appunti. Ogni formato è identificato da un valore Unsigned Integer. Per i formati degli Appunti standard (predefiniti), questo valore è una costante definita in winuser. h; per i formati degli Appunti registrati, è il valore restituito della funzione [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) .

Fatta eccezione per la registrazione dei formati degli Appunti, le singole finestre eseguono la maggior parte delle operazioni degli Appunti. In genere, una routine di finestra trasferisce le informazioni da e verso gli Appunti in risposta al messaggio del [**\_ comando WM**](/windows/desktop/menurc/wm-command) .

In questa sezione vengono descritte le operazioni seguenti:

-   [Comandi degli Appunti](#clipboard-commands)
-   [Numero di sequenza degli Appunti](#clipboard-sequence-number)
-   [Visualizzatori appunti](#clipboard-viewers)
    -   [Finestre Visualizzatore Appunti](#clipboard-viewer-windows)
    -   [Formati di visualizzazione](#display-formats)
    -   [Formato di visualizzazione del proprietario](#owner-display-format)
-   [Argomenti correlati](#related-topics)

## <a name="clipboard-commands"></a>Comandi degli Appunti

Un utente esegue in genere operazioni degli Appunti scegliendo comandi dal menu **modifica** di un'applicazione. Di seguito è riportata una breve descrizione dei comandi degli Appunti standard.



|            |                                                                                                                                                                                                                   |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Taglia**    | Inserisce una copia della selezione corrente negli Appunti ed elimina la selezione dal documento. Il contenuto precedente degli Appunti viene eliminato definitivamente.                                                          |
| **Copia**   | Inserisce una copia della selezione corrente negli Appunti. Il documento rimane invariato. Il contenuto precedente degli Appunti viene eliminato definitivamente.                                                                      |
| **Incolla**  | Sostituisce la selezione corrente con il contenuto degli Appunti. Il contenuto degli Appunti non è stato modificato.                                                                                                    |
| **Elimina** | Elimina la selezione corrente dal documento. Il contenuto degli Appunti non è stato modificato. Questo comando non riguarda gli appunti, ma dovrebbe essere visualizzato con i comandi degli Appunti nel menu **modifica** . |



 

## <a name="clipboard-sequence-number"></a>Numero di sequenza degli Appunti

Gli Appunti per ogni stazione della finestra hanno un numero di sequenza degli Appunti associato. Questo numero viene incrementato ogni volta che il contenuto degli Appunti viene modificato. Per ottenere il numero di sequenza degli Appunti, chiamare la funzione [**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) .

## <a name="clipboard-viewers"></a>Visualizzatori appunti

Un visualizzatore degli Appunti è una finestra in cui viene visualizzato il contenuto corrente degli Appunti. La finestra Visualizzatore Appunti rappresenta una praticità per l'utente e non influisce sulle funzioni di transazione dei dati degli Appunti.

In genere, una finestra del visualizzatore degli Appunti può visualizzare almeno i tre formati più comuni: **\_ testo CF**, **\_ bitmap CF** e **CF \_ METAFILEPICT**. Se una finestra non rende disponibili i dati in nessuno di questi tre formati, deve fornire dati in formato di visualizzazione o utilizzare il formato di visualizzazione del proprietario.

Una *catena di visualizzatore degli Appunti* è il collegamento tra due o più entità in modo che dipendano l'uno dall'altro per l'operazione. Questa interdipendenza (Chain) consente a tutte le applicazioni Visualizzatore Appunti in esecuzione di ricevere i messaggi inviati agli Appunti correnti.

In questa sezione vengono descritti gli argomenti seguenti.

-   [Finestre Visualizzatore Appunti](#clipboard-viewer-windows)
-   [Formati di visualizzazione](#display-formats)
-   [Formato di visualizzazione del proprietario](#owner-display-format)

### <a name="clipboard-viewer-windows"></a>Finestre Visualizzatore Appunti

Una finestra si aggiunge alla catena del visualizzatore degli Appunti chiamando la funzione [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) . Il valore restituito è l'handle per la finestra successiva nella catena. Per recuperare l'handle alla prima finestra della catena, chiamare la funzione [**GetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-getclipboardviewer) .

Ogni finestra del visualizzatore degli Appunti deve tenere traccia della finestra successiva nella catena del visualizzatore degli Appunti. Quando il contenuto degli Appunti viene modificato, il sistema invia un messaggio [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) alla prima finestra della catena. Dopo l'aggiornamento della visualizzazione, ogni finestra del visualizzatore degli Appunti deve passare questo messaggio alla finestra successiva della catena.

Prima di chiudere, una finestra del visualizzatore degli Appunti deve essere rimossa dalla catena del visualizzatore degli Appunti chiamando la funzione [**ChangeClipboardChain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) . Il sistema invia quindi un messaggio [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) alla prima finestra della catena.

Per ulteriori informazioni sull'elaborazione dei messaggi [**WM \_ DRAWCLIPBOARD**](wm-drawclipboard.md) e [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) , vedere la pagina relativa alla [creazione di una finestra Visualizzatore Appunti](using-the-clipboard.md).

### <a name="display-formats"></a>Formati di visualizzazione

Un formato di visualizzazione è un formato degli Appunti utilizzato per visualizzare le informazioni in una finestra del visualizzatore degli Appunti. Un proprietario degli appunti che utilizza un formato degli Appunti privato o registrato e nessuno dei formati standard più comuni, deve fornire dati in un formato di visualizzazione per la visualizzazione in una finestra del visualizzatore degli Appunti. I formati di visualizzazione sono destinati solo alla visualizzazione e non devono essere incollati in un documento.

I quattro formati di visualizzazione sono **: \_ CF DSPBITMAP**, **CF \_ DSPMETAFILEPICT**, **CF \_ DSPTEXT** e **CF \_ DSPENHMETAFILE**. Questi formati di visualizzazione vengono sottoposti a rendering in modo analogo ai formati standard, ossia: **\_ bitmap CF**, **\_ testo CF**, **CF \_ METAFILEPICT** e **CF \_ ENHMETAFILE**.

### <a name="owner-display-format"></a>Formato di visualizzazione del proprietario

Per un proprietario degli appunti che non usa uno dei formati degli Appunti standard comuni, un'alternativa a fornire un formato di visualizzazione consiste nell'usare il formato degli Appunti per la visualizzazione del proprietario (**CF \_ OWNERDISPLAY**).

Utilizzando il formato di visualizzazione del proprietario, un proprietario degli Appunti può evitare l'overhead del rendering dei dati in un formato aggiuntivo, assumendo il controllo diretto sul disegno della finestra Visualizzatore Appunti. La finestra Visualizzatore Appunti invia messaggi al proprietario degli Appunti ogni volta che è necessario ridisegnare una parte della finestra o quando viene eseguito lo scorrimento o il ridimensionamento della finestra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formati degli Appunti standard](standard-clipboard-formats.md)
</dt> </dl>

 

 